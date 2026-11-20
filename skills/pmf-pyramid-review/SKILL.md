---
name: pmf-pyramid-review
description: Reviews a product's path to product-market fit with the five layers Dan Olsen describes in The Lean Product Playbook - target customer, underserved needs, value proposition, feature set and user experience - states the hypothesis at each layer with its evidence, finds the lowest weak layer, and plans the next minimum viable product test. Use when someone asks about product-market fit, the product-market fit pyramid, The Lean Product Playbook, which customer needs to target, an MVP scope, why a product isn't catching on, or how to test a product idea step by step.
---

# Product-market fit pyramid review

Dan Olsen's The Lean Product Playbook (Wiley, 2015) lays out a Lean Product Process for reaching product-market fit: determine the target customers, identify their underserved needs, define the value proposition, specify the minimum viable product (MVP) feature set, create an MVP prototype, test it with customers, and iterate. He arranges the parts as a pyramid of five layers. The bottom two, the target customer and their underserved needs, are the market. The top three, value proposition, feature set and user experience (UX), are the product. Each layer rests on the one below, so a problem at a low layer can't be fixed by polishing a higher one. This skill writes the hypothesis for each layer, grades the evidence, and plans the next test at the lowest weak layer.

## When to use

- A product has users, but usage or sales don't take off and the team can't say why.
- Before building an MVP, to decide what goes in it.
- When a team debates features while nobody agrees who the customer is.
- Not for one A/B test's design: use experiment-plan. Not for scoring a backlog: use feature-prioritization. Not for testing a business idea's riskiest assumption in general: use build-measure-learn.

## What you need

- Who the product is for, in the team's words, and who actually uses or buys it.
- The needs the team believes it serves, and the evidence (interviews, usage, support tickets).
- What makes the product better than alternatives, and the current features.
- Usage and retention data, and what users say about the experience.
- Mark any layer without evidence "[no evidence]". Never invent interview results or metrics.

## Steps

1. **Write the target customer hypothesis.** One narrow description: who, in what situation. Note evidence that these people use or buy the product.
2. **List underserved needs.** For each need, rate how important it is to the customer and how satisfied they are with today's options. Olsen's point: the opportunity is in needs that are important and poorly met. Separate the problem (what customers need) from the solution (what you build).
3. **Write the value proposition.** Name the 3 to 5 needs the product will meet better than alternatives, the ones where it will merely match them, and the ones it won't address. Name the main alternatives.
4. **Check the feature set.** Map each feature to a need from the value proposition. List features that serve no chosen need (cut candidates) and chosen needs with no feature (gaps). Define the MVP as the fewest features that test the value proposition.
5. **Check the UX.** Note whether users can find and use the features that carry the value proposition, with evidence (usability tests, drop-off points, support tickets).
6. **Grade each layer.** Strong (evidence from customers' behavior), weak (opinions or a few anecdotes), or none. Find the lowest layer that is weak or none.
7. **Plan the next test.** Design one test for that layer: interviews for the bottom two layers, a landing page or prototype for the value proposition, a clickable or working MVP for features and UX. State what result would confirm or change the hypothesis.

## Output format

```markdown
# Product-market fit pyramid review: [product]

## The five layers
| Layer | Hypothesis | Evidence | Grade (strong / weak / none) |
|---|---|---|---|
| Target customer | | | |
| Underserved needs | | | |
| Value proposition | | | |
| Feature set | | | |
| UX | | | |

## Needs, by importance and satisfaction
| Need | Importance (1–5) | Satisfied today (1–5) | Opportunity |
|---|---|---|---|

## Value proposition
**Better than alternatives at:** [needs] · **Match on:** [needs] · **Won't address:** [needs]
**Main alternatives:** [list]

## Feature fit
**Cut candidates:** [features serving no chosen need] · **Gaps:** [chosen needs with no feature]
**MVP:** [fewest features]

## Lowest weak layer
**[layer]** — [why]

## Next test
**Test:** [what] · **With:** [who, how many] · **Confirms if:** [result] · **Changes the hypothesis if:** [result]
```

## Example

**Input:** "We built a shared shopping-list app for families in Brazil. 3,000 sign-ups from an Instagram campaign; 9% still use it after a month. Features: shared lists, recipe import, price comparison across supermarkets, meal planner, barcode scanner. We think it's for 'busy parents'. Interviews: 6 people, 4 of them said the price comparison was the only reason they'd pay. Support tickets mostly ask why prices are out of date. We have no data on who the 9% are."

**Output:**

```markdown
# Product-market fit pyramid review: family shopping-list app

## The five layers
| Layer | Hypothesis | Evidence | Grade |
|---|---|---|---|
| Target customer | "busy parents" | 3,000 sign-ups from Instagram; who the 9% are is unknown | weak |
| Underserved needs | saving money on groceries; coordinating the list | 4 of 6 interviewees named price comparison | weak |
| Value proposition | [check: not stated] | — | none |
| Feature set | 5 features | no usage by feature in the input | none |
| UX | — | tickets about out-of-date prices | weak |

## Needs, by importance and satisfaction
| Need | Importance | Satisfied today | Opportunity |
|---|---|---|---|
| Know where groceries are cheapest | 4 of 6 say so [check: rate 1–5 in interviews] | [check] | likely high |
| Share one list across the family | [check] | [check] | [check] |
| Plan meals | [check] | [check] | [check] |

## Value proposition
**Better than alternatives at:** [check: price comparison, if prices can be kept current] · **Match on:** shared lists · **Won't address:** [check]
**Main alternatives:** [check: WhatsApp messages, paper lists, supermarket apps]

## Feature fit
**Cut candidates:** meal planner, barcode scanner, recipe import [check: usage]
**Gaps:** up-to-date prices (the tickets)
**MVP:** a shared list with current prices for the family's usual supermarkets.

## Lowest weak layer
**Target customer** — "busy parents" is broad, and nobody knows who the 9% who stayed are.

## Next test
**Test:** interview 10 of the users still active after a month, and look at their usage by feature. · **With:** the 9% [check: how many reachable] · **Confirms if:** they share a narrower profile (for example, families who shop at several supermarkets to save money). · **Changes the hypothesis if:** they have no common profile or need.
```

## Checks before you send

- [ ] Every layer has a hypothesis and a grade with evidence from the input.
- [ ] Needs are separated from features.
- [ ] Each feature maps to a need, or is listed as a cut candidate.
- [ ] The next test targets the lowest weak layer, with results that confirm or change the hypothesis.
- [ ] No interview result or metric is invented.

## Common mistakes

- Starting at the top. Polishing UX can't fix a vague customer or an unimportant need.
- A target customer like "everyone who shops". Narrow it until the needs are shared.
- Treating a feature request as a need. Ask what problem the request solves.
- An MVP with every feature. The MVP tests the value proposition with the fewest features.
