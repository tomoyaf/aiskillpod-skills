---
name: quote-email
description: Writes the email that sends a price quote or pricing proposal to a buyer, stating what's included, the price and payment terms, the date the quote is valid until, exactly how to accept, and a one-line reminder of the value they said they want. Use when someone needs to send a quote, pricing email, estimate, or "here's the price" email after a call, or asks how to word a quote so the buyer can say yes.
---

# Quote email

A quote email should let the buyer say yes without another call. Put the price where they can't miss it, say what it buys in their words, and make accepting one step. Never hide the number under three paragraphs of thanks.

## When to use

- After a call where the buyer asked for a price, a quote, or an estimate.
- When a formal quote document is attached and needs a covering email.
- When resending a revised quote after a scope or price change.
- Not for negotiating a price objection: use objection-handling first, then send the revised quote with this skill.

## What you need

- What's included: products, quantities, services, and what's not included.
- Price, billing period, payment terms, currency, and taxes.
- The validity date. If none is given, ask once; if still none, use 30 days from the issue date (a common default: Xero's guide says most Australian businesses use 30 days from issue) and mark "[assumption]".
- How to accept: sign a link, reply "yes", issue a PO. If unknown, ask.
- The buyer's stated goal from the call, in their words. If you don't have it, skip the value line rather than invent one.
- Never invent a price, discount, or term. Anything not in the input becomes "[check: ...]".

## Steps

1. **Write the subject so it's findable.** "[Company] quote: [what], valid to [date]". The buyer will search their inbox for it in 3 weeks.
2. **Open with the price (our default).** The first 2 lines say what this is and the total. No "I hope you're well", no "As promised".
3. **List what's included as bullets.** One line each, in the buyer's terms ("onboarding for your 3 clinics", not "Implementation package B"). Add one "Not included" line if anything they might assume is excluded.
4. **State terms plainly.** A quote is generally treated as binding once the buyer accepts it, so vague terms turn into disputes. Billing period, payment terms (for example "net 30"), currency, tax, and the validity date in bold. If there's a discount, state the list price, the discount, and the condition and end date on it.
5. **Make accepting one step.** One instruction: "Reply 'approved' and I'll send the agreement today" or "Sign here: [link]". If they need a PO, say what the PO must reference.
6. **Add one value line.** Tie the price to the outcome they named: "This covers the no-show reminders you said would save the front desk about 6 hours a week." One sentence, their number, or skip it.
7. **Close with the next date.** Name what happens if you don't hear back: "I'll check in Friday 12 June." Our default: keep the whole email under 150 words, not counting the included list.

## Output format

```markdown
**Subject:** [Company] quote: [what], valid to [date]

Hi [first name],

Here's the quote for [what], at [total] [per period]. [One-line pointer to the attached quote, if any.]

**Included**
- [item in the buyer's words]
- [item]

**Not included:** [item, or remove this line]

**Terms**
- [Price breakdown, if more than one line item]
- Billed [period], [payment terms], [currency], [tax note]
- **Valid until [date]**

**To accept:** [one step]

[One value line in the buyer's words, or remove.]

I'll check in on [day date] if I haven't heard back. [Optional: one line on who to loop in.]

[Name]
```

## Example

**Input:** Quote for Harbor Dental, 3 locations, appointment reminders. 450 a month per location, billed annually = 16,200 a year, net 30, excl. VAT. Setup included. SMS over 2,000 a month per location billed separately at 0.04 each. Valid 30 days. Accept by e-signature link. Buyer (Jen Park, practice manager) said reminders would "stop us losing Monday mornings to no-shows". Sent by Sam on Wednesday 4 November 2026.

**Output:**

```markdown
**Subject:** Harbor Dental quote: appointment reminders for 3 locations, valid to 4 December

Hi Jen,

Here's the quote for appointment reminders at all 3 Harbor Dental locations: 16,200 a year, billed annually. The full quote is attached.

**Included**
- Appointment reminders for all 3 locations
- Setup
- Up to 2,000 SMS a month per location

**Not included:** SMS above 2,000 a month per location, billed at 0.04 each.

**Terms**
- 450 a month per location × 3 locations × 12 months
- Billed annually, net 30, excl. VAT
- **Valid until 4 December**

**To accept:** sign here: [e-signature link]. I'll start setup the same week.

This is the piece you said would stop you losing Monday mornings to no-shows.

I'll check in on Wednesday 11 November if I haven't heard back.

Sam
```

## Checks before you send

- [ ] The total price appears in the first 2 lines and matches the attached quote.
- [ ] The validity date is in the subject and in bold in the terms.
- [ ] Accepting takes one action, and the email says what it is.
- [ ] Every price, term, and discount comes from the input; anything else is marked "[check: ...]".
- [ ] The buyer's name and company are spelled as in their own email signature.
- [ ] Under 150 words outside the included list.

## Common mistakes

- Burying the price below a recap of the call. The recap belongs in follow-up-email.
- Offering a discount the buyer didn't ask for. It teaches them the first number wasn't real.
- Ending with "Let me know if you have any questions". End with the date you'll check in.
