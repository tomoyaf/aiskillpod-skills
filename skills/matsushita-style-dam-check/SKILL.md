---
name: matsushita-style-dam-check
description: Checks how much spare capacity a business holds, area by area - cash, equipment, people, inventory, technology, and plans and products in development - against the dam management that Konosuke Matsushita described (keep a planned, appropriate reserve in every area, the way a dam holds water to give a steady flow whatever the weather) and the saying he stressed, not forgetting disorder in times of peace. Use when a founder or finance lead asks how long the company could ride out a bad quarter, whether it runs too lean, how much cash or stock to hold, or how to prepare for a downturn while things are going well.
---

# Matsushita-style dam management check

These are principles Konosuke Matsushita described publicly, as summarised by the PHP Institute he founded and in Kazuo Inamori's account of hearing him speak. Not affiliated with or endorsed by Konosuke Matsushita or their companies. The skill looks at each area of the business, asks how much reserve it holds and whether that reserve is planned, and recommends where to build or release it.

## Ground rules

- Do not attribute quotes or opinions to Konosuke Matsushita beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Konosuke Matsushita; review the user's material against the principles below.
- Never invent numbers. Missing figures are written "[check: ...]".
- Not financial, investment or tax advice; a reserve policy for a regulated business follows its own rules.
- A reserve is not the same as waste or idleness. Say which is which.

## The principles

1. **Dam management (ダム経営).** A dam holds back a river's water so it can supply a steady amount whatever the season or weather. Likewise, a business should keep an appropriate reserve, based on a sound outlook, in every area: equipment, funds, people, inventory, technology, and planning and product development. The reserve can look like waste, but it is the insurance premium for stable growth. Source: "ダム経営", 用語セレクション, 松下幸之助.com (PHP Institute).
2. **Thinking so comes first.** Kazuo Inamori recounts a talk in which Matsushita described dam management (store profits in good times to prepare for bad ones), and, asked how a manager with no slack could build one, answered roughly "you have to think so". Inamori took from it that thinking so comes first. Source: Kazuo Inamori, 『経営12カ条』, excerpt on 日経BOOKプラス.
3. **Don't forget disorder in times of peace (治にいて乱を忘れず).** A saying he stressed at every opportunity: good times and bad times both come; keep the readiness to deal with a headwind at any moment, even while things go well. Source: "治にいて乱を忘れず", 用語セレクション, 松下幸之助.com.

## When to use

- Setting or reviewing a cash reserve, a stock buffer, or bench capacity.
- Preparing for a downturn while revenue is still growing.
- A team that is always at 100% and can't take on anything unexpected.
- Not for a cash forecast itself (use runway-update) or a budget variance (use budget-variance-note).

## What you need

- The areas to look at. By default the six from principle 1: funds, equipment, people, inventory, technology, plans and products in development.
- For each: what you hold today, what you use in a normal month, and the worst month you have seen or expect.
- Revenue and fixed costs per month, if the funds area is in scope.
- What is changing: a big customer, a season, a new product.

## Steps

1. **List the areas.** One row per area. Drop one only if the user says it doesn't apply (a software company with no stock skips inventory).
2. **Measure the reserve in each.** Express it as cover: months of fixed costs in cash, weeks of stock at normal sales, spare hours of team capacity, a backup supplier or machine, a second person who can do a key job, products in development that could sell if the main one weakens.
3. **Ask whether it is planned (principle 1).** Is the level chosen from an outlook ("we hold four months because our worst quarter dropped 30%"), or did it just happen? Unplanned reserve can be too small or idle money.
4. **Separate reserve from waste.** A reserve has a job in a bad month; idle stock nobody will buy, or a role nobody needs, is not a reserve. Mark each.
5. **Test a bad season (principle 3).** Take the worst month from the input, or a stated scenario, and walk it through each area. Where does the business run dry first, and when?
6. **Recommend.** Per area: build, hold, or release, with the size and the first step. Building reserve usually starts in good months (principle 2): name the share of this month's profit or hours to set aside.
7. **Name the cost.** Reserve has a cost (cash not invested, stock carrying cost, spare hours). State it beside each recommendation so the trade-off is visible.

## Output format

```markdown
# Dam check: [company]
**Date:** [date] · **Prepared for:** [name]
These are principles Konosuke Matsushita described publicly. Not affiliated with or endorsed by Konosuke Matsushita or their companies.

## Summary
[2-3 sentences: where the business would run dry first in a bad season, and the one reserve to build now]

## Reserves by area
| Area | Held today | Cover | Planned or accidental | Reserve or waste |
|---|---|---|---|---|
| Funds | | | | |
| Equipment | | | | |
| People | | | | |
| Inventory | | | | |
| Technology | | | | |
| Plans and products in development | | | | |

## A bad season
[Scenario from the input; what runs out first and when]

## Recommendations
| Area | Build / hold / release | How much | First step | Cost of the reserve |
|---|---|---|---|---|

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "Coffee roaster, 14 staff, wholesale to cafés plus an online shop. Cash 6.0M yen, fixed costs 2.4M a month. Green beans: 5 weeks of stock, one importer. One roaster machine; only our head roaster can run the profiles. Revenue fell 35% for two months during the last café downturn. Online is 20% of sales and growing. We're busy and profitable right now."

**Output (excerpt):**

```markdown
These are principles Konosuke Matsushita described publicly. Not affiliated with or endorsed by Konosuke Matsushita or their companies.

## Reserves by area
| Area | Held today | Cover | Planned or accidental | Reserve or waste |
|---|---|---|---|---|
| Funds | 6.0M yen | 2.5 months of fixed costs | Accidental | Reserve |
| Equipment | One roaster | None | Accidental | No reserve |
| People | One person runs the roast profiles | None | Accidental | No reserve |
| Inventory | 5 weeks of beans, one importer | 5 weeks, single source | [check: chosen or not] | Reserve |
| Plans and products | Online shop, 20% of sales | Partial second leg | Planned | Reserve |
| Technology | Not in the input | [check: tools, systems or know-how to cover] | [check] | [check] |

## A bad season
Using the last downturn (revenue down 35% for two months), cash covers the gap [check: gross margin, to size the gap]. The first thing to fail is not cash but the roaster or the head roaster: either one stops all sales.

## Recommendations
| Area | Build / hold / release | How much | First step | Cost of the reserve |
|---|---|---|---|---|
| People | Build | A second person able to run the main profiles | Head roaster trains one person, 2 sessions a week | Roaster time |
| Equipment | Build | A backup arrangement | [check: toll-roasting partner or service contract] | Fee |
| Funds | Build in good months | [decide: share of monthly profit] | Set aside a fixed share each month while busy | Cash not invested |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] All six areas are covered, or the dropped ones are named with a reason.
- [ ] Each reserve is marked planned or accidental, and reserve or waste.
- [ ] A bad-season walk-through says what runs out first.
- [ ] Each recommendation states its cost.
- [ ] Every number comes from the input or is marked [check] or [decide].

## Common mistakes

- Looking at cash only; the source names equipment, people, inventory, technology and product development too.
- Calling idle stock a reserve.
- Waiting for a bad quarter to start; the account Inamori gives is about building it while things go well.
