---
name: thiel-style-monopoly-check
description: Checks whether a business or product could come to dominate its market, against the points Peter Thiel made in his 2014 lecture "Competition is for Losers" (How to Start a Startup, published by Y Combinator) - value created versus value captured, an honest market definition, a small market to take over first and expand from, and the four characteristics he named (proprietary technology about an order of magnitude better, network effects, economies of scale, branding), plus whether the position can last. Use when sizing a market for a new product, reviewing a pitch or strategy that claims a big market, choosing a beachhead segment, or when someone asks whether a business has a moat, could become a monopoly or is the last mover.
---

# Thiel-style monopoly characteristics check

These are principles Peter Thiel has described publicly in his 2014 lecture "Competition is for Losers", part of the How to Start a Startup series published by Y Combinator. Not affiliated with or endorsed by Peter Thiel or their companies. The skill reviews the user's business or product against the points of that lecture and says where its position is strong, where it is weak, and which small market to take over first.

## Ground rules

- Do not attribute quotes or opinions to Peter Thiel beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Peter Thiel; review the user's material against the principles below.
- "Monopoly" here is the lecture's business sense: a large share of a market that the company has defined honestly. The skill never advises on conduct that could raise competition-law questions; if the user's question turns on that, say a lawyer should review it.
- Never invent market sizes, shares or growth rates. Unknowns are marked [check: ...] with where to find them.
- The lecture is cited from Y Combinator's video; the skill paraphrases it and does not quote it as exact wording.

## The principles

1. **Value created and value captured are separate.** Thiel said a valuable company does two things: it creates value for the world and it captures some share of that value, and the two are independent variables. Source: "Competition is for Losers", 2014 lecture (How to Start a Startup, lecture 5), video published by Y Combinator.
2. **Competition competes profits away.** He contrasted perfect competition, where profits are competed away, with monopoly, and argued that founders should aim for monopoly rather than competition. Source: same.
3. **Define the market honestly.** He said businesses misdescribe their markets in opposite directions: a company with no monopoly describes its market as a narrow intersection of categories so that it looks unique, and a monopoly describes its market as the union of large markets so that it looks small within it. Source: same.
4. **Start with a small market and take it over.** He said the way to a large share of a market is to start with a really small market, take over the whole of it, and expand in concentric circles; going after a giant market on day one usually means the categories are badly defined and there will be too much competition. His example was PayPal starting with power sellers on eBay. Source: same.
5. **The four characteristics.** He named four: proprietary technology, with a rough rule of thumb of being an order of magnitude better than the next best thing on some key dimension; network effects, which are valuable but very hard to get started, since a product must be valuable to its very first users too; economies of scale, typical of businesses with very high fixed costs and very low marginal costs, often software; and branding, which he called real but said he doesn't invest in when it is the only advantage. Source: same.
6. **Last, not first.** He said that rather than being the first mover, the better aim is to be the last company in a category, because most of a company's value lies far in the future, so the position must last. Source: same.

## When to use

- Sizing a market or choosing a first segment for a new product.
- Reviewing a pitch or strategy that claims a very large market.
- Asking whether a business has a durable position or is one of many similar offers.
- Not for checking whether the underlying thesis is non-consensus (use thiel-style-contrarian-check), and not for a feature comparison against named rivals (use competitor-battlecard).

## What you need

- The product and who buys it.
- How the user describes the market today, and its size if known.
- The alternatives a customer uses now, including doing nothing.
- What the product does better, with numbers if possible.
- Costs: what is fixed, what each extra customer costs.

## Steps

1. **Created and captured.** Write what value the product creates and how much of it the company keeps (price, retention, switching cost). Mark weak capture plainly (principle 1).
2. **Redefine the market both ways.** Write the market as the user describes it, then as a union (all the ways customers solve this problem, including substitutes) and as an intersection (the narrow niche). Say which description is honest and why (principle 3).
3. **Count the competition in the honest market.** List the real alternatives. Many near-identical alternatives means profits will be competed away (principle 2).
4. **Pick the small market to take over.** Name a segment small enough to win most of, the reason it's reachable, and the next two concentric circles after it (principle 4).
5. **Score the four characteristics.** For each, write the evidence and a rating of strong, weak or absent. For proprietary technology, name the key dimension and how many times better than the next best alternative the product is [check: ...] (principle 5).
6. **Test durability.** What would let the company still lead the category years from now? What would let a later entrant replace it (principle 6)?
7. **Verdict and next move.** One line on the position, and the single thing that would most strengthen it.

## Output format

```markdown
# Monopoly check: [business or product]
These are principles Peter Thiel has described publicly. Not affiliated with or endorsed by Peter Thiel or their companies.

## Value created and captured
**Created:** [ ] · **Captured:** [ ] · **Gap:** [ ]

## Market, three ways
| As described | As a union | As an intersection | Honest definition |
|---|---|---|---|

## Competition in the honest market
- [Alternative] - [how close a substitute]

## The small market to take over first
**Segment:** [ ] · **Why we can win most of it:** [ ] · **Next circles:** [ ] → [ ]

## The four characteristics
| Characteristic | Evidence | Rating |
|---|---|---|
| Proprietary technology ([dimension], [n]x the next best) | | strong / weak / absent |
| Network effects | | |
| Economies of scale | | |
| Branding | | |

## Durability
[What keeps it the last company in the category; what could replace it]

## Verdict
[One line] · **Next move:** [one thing]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We make bookkeeping software for freelancers. The bookkeeping software market is worth billions, so there's room for us. Our edge: we read receipts from photos. There are dozens of apps that do this. 70% of our users are freelance translators, because we added a feature that converts foreign-currency invoices at the tax authority's daily rate. Hosting costs are small per user; our cost is the team."

**Output (excerpt):**

```markdown
These are principles Peter Thiel has described publicly. Not affiliated with or endorsed by Peter Thiel or their companies.

## Market, three ways
| As described | As a union | As an intersection | Honest definition |
|---|---|---|---|
| Bookkeeping software (billions) | All ways freelancers keep books, incl. accountants and spreadsheets | Receipt-scanning bookkeeping for freelancers | Receipt scanning is crowded; the honest niche is freelancers invoicing in foreign currencies |

## The small market to take over first
**Segment:** freelance translators who invoice in foreign currencies [check: how many in our country]
**Why we can win most of it:** the currency feature already drew most of our users
**Next circles:** other freelancers paid in foreign currencies → small agencies that pay them

## The four characteristics
| Characteristic | Evidence | Rating |
|---|---|---|
| Proprietary technology (time to book a foreign-currency invoice, [check: n]x faster than a spreadsheet) | Currency conversion at the tax authority's daily rate | weak until measured |
| Network effects | None today; a shared ledger with an accountant could start one | absent |
| Economies of scale | Fixed cost is the team; cost per extra user is small | strong |
| Branding | Known among translators [check: referrals] | weak |

## Verdict
Crowded as described; promising in the translator niche. **Next move:** measure the speed-up on foreign-currency invoices against the next best alternative.
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] The market is written three ways and one honest definition is chosen.
- [ ] A small first market is named with its next circles.
- [ ] All four characteristics have evidence and a rating.
- [ ] Proprietary technology names a key dimension and a multiple, or a [check].
- [ ] Durability is addressed, not only today's position.
- [ ] No market numbers are invented; nothing is quoted from the lecture as exact wording.

## Common mistakes

- Citing a huge market size as evidence of opportunity.
- Defining the market so narrowly that the company is alone in it by construction.
- Rating branding strong because the product has a good name.
- Counting a feature competitors can copy in a month as proprietary technology.
