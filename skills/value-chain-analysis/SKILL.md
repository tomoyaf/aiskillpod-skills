---
name: value-chain-analysis
description: Maps a business's value chain - primary activities (inbound logistics, operations, outbound logistics, marketing and sales, service) and support activities (procurement, technology development, human resource management, firm infrastructure) - with each activity's share of cost, what drives its cost, and what in it buyers value, then checks how well the activities fit one strategy and picks the 2 to 3 changes that matter most. Use when someone asks for a value chain analysis, a value chain example or template, where the company's costs really sit, where it creates value for customers, why margins are thin, or which activities to change, outsource, or invest in.
---

# Value chain analysis

A company is a set of activities: buying inputs, making or delivering the product, selling it, serving customers, and the functions that support all of these. Each activity costs money, and each can add to what buyers will pay. A value chain analysis lists those activities, puts a cost share and a cost driver on each, notes where buyers see value, and asks whether the activities reinforce one another. Michael E. Porter set out the value chain, with its primary and support activities, in Competitive Advantage (1985). His article "What Is Strategy?" (HBR, 1996) adds the point this skill ends on: advantage that lasts comes from activities that fit together, which rivals find much harder to copy than any single activity.

## When to use

- Margins are thin and the team doesn't know which activities eat them.
- Deciding what to outsource, automate, or invest in.
- After choosing a strategy, to check that day-to-day activities support it.
- Comparing your setup with a rival that wins on cost or on a feature customers love.
- Not for judging how profitable the whole industry is (use five-forces-analysis), and not for choosing between cost and differentiation in the first place (use generic-strategy-choice).

## What you need

- What the business sells, to whom, and its chosen basis of competing (low cost, a distinct offer, a segment). If none is stated, ask once; otherwise analyze both cost and value and say the strategy is open.
- Costs by activity or by department: a profit and loss statement, headcount by team, or rough shares from the user. Never invent shares; mark them "[check: ...]" and say how the conclusion would change.
- What customers value and complain about: reviews, sales notes, churn reasons, win-loss records.
- What rivals do differently in any activity, if known.

## Steps

1. **Set the unit and the strategy.** Name the business unit you're mapping (one product line or one business, not a whole group with different businesses) and the strategy it's meant to serve. Every later judgment is against that strategy.
2. **List the activities.** Use Porter's categories as a checklist, then name the company's own activities under each. Primary: inbound logistics, operations, outbound logistics, marketing and sales, service. Support: procurement, technology development, human resource management, firm infrastructure (finance, planning, legal, management). Split a category into separate activities when they have different costs or different value to buyers; merge or skip ones that are tiny.
3. **Put a cost share on each activity.** Assign operating costs and the people working on each activity, and give each a share of total cost. Use the user's numbers; where they're estimates, label them as such, and where they're missing, mark "[check: ...]". Show large purchased inputs (raw materials, goods for resale) on their own line, since they often outweigh any single activity. The shares should add to about 100%.
4. **Find the cost drivers.** For the activities with the largest shares, write what makes their cost go up or down: volume and scale, utilization, learning, location, input prices, how one activity's choices change another's cost (a better file check upstream cuts reprints downstream), and policy choices the company makes. Note where rivals have a structurally lower cost and why.
5. **Find the value drivers.** For each activity, write what in it buyers notice and would pay for or would leave over, using customer evidence. Mark the activities that make the offer different from rivals'. An activity can be a large cost and still where the premium comes from.
6. **Check fit.** Test three things: does each activity match the strategy, do activities reinforce one another, and does the setup avoid doing work twice. List activities that pull against the strategy (a discount program in a premium business) and pairs that reinforce each other.
7. **Pick the 2 to 3 changes.** Rank candidate changes by size of cost or value at stake and by fit. For each change, state the activity, the change, the expected effect on cost or price with the reasoning, and what it gives up. Prefer changes that strengthen links between activities over isolated cost cuts rivals can copy.
8. **End with owners and the facts to check.** Give the first step for each change, an owner if named, and the open "[check: ...]" items that could reverse a conclusion.

## Output format

```markdown
# Value chain: [business unit]
**Strategy it serves:** [one sentence] · **Prepared for:** [name or team] · **Date:** [date]

## Activity map
| Activity | Type | Cost share | Cost drivers | Value to buyers | Fit with strategy |
|---|---|---|---|---|---|
| [activity] | Primary / Support / Purchased input | [%] | | | Fits / Pulls against |

## Where cost sits
[2–4 sentences: the largest cost activities and their drivers; where rivals are structurally cheaper.]

## Where value is created
[2–4 sentences: the activities buyers pay for, with the customer evidence.]

## Fit
- Reinforcing: [activity] + [activity]: [how]
- Pulling against the strategy: [activity]: [why]

## The changes that matter
| # | Activity | Change | Expected effect | What it gives up |
|---|---|---|---|---|

## Next steps and checks
- [ ] [First step] ([owner])
- [ ] [check: ...]
```

