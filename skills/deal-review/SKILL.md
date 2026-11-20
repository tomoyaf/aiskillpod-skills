---
name: deal-review
description: Qualifies a sales deal against MEDDICC (or BANT for small deals), scores each element 0 to 2 with the evidence behind it, lists the gaps with one next action each, and suggests a forecast category. Use when a rep or manager asks for a deal review, pipeline review, deal qualification, "is this deal real?", MEDDICC or BANT scoring, or which forecast category a deal belongs in.
---

# Deal review (MEDDICC or BANT)

A good deal review tells the rep what they don't know yet and what to do this week to find out. Score only what the buyer said or did, never what the rep hopes. A deal with no evidence for a champion or a decision process is not a commit, however warm the calls felt.

## When to use

- Before a weekly pipeline or forecast call, on any deal in the current or next quarter.
- When a deal has stalled or the close date has moved twice.
- When a manager asks "is this deal real?" or "what's the forecast category?".
- Not for scoring leads before a first call: use discovery-call-prep to plan what to ask.

## What you need

- Deal notes: call summaries, CRM notes, emails. Buyer quotes beat rep summaries.
- Deal size, stage, and expected close date. If missing, ask once; if still missing, write "[assumption]" and say what you assumed.
- Optional: the team's own stage definitions or forecast categories. If given, use theirs instead of the defaults below.

## Steps

1. **Pick the framework.** BANT (Budget, Authority, Need, Timeline) suits short sales cycles; MEDDICC suits complex B2B deals with several stakeholders and longer cycles. Our default cut-off: BANT if the deal is under about 10,000 a year, has one decision maker, and closes in under 30 days; MEDDICC for everything else. Say which you used and why in one line.
2. **Collect evidence per element.** For each element, quote or paraphrase what the buyer said or did, with the date. "Rep thinks" is not evidence. MEDDICC: Metrics, Economic buyer, Decision criteria, Decision process, Identify pain (MEDDICC.com now calls it Implicate the pain), Champion, Competition. If the team uses MEDDPICC, add Paper process (the contract and procurement steps after the decision) and score out of 16. BANT: Budget, Authority, Need, Timeline.
3. **Score each element 0, 1, or 2 (our default scale).** 0 = no evidence or only the rep's guess. 1 = named or mentioned, not confirmed by the person who owns it. 2 = confirmed by the buyer in their words, with a number, name, or date. MEDDICC defines the economic buyer as the person with overall authority in the buying decision, and a champion as someone with power, influence, and credibility inside the customer. So a champion scores 2 only with evidence of that influence in action (shared an internal doc, set up a meeting with the economic buyer); liking the product is a 1.
4. **Find the gaps.** Every element at 0 or 1 is a gap. Rank them by risk: economic buyer, decision process, and champion gaps first, because they kill deals late.
5. **Write one next action per gap.** Verb-first, one owner, one date, and the question to ask or the thing to send. "Ask Dana who signs above 20,000 and when that person last bought software" beats "Confirm economic buyer".
6. **Suggest a forecast category.** Salesforce's default set is Pipeline, Best Case, Most Likely, Commit, Closed, Omitted; this review uses all but Most Likely. Each team defines what its categories mean, so if the user gave definitions, use theirs. Our default rules: Commit: total at least 11 of 14 (MEDDICC) or 7 of 8 (BANT), economic buyer and decision process both 2, close date agreed by the buyer. Best case: total at least 8 of 14 or 5 of 8, no 0 on economic buyer. Pipeline: everything else. Omitted: no pain scored above 0, or no contact in 21 days. State the rule that put the deal there.
7. **Flag the close date.** If the decision process has steps that can't fit before the close date (legal review, security review, a board meeting), say the date is at risk and propose a realistic one.

## Output format

```markdown
# Deal review: [account] — [date]

**Framework:** [MEDDICC or BANT] — [one-line reason]
**Size / stage / close date:** [amount] / [stage] / [date]
**Score:** [total] of [14 or 8]
**Forecast suggestion:** [Commit / Best Case / Pipeline / Omitted] — [rule that applied]

## Scorecard
| Element | Score | Evidence (who said it, when) |
|---|---|---|
| [element] | [0/1/2] | [quote or "none"] |

## Gaps and next actions
| Gap | Risk | Next action | Owner | By |
|---|---|---|---|---|
| [element] | [high/medium/low] | [verb-first action with the question to ask] | [name] | [date] |

## Close date
[Holds / At risk: reason, and a realistic date]
```

## Example

**Input:** Northwind Clinics, 36,000 a year, stage "Proposal", close Tuesday 30 June 2026, owner Alex (AE), reviewed Tuesday 9 June 2026. Notes: "Ops lead Dana Ruiz says no-shows are their biggest ops problem and cost them about 400 appointments a month (call, 2 June). Dana loves the demo. IT asked for our security pack. Dana says the COO, Marcus Hale, signs anything over 20,000. They also looked at BookWell. No call with Marcus yet."

**Output:**

```markdown
# Deal review: Northwind Clinics — 9 June

**Framework:** MEDDICC — 36,000 a year with IT and a COO involved.
**Size / stage / close date:** 36,000 / Proposal / 30 June
**Score:** 6 of 14
**Forecast suggestion:** Pipeline — under 8 of 14, and the economic buyer has had no contact.

## Scorecard
| Element | Score | Evidence (who said it, when) |
|---|---|---|
| Metrics | 1 | Dana: about 400 no-shows a month (2 June). No cost per no-show yet. |
| Economic buyer | 1 | Dana named Marcus Hale, COO, as signer over 20,000. No contact. |
| Decision criteria | 0 | None stated. |
| Decision process | 1 | IT security review mentioned; other steps unknown. |
| Identify pain | 2 | Dana: no-shows are their biggest ops problem (2 June). |
| Champion | 1 | Dana likes the demo; has not acted for the deal yet. |
| Competition | 0 | BookWell evaluated; where they stand is unknown. |

## Gaps and next actions
| Gap | Risk | Next action | Owner | By |
|---|---|---|---|---|
| Economic buyer | high | Ask Dana for 20 minutes with Marcus to agree the no-show cost and the decision date | Alex (AE) | 15 June |
| Decision process | high | Ask Dana: "After IT's review, who else has to say yes, and how long did your last software purchase take?" | Alex | 11 June |
| Champion | high | Send Dana a one-page business case she can forward to Marcus; see if she does | Alex | 12 June |
| Decision criteria | medium | Ask what would make them pick one vendor over another | Alex | 11 June |
| Competition | medium | Ask what they liked about BookWell | Alex | 11 June |
| Metrics | medium | Ask what one no-show costs them, to turn 400 a month into money | Alex | 11 June |

## Close date
At risk: the security review and a first COO meeting are both still ahead. Propose 21 July.
```

## Checks before you send

- [ ] Every score of 2 has a buyer quote or action with a date; no score rests on "rep thinks".
- [ ] Every 0 or 1 has exactly one next action with an owner and a date.
- [ ] The forecast category names the rule that put it there.
- [ ] The economic buyer is a named person, not a title or "leadership".
- [ ] No number appears that isn't in the notes.

## Common mistakes

- Scoring the champion on enthusiasm. A champion sells for you when you're not in the room.
- Treating "they have budget" as a 2. It's a 2 when the economic buyer confirms the amount for this purchase.
- Writing next actions like "Follow up". Say the exact question and who asks it.
