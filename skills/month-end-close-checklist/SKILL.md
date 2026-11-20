---
name: month-end-close-checklist
description: Builds a month-end close checklist for a small company with each task, an owner, and a business-day offset from month end, covering transaction capture, bank and card reconciliations, receivables and payables, accruals and prepaids, deferred revenue, payroll, fixed assets, reports, and review and lock. Use when someone asks for a month-end close checklist, a close calendar, "how do we close the books", a bookkeeping checklist, or wants to tighten a slow or messy close.
---

# Month-end close checklist

A close is done when the numbers for the month are reconciled, reviewed by someone other than the preparer, and locked. A checklist makes that repeatable: every task has one owner and a day it's due, counted in business days from month end, and the review step is never optional.

## When to use

- Setting up the first proper close at a small company.
- The close takes too long or numbers keep changing after the reports go out.
- A new bookkeeper or outsourced accountant starts.
- Not for checking a single supplier invoice: use invoice-check. Not tax filing deadlines: those depend on your jurisdiction; confirm with your accountant.

## What you need

- Who does the books: in-house, an outsourced bookkeeper, an accountant, the founder. Names or roles.
- The accounting system and what's connected (bank feeds, card feeds, payroll, billing such as Stripe).
- What the business has: subscriptions or annual prepayments (deferred revenue), inventory, payroll, contractors, fixed assets, more than one entity or currency.
- Target close day, if any. Our default for a small company with no inventory: day 5. If not given, use it and say so.
- If something isn't given, include the task with "[check: applies?]" rather than dropping it.

## Steps

1. **List the tasks in close order.** Use this order: capture and code transactions; reconcile cash (bank, cards, payment processors); reconcile receivables and payables to the ledger; post accruals and prepaids; recognize deferred revenue; record and check payroll; fixed assets and depreciation; produce reports and variance review; review, approve, and lock the period.
2. **Fit tasks to the business.** Drop tasks that clearly don't apply (no inventory, no fixed assets) and say so in one line. Add tasks the input calls for: multi-currency revaluation, intercompany, sales tax or VAT accruals.
3. **Assign one owner per task.** A named person or role from the input. Preparer and reviewer must be different people for reconciliations and the final review; if the company has one person doing everything, flag it and suggest the founder or outside accountant reviews.
4. **Set day offsets.** Day 0 is the last day of the month; days after are business days. Our default for a day-5 close: day −2 to 0 pre-close (chase receipts, confirm payroll), days 1 to 2 transactions and cash, days 3 to 4 accruals, deferred revenue and subledgers, day 5 reports, review, and lock.
5. **Define done for each task.** A reconciliation is done when the ledger balance matches the statement and every difference is explained. An accrual is done when it has support (an invoice, contract, or estimate with its basis). Write the done rule in a few words.
6. **Add the review and lock.** Reviewer checks the balance sheet line by line, compares the P&L to last month and budget, and asks about any big change; then the period is locked in the system so later edits need approval.

## Output format

```markdown
# Month-end close — [company] — target day [n]

**Owners:** [names and roles] · **System:** [accounting system]
**Not included:** [tasks dropped and why]

| Day | Task | Owner | Reviewer | Done when |
|---|---|---|---|---|
| −2 | [Task] | [Name] | | [Rule] |
| 1 | [Task] | [Name] | [Name] | [Rule] |

## Notes
- [Risks, e.g. one-person close, missing feeds]
- [check: items to confirm]
```

## Example

**Input:**

> Pinewell (12 people, SaaS). Xero with bank and card feeds. Stripe for billing; about 30% of customers prepay annually. Payroll through an outside provider, paid on the 25th. No inventory. A few laptops capitalized. Bookkeeper: Femi (part-time, outsourced). Founder Ada reviews. Wants close by day 5.

**Output:**

```markdown
# Month-end close — Pinewell — target day 5

**Owners:** Femi (bookkeeper), Ada (founder, reviewer) · **System:** Xero
**Not included:** inventory (none).

| Day | Task | Owner | Reviewer | Done when |
|---|---|---|---|---|
| −2 | Chase missing receipts and card explanations from staff | Femi | | All card lines have a receipt or note |
| 0 | Confirm payroll report from the provider received | Femi | | Report in hand for the 25th run |
| 1 | Code all bank and card transactions | Femi | | No uncoded lines |
| 1 | Reconcile bank accounts | Femi | Ada | Ledger = statement, differences explained |
| 2 | Reconcile cards and Stripe payouts (fees, refunds) | Femi | Ada | Stripe payouts match bank deposits |
| 2 | Reconcile receivables and payables to aging reports | Femi | Ada | Aging totals = ledger |
| 3 | Post accruals (bills received after month end for this month) | Femi | Ada | Each accrual has an invoice or basis |
| 3 | Recognize deferred revenue for annual prepayments | Femi | Ada | Schedule ties to the deferred revenue balance |
| 3 | Record payroll and check against the provider report | Femi | Ada | Gross pay, taxes, and net match |
| 4 | Book laptop depreciation | Femi | | Fixed asset register ties to ledger |
| 4 | P&L, balance sheet, cash flow; variance vs last month | Femi | | Reports drafted |
| 5 | Review balance sheet and big P&L changes | Ada | | Questions answered |
| 5 | Lock the period in Xero | Ada | | Lock date set |

## Notes
- Femi prepares and Ada reviews; keep the two roles split.
- [check: does Pinewell need a sales tax or VAT accrual?]
```

## Checks before you send

- [ ] Every task has one owner and a day offset.
- [ ] Every reconciliation and the final review has a reviewer who isn't the preparer, or the gap is flagged.
- [ ] Deferred revenue is included if the business takes prepayments.
- [ ] The last task is review and lock.
- [ ] Tasks that may apply but weren't confirmed are marked "[check: ...]", not dropped.

## Common mistakes

- Reconciling bank but not the payment processor; fees and refunds hide there.
- Booking an annual prepayment as revenue in the month it's paid.
- Skipping the lock, so last month's numbers change after the report went out.
