---
name: prd-from-notes
description: Turns messy notes, Slack threads, call notes, or a founder's brain dump into a product requirements document (PRD) with the problem and its evidence, users, goals and non-goals, success metrics, must/should/could requirements, open questions, and risks. Flags gaps instead of inventing them. Use when someone asks for a PRD, a spec, a one-pager, or "write this up so engineering can build it" from scattered notes.
---

# PRD from notes

A good PRD lets an engineer and a designer start work without a meeting, and lets a reader see what is known versus guessed. Write the problem before the solution, tie every requirement to the problem, and mark every gap out loud: a PRD that hides gaps gets built wrong.

## When to use

- You have notes, a Slack thread, call notes, or customer quotes about a feature and need a PRD.
- A founder says "write this up for the team" after a call or a whiteboard session.
- Someone wants a one-page brief before deciding whether to build.
- Not for reviewing a finished PRD: use spec-review. Not for splitting work into tickets: use user-stories.

## What you need

- The raw material: notes, threads, transcripts, quotes, screenshots described in text.
- Who the feature is for, if the notes don't say. Ask once; if still missing, write "[assumption: target user]".
- Any known deadline, constraint, or metric target. If none, leave the target as "[open: target not set]".

## Steps

1. **Pull out the problem and its evidence.** Answer the first question of Marty Cagan's opportunity assessment: what problem does this solve, and for whom? Write the problem as what a user can't do today or what it costs them. List the evidence under it: quotes, ticket counts, lost deals, numbers. If the notes contain no evidence, say "No evidence in the notes" rather than inventing a rationale.
2. **Name the users.** One primary user and at most 2 secondary ones, each with the situation they are in when the problem bites. "Small business owners" is too broad; "an owner sending their first invoice from a phone" is right.
3. **Separate goals from non-goals.** Goals are outcomes, not features. Write at least 2 non-goals; anything discussed in the notes and dropped belongs here, so nobody reopens it.
4. **Set success metrics.** One primary metric that moves if the problem is solved, plus 1 or 2 guardrails that must not get worse. Each needs a baseline and a target; if the notes don't give them, write "[open: baseline]" and "[open: target]".
5. **Write requirements as must/should/could (MoSCoW).** Must = the solution isn't viable without it. Should = important, painful to leave out, but there's a workaround. Could = desirable, the first thing cut when the date is at risk. Won't (this time) goes into non-goals so it isn't quietly reintroduced. Each line is testable ("A user can export to CSV"), not vague ("easy export"). The Agile Business Consortium's guide keeps "must" to typically no more than 60% of the effort; if the musts look bigger than that, say the scope is too big for one release.
6. **List open questions and risks.** Every contradiction between two notes becomes an open question naming both positions. Risks cover what could make the feature fail: adoption, technical, legal, dependency on another team. Give each an owner when the notes name one.
7. **Mark the source of each claim.** Facts from the notes stand plain. Anything you inferred gets "[assumption]". Never fill a number, date, or customer name that isn't in the input.

## Output format

```markdown
# PRD: [feature name]

**Author:** [name] · **Status:** Draft · **Last updated:** [date]

## Problem
[2 to 4 sentences: what users can't do today and what it costs them.]

**Evidence**
- [quote, count, or data point, with its source]

## Users
- **Primary:** [who, in what situation]
- **Secondary:** [who, in what situation]

## Goals
- [outcome]

## Non-goals
- [what this release won't do, and why if known]

## Success metrics
| Metric | Type | Baseline | Target |
|---|---|---|---|
| [metric] | Primary | [value or open] | [value or open] |
| [metric] | Guardrail | [value or open] | [must not drop below ...] |

## Requirements
| # | Requirement | Priority | Notes |
|---|---|---|---|
| R1 | [testable statement] | Must | [source or assumption] |

## Open questions
- [question] — [owner, if known]

## Risks
- [risk] — [mitigation or "none yet"]

## Gaps in the notes
- [what's missing that the team must decide before build]
```

## Example

**Input (excerpt):**

> Slack, Dana (CS): 3 customers this week asked to invite their accountant without paying for a seat.
> Call notes, Marco (founder): "Read-only seat? Maybe free. Don't want to build roles yet."
> Ravi (eng): we'd need a permission check on every write endpoint, maybe 2 weeks.

**Output:**

```markdown
# PRD: Free read-only seat for accountants

**Author:** [name] · **Status:** Draft · **Last updated:** [date]

## Problem
Customers can't give their accountant access to their books without paying for a full seat.

**Evidence**
- 3 customer requests in one week (Dana, CS, Slack).

## Users
- **Primary:** an account owner who needs their accountant to review numbers each month.
- **Secondary:** the accountant, who views but never edits.

## Goals
- Owners can give an outside reviewer access without paying for a seat.

## Non-goals
- A full roles and permissions system (Marco: "don't want to build roles yet").
- Edit access for the accountant: the seat is read-only (Marco: "Read-only seat?").

## Success metrics
| Metric | Type | Baseline | Target |
|---|---|---|---|
| Accounts with 1 or more read-only seats | Primary | 0 | [open: target] |
| Paid seat count | Guardrail | [open: baseline] | No drop |

## Requirements
| # | Requirement | Priority | Notes |
|---|---|---|---|
| R1 | An owner can invite a person as read-only by email | Must | Dana's requests |
| R2 | A read-only user can't create, edit, or delete anything | Must | Ravi: check on every write endpoint |
| R3 | Read-only seats don't count toward billing | Must | Marco: "maybe free" (to confirm) |
| R4 | An owner can remove a read-only user | Should | [assumption] |

## Open questions
- Is the seat free, or a lower price? Marco said "maybe free". — Marco
- How many read-only seats per account? — not discussed

## Risks
- Paid users downgrade teammates to read-only to save money. — consider a cap per account

## Gaps in the notes
- No target for adoption.
- No word on what the accountant sees on first login.
- No word on how customers get their books to the accountant today.
```

## Checks before you send

- [ ] The problem section names a user and a cost, and says nothing about the solution.
- [ ] Every number, name, and quote appears in the input; everything else is marked "[assumption]" or "[open]".
- [ ] Each requirement is testable and has a priority; "must" items look like 60% of the effort or less.
- [ ] There are at least 2 non-goals.
- [ ] Every contradiction in the notes appears as an open question.
- [ ] The primary metric has a baseline and target, or both are marked open.

## Common mistakes

- Writing the solution into the problem ("Users need a read-only role"). The problem is what hurts, not what you'll build.
- Smoothing over a disagreement between two people. Quote both and leave it open.
- Metrics like "user satisfaction" with no way to measure. Name the event or number you'd count.
