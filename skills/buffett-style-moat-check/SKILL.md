---
name: buffett-style-moat-check
description: Checks a business - your own, a product line, or a company you might buy or partner with - against three ideas Warren Buffett has described in the Berkshire Hathaway shareholder letters - an enduring moat that protects high returns from competitors, a circle of competence whose boundaries you know, and a margin of safety between value and price. Use when a founder asks what protects their business from competitors, whether an acquisition or a big purchase is understood well enough, how much room for error a plan or a price leaves, or for a moat analysis. Not investment advice.
---

# Buffett-style moat and margin-of-safety check

These are principles Warren Buffett has described publicly in the Berkshire Hathaway shareholder letters. Not affiliated with or endorsed by Warren Buffett or their companies. The skill looks at one business through three questions from the letters (what protects it, do we understand it, how much room for error is there) and reports the evidence for each.

## Ground rules

- Do not attribute quotes or opinions to Warren Buffett beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Warren Buffett; review the user's material against the principles below.
- This is not investment advice and makes no buy or sell recommendation on any security. It checks the user's own reasoning.
- A moat is claimed only with evidence (cost data, retention, share, pricing). A claim without evidence is written "[check: evidence]".
- Never invent numbers.

## The principles

1. **An enduring moat.** A truly great business must have an enduring "moat" that protects excellent returns on invested capital, because competitors will keep attacking any business "castle" that earns high returns. The letter names being the low-cost producer or owning a powerful world-wide brand as examples of a formidable barrier. Source: 2007 letter.
2. **Enduring rules out fast change.** The same letter rules out industries prone to rapid and continuous change, and says a moat that must be continuously rebuilt will eventually be no moat at all. Source: 2007 letter.
3. **What builds a moat.** The letters point to brand strength, product attributes and distribution (1993), rock-bottom operating costs (1995), and economies of scale (1996). Sources: 1993, 1995 and 1996 letters.
4. **Circle of competence.** You only have to be able to evaluate companies within your circle of competence; the size of the circle is not very important, but knowing its boundaries is vital. Source: 1996 letter. In 1992 the letter says Berkshire tries to stick to businesses it believes it understands, relatively simple and stable in character. Source: 1992 letter.
5. **Margin of safety.** Berkshire insists on a margin of safety in its purchase price: if the calculated value is only slightly higher than the price, it isn't interested. The letter calls this principle, which Ben Graham emphasised, the cornerstone of investment success. Source: 1992 letter.

## When to use

- A founder or strategy lead asks what protects the business from competitors.
- Before buying a company, a product line, or making a large long-term commitment (a supplier, a building).
- A plan that only works if every assumption goes right.
- Not for valuing a public stock or giving investment advice. Use competitor-battlecard for a sales comparison and unit-economics-check for per-customer economics.

## What you need

- The business: what it sells, to whom, and how it makes money.
- Competitors and what customers would switch to.
- Evidence about returns: margins, return on capital, retention, pricing history, cost per unit versus competitors.
- For a purchase or commitment: the price, and your estimate of value with its assumptions.
- What the people deciding know well, and what they don't.

## Steps

1. **State what the business earns.** Margins and returns on capital from the input. If returns are ordinary, say so: principle 1 is about protecting excellent returns.
2. **Name the candidate moats.** For each source of protection (low cost, brand, distribution, scale, others the user names), write the evidence and how a competitor would try to cross it.
3. **Test "enduring" (principles 1 and 2).** Would the moat still stand in five to ten years? Is the industry changing fast? Does the moat need constant rebuilding (heavy spend just to stay level)? Mark each moat strong, weak or unproven.
4. **Draw the circle of competence (principle 4).** List what the deciders understand well (customers, costs, technology, regulation) and what they don't. Mark where the decision depends on something outside the circle. The boundary matters more than the size.
5. **Size the margin of safety (principle 5).** Compare price (or the plan's cost) with your estimate of value. Show the gap and the assumptions under the value. Recompute with the two most important assumptions made worse. If the gap disappears, the margin is thin.
6. **Report.** One verdict per question, the evidence, what would change it, and what to find out first. No investment recommendation.

## Output format

```markdown
# Moat and margin-of-safety check: [business]
These are principles Warren Buffett has described publicly in the Berkshire Hathaway shareholder letters. Not affiliated with or endorsed by Warren Buffett or their companies. Not investment advice.

## Summary
[Three lines: moat verdict, circle verdict, margin verdict]

## Returns
[Margins, return on capital, from the input]

## Moats
| Candidate moat | Evidence | How a competitor would attack | Enduring? |
|---|---|---|---|

## Circle of competence
| We understand well | We don't | Does the decision depend on it? |
|---|---|---|

## Margin of safety
| | Base case | Worse case ([assumptions changed]) |
|---|---|---|
| Value | | |
| Price or cost | | |
| Margin | | |

## What to find out first
[1-3 items]

## Principles used
[Numbered, with the letter year for each]
```

## Example

**Input:** "We run a regional laundry service for hotels, 18 hotel clients, 34% gross margin (competitors run about 25%, from a trade survey). We're the only plant within 60 km; a new plant costs about 300M yen. Thinking of buying a smaller competitor in the next city for 120M yen; our estimate of its value is 140M, assuming we keep all 9 of its hotel contracts and cut its energy cost by 20% with our process. We've never run a plant in that city."

**Output (excerpt):**

```markdown
These are principles Warren Buffett has described publicly in the Berkshire Hathaway shareholder letters. Not affiliated with or endorsed by Warren Buffett or their companies. Not investment advice.

## Moats
| Candidate moat | Evidence | How a competitor would attack | Enduring? |
|---|---|---|---|
| Low cost | Gross margin 34% vs about 25% in the trade survey | Copy the process | [check: what drives the 9-point gap] |
| Local scale | Only plant within 60 km; a new one costs about 300M yen | Build a plant | Strong while hotel demand holds |

## Circle of competence
| We understand well | We don't | Does the decision depend on it? |
|---|---|---|
| Running a hotel laundry plant | The other city's hotels and their contracts | Yes: value assumes all 9 contracts stay |

## Margin of safety
| | Base case | Worse case (3 of 9 contracts lost, energy saving 10%) |
|---|---|---|
| Value | 140M yen | [check: recompute from contract revenue] |
| Price | 120M yen | 120M yen |
| Margin | 20M yen (about 14% of value) | Likely gone |

## What to find out first
1. The length and termination terms of the 9 hotel contracts.
```

## Checks

- [ ] The attribution, not-affiliated and not-investment-advice lines are in the output.
- [ ] Every moat has evidence or is marked [check].
- [ ] "Enduring" is tested, including how fast the industry changes.
- [ ] The circle shows what the deciders don't know and whether the decision depends on it.
- [ ] The margin of safety is recomputed with worse assumptions.
- [ ] Each principle cites its letter year.

## Common mistakes

- Calling a good product a moat; a moat is what stops a competitor from copying the returns.
- Overstating where the circle of competence ends; the 1996 letter stresses knowing its boundaries.
- Treating the base-case gap as the margin of safety without testing worse assumptions.
