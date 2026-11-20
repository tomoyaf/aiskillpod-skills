---
name: reply-in-our-tone
description: Drafts a customer support reply in the team's own tone, using a short tone guide or 3 past replies the team pastes in. Answers the actual question first, owns mistakes without blame, drops jargon, and ends with one clear next step. Use when a customer email, chat, or ticket needs a reply, when someone asks to "answer this customer", "draft a support reply", "make this sound like us", or to rewrite a reply that sounds cold or defensive.
---

# Reply in our tone

A good support reply answers the question in the first 2 lines, sounds like the same person wrote every reply, and leaves the customer knowing exactly what happens next. Tone is a team decision, not the AI's: it lives in the "Our tone" section below, and the team edits it once.

## Our tone

Edit this section once for your team: paste a short tone guide, or 3 past replies you liked. Until then, use these defaults.

- **Warm.** Use the customer's first name. One friendly line, not three.
- **Direct.** Answer first, explain after. Short sentences.
- **No blame.** Never "you should have", "as stated", "unfortunately you". If the customer misread something, the page was unclear.
- **Answer first.** The first sentence answers the question or says what we did.
- **One next step.** End with a single action: what they do, or what we do and when.
- Sign-off: "[First name], [Team name] support". No "Best regards" chains.
- Words we avoid: [e.g. "ticket", "escalate", "per our policy"].

If past replies are pasted here, copy their length, greeting, sign-off and sentence rhythm. They win over the defaults.

## When to use

- A customer email, chat, or ticket needs a reply.
- A draft reply exists but sounds cold, defensive, or too long.
- A reply has to say no (refund refused, feature missing) without losing the customer.
- Not for incident or outage notices to many customers: use incident-customer-notice.

## What you need

- The customer's message, and the thread if there is one.
- The facts of the answer: what is true, what was done, what the policy is. If a fact is missing, write "[check: ...]" in the draft. Never guess a refund amount, a date, or a feature.
- The "Our tone" section above, edited or default.

## Steps

1. **Find the real question.** Customers often ask 2 things or bury the question under frustration. List each question in one line. If there are more than 2, answer all of them in the order the customer cares about, not the order they wrote.
2. **Answer first.** The first sentence is the answer: "Yes, you can export to CSV", "We refunded the charge today". If the answer is no, say no in the first sentence, then the reason in one line, then what they can do instead.
3. **Own mistakes plainly.** If we got it wrong, say so once: "That was our mistake." Then what we did about it. No "we apologize for any inconvenience this may have caused". One apology, specific to what happened.
4. **Remove jargon.** Replace internal words (SKU, tier, workspace ID, escalate, P2) with what the customer sees on screen. Name buttons and menus exactly as the product shows them, in bold.
5. **Give one next step.** End with a single action, with a time if we own it: "I'll email you by Thursday when the fix ships." If they own it: "Click **Export** and pick CSV." Never "let us know if you have any questions" as the last line.
6. **Match the tone and length.** Apply "Our tone". Default length is 40 to 120 words. A one-line question gets a 2 to 3 sentence answer.

## Output format

```markdown
**Subject:** [Re: their subject, or a short answer-first subject]

Hi [first name],

[Answer in 1–2 sentences.]

[Why or how, 1–3 short sentences or numbered steps if they need to do something.]

[One next step, with a time if we own it.]

[Sign-off from Our tone]

---
Facts to confirm before sending: [list of "[check: ...]" items, or "none"]
```

## Example

**Input:**

> Customer (Dana, Lumen Bakery): I was charged twice this month!! I only have one account. This is the second time this happened and nobody told me why last time.
>
> Facts: duplicate charge confirmed, refund of the second charge issued today, takes 5 to 10 business days to show. Cause: card retry bug, fixed last week. Next step we can offer: check the account on the next billing date and email the customer. Replying: Mira, Panlo support.

**Output:**

```markdown
**Subject:** Re: Charged twice — refund sent today

Hi Dana,

You were charged twice, and that was our mistake. I refunded the second charge today.

The refund takes 5 to 10 business days to appear on your card. The cause was a bug in how we retried failed card payments; we fixed it last week, so it shouldn't happen again. I'm sorry we didn't explain this the first time.

I'll check your account on your next billing date and email you to confirm you were charged once.

Mira, Panlo support

---
Facts to confirm before sending: none
```

## Checks before you send

- [ ] The first sentence answers the question or says what we did.
- [ ] Every question the customer asked has an answer.
- [ ] No blame on the customer, and at most one apology, specific to what happened.
- [ ] No internal word the customer wouldn't see on screen.
- [ ] The last line is one next step, with a time if we own it.
- [ ] Every amount, date and promise is in the facts given, or marked "[check: ...]".

## Common mistakes

- Opening with "Thank you for reaching out" and pushing the answer to paragraph 2.
- Promising a date nobody gave you. Mark it "[check: date]" instead.
- Copying the customer's anger back ("I understand you are very frustrated"). Fix the problem; that shows you understood.
