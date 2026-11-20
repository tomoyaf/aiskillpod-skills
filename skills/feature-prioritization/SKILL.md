---
name: feature-prioritization
description: Scores a product backlog or feature list with RICE (reach, impact, confidence, effort), or ICE when reach data is missing, shows the math for every item, tests how sensitive the ranking is to the shakiest estimates, recommends a cut line for the available capacity, and calls out dependencies. Use when someone shares a backlog, a feature wishlist, or a roadmap list and asks what to build first, to prioritize, rank, or score features.
---

# Feature prioritization

A score is only as good as its inputs, so the output shows every input, where it came from, and whether the ranking survives if the shakiest guess is wrong. The goal is a defensible cut line, not false precision.

## When to use

- Before a planning cycle, with a backlog or list of candidate features.
- When stakeholders disagree on what to build next and need a shared method.
- When a team has more requests than capacity and needs a cut line.
- Not for picking between 2 options with very different strategy: write a decision-memo instead.

## What you need

- The list of items, with a one-line description each.
- For RICE: reach (users or accounts per quarter), impact, confidence, effort (person-weeks). If any input is missing for an item, ask once; then estimate and mark it "[estimate]".
- Capacity for the period in person-weeks. If missing, rank without a cut line and say so.
- Optional: strategic goal for the period, known dependencies, deadlines.

## Steps

1. **Choose RICE or ICE.** Use RICE when you have usage data to estimate reach: Intercom, who published RICE, measures reach as people or events per time period from real product metrics. Use ICE (impact, confidence, ease, each scored 1 to 10 and multiplied, for 1 to 1,000) when reach can't be estimated, for example pre-launch or when every item reaches everyone. Say which you used and why.
2. **Fix the scales before scoring.** Use Intercom's scales. Impact per person reached: 3 = massive, 2 = high, 1 = medium, 0.5 = low, 0.25 = minimal. Confidence: 100% = high, 80% = medium, 50% = low; below 50% Intercom calls a moonshot, so treat it as needing research, not scoring. Effort: Intercom counts person-months across product, design, and engineering; our default for short cycles is person-weeks, same rule. For ICE, write down what a 3, 6, and 9 mean before anyone scores, so two people's "7" mean the same.
3. **Score each item and show the math.** RICE = reach × impact × confidence ÷ effort, which reads as total impact per unit of work. Write the formula with numbers for every row, so anyone can recompute it. Tag each input with its source: data, customer requests, or estimate.
4. **Test sensitivity.** For the top 5 items, find the input with the lowest confidence and halve or double it. This test is our default, not part of RICE. If an item drops below the cut line under that change, flag it "fragile". Fragile items near the line need a quick check before committing.
5. **Map dependencies.** If item B needs item A, B can't start before A, whatever its score. Note blockers outside the team (legal, a partner API, another team).
6. **Draw the cut line.** Add up effort from the top until capacity is reached; keep 20% of capacity as a buffer for bugs and surprises (our default). Items that are required regardless of score (a legal deadline, a contract commitment) go above the line first and are labeled "committed".
7. **Recommend.** Name what's in, what's out, what's fragile, and the one estimate that most changes the answer.

## Output format

```markdown
# Prioritization: [period]

**Method:** [RICE or ICE] — [why] · **Capacity:** [n] person-weeks ([n] after 20% buffer)

## Ranking
| Rank | Item | Reach | Impact | Confidence | Effort | Score (math) | Inputs from |
|---|---|---|---|---|---|---|---|
| 1 | [item] | [n] | [n] | [%] | [n] | [R×I×C÷E = score] | [data / requests / estimate] |

**Cut line:** above this line = [n] person-weeks

## Sensitivity
- [Item]: if [input] is [halved/doubled], score becomes [n] → [stays / falls below line]

## Dependencies
- [Item B] needs [Item A]

## Recommendation
- **Build:** [items]
- **Not this period:** [items]
- **Check before committing:** [fragile items and what to check]
- **The estimate that matters most:** [input]
```

## Example

**Input:** Q2. Capacity 10 person-weeks. Items: CSV export (reach 400 accounts/quarter, medium impact, data, 1 week); auto reminders (reach 900 from data, high impact, a guess, 4 weeks); read-only seat (reach 150 from customer requests, high, some evidence, 2 weeks); SSO (reach 20, massive, data, 3 weeks, promised in a signed contract).

**Output:**

```markdown
# Prioritization: Q2

**Method:** RICE — usage data gives reach for all items · **Capacity:** 10 person-weeks (8 after 20% buffer)

## Ranking
| Rank | Item | Reach | Impact | Confidence | Effort | Score (math) | Inputs from |
|---|---|---|---|---|---|---|---|
| 1 | CSV export | 400 | 1 | 100% | 1 | 400×1×1.0÷1 = 400 | data |
| 2 | Auto reminders | 900 | 2 | 50% | 4 | 900×2×0.5÷4 = 225 | reach: data; impact: estimate |
| 3 | Read-only seat | 150 | 2 | 80% | 2 | 150×2×0.8÷2 = 120 | requests |
| 4 | SSO | 20 | 3 | 100% | 3 | 20×3×1.0÷3 = 20 | data |

**Cut line:** SSO (committed, 3) + CSV export (1) + auto reminders (4) = 8 person-weeks

## Sensitivity
- Auto reminders: if impact is 1 instead of 2, score becomes 112.5 → falls below read-only seat; stays above the line only if capacity allows.
- CSV export: halving reach gives 200 → still rank 2 or better.
- Read-only seat: doubling reach (from requests) to 300 gives 240 → passes auto reminders and moves above the line.
- SSO: halving reach to 10 gives 10 → committed, so it stays above the line at any score.

## Dependencies
- None between these items. SSO depends on the customer's identity provider details [check: received?].

## Recommendation
- **Build:** SSO (committed by contract), CSV export, auto reminders.
- **Not this period:** read-only seat.
- **Check before committing:** auto reminders is fragile; run 5 customer interviews to confirm impact before week 2.
- **The estimate that matters most:** impact of auto reminders.
```

## Checks before you send

- [ ] Every score shows its formula with the numbers used.
- [ ] Every input is tagged data, requests, or estimate.
- [ ] Effort above the cut line fits capacity minus the 20% buffer.
- [ ] Committed items are labeled and placed above the line regardless of score.
- [ ] The top 5 items have a sensitivity line.
- [ ] No reach or effort number appears that the user didn't give or that isn't marked "[estimate]".

## Common mistakes

- Treating a score of 225 vs. 210 as a real difference. Our rule: scores within about 20% of each other are a tie; break ties on strategy or dependencies.
- Leaving design and QA out of effort. Small items then crowd the top.
- Scoring confidence at 100% for a stakeholder's strong opinion. Without data, it is 50% at most.
