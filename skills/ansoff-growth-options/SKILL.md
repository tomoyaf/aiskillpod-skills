---
name: ansoff-growth-options
description: Lays out a company's growth options on the product-market matrix (market penetration, market development, product development, diversification) - defines the current products and markets first, generates options in each quadrant from the facts given, writes the evidence, what is new to the firm, and the risk of each, and ends with a ranked shortlist and the first cheap test for each option. Use when someone asks for an Ansoff matrix example or template, growth strategy options, where to grow next, whether to launch a new product or enter a new market, how to grow revenue next year, or a diversification decision.
---

# Growth options matrix

The growth options matrix sorts ways to grow by two questions: is the product one the company already sells or a new one, and is the market one it already serves or a new one? That gives four routes: market penetration (sell more of the current products to current markets), market development (take current products to new markets), product development (new products for current markets), and diversification (new products for new markets). H. Igor Ansoff introduced it in "Strategies for Diversification," Harvard Business Review 35(5), September–October 1957, pp. 113–124, and developed it in his book Corporate Strategy (McGraw-Hill, 1965); it is widely known as the Ansoff matrix. Risk rises as an option moves away from what the company already knows, so diversification is usually the riskiest. This skill uses the matrix to generate and compare real options, then turns the best ones into small tests.

## When to use

- Annual or quarterly planning, when the team must choose where next year's growth comes from.
- When someone proposes a new product, a new city or country, or a new customer type, and the team wants to compare it with the alternatives.
- When current sales growth is slowing and the team wonders whether the current market is used up.
- Before asking for budget or investment for a growth move.
- Not for judging whether an industry is profitable (use five-forces-analysis), not for imagining how the outside world might change (use scenario-planning), and not for differentiating an offering in its current market (use errc-strategy-canvas).

## What you need

- The current products and markets, stated precisely: what is sold, to which customer groups, in which places, through which channels.
- The growth goal and time frame (for example, revenue target for next year). If missing, ask once; otherwise write "[goal: to confirm]".
- Facts about the current market: share or penetration, repeat rate, churn, how many potential customers are not yet buying.
- Ideas already on the table, and the capabilities and constraints (money, people, skills, licences).
- Never invent market sizes, growth rates, or demand. Mark unknowns "[check: ...]" and say what fact would change the ranking.

## Steps

1. **Define the base.** Write the current products and the current markets as two short lists. "Market" means a customer group in a place reached through a channel, not a whole industry. "New" always means new to this company, not new to the world.
2. **Check penetration headroom first.** From the facts, estimate how much more the current products could sell to the current markets: customers not yet reached, buyers who could buy more often, lost customers who could come back. If the facts are missing, list the questions to answer. Penetration is the lowest-risk route, so a team that skips it needs a reason.
3. **Generate options in all four quadrants.** Write 1 to 3 options per quadrant from the user's ideas and the facts given. If a quadrant has no realistic option, say so rather than filling it. For diversification, say whether it is related (shares customers, skills, or channels with the current business) or unrelated.
4. **Write what is actually new for each option.** List what the company would have to learn or build: a product, a channel, a customer type, a place, a regulation, a skill. Label quadrants carefully: as John Dawes (2018) points out, a "new product" often brings new buyers too, and a "new market" sometimes needs a changed product. Classify by what is truly new, and note the doubt when an option sits on a border.
5. **Rate evidence and risk.** For each option write the evidence for demand from the input (or "[check: ...]"), the main risk, and a risk rating (Low, Medium, High). Start from the quadrant (penetration lowest, diversification highest) and adjust for the specific facts: an option backed by paying customers' requests carries less risk than its quadrant suggests.
6. **Estimate the size of the prize where possible.** For each option, give the revenue or margin it could add within the time frame, only from numbers in the input, with the math shown. Otherwise write "[check: ...]".
7. **Rank and shortlist.** Rank options by expected contribution to the goal against risk and the resources they need. Pick 2 or 3 for the shortlist, and say what the company is choosing not to do.
8. **Name the first test for each shortlisted option.** Each test is small, cheap, and answers the riskiest question about that option within weeks: a pre-sale, a pilot with a few customers, a landing page, a trial in one location. Give the test a pass line set in advance.
9. **End with the decision and next actions.** One paragraph answering the growth question, then the tests with owners and dates if the user gave names.

## Output format

```markdown
# Growth options: [company]
**Goal:** [goal and time frame] · **Prepared for:** [name or team] · **Date:** [date]

## Current base
- **Products:** [list]
- **Markets:** [customer group, place, channel]

## Penetration headroom
[What more the current products could sell to current markets, with evidence or questions.]

## Options matrix
| | Current products | New products |
|---|---|---|
| **Current markets** | Market penetration: [options] | Product development: [options] |
| **New markets** | Market development: [options] | Diversification: [options, related or unrelated] |

## Options compared
| Option | Quadrant | What is new to us | Evidence of demand | Size of prize | Main risk | Risk |
|---|---|---|---|---|---|---|
| [option] | [quadrant] | [list] | [source or "[check: ...]"] | [math or "[check: ...]"] | [risk] | Low / Medium / High |

## Shortlist and what we won't do
1. [Option]: [why]
- Not now: [option], because [reason]

## First tests
| Option | Riskiest question | Test | Pass line | Owner | By |
|---|---|---|---|---|---|

## Decision
[One paragraph answering the growth question.]
```

