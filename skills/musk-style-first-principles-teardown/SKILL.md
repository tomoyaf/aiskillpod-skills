---
name: musk-style-first-principles-teardown
description: Breaks a product, service or cost line down to what it is actually made of and prices those inputs, built on the first-principles approach Elon Musk described in his 2013 TED interview and his 2012 Wired interview - list the fundamental inputs, price each at its market rate, compare that floor with the price paid today, and name where the gap comes from. Use when a cost or price is taken as given because the industry has always charged it, when a quote or a bill of materials looks high, when planning a cheaper version of an existing product, or when someone asks for a first-principles cost breakdown or a should-cost estimate.
---

# Musk-style first-principles cost teardown

These are principles Elon Musk has described publicly in his 2013 TED interview with Chris Anderson and his 2012 Wired interview, "Elon Musk's Mission to Mars". Not affiliated with or endorsed by Elon Musk or their companies. The skill takes one thing you buy or make, rebuilds its cost from its basic inputs, and shows how far today's price sits above that floor and why.

## Ground rules

- Do not attribute quotes or opinions to Elon Musk beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Elon Musk; review the user's material against the principles below.
- Never invent prices, quantities or rates. A number the user didn't give and you can't derive is marked [check: ...] with where to find it.
- The floor is a floor, not a target: say plainly that real costs include labour, tooling, overhead, risk and margin, and that a gap is a place to look, not proof of waste.
- Say when the method doesn't fit: a cost driven mostly by regulation, licences or scarce skills has no meaningful materials floor.

## The principles

1. **Reason from fundamentals, not by analogy.** In the TED interview Musk described first-principles reasoning as boiling things down to their fundamental truths and reasoning up from there, as opposed to reasoning by analogy, which he described as copying what others do with slight variations. He added that analogy is how people get through daily life, and that the physics approach is for doing something new. Source: TED 2013, "The mind behind Tesla, SpaceX, SolarCity ...", closing answer.
2. **Price the inputs.** In the Wired interview he described asking what a rocket is made of (aerospace-grade aluminium alloys, some titanium, copper and carbon fibre) and what those materials are worth on the commodity market. Source: Wired, 2012, "Elon Musk's Mission to Mars".
3. **Compare the floor with the price.** He said the materials came to around 2 percent of the typical price of a rocket, which he called a crazy ratio for a large mechanical product, and compared it with roughly 20 to 25 percent for a Tesla car. Source: same interview.
4. **A large gap means something in the market is worth examining.** From that ratio he concluded that a much cheaper rocket should be possible. Two reasons he gave in that interview were a strong aversion to risk, which kept decades-old components in use, and outsourcing through several layers of subcontractors, each adding its own profit. Source: same interview.
5. **Ask for negative feedback.** In the same TED answer he advised paying attention to negative feedback and asking for it, particularly from friends. Source: TED 2013, closing answer.

## When to use

- A price or cost is accepted because "that's what it costs in this industry".
- A supplier quote, a bill of materials or a service fee looks high and you want to know what it should cost.
- You're planning a cheaper version of an existing product or service.
- Not for a full unit-economics model of your own business (use unit-economics-check), and not for comparing vendors on features (use vendor-comparison).

## What you need

- The thing to tear down: a product, a component, a service, or a recurring cost line.
- Today's price or cost, and the quantity it covers.
- What it is made of, as far as you know: materials, parts, hours, licences, data, compute.
- Any market prices you already have for those inputs, with their source.

## Steps

1. **State the analogy.** Write the price as it is usually justified ("industrial label printers cost about this", "agencies charge this per page"). This is the reasoning by analogy to set aside (principle 1).
2. **List the fundamental inputs.** Break the thing down until each line is something with a market price: kilograms of a material, hours of a skill, units of compute, a licence. Stop when a further breakdown wouldn't change the number.
3. **Price each input.** Use the user's figures or a market rate with its source; mark the rest [check: ...] (principle 2). Never fill a gap with a guess presented as a fact.
4. **Add the floor up.** Sum the inputs per unit. Show the ratio floor / price as a percentage (principle 3).
5. **Explain the gap.** For each layer between the floor and the price, name what it pays for: conversion labour, tooling, overhead, margin at each intermediary, risk premiums, legacy specifications (principle 4). Mark which you have evidence for and which are hypotheses.
6. **Pick what to test.** Choose the one or two gap layers most likely to shrink and write a test for each (a quote from a second supplier, making one part in-house, a simpler specification).
7. **Ask for criticism.** List who could tell you the teardown is wrong (a supplier, an engineer, a customer) and what you'll ask them (principle 5).

## Output format

```markdown
# First-principles teardown: [thing]
These are principles Elon Musk has described publicly. Not affiliated with or endorsed by Elon Musk or their companies.

## The analogy we're setting aside
[How the current price is usually justified]

## Today's price
[Price] per [unit] · Source: [quote / invoice / list price]

## Fundamental inputs
| Input | Quantity per unit | Market rate | Source | Cost per unit |
|---|---|---|---|---|
| | | | | |
| **Floor** | | | | **[sum]** |

**Floor as share of price:** [n]%

## Where the gap goes
| Layer | What it pays for | Evidence or hypothesis | Could it shrink? |
|---|---|---|---|
| | | | |

## What we'll test
1. [Test, owner, date]

## Who should tell us we're wrong
- [Person or role]: [question]

## Limits
[What this floor leaves out; inputs marked check]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We run a small coffee roastery. Our printed retail bag with a one-way valve costs us 0.92 per bag at 5,000 bags from our packaging agency. Everyone in the trade says that's normal. The bag is kraft paper laminated to a PE film, about 18 g, plus a valve. Our printer friend says film-and-paper laminate runs around 4.00 per kg and valves around 0.06 each when bought by the thousand."

**Output (excerpt):**

```markdown
These are principles Elon Musk has described publicly. Not affiliated with or endorsed by Elon Musk or their companies.

## Fundamental inputs
| Input | Quantity per unit | Market rate | Source | Cost per unit |
|---|---|---|---|---|
| Kraft/PE laminate | 18 g | 4.00 per kg | Printer friend | 0.072 |
| One-way valve | 1 | 0.06 each | Printer friend | 0.06 |
| Ink and printing | [check: printer's rate per bag at 5,000] | | | [check] |
| **Floor (materials only)** | | | | **0.132 + printing** |

**Floor as share of price:** about 14% before printing

## Where the gap goes
| Layer | What it pays for | Evidence or hypothesis | Could it shrink? |
|---|---|---|---|
| Bag converting | Cutting, sealing, fitting the valve | Hypothesis | Ask a converter directly |
| Agency margin | The agency resells a converter's bags | Hypothesis: the invoice names no factory | Yes, if we buy direct |
| Short-run setup | Plates and setup spread over 5,000 bags | [check: setup fee on the quote] | A larger, less frequent order |

## What we'll test
1. Ask two converters for a direct quote on the same specification - [owner], [date].

## Limits
Printing, freight, minimum order quantities and the time we'd spend managing a converter are not in the floor yet.
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] The analogy being set aside is written down.
- [ ] Every input has a quantity, a rate and a source, or is marked [check].
- [ ] The floor and the floor-to-price ratio are shown.
- [ ] Each layer of the gap is labelled evidence or hypothesis.
- [ ] The limits of the floor are stated.
- [ ] At least one test and one person who could prove it wrong are named.

## Common mistakes

- Treating the materials floor as the price you should pay.
- Stopping the breakdown at another finished product ("a valve bag") instead of its inputs.
- Filling unknown rates with plausible guesses.
- Using the method on a cost that is mostly a licence or a regulated fee.
