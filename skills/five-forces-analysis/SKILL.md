---
name: five-forces-analysis
description: Runs a Porter five forces industry analysis - defines the industry boundary first, rates rivalry, threat of new entrants, supplier power, buyer power, and threat of substitutes with evidence for each, names the forces that set the industry's profit level, checks the result against actual profitability, and ends with where to compete and what to change. Use when someone asks for a five forces analysis, a Porter five forces template or example, an industry analysis, whether a market is attractive, why margins in an industry are low, or where to position before entering a market.
---

# Five forces industry analysis

The five forces explain why an industry earns what it earns. Profit in any industry is split five ways: rivals compete it away, buyers bargain it down, suppliers bargain it up, substitutes cap prices, and the threat of new entrants holds prices low. Michael E. Porter introduced the framework in Harvard Business Review in 1979, built it out in his book Competitive Strategy (1980), and restated it in "The Five Competitive Forces That Shape Strategy" (HBR, January 2008). This skill follows the 2008 version: define the industry first, rate each force from its drivers, find the one or two forces that control profitability, and turn that into a choice of where to compete.

## When to use

- Before entering a market, or when deciding which segment of a market to serve.
- When margins in an industry are low and the team wants to know why.
- When a price, a supplier, a big customer, or a new kind of competitor is changing the business.
- Preparing an investor memo, a business plan, or a strategy offsite where industry attractiveness comes up.
- Not for choosing how your own company competes inside the industry (use generic-strategy-choice), and not for a cost and value map of your own operations (use value-chain-analysis).

## What you need

- The industry as the user sees it: the product or service, the customers, and the area where competition happens. You will test and maybe narrow this in step 1.
- Facts on each force: number and size of rivals, main customer groups and their share of volume, key suppliers and inputs, alternatives customers use instead, and what it takes to enter.
- Profitability evidence if any: margins, return on invested capital, price trends, exits and entries in recent years.
- The decision the analysis should serve (enter or not, which segment, what to negotiate). If missing, ask once; otherwise write "[decision: to confirm]".
- Never invent market data. If a fact is missing, ask for it or mark it "[check: ...]" and say how the rating would change if it came out the other way.

## Steps

