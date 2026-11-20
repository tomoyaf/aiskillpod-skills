---
name: disruption-threat-check
description: Checks whether a cheaper, simpler or new-market rival could disrupt a business, using Clayton Christensen's ideas from The Innovator's Dilemma - sustaining versus disruptive innovation, low-end and new-market footholds, performance overshoot, and why good management ignores the threat - and plans a response such as a separate unit with its own cost structure. Use when someone asks about the innovator's dilemma, disruptive innovation, a low-cost entrant, whether a startup is a real threat, overserving customers, or whether to launch a cheaper product that may eat into the core one.
---

# Disruption threat check

Clayton Christensen's The Innovator's Dilemma (1997) explains how well-run market leaders lose to entrants. Leaders improve their products for their most demanding customers, which Christensen calls sustaining innovation. An entrant starts with something worse by the leader's measures but cheaper, simpler or more convenient, sold to customers the leader doesn't value: the low end, or people who weren't buying at all. The leader's best customers don't want it and its margins look poor, so ignoring it is the rational choice. The entrant improves until it is good enough for the mainstream, and then the leader's customers move. This skill checks a named rival or idea against that pattern and plans a response.

## When to use

- A cheaper or simpler rival is winning customers the team calls "not our market".
- Customers use a fraction of the product's features, and price pressure is growing.
- The team is deciding whether to launch a low-cost product that could eat into the core one.
- Not for a rival that competes head-on with a better product for the same customers: that is sustaining competition, use competitor-battlecard. Not for the industry's overall profitability: use five-forces-analysis.

## What you need

- The business: product, customers by tier, price points, margins, and how performance is measured.
- The rival or new approach: what it offers, its price, who buys it, how fast it has improved.
- What the most demanding customers ask for, and what typical customers actually use.
- If growth or improvement rates are missing, mark them "[check]". Never invent a rival's numbers.

## Steps

1. **Name the performance measure.** Write the measure the market uses to judge products today (speed, accuracy, capacity, range of features) and what the leader's best customers want next.
2. **Check for overshoot.** Compare what typical customers need with what the product delivers. Signs of overshoot: most customers use few features, they won't pay for the newest improvements, they choose on price or convenience. Rate overshoot low, medium or high with the evidence.
3. **Classify the rival.** Sustaining: better on today's measure for the same customers. Low-end disruptive: good enough for the least demanding customers at a lower cost, often with a different business model. New-market disruptive: makes the job possible for people who weren't buying (cheaper, simpler, available in new places). The low-end and new-market labels come from Christensen's later book, The Innovator's Solution (2003). Say which it is and why.
4. **Test the foothold.** Who buys the rival now, and why does the leader not want them? Check the leader's view: are those customers low margin, small, or outside the sales team's targets? That reluctance is the dilemma.
5. **Estimate the trajectory.** How fast is the rival improving on the measure that matters to the mainstream? When, roughly, would it be good enough for typical customers? Mark guesses "[check]".
6. **Check the value network.** List what makes the rival's model work (cost structure, channel, partners, price) and whether the leader's current organization could match it without changing its own margins and processes.
7. **Plan the response.** Options include: ignore and monitor with a named signal; compete at the low end through a separate unit with its own costs, targets and customers (Christensen's main advice); acquire; or retreat upmarket on purpose. Recommend one, with the signal that would change the decision and the first step.

## Output format

```markdown
# Disruption threat check: [business] vs [rival or approach]

**Date:** [date] · **Owner:** [name]

## Performance measure today
[The measure, and what the best customers want next.]

## Overshoot
**Rating:** low / medium / high
**Evidence:** [features used, willingness to pay, how customers choose]

## The rival
**Type:** sustaining / low-end disruptive / new-market disruptive
**Why:** [reasoning]
**Its foothold:** [who buys it, why we don't want them]

## Trajectory
[Improvement rate and when it might be good enough for typical customers, with [check] marks.]

## Value network
| What makes their model work | Could we match it inside our current organization? |
|---|---|

## Response
**Recommend:** [option] — [why]
**Signal that would change this:** [measurable signal]
**First step:** [action, owner, date]
```

## Example

**Input:** "We sell desktop accounting software to accountancy firms, about 900 euros per seat per year, with deep audit and consolidation features. Our gross margin is 82%. A cloud app called Cuadrix (fictional) sells to freelancers and micro-businesses at 15 euros a month and has none of our audit tools. Our sales team ignores those customers. Two years ago Cuadrix couldn't do multi-currency; now it can, and last quarter it added accountant access. A survey of our users says 70% use only invoicing, bank reconciliation and VAT returns."

**Output:**

```markdown
# Disruption threat check: desktop accounting software vs Cuadrix

**Date:** [date] · **Owner:** [check: owner]

## Performance measure today
Depth of audit and consolidation features; our largest firms ask for more consolidation [check: what the top accounts asked for last].

## Overshoot
**Rating:** high
**Evidence:** 70% of our users use only invoicing, bank reconciliation and VAT returns, which Cuadrix covers [check: VAT coverage by country].

## The rival
**Type:** low-end disruptive, moving toward new-market
**Why:** worse on our measure (no audit tools) but much cheaper and simpler, sold to freelancers and micro-businesses we don't target.
**Its foothold:** micro-businesses; we don't want them because a 15-euro customer doesn't fit an 82% margin model sold by a sales team.

## Trajectory
Multi-currency in two years, accountant access last quarter: it is moving toward the firms that serve its customers. Good enough for small accountancy firms in [check: 1 to 3 years].

## Value network
| What makes their model work | Could we match it inside our current organization? |
|---|---|
| Self-serve sign-up, no sales team | No: our sales targets reward seats at 900 euros |
| Low price per month | Not without lowering the margin the board tracks |
| Accountants invited by their clients | Partly: we have firm relationships, but no client-side product |

## Response
**Recommend:** a separate unit with its own price, costs and targets, building a client-side cloud product that accountants on our software can connect to.
**Signal that would change this:** if Cuadrix's accountant access shows no adoption by firms over [check: period], monitor instead.
**First step:** name a unit lead and a budget outside the core sales targets [check: owner, date].
```

## Checks before you send

- [ ] The rival is classified as sustaining, low-end or new-market, with the reason.
- [ ] Overshoot is rated with evidence from the input.
- [ ] The answer explains why the business's own incentives make the threat easy to ignore.
- [ ] Rival growth and improvement numbers come from the input or are marked "[check]".
- [ ] The response names one option, a signal that would change it, and a first step.

## Common mistakes

- Calling every successful rival disruptive. A better product for the same customers is sustaining competition.
- Testing the threat against today's best customers. They are the last to move.
- Running the low-end response inside the core business, where its margins and targets will starve it.
- Assuming disruption always wins. Christensen describes a pattern, and scholars dispute how often it holds; use the check to ask better questions, not to predict.
