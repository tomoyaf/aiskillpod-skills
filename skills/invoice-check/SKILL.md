---
name: invoice-check
description: Checks an incoming vendor invoice against the purchase order, contract, or quote - vendor details, amounts, quantity times rate, tax, due date and payment terms, possible duplicates, and changed bank details as a fraud flag - and returns approve or hold with reasons. Use when someone shares a supplier invoice, bill, or PO and asks "can we pay this", to check an invoice, match it to the PO, or review a bill before payment.
---

# Invoice check

The goal is that nothing gets paid that wasn't agreed, nothing gets paid twice, and no payment goes to a fraudster's account. Compare line by line against the agreement, do the arithmetic yourself, and hold whenever bank details changed, however small the invoice.

## When to use

- Before approving a vendor or contractor invoice for payment.
- When an invoice doesn't look like last month's and someone wants a second pair of eyes.
- Matching an invoice to a PO, signed quote, or contract rate card.
- Not for chasing a customer who owes you money (use payment-reminder-email) or for reviewing your own expense claims (use expense-policy-check).

## What you need

- The invoice (text, PDF content, or a photo transcription).
- What was agreed: PO, signed quote, contract, or rate card. If none is provided, say the check is arithmetic and fraud only, and mark every amount "[check: no agreement to compare]".
- Optional: past invoices from this vendor, the vendor's bank details on file, and the delivery or timesheet record.
- Never assume a tax rate, payment term, or legal requirement. Anything not in the inputs is "[check: ...]".

## Steps

1. **Match the vendor.** Legal name, address, tax or VAT number, and invoice addressed to your correct company name. A mismatch with the agreement or past invoices is a hold.
2. **Check bank details first.** Compare account name, number, and bank against the details on file. If they differ, or the invoice or email says "our bank details have changed", the result is hold. The FBI's guidance on business email compromise is to verify account changes through a second channel; our default is a phone call to a number from the contract or your records, never from the invoice or the email. If no details are on file, write "[check: bank details on file]".
3. **Redo the arithmetic.** For every line: quantity × rate = line total. Then subtotal, discount, tax, total. Show each calculation. Any difference over 0 is noted; our default: a difference is a hold unless it's under 1 currency unit from rounding.
4. **Compare to what was agreed and received.** A three-way match checks items, quantities, and prices across the PO, the delivery or timesheet record, and the invoice; without a receipt record it is only a two-way match, so say so. Flag items not on the PO, quantities over what was delivered, and rates higher than agreed. Show the agreed figure next to the invoiced one.
5. **Check tax and terms.** Tax rate and amount as stated in the agreement or on prior invoices; if unknown, "[check: correct tax rate]". Due date against the agreed payment terms (for example, net 30 from invoice date). Note early-payment discounts and late fees.
6. **Look for duplicates.** Our default signs: the same invoice number, the same amount within 60 days, or the same work period already billed. Any match is a hold until explained.
7. **Decide.** Approve only if every check passes. Otherwise hold, with each reason and the one action that clears it. Put the bank detail result in its own line so nobody misses it.

## Output format

```markdown
**Invoice check — [vendor], invoice [number], [date]**

**Result: [Approve / Hold]**
**Bank details:** [Match on file / CHANGED — verify by phone before paying / [check: no details on file]]

| Check | Result | Detail |
|---|---|---|
| Vendor details | [pass/flag] | [detail] |
| Arithmetic | [pass/flag] | [calculation] |
| Matches PO/quote | [pass/flag] | [agreed vs invoiced] |
| Tax | [pass/flag/check] | [detail] |
| Due date and terms | [pass/flag] | [detail] |
| Duplicate | [pass/flag] | [detail] |

**To clear the hold**
1. [Action, who does it]

**Pay:** [amount] by [due date] — only after the hold is cleared.
```

## Example

**Input:** Invoice INV-2207 from Kestrel Print Ltd, dated 3 Oct, net 30. Lines: 500 brochures × 1.20 = 600.00; design fee 150.00. Subtotal 750.00, VAT 20% 150.00, total 900.00. Note: "Please note our new bank: Harbor Bank, acct 55120934." PO 1188: 500 brochures at 1.10, no design fee, net 30. Bank on file: Northgate Bank, acct 20117745.

**Output:**

```markdown
**Invoice check — Kestrel Print Ltd, invoice INV-2207, 3 October**

**Result: Hold**
**Bank details:** CHANGED — Harbor Bank 55120934 vs Northgate Bank 20117745 on file. Verify by phone before paying.

| Check | Result | Detail |
|---|---|---|
| Vendor details | pass | Name matches PO 1188 |
| Arithmetic | pass | 500 × 1.20 = 600.00; 600 + 150 = 750.00; 750 × 20% = 150.00; total 900.00 |
| Matches PO/quote | flag | Rate 1.20 vs 1.10 on PO (+50.00); design fee 150.00 not on PO |
| Tax | check | 20% VAT applied — [check: correct rate for this supply] |
| Due date and terms | pass | Net 30 → due 2 November, matches PO |
| Duplicate | pass | No other INV-2207 found in what was shared |

**To clear the hold**
1. Accounts payable: call Kestrel on the number in the vendor file (not the invoice) to confirm the bank change.
2. Buyer: ask Kestrel to reissue at 1.10 or show an approved rate change, and to remove or justify the design fee.

**Pay:** 660.00 (550.00 + 20% VAT, if the rate is confirmed) by 2 November — only after the hold is cleared.
```

## Checks before you send

- [ ] Every line's arithmetic is shown and re-added.
- [ ] Bank details are compared and stated on their own line.
- [ ] Every agreed vs invoiced difference shows both figures.
- [ ] No tax rate, term, or rule appears that isn't in the inputs; the rest is "[check: ...]".
- [ ] A hold lists one action per reason, with who does it.
- [ ] The phone verification uses a number from your records, never the invoice.

## Common mistakes

- Approving a small invoice with new bank details because "it's only 300". If a fraudulent payment does go out, call your bank at once to request a recall; speed matters.
- Checking the total but not quantity × rate per line; errors cancel out.
- Treating "close enough" to the PO as a match. Show the difference and let the approver decide.
