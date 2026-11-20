---
name: budget-variance-note
description: Explains budget vs actual variances for a month or quarter. Applies a materiality threshold (a percent and an amount), labels each variance favorable or unfavorable, names its driver (timing, volume, price or rate, one-off), and states the impact on the full-year forecast. Use when someone shares a budget vs actuals table, a P&L against budget, or department spend and asks for a variance analysis, variance commentary, "why are we over budget", or a BvA note.
---

# Budget variance note

A variance note tells leadership which differences from budget matter, why they happened, and whether they change the year. Filter first with a threshold so the note covers the few lines that matter, then give each one a driver and a forecast impact. If the input doesn't say why, the note says so.

## When to use

- Month or quarter closed and you have budget vs actual by line.
- A department head asks why their spend is over.
- Before a forecast update, to decide what to re-forecast.
- Not for a KPI read-out: use monthly-kpi-summary.

## What you need

- Budget and actual per line (revenue, cost of sales, each expense line), for the period and year to date if available.
- The threshold. If none is given, use our default: explain any line over both 10% and [amount] from budget, and mark the amount "[check: threshold amount]". Never pick the amount yourself.
- Context for drivers: hires and their start dates, contracts, price changes, invoices that arrived early or late, one-off events. If missing, the driver is "not given".
- The current full-year forecast, if any.

## Steps

1. **Compute each variance.** Variance = actual − budget, and % = variance ÷ budget. Label favorable or unfavorable: for revenue, actual above budget is favorable; for costs, actual below budget is favorable. Don't use + and − alone; readers misread them.
2. **Apply the threshold.** Keep lines over both the percent and the amount. List the rest as "within threshold" in one line. Always keep revenue and total operating expenses, even if within threshold. Explain large favorable variances too; they often mean a padded budget or a delay. A line that moved from or to zero is tested on the amount alone.
3. **Name the driver.** One of: timing (spend or revenue moved between periods, no change to the year), volume (more or fewer units, customers, hours, people), price or rate (same volume, different price or rate), one-off (won't recur), or not given. A line can have 2 drivers; split the amount if the input lets you.
4. **State the forecast impact.** Timing: no full-year impact, reverses in [month]. Volume or price: likely continues; show the run-rate effect only with a formula from the input. One-off: none beyond this period. If you can't tell, say "[check: does this continue?]".
5. **Write the headline.** Total variance vs budget and the 1 to 2 lines that explain most of it.
6. **List questions for line owners.** One per line where the driver is "not given".

## Output format

```markdown
# Budget vs actual — [period]

**Headline:** [total variance, favorable/unfavorable, and the main lines]
**Threshold:** over [x]% and over [amount] [our default / company rule]

| Line | Budget | Actual | Variance | % | F/U | Driver | Forecast impact |
|---|---|---|---|---|---|---|---|
| [Line] | [n] | [n] | [n] | [%] | F / U | [timing/volume/price/one-off/not given] | [none / continues / reverses in month / check] |

## Notes per line
- **[Line]:** [what happened, from the input; split by driver if possible]

**Within threshold:** [lines, one line]

## Questions for owners
- [Line] — [owner]: [question]
```

## Example

**Input:**

> Q2 budget vs actual, Marlow Health (thousands). Threshold: 10% and 15.
> Revenue: budget 900, actual 860
> Salaries: budget 520, actual 488 — 2 engineering hires started in June, planned for April
> Software: budget 40, actual 61 — annual analytics licence paid upfront in May, budget spread it monthly
> Marketing: budget 120, actual 152 — conference sponsorship added in May
> Rent: budget 60, actual 60
> Travel: budget 18, actual 22

**Output:**

```markdown
# Budget vs actual — Q2 (thousands)

**Headline:** Revenue is 40 (4%) under budget; costs are 25 over overall, mostly the conference sponsorship and the upfront software licence, partly offset by late hires.
**Threshold:** over 10% and over 15 (company rule)

| Line | Budget | Actual | Variance | % | F/U | Driver | Forecast impact |
|---|---|---|---|---|---|---|---|
| Revenue | 900 | 860 | 40 | 4% | U | not given | [check: does this continue?] |
| Software | 40 | 61 | 21 | 53% | U | timing (annual licence paid upfront) | None for the year; lower than budget in later months [check: licence amount] |
| Marketing | 120 | 152 | 32 | 27% | U | one-off (conference sponsorship) | None if not repeated |
| Total operating expenses | 758 | 783 | 25 | 3% | U | sum of the cost lines | See the lines above |

## Notes per line
- **Revenue:** within threshold but shown as a key line; reason not given.
- **Software:** the analytics licence was paid in full in May; the budget spreads it monthly.
- **Marketing:** conference sponsorship added in May, not in budget.
- **Total operating expenses:** within threshold (3%) but shown as a key line; salaries, software, marketing, rent and travel add up to 758 budget and 783 actual.

**Within threshold:** Salaries (32 favorable, 6%: 2 engineering hires started in June instead of April), Rent (0), Travel (4, 22% but under 15).

## Questions for owners
- Revenue — sales lead: what caused the 40 shortfall, and does it continue in Q3?
- Marketing — marketing lead: is the sponsorship a one-time event?
```

## Checks before you send

- [ ] Every variance is actual − budget, with favorable/unfavorable labelled correctly for revenue and costs.
- [ ] Only lines over both thresholds are explained, plus revenue and total costs.
- [ ] Each driver comes from the input or says "not given".
- [ ] Timing variances say when they reverse; nothing is called one-off without evidence.
- [ ] No number appears that isn't in the input or computed from it.

## Common mistakes

- Calling every overspend "timing" because it sounds harmless. Ask for the evidence.
- Explaining 15 small lines and burying the 2 that matter.
- Using percent alone. A 50% variance on a small line can matter less than 5% on salaries.
