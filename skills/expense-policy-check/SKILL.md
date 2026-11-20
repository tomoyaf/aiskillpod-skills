---
name: expense-policy-check
description: Checks submitted expenses, from receipt text or an expense list, against the company's expense policy and marks each line pass, flag, or fail with the reason, lists missing receipts, and totals what is out of policy. Uses a default policy skeleton when none is pasted. Use when someone shares an expense report, receipts, a card statement, or reimbursement claims and asks to "check these expenses", review a claim, or find out-of-policy spend.
---

# Expense policy check

An expense check gives the approver a fast, fair decision on every line: pass, flag for a question, or fail with the rule it breaks. Judge each line against the written policy only. Where the policy says nothing, flag it and ask; don't make up a rule.

## When to use

- An employee submitted an expense report or reimbursement claim.
- A company card statement needs a monthly review.
- Before month-end, to catch missing receipts.
- Not for checking a supplier invoice: use invoice-check. Not tax advice: what's deductible depends on your jurisdiction and accountant.

## What you need

- The expenses: date, merchant, amount, currency, category, purpose, attendees for meals, and whether a receipt is attached.
- The company's expense policy. If none is pasted, use the skeleton below, say so at the top of the output, and mark every limit "[check: policy limit]". Never pick a limit yourself.
- Who submitted it and their role, if limits differ by role.

## Default policy skeleton (fill in your numbers)

- Receipts: required for every line over [amount], and for all lodging. (A US reference point: IRS Publication 463 asks for documentary evidence for all lodging and any other expense of $75 or more. Your policy can be stricter.)
- Each line needs a business purpose; meals with others need the attendees' names.
- Meals: up to [amount] per person. Alcohol: [allowed / not allowed].
- Travel: [class] for flights under [hours]; lodging up to [amount] per night.
- Not reimbursed: [personal items, fines, upgrades, family travel, gifts over [amount]].
- Submit within [number] days of the expense. Approver: [role].

## Steps

1. **Normalize each line.** One row per expense: date, merchant, amount in the original currency, category. If a receipt shows a total that differs from the claimed amount, use the receipt and flag the difference.
2. **Check the receipt.** Mark "missing receipt" if the policy requires one and none is attached, or the receipt lacks date, merchant, or amount. Note it in the missing receipts list.
3. **Check purpose and attendees.** Fail no line for a vague purpose; flag it ("Purpose: 'meeting' — which client or project?").
4. **Check against each policy rule.** Compare amount, category, timing, and what was bought. For per-person limits, divide by the attendees listed. Quote the rule that applies in the reason.
5. **Decide pass, flag, or fail.** Pass: meets every rule. Flag: may be fine but something is missing or unclear, or the policy doesn't cover it. Fail: clearly breaks a written rule. If the policy doesn't cover the case, it's a flag, never a fail.
6. **Total the result.** Totals for passed, flagged, and failed, by currency. Out-of-policy amount is the part over the limit, not the whole line, when the policy reimburses up to the limit; say which you used.
7. **Write the questions.** One question per flagged line that the approver can send the employee.

## Output format

```markdown
# Expense check — [employee], [period]

**Policy used:** [company policy, dated] / [default skeleton — limits marked "[check: ...]"]

| # | Date | Merchant | Amount | Category | Result | Reason |
|---|---|---|---|---|---|---|
| 1 | [date] | [merchant] | [amount, currency] | [category] | Pass / Flag / Fail | [rule quoted, or what's missing] |

## Missing receipts
- Line [n]: [merchant, amount]

## Totals
| | Lines | Amount |
|---|---|---|
| Pass | [n] | [amount] |
| Flag | [n] | [amount] |
| Fail | [n] | [amount] |
| Out of policy | | [amount] — [whole line / over-limit part] |

## Questions for the employee
- Line [n]: [question]
```

## Example

**Input:**

> Policy (Harbor Labs, v3): receipts for anything over 30. Meals up to 60 per person, attendees required. No alcohol. Lodging up to 220 per night. Submit within 30 days.
> Claims from Leo, October:
> 1. 3 Oct, Rail Co, 84.00, travel, receipt yes
> 2. 3 Oct, Hotel Arden, 260.00 (1 night), lodging, receipt yes
> 3. 4 Oct, Bistro Nove, 150.00, client dinner, attendees: Leo + 1 (Priya, Delta Corp), receipt shows 2 glasses of wine 24.00
> 4. 5 Oct, Corner Cafe, 22.00, meal, no receipt
> 5. 6 Oct, Office Depot, 45.00, "supplies", no receipt

**Output:**

```markdown
# Expense check — Leo, October

**Policy used:** Harbor Labs expense policy v3

| # | Date | Merchant | Amount | Category | Result | Reason |
|---|---|---|---|---|---|---|
| 1 | 3 Oct | Rail Co | 84.00 | Travel | Pass | Receipt attached |
| 2 | 3 Oct | Hotel Arden | 260.00 | Lodging | Fail | "Lodging up to 220 per night"; 40.00 over |
| 3 | 4 Oct | Bistro Nove | 150.00 | Meal | Fail | "No alcohol": 24.00 of wine. Food 126.00 for 2 = 63.00 per person, over the 60 limit by 6.00 total |
| 4 | 5 Oct | Corner Cafe | 22.00 | Meal | Flag | Under the 30 receipt threshold; attendees and purpose missing |
| 5 | 6 Oct | Office Depot | 45.00 | Supplies | Flag | "Receipts for anything over 30": none attached |

## Missing receipts
- Line 5: Office Depot, 45.00

## Totals
| | Lines | Amount |
|---|---|---|
| Pass | 1 | 84.00 |
| Flag | 2 | 67.00 |
| Fail | 2 | 410.00 |
| Out of policy | | 70.00 — over-limit part (40.00 lodging + 24.00 wine + 6.00 meal) [check: does policy v3 reimburse up to the limit or reject the line?] |

## Questions for the employee
- Line 4: Who was this meal with, and for which client or project?
- Line 5: Can you attach the receipt, and what supplies were these for?
```

## Checks before you send

- [ ] Every line has one result and a reason that quotes a rule or names what's missing.
- [ ] Nothing fails on a rule that isn't in the policy; uncovered cases are flags.
- [ ] Per-person limits are divided by the attendees listed.
- [ ] Totals add up, by currency, and say how out-of-policy was counted.
- [ ] No limit or amount appears that isn't in the policy or the claims; gaps are "[check: ...]".

## Common mistakes

- Failing a whole line when only part is out of policy, without saying which approach the policy uses.
- Applying a limit from "common practice" when the pasted policy is silent.
- Converting currencies with a guessed rate. Keep the original currency or mark "[check: rate]".
