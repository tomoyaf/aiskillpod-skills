---
name: strategy-style-selector
description: Diagnoses a business environment on predictability, malleability, and harshness, matches each business unit to one of five strategy styles (classical, adaptive, visionary, shaping, renewal), and says what to change in the planning process for each. Use when someone asks which strategy approach fits their market, why the annual plan keeps going stale, whether to plan or experiment, how to run different units with different strategy processes, or mentions the strategy palette, BCG strategy styles, or Your Strategy Needs a Strategy.
---

# Strategy style for your environment

Different environments call for different ways of making strategy, not just different strategies. A detailed five-year plan suits a stable industry and fails in a market that changes every quarter. Martin Reeves, Claire Love, and Philipp Tillmanns of BCG set out the idea in "Your Strategy Needs a Strategy" (Harvard Business Review, September 2012), and Reeves, Knut Haanæs, and Janmejaya Sinha developed it in the book of the same name (Harvard Business Review Press, 2015), which BCG calls the strategy palette. You judge the environment on three dimensions: how far you can predict it, how far you can change it, and how harsh it is. Five styles follow. Classical: be big. Adaptive: be fast. Visionary: be first. Shaping: be the orchestrator. Renewal: be viable. This skill diagnoses the environment with evidence, picks a style per business unit, and names the changes to planning practice.

## When to use

- The annual plan is out of date by the second quarter, or forecasts keep missing.
- Leadership argues about planning versus experimenting, and both sides are partly right.
- A company runs units in very different markets and uses one planning process for all of them.
- A downturn, a cash squeeze, or a broken business model forces a rethink.
- Not for choosing which strategy framework to use for a specific analysis (use strategy-approach-picker), and not for writing the strategy itself once the style is known (use strategy-kernel or strategy-choice-cascade).

## What you need

- The business units or product lines to assess, one line each: what they sell and to whom.
- Evidence on predictability: how accurate past forecasts were, how often market rankings change, how fast technology or customer needs shift.
- Evidence on malleability: market share and influence, whether the market is young or consolidated, whether standards, rules, or ecosystems are still forming.
- Evidence on harshness: cash runway, margin trend, debt, whether the current business model still earns its cost of capital.
- The current planning process: cycle length, who writes the plan, how budgets are set, how often it is revised.
- Never invent market data or forecast errors. If evidence is missing, ask once, then mark it "[check: ...]" and say which way the rating would move.

## Steps

1. **List the units.** Split the business where environments differ: a mature product line and a new one in an emerging market are separate rows even if one team runs both. Assess each row on its own.
2. **Check harshness first.** Ask whether the unit can survive on its current path: cash runway, falling margins, debt covenants, a collapsing core market. If survival is at risk, the style is renewal for now, whatever the other two dimensions say. Write the evidence and a rating (Low, Medium, High).
3. **Rate predictability with evidence.** Look at how far off past forecasts were, how stable market shares and rankings have been, and how often customers, technology, or competitors change. Rate High or Low and give the two or three facts behind it. Do not rate from mood; a market that feels busy can still be forecastable.
4. **Rate malleability with evidence.** Ask whether this unit, alone or with partners, can change the market's structure: set a standard, build a platform others join, create a new category, change the rules. Young, fragmented markets with low entry barriers are usually more malleable; mature, consolidated ones less. Rate High or Low with facts, and be honest about the unit's real size and influence.
5. **Map each unit to a style.** Predictable and hard to change: classical (be big). Analyse, plan, and execute for scale and position. Unpredictable and hard to change: adaptive (be fast). Vary, select, and scale what works, faster than rivals. Predictable and changeable: visionary (be first). Envision an end state, build it first, persist on the goal while staying flexible on means. Unpredictable and changeable: shaping (be the orchestrator). Engage partners, build a platform, and let the ecosystem evolve. Harsh: renewal (be viable). React early, economize to stay alive, then pivot to one of the other four styles for growth. Mark borderline ratings and give the second-best style.
6. **Name the mismatch.** Compare each unit's style with how it plans today. Common mismatches: a classical annual plan run in an adaptive market; experiments without end in a classical market where scale is the advantage; a visionary bet made by a unit too small to change the market.
7. **Say what to change in planning practice.** For each unit, list three to five concrete changes: plan horizon and cycle, the role of forecasts, how budgets are released (annual allocation versus staged funding for experiments), which metrics leaders watch, who decides, and how often the plan is reopened. Tie each change to the style.
8. **Decide how to run several styles at once.** If units need different styles, say how to separate them (different processes, budgets, metrics, or teams) and where they must connect. The book calls running several approaches at once ambidexterity.
9. **End with decisions and next actions.** The style per unit, the two or three planning changes to make first, owners if given, and the evidence still to collect.

## Output format