## Example

**Input:** "We're Hoshi Coffee, a specialty roaster in Fukuoka, 14 staff. Strategy: premium beans with the freshest roast, sold to independent cafés (60% of revenue) and an online subscription (40%). Yearly costs, roughly: green beans 34%, roasting (2 roasters, staff, gas) 16%, packing and shipping 18%, sales to cafés (1 rep) 6%, online marketing and the subscription website 9%, barista training we give cafés for free 5%, admin and finance 8%, sourcing trips to farms 4%. Cafés say the free barista training and roast date on every bag are why they stay; 3 cafés left last year over price. Subscribers cancel most over shipping delays (delivery takes 4 to 6 days after roasting). We ship each subscription order separately by courier. A rival roaster in Fukuoka buys beans through a trader at lower prices and ships weekly by pallet."

**Output:**

```markdown
# Value chain: Hoshi Coffee, roasted beans for cafés and subscribers
**Strategy it serves:** premium, freshest-roast beans for independent cafés and home subscribers · **Prepared for:** Hoshi Coffee · **Date:** [date]

## Activity map
| Activity | Type | Cost share | Cost drivers | Value to buyers | Fit with strategy |
|---|---|---|---|---|---|
| Sourcing trips to farms | Support (procurement) | 4% | Number of trips | Bean quality and story [check: do customers cite it?] | Fits |
| Green beans | Purchased input (bought through procurement) | 34% | Bean grade, buying volume, direct versus trader | Taste | Fits |
| Roasting | Primary (operations) | 16% | Roaster utilization, gas price | Roast date on every bag | Fits |
| Packing and shipping | Primary (outbound) | 18% | One courier parcel per subscription order | Freshness on arrival; delays drive cancellations | Pulls against (slow, costly) |
| Sales to cafés | Primary (marketing and sales) | 6% | One rep | [check: customer evidence] | Fits |
| Online marketing and website | Primary (marketing and sales) | 9% | Ad spend [check: split ads versus site] | [check: customer evidence] | Neutral |
| Barista training for cafés | Primary (service) | 5% | Trainer hours | Main reason cafés stay | Fits |
| Admin and finance | Support (infrastructure) | 8% | Headcount | Not seen by buyers | Neutral |

## Where cost sits
Green beans (34%) and packing and shipping (18%) are over half of cost. The rival buys beans more cheaply through a trader and ships by weekly pallet, which is likely cheaper per bag too [check: rival's shipping cost]. Matching its bean cost would mean lower grades or giving up direct sourcing, which works against the premium strategy.

## Where value is created
Cafés stay for the barista training and the roast date, so service and roasting carry the premium with cafés. For subscribers, freshness is the promise, and shipping delays break it: delay is the top cancellation reason.

## Fit
- Reinforcing: roasting + roast date + barista training: cafés taste the freshness and know how to serve it.
- Pulling against the strategy: packing and shipping: separate courier parcels are slow (4 to 6 days) and costly, and undercut the freshness promise.

## The changes that matter
| # | Activity | Change | Expected effect | What it gives up |
|---|---|---|---|---|
| 1 | Packing and shipping | Roast subscription orders on 2 fixed days a week and ship that day | Shorter time from roast to door; fewer cancellations [check: courier times]; fewer roaster setups | Subscribers can't choose any delivery day |
| 2 | Barista training | Make training part of a café contract with a yearly volume commitment, not free on request | Keeps the reason cafés stay while tying its cost to revenue | Some small cafés may not sign |
| 3 | Green beans | Keep direct sourcing, but buy more lots per trip [check: storage and freshness limits] | Lower cost per kilo without lower grades | More cash tied up in stock |

## Next steps and checks
- [ ] Get courier transit times for fixed-day shipping (operations)
- [ ] Draft the café contract with training included (café sales rep)
- [ ] Check whether customers mention farm sourcing when they choose Hoshi (online marketing)
- [ ] Check storage and freshness limits for buying more lots per trip ([owner: to confirm])
- [ ] [check: what the 3 cafés that left over price were paying]
```

## Checks before you send

- [ ] The map covers one business unit and names the strategy it serves.
- [ ] Primary and support activities are both covered, in the company's own activity names.
- [ ] Cost shares come from the input, are labelled as estimates, or are marked "[check: ...]", and add to about 100%.
- [ ] Each large activity has a cost driver, and value claims rest on customer evidence.
- [ ] Fit is checked: at least one reinforcing link and any activity that pulls against the strategy.
- [ ] It ends with 2 to 3 changes, each with its effect and what it gives up, and owners.

## Common mistakes

- Copying the textbook diagram with generic labels instead of the company's actual activities and numbers.
- Mapping departments instead of activities, so one department doing three different things hides their costs.
- Cutting the largest cost without asking whether it is where buyers' value comes from.
- Treating activities one at a time and missing the links: a change in one activity often shifts cost in another.
- Ending with a long list of improvements. Pick the few that fit the strategy and say what each gives up.
