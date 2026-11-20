---
name: spec-review
description: Reviews a PRD, product spec, or feature brief before the team builds it, finding ambiguous wording, missing states (empty, loading, error, no permission), missing success metrics, a missing rollout and rollback plan, and walking the flow step by step as a first-time user. Returns blocking issues and questions ranked by severity. Use when someone shares a PRD or spec and asks for a review, a sanity check, feedback, gaps, or "is this ready to build?".
---

# Spec review

A spec is ready when an engineer, a designer, and a tester would each build and test the same thing from it. The review hunts for places where they would diverge, and for the states nobody wrote down. Walk the flow as a first-time user before reading the requirements list: the gaps show up in the walk.

## When to use

- Before engineering estimates or starts building from a PRD or spec.
- When a spec has been revised and needs a second look.
- When a feature shipped with surprises and you want to check the next spec harder.
- Not for writing the spec from notes: use prd-from-notes. Not for reviewing finished screens or copy: use landing-copy-review or a design review.

## What you need

- The spec or PRD text, including any mockup descriptions.
- Who the target user is, if the spec doesn't say. If missing, review as a first-time user with no training and note "[assumption]".
- Optional: the deadline and team, so you can judge scope.

## Steps

1. **Walk the flow as a first-time user.** Start from where the user arrives (email link, nav item, empty account) and narrate each step: what they see, what they must decide, what they click. Wherever the spec doesn't say what appears next, log a gap. Wherever a label or question would puzzle someone new, log it.
2. **Check every screen's states.** For each screen or component, look for: empty (first use, no results), loading, error, partial data, no permission, and success. NN/g advises that an empty state show system status, teach how to start, and give a direct path to the task, and that a "no records" message never shows while data is still loading. Error messages should be visible, plain-language, constructive, and keep the user's input.
3. **Find ambiguous words.** Flag "fast", "easy", "simple", "intuitive", "should", "etc.", "and/or", "some", and "as needed". Each needs a number, a list, or a decision. Flag any requirement two readers could test differently.
4. **Check rules and limits.** Who can do this? How many? What happens at the limit? What about existing data and users when this ships? Missing answers are blocking if they change the data model.
5. **Check metrics.** There must be one primary metric tied to the problem, a baseline, a target, and how it will be measured. If the event to count doesn't exist yet, that is a requirement the spec is missing.
6. **Check rollout and rollback.** Is it behind a flag? Who sees it first (internal, a percentage, a segment)? What metric triggers a rollback, and can it be turned off without a release? Martin Fowler's feature-toggle guidance separates release toggles, gradual percentage rollouts, and kill switches; a kill switch must flip fast, without a new release.
7. **Rank and write findings.** Blocking = the team can't build or test it, or it risks data or trust. Should fix = it will cause rework or confusion. Nit = wording. Each finding quotes the spec, says why it matters, and proposes a fix or a question.

## Output format

```markdown
# Spec review: [spec name]

**Verdict:** [Ready / Ready after blocking fixes / Not ready] — [one sentence why]

## First-time user walk-through
1. [Step: what the user sees and does] — [gap or "clear"]

## Blocking
| # | Spec says | Problem | Fix or question |
|---|---|---|---|
| B1 | "[quote]" | [why it blocks] | [proposal] |

## Should fix
| # | Spec says | Problem | Fix or question |
|---|---|---|---|

## Missing states
| Screen | Empty | Loading | Error | No permission | Notes |
|---|---|---|---|---|---|
| [screen] | [covered / missing] | ... | ... | ... | [note] |

## Metrics and rollout
- Primary metric: [present / missing] — [note]
- Rollout: [present / missing] — [note]
- Rollback trigger and kill switch: [present / missing] — [note]

## Nits
- [wording]
```

## Example

**Input (excerpt):** "Users can invite their accountant as read-only. Invites should be easy. Read-only users can't edit. We'll measure adoption. Launch to everyone on the 1st."

**Output:**

```markdown
# Spec review: Read-only seat

**Verdict:** Not ready — no defined states, an unmeasurable metric, and a launch with no way back.

## First-time user walk-through
1. Owner looks for where to invite — spec doesn't say which page; gap.
2. Owner enters an email — spec doesn't say what happens if the email is already a member; gap.
3. Accountant opens invite email — no email content specified; gap.
4. Accountant lands in the app — what do they see first? An empty dashboard would read as "broken"; gap.

## Blocking
| # | Spec says | Problem | Fix or question |
|---|---|---|---|
| B1 | "can't edit" | Is export an edit? Are comments? Two engineers will answer differently. | List allowed actions: view, export [to confirm], nothing else. |
| B2 | "Launch to everyone on the 1st" | No flag, no rollback trigger. A permissions bug would expose every account. | Release behind a flag to internal accounts, then 10% [our default]; add a kill switch. |
| B3 | "We'll measure adoption" | No event, baseline, or target. | Count accounts with 1 or more accepted read-only invites per week; target to be set. |

## Should fix
| # | Spec says | Problem | Fix or question |
|---|---|---|---|
| S1 | "Invites should be easy" | Untestable. | "An owner can send an invite in 3 clicks or fewer from the Team page." [our suggestion] |
| S2 | (none) | No limit on read-only seats. | Decide a cap or state "no cap". |

## Missing states
| Screen | Empty | Loading | Error | No permission | Notes |
|---|---|---|---|---|---|
| Team page invite | n/a | missing | missing | missing | What does a non-owner see? |
| Accountant's first screen | missing | missing | missing | n/a | Needs a "you have view-only access" note |

## Metrics and rollout
- Primary metric: missing — see B3.
- Rollout: missing — see B2.
- Rollback trigger and kill switch: missing — see B2.

## Nits
- "Accountant" and "read-only user" are used for the same role; pick one.
```

## Checks before you send

- [ ] The walk-through starts where a real user arrives and covers every step to success.
- [ ] Every finding quotes the spec or says "(none)" for an omission.
- [ ] Every blocking finding has a proposed fix or a direct question.
- [ ] The states table covers every screen named in the spec.
- [ ] Metrics, rollout, and rollback are each marked present or missing.
- [ ] Defaults you suggest (percentages, click counts) are marked as suggestions, not as the spec's.

## Common mistakes

- Reviewing only the requirements list. Most gaps live between steps, so walk the flow first.
- Listing 40 nits. Lead with blocking items; cap nits at 5.
- Rewriting the spec. Point to the gap and propose; the author owns the fix.