```markdown
# Strategy style: [company or scope]
**Date:** [date] · **Prepared for:** [name or team]

## Summary
[2–3 sentences: the style chosen for each unit and the biggest change to planning practice.]

## Environment diagnosis
| Unit | Harshness (evidence → rating) | Predictability (evidence → rating) | Malleability (evidence → rating) | Style | Runner-up |
|---|---|---|---|---|---|
| [unit] | [facts] → [Low/Med/High] | [facts] → [High/Low] | [facts] → [High/Low] | [style: motto] | [style or none] |

## Mismatches today
- **[Unit]:** plans as [current practice], but its environment calls for [style]. Consequence: [what goes wrong].

## Changes to planning practice
### [Unit] — [style]
| Area | Today | Change to |
|---|---|---|
| Horizon and cycle | | |
| Forecasts | | |
| Funding | | |
| Metrics | | |
| Decision rights | | |

## Running several styles
[How units are kept apart and where they connect. Omit if one style.]

## Decisions and next actions
1. [Decision or action] — [owner] — [date]
**Evidence to collect:** [check: ...]
```

## Example

**Input:** "We're a 60-person company. Unit A: payroll software for Japanese clinics, 11 years old, about 900 customers, churn steady at about 1% a month, revenue forecast within 5% each of the last four years. Two competitors, both bigger. Unit B: a new AI scheduling assistant for clinics, launched 8 months ago, 40 paying clinics, our forecasts for it have been off by 50% or more every quarter, at least six startups launched similar tools this year, no standard yet for how scheduling tools connect to clinic records. Cash: 22 months of runway at current burn. We run one annual plan in January for both units, with fixed budgets per team."

**Output:**

```markdown
# Strategy style: payroll (A) and AI scheduling (B)
**Date:** [date] · **Prepared for:** leadership team

## Summary
Unit A fits a classical style: plan for scale and efficiency. Unit B fits an adaptive style now, with a shaping option if the company can lead an open way for scheduling tools to connect to clinic records. The biggest change: take Unit B out of the January plan and fund it in short stages tied to experiments.

## Environment diagnosis
| Unit | Harshness | Predictability | Malleability | Style | Runner-up |
|---|---|---|---|---|---|
| A: clinic payroll | 22 months runway; steady churn → Low | Forecasts within 5% for 4 years; 2 stable rivals → High | Mature niche, both rivals larger → Low | Classical: be big | none |
| B: AI scheduling | Same runway, but B burns cash [check: B's share of burn] → Medium | Forecasts off by 50%+ each quarter; 6+ new entrants this year → Low | No connection standard yet and the market is 8 months old, so the market could be changed, but 40 clinics give B little influence [check: partners willing to join] → Low (borderline) | Adaptive: be fast | Shaping: be the orchestrator |

## Mismatches today
- **Unit B:** planned once a year with a fixed budget, but its environment changes every quarter. Consequence: the team keeps executing a January plan the market has already moved past.
- **Unit A:** no mismatch in process; check whether it plans for scale (cost per customer, share of the clinic segment) or only for growth targets [check: A's current plan].

## Changes to planning practice
### Unit A — classical
| Area | Today | Change to |
|---|---|---|
| Horizon and cycle | Annual plan | Keep the annual plan; add a 3-year view of share and cost per customer |
| Forecasts | Revenue forecast | Keep; they have been reliable |
| Funding | Fixed team budgets | Keep; fund the efficiency projects with the best payback |
| Metrics | [check: current KPIs] | Share of clinic segment, cost to serve per customer, churn |
| Decision rights | Leadership in January | No change |

### Unit B — adaptive
| Area | Today | Change to |
|---|---|---|
| Horizon and cycle | Annual plan | Review every 6 weeks |
| Forecasts | Revenue forecast | Replace with a list of live experiments and the signal each should produce |
| Funding | Fixed annual budget | Stage funding: a small budget per experiment, more only for what shows results |
| Metrics | [check: current KPIs] | Experiments run per cycle, time from idea to result, retention of paying clinics |
| Decision rights | Leadership in January | Unit lead decides within the stage budget |

## Running several styles
Separate processes and metrics for A and B; share the customer base (B can test with A's clinics) and one cash view so B's burn stays visible against the 22-month runway.

## Decisions and next actions
1. Approve a separate 6-week cycle and staged budget for Unit B — CEO — [date]
2. Ask three clinic-records vendors whether they would back a shared connection standard; their answers decide whether shaping is a real option — Unit B lead — [date]
3. Set Unit A's scale metrics in the next plan — Unit A lead — [date]
**Evidence to collect:** [check: B's share of burn], [check: partners willing to join a standard], [check: A's current plan and KPIs]
```

## Checks before you send

- [ ] Harshness was checked before the other two dimensions.
- [ ] Every rating names the facts behind it, or is marked "[check: ...]".
- [ ] Each unit has one style and, where the ratings are borderline, a runner-up.
- [ ] Malleability reflects the unit's real influence, not the market's alone.
- [ ] Each planning change is concrete (cycle, funding, metric, decision right), not "be more agile".
- [ ] It ends with decisions, owners, and the evidence still missing.

## Common mistakes

- Choosing the style the team likes (visionary is the favourite) instead of the one the evidence supports.
- Rating the whole company once when its units face different environments.
- Calling a market unpredictable because it is busy; check forecast accuracy and how stable rankings are.
- Treating renewal as the strategy. It buys time; the unit then needs another style to grow.
- Naming a style and changing nothing in budgets, cycles, or metrics. The style lives in the planning process.
