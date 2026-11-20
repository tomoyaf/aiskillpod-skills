---
name: ai-output-review
description: Reviews an AI-generated draft before anyone uses it - lists every factual claim to verify, flags sources, quotes, and citations that may be invented, checks numbers, tone, company policy, and whether the draft actually answers the request - and returns a prioritized fix list. Use when someone asks to check, fact-check, proofread, or sanity-check something ChatGPT, Claude, Gemini, or Copilot wrote, before sending, publishing, or filing it, or asks "can I trust this AI draft?".
---

# AI output review

AI drafts read fluently whether or not they're right. The UK government's AI Playbook warns that language models produce plausible but incorrect content and are not a substitute for professional advice; in a 2024 Stanford study, GPT-3.5, Llama 2, and PaLM 2 hallucinated in 69% to 88% of answers to specific legal queries. So the review doesn't judge whether the draft sounds right. It pulls out every checkable claim, marks how to verify it, and returns a fix list the author works through before use.

## When to use

- Before sending, publishing, or filing anything an AI drafted: client emails, reports, articles, proposals, policies.
- When a draft cites studies, laws, statistics, quotes, or URLs.
- When someone else's AI-written work lands on your desk for approval.
- Not a substitute for a lawyer, accountant, or doctor reviewing legal, financial, or medical content: flag those for an expert.

## What you need

- The draft.
- The original request or prompt: what was it supposed to do, for whom.
- Any source material the AI was given. Claims not traceable to it need outside checking.
- Company policy or style rules that apply. If none, check against the general rules in step 5 and say so.

## Steps

1. **Check it answers the request.** Compare the draft to the request point by point: every question answered, the requested format and length, the right audience. List anything missing or added that wasn't asked for.
2. **Extract every factual claim.** Numbers, dates, names, prices, product features, legal or policy statements, "studies show", quotes. One line each, with its location in the draft.
3. **Classify each claim.** Supported (traceable to the provided source, give the location); checkable (could be true, needs an outside check, say where to check); suspect (specific but unsourced, too precise to be a guess, or contradicts the source). Every statistic without a source is at least checkable.
4. **Hunt for invented sources.** For each cited study, article, URL, case, statute, or quote: does the title, author, date, and URL exist and say what's claimed? Mark any you cannot confirm as "verify before use; possibly invented". Never confirm a citation from memory.
5. **Check tone and policy.** Promises the company can't keep (dates, discounts, guarantees), confidential or personal data, claims marketing can't make ("best", "guaranteed", "100%"), tone that doesn't fit the audience, and filler.
6. **Check internal consistency.** Numbers that don't add up, names spelled two ways, a date that conflicts with another, conclusions the body doesn't support.
7. **Write the fix list.** Ordered by severity: must fix (wrong, invented, risky), should fix (missing, unclear), could fix (style). Each item: location, problem, the fix or how to verify. End with a verdict: ready, ready after must-fixes, or redo.

## Output format

```markdown
# AI output review — [draft title]
**Request:** [one line] · **Verdict:** [ready / ready after must-fixes / redo]

## Does it answer the request?
- [Covered / missing / added without being asked]

## Claims to verify
| # | Claim | Where | Status | How to verify |
|---|---|---|---|---|
| 1 | [claim] | [para] | supported / checkable / suspect | [source location or where to check] |

## Sources and citations
| Citation | Exists? | Says what's claimed? |
|---|---|---|
| [title, author, year, URL] | verify before use | [ ] |

## Fix list
**Must fix**
1. [Location] — [problem] → [fix]
**Should fix**
1. [Location] — [problem] → [fix]
**Could fix**
1. [Location] — [problem] → [fix]

## Needs an expert
- [Legal / financial / medical point] → [who]
```

## Example

**Input:** Request: "Write a 150-word LinkedIn post on why small clinics should switch to online booking, for our scheduling app Bookwell." Draft: "Studies show 67% of patients prefer booking online (Accenture, 2023). Clinics using Bookwell cut no-shows by 50%, guaranteed. Online booking is fully HIPAA-exempt, so there's no compliance work. Switch today and join 10,000 happy clinics!"

**Output:**

```markdown
# AI output review — Bookwell LinkedIn post
**Request:** 150-word post on online booking for small clinics · **Verdict:** ready after must-fixes

## Does it answer the request?
- Covered: why to switch. Length: 35 words, well under 150. No call to action beyond "switch today".

## Claims to verify
| # | Claim | Where | Status | How to verify |
|---|---|---|---|---|
| 1 | 67% of patients prefer booking online | line 1 | suspect | Find the Accenture 2023 report and the exact figure |
| 2 | Bookwell cuts no-shows by 50% | line 2 | suspect | Bookwell's own data; "guaranteed" can't stay |
| 3 | Online booking is "fully HIPAA-exempt" | line 3 | suspect | Expert check; booking data is usually patient information |
| 4 | 10,000 clinics use Bookwell | line 4 | checkable | Internal customer count |

## Sources and citations
| Citation | Exists? | Says what's claimed? |
|---|---|---|
| Accenture, 2023 | verify before use; possibly invented | [ ] |

## Fix list
**Must fix**
1. Line 3 — compliance claim is likely false and risky → remove; mention compliance only after expert review.
2. Line 2 — "guaranteed" is a promise → remove; use a verified customer result with its source, or drop the number.
3. Line 1 — unverified statistic → confirm the report or remove.
**Should fix**
1. Length — 35 words vs 150 requested → add one customer example and a clear next step.
**Could fix**
1. Line 4 — "happy clinics" is filler → use the verified number only.

## Needs an expert
- HIPAA statement → compliance or legal counsel.
```

## Checks before you send

- [ ] Every number, name, date, and citation in the draft appears in the claims table.
- [ ] No citation is marked as real unless it was checked against the actual source.
- [ ] Every must-fix item has a location and a specific fix.
- [ ] Legal, financial, and medical points are routed to an expert, not approved.
- [ ] The verdict matches the fix list (no "ready" with open must-fixes).

## Common mistakes

- Fixing the wording and leaving the facts. Polished false claims are worse than rough ones.
- Asking the same AI "are these sources real?" and accepting yes. Check the source itself.
- Reviewing only what's there. A draft that skips half the request fails, however accurate it is.
