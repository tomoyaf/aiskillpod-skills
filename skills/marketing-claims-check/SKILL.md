---
name: marketing-claims-check
description: Checks marketing copy (landing page, ad, email, sales deck, social post) for risky claims such as unproven superlatives, comparisons with competitors, testimonials and reviews, "free" offers, pricing and discount claims, and health or finance claims, then asks for the substantiation each one needs. Use when someone asks "can we say this?", wants copy checked before launch, or a claim like "#1", "fastest", or "guaranteed" appears.
---

# Marketing claims check

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A claim is safe to publish when the team could show the proof tomorrow if a customer, competitor, or regulator asked. This check finds every claim a reader could take as a fact and asks for that proof before launch, not after.

## When to use

- Before publishing a landing page, ad set, email campaign, press release, or sales deck.
- When copy says "#1", "fastest", "best", "guaranteed", "free", "save 40%", or names a competitor.
- When a testimonial, review, or customer logo is added.
- Not for brand voice or conversion edits. This check is about whether claims are supportable.

## What you need

- The copy, exactly as it will appear, including footnotes and fine print.
- Where it runs (website, paid ads, email, a specific country). If unknown, ask once; rules and ad platform policies differ.
- Any proof the user already has: data, studies, customer permissions, pricing history. If none is given, every factual claim gets "[check: proof]".
- The industry, because health, finance, children, and environmental claims carry extra risk.

## Steps

1. **List every claim.** A claim is any sentence a reader could check: numbers, rankings, comparisons, results, "only", "first", "no. 1", "guaranteed", "secure", "compliant", "certified". Puffery ("delightful", "you'll love it") is listed but rated low.
2. **Classify each one.** Superlative, comparative (names or implies a competitor), result or performance, testimonial or endorsement, price or discount, "free" or trial, safety or compliance, health, finance or earnings, environmental.
3. **Name the proof each needs.** The FTC's policy statement on advertising substantiation says objective claims need a reasonable basis before they run, and a claim like "tests prove" needs at least the level of proof it states. Superlatives and comparisons: a current, like-for-like test or third-party data, with date and method. Results: data from real customers, and a note on whether typical users get them. Testimonials: the FTC's Endorsement Guides say an endorsement must reflect the endorser's honest experience, material connections (payment, free product, employment) are disclosed clearly, and exceptional results come with what people can generally expect. Add written permission as our default. Prices and discounts: the reference price was actually charged; the discount's terms. "Free": the FTC's guide on the word "free" (16 CFR 251.1) says terms and conditions are stated clearly and conspicuously at the outset, and that an asterisk to a footnote is not enough; it also defines a "regular price" as one actually charged, generally for 30 days.
4. **Rate risk.** High: health, finance, earnings, safety, compliance or certification claims, named competitor comparisons, "guaranteed", and anything with no proof. Medium: unnamed comparisons, performance numbers with proof older than 12 months (our default cut-off), testimonials without written permission. Low: puffery. These tiers are our default, not a legal standard.
5. **Check the fine print.** A footnote must not contradict the headline. If the headline says "free" and the conditions sit only in a footnote ("card required, billed after trial"), flag it: the FTC guide wants them next to the offer.
6. **Suggest a safer line.** For each high or medium claim, offer a version that says only what the proof supports ("Up to 3x faster exports in our March 2026 test of 200 files" instead of "The fastest exports").
7. **Write the table and questions.** Questions about what a law or regulator requires go to counsel as "[ask counsel: ...]".

## Output format

```markdown
# Marketing claims check — [asset], [channel], [date]

_Not legal advice. Flags claims and the proof they need, for review by counsel._

| # | Claim (quote) | Type | Risk | Proof needed | Proof we have | Safer line |
|---|---|---|---|---|---|---|
| 1 | "[quote]" | [type] | [high/medium/low] | [what would back it] | [given / check: proof] | "[rewrite]" |

## Fine print gaps
- [headline vs footnote, or "none"]

## Questions for counsel
- [ask counsel: ...]

## Ready to publish?
[No: [n] high-risk claims without proof / Yes, once [items] are confirmed]
```

## Example

**Input:** Jonas at Tidewell (expense app), landing page for the US. Proof given: an internal test in May 2026 where 40 users submitted receipts in an average of 11 seconds.

> The #1 expense app for startups. Submit receipts in seconds, 5x faster than Expensify. "Tidewell saved us 20 hours a month" — Finance lead. Free forever. Card required.

**Output:**

```markdown
# Marketing claims check — Tidewell landing page, US website, 4 November

_Not legal advice. Flags claims and the proof they need, for review by counsel._

| # | Claim (quote) | Type | Risk | Proof needed | Proof we have | Safer line |
|---|---|---|---|---|---|---|
| 1 | "The #1 expense app for startups" | superlative | high | Ranking source, date, and what "#1" measures | check: proof | "Expense app built for startups" |
| 2 | "Submit receipts in seconds" | performance | low | Timing data | May 2026 test, 40 users, 11 seconds average | "Submit a receipt in about 11 seconds" |
| 3 | "5x faster than Expensify" | comparative, named | high | Like-for-like test against Expensify, method, date | check: proof | Remove, or state the test and its method |
| 4 | "saved us 20 hours a month" — Finance lead | testimonial | medium | Real customer, written permission, exact words, any payment disclosed | check: proof | Same quote with name and company, once permission is on file |
| 5 | "Free forever. Card required." | free | high | What is free, limits, what triggers a charge | check: proof | "Free plan for up to [n] users. Card required to start." |

## Fine print gaps
- "Free forever" sits next to "Card required" with no word on when the card is charged.

## Questions for counsel
- [ask counsel: what do we need on file before naming Expensify in a comparison in the US?]
- [ask counsel: does "free" with a card required need extra disclosure in the US?]

## Ready to publish?
No: 3 high-risk claims without proof (#1, #3, #5).
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] Every checkable sentence in the copy has a row.
- [ ] Each high or medium claim has a safer line limited to the proof given.
- [ ] Proof marked "given" was actually provided by the user, with date or source.
- [ ] No sentence states what a law or regulator requires; those are questions for counsel.
- [ ] The verdict counts the high-risk claims without proof.

## Common mistakes

- Treating a competitor comparison as fine because it's "obviously true". Proof must exist on paper.
- Fixing the headline and missing the same claim repeated in the ad, email subject, or alt text.
- Accepting a testimonial from a team member or investor without disclosing the relationship. The FTC says listing an employer on a profile page isn't enough disclosure for an employee.
