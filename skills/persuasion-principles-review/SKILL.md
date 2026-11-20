---
name: persuasion-principles-review
description: Reviews a page, email, offer or sales sequence against Robert Cialdini's principles of influence - reciprocity, commitment and consistency, social proof, liking, authority, scarcity and unity - showing which principles it uses, which it misses, and where a use would be false or manipulative, with honest rewrites. Use when someone asks to apply Influence or Cialdini, make a landing page or offer more persuasive, add social proof, check whether urgency or scarcity is honest, or review a sales email for persuasion.
---

# Persuasion principles review

Robert Cialdini's Influence (first published 1984) describes shortcuts people use to decide whether to say yes, and how "compliance professionals" exploit them. The book named six principles: reciprocity, commitment and consistency, social proof, liking, authority and scarcity. A seventh, unity (a shared identity), was added in a later edition. Cialdini's own site describes using them ethically. This skill reviews a piece of persuasion against all seven, and treats a false use (invented scarcity, fake reviews, borrowed authority) as a defect to remove, not an opportunity.

## When to use

- A landing page, offer, email or pitch converts poorly and nobody knows why.
- Before launching a promotion with a deadline, a limited quantity or testimonials.
- To check that urgency, scarcity and social proof are true.
- Not for a line-by-line copy edit: use landing-copy-review. Not for whether claims are legally risky: use marketing-claims-check, which this review hands off to.

## What you need

- The text or a description of the page, email or sequence, and its one goal (sign up, book a call, buy).
- Who it is for and what they believe before reading.
- The true facts available: customer counts, reviews and who wrote them, real deadlines, stock, credentials, free value offered.
- Never invent a testimonial, number, deadline or credential. A principle without a true fact behind it stays unused.

## Steps

1. **State the ask.** Write the single action the reader should take and what they give (money, time, data).
2. **Map the principles in use.** For each of the seven principles, quote the line that uses it, or write "not used".
   - Reciprocity: something useful given first, before the ask.
   - Commitment and consistency: a small first step that fits what the reader already said or did.
   - Social proof: people like the reader doing it, with numbers or names.
   - Liking: similarity, genuine compliments, cooperation, a human voice.
   - Authority: real expertise or credentials, shown, not claimed.
   - Scarcity: a real limit on time or quantity, or what the reader loses by waiting.
   - Unity: a shared identity ("for other clinic owners", "from one founder to another").
3. **Test each use for truth.** For every use, name the fact behind it from the input. Mark any use with no fact behind it as **false** (a countdown that resets, "only 3 left" with no limit, logos of companies that aren't customers). False uses come out first.
4. **Find the missing honest uses.** For each unused principle, check whether a true fact in the input would support it, and draft one line. If no true fact exists, leave it unused and say what fact would be needed.
5. **Check the order.** Persuasion usually lands better when the reader gets value and proof before the ask. Recommend the order of sections.
6. **Hand off claims.** List any statement that is a comparison, a superlative, a testimonial or a deadline, for marketing-claims-check.

## Output format

```markdown
# Persuasion review: [page or email]

**Ask:** [action] · **Reader:** [who]

## Principles in use
| Principle | Line or element | Fact behind it | Verdict (keep / fix / remove) |
|---|---|---|---|

## Remove first
- [false use and why]

## Add (true facts only)
| Principle | Draft line | Fact it rests on |
|---|---|---|

## Unused, and what would be needed
- [principle]: needs [fact]

## Suggested order
1. [section]

## For the claims check
- [statement]
```

## Example

**Input:** "Landing page for our bookkeeping service for Mexican freelancers. Headline: 'Stop drowning in receipts.' A banner says 'Offer ends in 23:59:59' (the timer restarts for every visitor). There's a 'Trusted by top companies' strip with Google and Amazon logos; our clients are freelancers, not those companies. CTA: 'Book a call'. True facts: 214 freelancers use us; 38 left a Google review, average 4.7; our founder was an accountant at the SAT, Mexico's tax authority, for 9 years; we publish a free monthly checklist of SAT deadlines; the price goes from 499 to 599 pesos a month for new clients on 1 March."

**Output:**

```markdown
# Persuasion review: bookkeeping landing page

**Ask:** book a call · **Reader:** freelancers in Mexico who do their own bookkeeping

## Principles in use
| Principle | Line or element | Fact behind it | Verdict |
|---|---|---|---|
| Scarcity | "Offer ends in 23:59:59" timer | None: the timer restarts for each visitor | Remove |
| Social proof / authority | Google and Amazon logos | None: they aren't clients | Remove |
| Liking | "Stop drowning in receipts" | Speaks the reader's problem | Keep |

## Remove first
- The resetting timer: it states a deadline that doesn't exist.
- The logo strip: it implies clients we don't have.

## Add (true facts only)
| Principle | Draft line | Fact it rests on |
|---|---|---|
| Social proof | "214 freelancers use us. 4.7 average from 38 Google reviews." | 214 clients; 38 reviews at 4.7 |
| Authority | "Founded by an accountant who spent 9 years at the SAT." | the founder's 9 years at the SAT |
| Reciprocity | "Get the free monthly SAT deadline checklist." | the checklist exists |
| Scarcity | "New clients pay 499 pesos a month until 1 March, then 599." | the real price change |
| Unity | "Bookkeeping for freelancers, by people who file for freelancers every month." | [check: whether the team are freelancers themselves; drop "by people like you" if not] |

## Unused, and what would be needed
- Commitment and consistency: a small first step, such as the checklist sign-up before the call, then an invitation to book.

## Suggested order
1. Headline and the problem
2. The free checklist (reciprocity)
3. Clients and reviews (social proof), the founder (authority)
4. The price and the 1 March change (scarcity)
5. Book a call

## For the claims check
- "4.7 average from 38 Google reviews"
- "9 years at the SAT"
- The 1 March price change
```

## Checks before you send

- [ ] All seven principles appear in the map, as used or "not used".
- [ ] Every kept or added use names the true fact behind it from the input.
- [ ] False urgency, fake scarcity and borrowed logos or authority are marked remove, never improved.
- [ ] No testimonial, number, deadline or credential is invented.
- [ ] Claims are listed for marketing-claims-check.

## Common mistakes

- Stacking every principle on one page. Two or three true ones beat seven thin ones.
- Fake urgency. Resetting timers and invented limits break trust and may break consumer law.
- Social proof from the wrong crowd. Proof works best from people like the reader.
- Treating the principles as tricks. Cialdini's own site describes using them ethically; using them on false facts is manipulation.
