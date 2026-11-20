---
name: payment-reminder-email
description: Writes overdue invoice reminder emails by stage (a few days before due, 1 week, 2 weeks, and 30 or more days overdue) that are firm but polite, carry the invoice number, amount, due date, and how to pay, and escalate in tone only as the delay grows. Use when an invoice is about to fall due or is unpaid, when someone asks for a payment reminder, a past-due notice, a dunning email, a collections email, or a polite chase for an overdue invoice.
---

# Payment reminder email

A good reminder gets paid without hurting the relationship. Every email makes paying easy: invoice number, amount, due date, and how to pay are in the first lines. Tone gets firmer by stage, and the email states the next step only if the company will actually take it.

## When to use

- An invoice is due in a few days and the customer has a history of paying late.
- An invoice is 7, 14, or 30 or more days overdue.
- A customer went quiet after a first reminder.
- Not for checking an invoice you received: use invoice-check. Not legal demand letters; late fees and interest depend on your contract and local law.

## What you need

- Invoice number, amount and currency, issue date, due date, what it covers.
- How to pay: payment link, bank details, or where to find them. If missing, write "[check: payment details]". Never write bank details from memory.
- The customer contact's name, and the sender's name and role.
- The terms: payment terms, any late fee or interest in the contract. If the contract terms aren't given, don't mention fees.
- History: earlier reminders, any dispute or promise to pay.

## Steps

1. **Pick the stage from the days overdue.** Before due (3 to 5 days before): friendly heads-up. 7 days overdue: polite reminder, assume an oversight. 14 days: firmer, ask for a payment date. 30 or more days: formal, state the consequence the company has decided on. These stages are our default; use the company's own schedule if given.
2. **Put the facts first.** Subject line names the invoice number and status: "Invoice 1042 — due Friday" or "Invoice 1042 — 14 days overdue". The first 2 lines give amount, due date, and how to pay.
3. **Match tone to stage.** Before due and 7 days: warm, no blame, "in case it slipped through". 14 days: direct, ask for a date, offer to resolve any problem with the invoice. 30 or more: formal, short, state the next step and the date it happens.
4. **State consequences only if they're real and allowed.** Late fees, interest, pausing service, or passing to collections only if the input says the contract allows it and the company will do it. Quote the contract term if given. In the UK, businesses can claim statutory interest (Bank of England base rate plus 8 points) and a fixed recovery fee on late business-to-business payments; mention them only if the company has decided to claim them.
5. **Handle disputes and partial payments.** If the customer disputed the invoice, don't send a standard reminder; acknowledge the dispute and address it. If they paid part, state the balance.
6. **Make replying easy.** End with one ask: pay via [link], or reply with a payment date, or tell us if something is wrong with the invoice. Copy the person who approves invoices if known, at 14 days or later.

## Output format

```markdown
**Subject:** Invoice [number] — [due on date / [n] days overdue]

Hi [name],

[Stage-appropriate opening, 1 sentence.]

- **Invoice:** [number], issued [date]
- **Amount:** [amount, currency] [balance if partial]
- **Due:** [date]
- **Pay:** [link or how to pay, or "[check: payment details]"]

[1–2 sentences: the ask, and the next step if any.]

[Sign-off: name, role]
```

## Example

**Input:**

> Invoice INV-2207 from Quill & Co to Orbit Retail, 4,800 EUR, issued 1 March, due 31 March (net 30), for March design retainer. Pay by link: pay.quillco.example/2207. Contact: Sasha Klein. Sender: Tom Ruiz, finance. No contract late-fee terms given. Today: 14 April (14 days overdue). A 7-day reminder was sent 7 April, no reply.

**Output:**

```markdown
**Subject:** Invoice INV-2207 — 14 days overdue

Hi Sasha,

I'm following up on invoice INV-2207, which is now 14 days past due.

- **Invoice:** INV-2207, issued 1 March, March design retainer
- **Amount:** 4,800 EUR
- **Due:** 31 March
- **Pay:** pay.quillco.example/2207

Could you pay this week, or reply with the date it will be paid? If anything on the invoice is wrong or needs a different approver, tell me and I'll sort it out.

Tom Ruiz, Finance, Quill & Co
```

## Checks before you send

- [ ] Subject line has the invoice number and its status.
- [ ] Amount, due date, and how to pay appear before any explanation.
- [ ] Every number and payment detail comes from the input or is "[check: ...]".
- [ ] Late fees, interest, or service pauses appear only if the input says the contract allows them.
- [ ] Tone fits the stage; no threats at 7 days, no "just checking in" at 30 or more.
- [ ] The email ends with one clear ask.

## Common mistakes

- Burying the amount in paragraph 3. Put it in the first lines.
- Threatening collections the company won't actually use. It weakens every later email.
- Sending a standard chase after the customer disputed the invoice.
