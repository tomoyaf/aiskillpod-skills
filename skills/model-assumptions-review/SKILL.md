---
name: model-assumptions-review
description: Reviews the assumptions in a financial model or forecast. Lists every assumption with its value, source, and owner, tests sensitivity one input at a time, checks plausibility against benchmarks the user provides and against the company's own history, and names the 3 assumptions that move the result most. Never invents benchmarks. Use when someone shares a financial model, forecast, budget, or fundraising plan and asks to review the assumptions, stress-test the model, or "what has to be true".
---

# Model assumptions review

A financial model is only as good as its assumptions, and a few of them usually drive most of the result. The review makes every assumption visible with its source, measures which ones move the output most, and tests those against history and the benchmarks the user provides. It doesn't rebuild the model.

## When to use

- Before a model goes to the board, a lender, or investors.
- When a forecast looks too good and nobody can say why.
- When a new finance lead inherits a model.
- Not for checking CAC and LTV math alone: use unit-economics-check. Not for a monthly runway number: use runway-update.

## What you need

- The model, or its assumptions and outputs: inputs tab, drivers, key outputs (revenue, burn, cash, runway, profit).
- The company's actual history for the same drivers, if available (last 6 to 12 months).
- Benchmarks the user trusts, with their source. If none are given, compare to history only and say so. Never supply a benchmark from memory.
- The output that matters most for the decision (cash-out month, break-even month, year-end revenue). If not given, use cash-out month.

## Steps

1. **List every assumption.** Include hard-coded numbers inside formulas, not only the inputs tab. For each: what it is, value, unit, period, source (history, contract, plan, guess), and who set it. Our default: if the source is blank, mark it "guess".
2. **Separate drivers from results.** Drivers are inputs (conversion rate, price, churn, hiring plan, salary). Results are computed (revenue, burn). Flag any result typed in as a number instead of computed.
3. **Run sensitivity one input at a time.** For each driver, change it by a set step (our default: ±20%, or a realistic range the user gives) and record the change in the key output. Rank drivers by the size of that change.
4. **Check plausibility.** Compare each top driver to the company's own history: a growth rate double the best month so far, or churn half of history, needs a reason. Compare to user-given benchmarks, citing them. If neither exists, write "[check: no history or benchmark]".
5. **Name the 3 that matter most.** The 3 drivers with the largest effect on the key output, each with: current value, the evidence for it, what happens to the output if it's wrong in the downside direction, and what would raise confidence (data to gather, a test to run).
6. **Note structural issues.** Units that don't match (monthly vs annual), timing (hires starting at month 1 of the plan with no recruiting time), drivers that should depend on each other but don't (sales hires up, quota per rep unchanged, revenue doesn't move).
7. **Write the summary.** 2 to 3 sentences: what the model says, the 3 assumptions it rests on, and the biggest risk.

## Output format

```markdown
# Assumptions review — [model name], [date]

**Key output:** [e.g. cash-out month: [value]]
**Summary:** [2–3 sentences]

## The 3 that matter most
| # | Assumption | Value | Evidence | If wrong (downside) | To raise confidence |
|---|---|---|---|---|---|
| 1 | [Driver] | [value] | [history / benchmark / guess] | [output change] | [data or test] |

## Sensitivity (each input changed alone)
| Driver | Base | Step | Key output at −step | Key output at +step |
|---|---|---|---|---|
| [Driver] | [value] | [±20%] | [value] | [value] |

## All assumptions
| Assumption | Value | Unit/period | Source | Set by | Plausibility |
|---|---|---|---|---|---|
| [Name] | [n] | [unit] | [source or "guess"] | [name] | [vs history/benchmark, or "[check: ...]"] |

## Structural issues
- [Issue and where in the model]
```

## Example

**Input:**

> Kestrel (B2B SaaS) 2-year plan. Starting MRR 60,000. New MRR per month 9,000 growing 10% monthly. Monthly revenue churn 1%. Gross margin 80%. Headcount 14 → 30 by month 12; average cost 9,000 per person per month. Cash 2,400,000. Model says cash-out month 26. History (last 6 months): new MRR averaged 6,500, best month 8,100; revenue churn averaged 2.2%. User benchmark: none given.

**Output (excerpt):**

```markdown
# Assumptions review — Kestrel 2-year plan

**Key output:** cash-out month: 26
**Summary:** The plan reaches month 26 on cash by assuming new MRR starts above the best month so far and grows 10% every month, with churn less than half of history. If new MRR and churn stay at their 6-month history, cash runs out earlier [check: rerun the model with history values].

## The 3 that matter most
| # | Assumption | Value | Evidence | If wrong (downside) | To raise confidence |
|---|---|---|---|---|---|
| 1 | Starting new MRR per month | 9,000 | Guess; history avg 6,500, best 8,100 | [check: rerun at 6,500] | Show the pipeline that supports 9,000 |
| 2 | New MRR growth | 10% per month | Guess; no history given | [check: rerun at 0% and 5%] | Tie to planned sales hires and quota |
| 3 | Revenue churn | 1% per month | History 2.2% | [check: rerun at 2.2%] | Name the retention changes that halve churn |

## Structural issues
- Headcount more than doubles by month 12, but new MRR growth isn't linked to sales hires; the 2 should move together.
```

## Checks before you send

- [ ] Every assumption has a value, unit, and source, or "guess".
- [ ] Sensitivity changes one input at a time, with the step stated.
- [ ] The top 3 are ranked by effect on the key output, not by opinion.
- [ ] Every benchmark cited came from the user; history comparisons use the user's data.
- [ ] No output number is stated that the model or a shown calculation didn't produce; reruns are "[check: ...]".

## Common mistakes

- Reviewing only the inputs tab and missing numbers typed inside formulas.
- Changing several inputs at once and calling it sensitivity. That's a scenario; label it as one.
- Bringing an outside benchmark from memory to judge a growth rate.