## Example

**Input:** "We're Northfold Roasters, a coffee roaster in Leeds. Revenue last year was £640k: 70% wholesale beans to 48 independent cafés in Leeds and York, 30% online bean subscriptions (about 900 subscribers, mostly in the north of England). Goal: grow revenue 25% next year without new outside money. Facts: we lose about 4% of subscribers a month; our account manager thinks there are 150+ independent cafés in Leeds and York we don't supply; 11 of our cafés asked if we could supply milk and syrups too; several offices in Leeds have asked about bean-to-cup machines with beans included; a Manchester café group (6 sites) approached us last month; someone suggested we open our own café. We have one van, one roaster running at about 60% of capacity, and 9 staff."

**Output:**

```markdown
# Growth options: Northfold Roasters
**Goal:** revenue +25% next year (about £160k on £640k), no outside money · **Prepared for:** Northfold Roasters · **Date:** [date]

## Current base
- **Products:** roasted coffee beans (wholesale and subscription)
- **Markets:** independent cafés in Leeds and York (direct, by van); home buyers in the north of England (online subscription)

## Penetration headroom
Two clear sources. Cafés: the account manager estimates 150+ independent cafés in Leeds and York not supplied by us [check: count and how many use a rival on contract]. Subscribers: a 4% monthly loss means roughly 430 of 900 subscribers leave in a year (900 × 4% × 12, before replacements), so cutting churn is growth we already paid to acquire [check: reasons for cancelling]. The roaster at 60% of capacity can take more volume.

## Options matrix
| | Current products | New products |
|---|---|---|
| **Current markets** | Market penetration: win more Leeds and York cafés; cut subscriber churn | Product development: supply milk and syrups to current cafés |
| **New markets** | Market development: Manchester café group; offices in Leeds | Diversification: own café (related: same product, new role as a retailer) |

## Options compared
| Option | Quadrant | What is new to us | Evidence of demand | Size of prize | Main risk | Risk |
|---|---|---|---|---|---|---|
| More Leeds and York cafés | Penetration | Nothing | 150+ cafés not supplied (estimate) | [check: average café spend] | Rivals' contracts lock cafés in | Low |
| Cut subscriber churn | Penetration | Nothing | 4% monthly loss | [check: subscription price] | Churn reasons may be price, which we can't fix cheaply | Low |
| Milk and syrups for current cafés | Product development | Chilled and ambient stock, new suppliers | 11 of 48 cafés asked | [check: margin on resale] | Low margin; van space; chilled handling | Medium |
| Manchester café group | Market development | A new city for deliveries | They approached us; 6 sites | [check: their weekly volume] | One van; delivery cost to Manchester | Medium |
| Offices in Leeds with machines | Market development, near the border | Machine leasing and servicing, a new buyer type | Several enquiries | [check] | Machine servicing is a new skill and ties up capital | High |
| Own café | Diversification (related) | Retail site, staff, lease | Suggestion only, no evidence | [check] | Lease and staffing with no outside money; competes with our customers | High |

## Shortlist and what we won't do
1. More Leeds and York cafés, with spare roaster capacity and no new skills.
2. Cut subscriber churn, which keeps revenue we already earn.
3. Manchester café group, as one test account, since they came to us.
- Not now: own café (high risk, no evidence, and it would compete with the cafés we supply); office machines (a servicing business we don't have). Milk and syrups wait until the margin is known.

## First tests
| Option | Riskiest question | Test | Pass line | Owner | By |
|---|---|---|---|---|---|
| More cafés | Will cafés switch from their current roaster? | Free sample visit to 20 unsupplied cafés | 3 or more trial orders | Account manager | [date] |
| Cut churn | Why do subscribers leave? | Exit question in the cancel flow for one month | A reason we can fix covers half or more of answers | [owner] | [date] |
| Manchester group | Can we deliver at a profit? | Quote with delivery cost; trial at 2 of their 6 sites | Margin after delivery at or above our Leeds average [check: figure] | [owner] | [date] |

## Decision
Grow mainly from the current market first: more cafés in Leeds and York and lower subscriber churn use spare capacity and need no new skills. Test Manchester as the one new market, through a group that asked for us. Whether these reach £160k depends on the average café spend and the churn reasons, both still to check; decide on milk and syrups once the margin is known.
```

## Checks before you send

- [ ] The current products and markets are defined before any option is listed.
- [ ] Penetration headroom is estimated or its open questions are listed.
- [ ] Every quadrant has options or a stated reason why it has none.
- [ ] Each option says what is new to the company, the evidence of demand, the main risk, and a risk rating.
- [ ] Every number comes from the input, with the math shown, or is marked "[check: ...]".
- [ ] The shortlist says what the company won't do now.
- [ ] Each shortlisted option has a first test with a pass line set in advance.

## Common mistakes

- Defining the market as a whole industry ("coffee"), so every option looks like penetration.
- Treating "new" as new to the world instead of new to the company.
- Jumping to diversification because it is exciting, before checking how much the current market still holds.
- Filling every quadrant for symmetry with options no one would fund.
- Rating risk by quadrant alone and ignoring evidence: a new product that customers already asked for can carry less risk than a new market no one has checked.
- Ending with a filled-in matrix instead of a shortlist, a decision, and tests.