1. **Define the industry boundary.** Write the product scope (which products or services are in, which belong to a neighbouring industry) and the geographic scope (local, national, regional, global). Porter's test: if two products or regions have the same buyers, suppliers, entry barriers and so on, they are one industry; if the structure differs a lot in one or more forces, treat them as separate industries and analyze the one that matters for the decision. State the boundary in one sentence at the top.
2. **List the participants.** Name the rivals, the buyer groups, the supplier groups, the substitutes, and the likely entrants. Segment buyers and suppliers into groups when their power differs (a hotel chain and a single guesthouse are different buyers). Ask the user for any group you can't fill.
3. **Rate each force from its drivers, with evidence.** For each force, write the drivers that apply, the evidence from the input, and a rating of Low, Medium, or High pressure on industry profit. Typical drivers: rivalry (number and balance of rivals, industry growth, fixed costs, exit barriers, whether rivals compete on price), new entrants (scale economies, switching costs, capital needed, access to distribution, incumbent advantages not tied to size, government policy, expected retaliation), suppliers (concentration versus the industry, switching costs, whether the supplier depends on this industry, whether it can integrate forward), buyers (concentration and volume, standardized products, switching costs, ability to integrate backward, price sensitivity), substitutes (price-performance against the product, the buyer's cost of switching, doing without or doing it in-house). Mark a rating "[check: ...]" when it rests on a missing fact.
4. **Put the other factors through the forces, not beside them.** Industry growth rate, technology and innovation, government policy, and complements are not extra forces. For each one that matters, write which force it moves and in which direction (a licence requirement raises entry barriers; a complementary product can raise or lower switching costs). Fast growth alone does not make an industry attractive.
5. **Name the controlling forces and explain the profit level.** Pick the one or two forces that most limit profit and say why the industry earns what it does. Then test the story against the numbers: if your ratings were right, would the industry earn the margins it actually earns over several years, and do the companies that earn most stand where these forces press them least? If the user has no profitability data, say the test is open and mark it "[check: industry margins or ROIC over several years]".
6. **Look at change.** For each force, note recent and likely changes (new substitutes, consolidation among buyers, new regulation, a supplier gaining power). Separate structural change from a cyclical swing or a one-off.
7. **Turn it into where to compete and what to change.** Give 2 to 4 strategic moves under three headings: position (segments or customers where the forces are weakest, defences against the strongest force), exploit change (a shift in the forces the company can get ahead of), and shape the structure (moves that raise barriers, lower buyer or supplier power, or grow the profit pool for the whole industry). Each move names the force it addresses.
8. **End with the decision and next actions.** Answer the decision from the input in one paragraph, then list the facts still to check, each with an owner if the user gave names.

## Output format

```markdown
# Five forces: [industry as defined]
**Decision this serves:** [decision] · **Prepared for:** [name or team] · **Date:** [date]

## Industry boundary
[One sentence: product scope and geographic scope.] [What was excluded and why.]

## Forces
| Force | Key drivers | Evidence | Pressure on profit |
|---|---|---|---|
| Rivalry among existing competitors | | | Low / Medium / High |
| Threat of new entrants | | | |
| Bargaining power of suppliers | | | |
| Bargaining power of buyers | | | |
| Threat of substitutes | | | |

## Other factors, read through the forces
| Factor | Force it moves | Direction |
|---|---|---|

## Profit structure
[Which 1–2 forces control profitability and why the industry earns what it does. Consistency check against actual profitability.]

## Changes to watch
- [Force]: [change], structural or cyclical

## Where to compete and what to change
| Move | Type (position / exploit change / shape structure) | Force it addresses |
|---|---|---|

## Decision and next actions
[One paragraph answering the decision.]
- [ ] [Fact to check] ([owner])
```

## Example

**Input:** "We run a commercial laundry in Kyoto (Asahi Linen). Should we invest ¥60M to double capacity for hotel linen? Facts: we wash sheets and towels for hotels and guesthouses in Kyoto city. 4 laundries serve this market; the two largest (us and Kamo Laundry) handle about 70% of volume. Customers: 2 hotel chains give us 45% of our volume and re-tender every year on price; about 120 independent guesthouses make up the rest and rarely switch. Inputs: detergent from several suppliers; gas prices rose about 30% in two years; staff are hard to hire and wages went up 8% last year. A new plant costs around ¥180M and needs steady hotel contracts to fill it. Many small guesthouses (under 10 rooms) wash in-house with coin machines or their own washers. Tourist arrivals to Kyoto are growing. Our operating margin is 6%; we don't know the others'."

**Output:**

```markdown
# Five forces: hotel and guesthouse linen laundry, Kyoto city
**Decision this serves:** invest ¥60M to double capacity for hotel linen? · **Prepared for:** Asahi Linen · **Date:** [date]

## Industry boundary
Commercial washing of hotel and guesthouse sheets and towels within Kyoto city. Excluded: restaurant and hospital linen, which may have different buyers and rules [check: whether Asahi serves them], and other cities, since laundry is bulky and served locally.

## Forces
| Force | Key drivers | Evidence | Pressure on profit |
|---|---|---|---|
| Rivalry among existing competitors | 2 large rivals hold most volume [check: their relative size]; fixed costs [check: plant and labour cost share]; growing demand | 4 laundries, top 2 hold about 70% | Medium |
| Threat of new entrants | Capital needed; need for steady contracts | New plant about ¥180M, needs hotel contracts to fill | Low |
| Bargaining power of suppliers | Labour scarce; gas price | Wages +8% last year; gas +30% in two years; detergent has many suppliers | High (labour and energy) |
| Bargaining power of buyers | Chains buy large volumes and re-tender yearly; independents fragmented, rarely switch | 2 chains = 45% of Asahi's volume | High for chains, Low for independents |
| Threat of substitutes | Washing in-house | Small guesthouses use coin or own machines | Medium for small guesthouses, Low for hotels |

## Other factors, read through the forces
| Factor | Force it moves | Direction |
|---|---|---|
| Tourist growth | Rivalry; new entrants | Eases rivalry now; may attract an entrant from a nearby city [check: plans of laundries in Osaka] |

## Profit structure
Buyer power from the two chains and supplier power from labour and gas control profit. The chains re-tender on price every year, so cost increases are hard to pass on to them; rising wages and gas take the rest. The 6% margin fits this picture, but the consistency check is open: [check: margins of Kamo Laundry or industry figures for several years].

## Changes to watch
- Suppliers: wage rises look structural (hiring is hard), gas prices may be partly cyclical [check: gas contract terms].
- Buyers: if more chain hotels open, chain share of the market grows and buyer power rises.

## Where to compete and what to change
| Move | Type (position / exploit change / shape structure) | Force it addresses |
|---|---|---|
| Grow the independent guesthouse share before adding chain volume | Position | Buyer power |
| Offer guesthouses a pickup schedule and linen supply that beats washing in-house | Position | Substitutes |
| Index chain contracts to gas and wage costs at the next tender | Shape structure | Supplier power passed through buyers |
| Automate folding to cut labour per kilo [check: equipment cost] | Position | Supplier power (labour) |

## Decision and next actions
Doubling capacity mostly for chain hotels would add volume in the segment where buyer power is highest, at a time when labour and gas take more of each yen. We recommend not committing the full ¥60M now. Add capacity in step with independent guesthouse demand, and make cost-indexed pricing a condition of new chain volume.
- [ ] Get margins of rivals or industry data for several years (Asahi finance)
- [ ] Count guesthouses that wash in-house and would switch at a given price (Asahi sales)
- [ ] Check gas contract terms (Asahi operations)
```

## Checks before you send

- [ ] The industry boundary (product and geography) is stated before any force is rated.
- [ ] All five forces are rated, each with drivers and evidence from the input, not a bare adjective.
- [ ] Growth, technology, government, and complements appear only through the force they move, never as a sixth force.
- [ ] The controlling forces are named, and the result is checked against actual profitability or the check is marked open.
- [ ] Every number comes from the input or is marked "[check: ...]".
- [ ] It ends with an answer to the decision and moves tied to specific forces, not a summary.

## Common mistakes

- Drawing the industry too broadly ("the laundry industry") or too narrowly, so the forces describe a market no one competes in.
- Making a list of facts under each force instead of judging how strong the force is and why.
- Giving every force equal space instead of digging into the one or two that limit profit.
- Confusing an effect (buyers are price sensitive) with its cause (the product is a large share of the buyer's costs, or it is standardized).
- Treating a fast-growing or high-tech market as attractive by default.
- Calling the industry attractive or unattractive and stopping there, instead of choosing where to compete.
