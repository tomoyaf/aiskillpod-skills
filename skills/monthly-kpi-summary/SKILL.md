---
name: monthly-kpi-summary
description: Writes a monthly KPI summary for leadership from a metrics table, with a one-line headline, each KPI against last month and against target with the reason behind the change, and 3 things to act on. Never invents numbers and marks every gap. Use when someone shares a metrics sheet, dashboard export, or KPI table and asks for the monthly report, a board or leadership summary, "how did we do this month", or a KPI recap.
---

# Monthly KPI summary

Leadership reads the summary to decide where to spend next month's attention. Lead with the one sentence they'd repeat, show each KPI against last month and target, explain the why only where you have evidence, and end with 3 actions. A gap marked as a gap beats a number that sounds right.

## When to use

- Month closed and leadership wants the KPI read-out.
- Before a monthly leadership, all-hands, or board prep meeting.
- A dashboard exists but nobody has written what it means.
- Not for an investor-facing update: use investor-update. Not for budget lines: use budget-variance-note.

## What you need

- The metrics table: each KPI's value this month, last month, and target. If last month or target is missing for a KPI, write "[check: last month]" or "no target set" in that cell.
- How each KPI is defined, if not obvious (what counts as an active user, is revenue booked or recognized). If a definition is unclear, state the one you assumed.
- Context for the why: launches, campaigns, price changes, incidents, staffing. If none is given, write "reason not given" rather than guessing.

## Steps

1. **Check the table before writing.** Compute each change yourself: absolute and percent vs last month, and gap to target. If a number in the table looks inconsistent (a total that doesn't match its parts), flag it at the top; don't fix it silently.
2. **Mark status per KPI.** Our default: on track if at or above target; at risk if within 10% below target; off track if more than 10% below. For KPIs where lower is better (churn, cost, response time), flip the direction.
3. **Explain the why only from evidence.** Tie each notable change to a fact in the input: "Signups +18% after the 9 May webinar". If no fact explains it, write "reason not given" and add it to questions. Never fill in a plausible story.
4. **Write the headline.** One sentence: the most important result and its consequence. "Revenue hit target for the first time this year, but churn rose to 3.1%." Not "Mixed month".
5. **Pick 3 things to act on.** Each names the KPI, the action, and an owner if one was given. Prefer off-track KPIs with a known cause. If there aren't 3 that warrant action, list fewer.
6. **List the gaps.** Every missing number, definition, or reason, as a short list at the end.

## Output format

```markdown
# KPI summary — [month year]

**Headline:** [one sentence]

| KPI | This month | Last month | Change | Target | Status |
|---|---|---|---|---|---|
| [KPI] | [value] | [value] | [+/- abs, %] | [value] | On track / At risk / Off track |

## What moved and why
- **[KPI]:** [change] — [reason from input, or "reason not given"]

## 3 things to act on
1. [KPI]: [action] — [owner, or "owner to assign"]

## Gaps and questions
- [Missing number, definition, or reason]

**Data notes:** [inconsistencies found, definitions assumed]
```

## Example

**Input:**

> May metrics, Corvid Analytics:
> MRR: 182,000 (April 171,000; target 180,000)
> New customers: 41 (April 38; target 50)
> Logo churn: 2.9% (April 1.8%; target under 2%)
> Support first response (hours): 5.2 (April 3.1; target 4)
> Notes: price increase for new customers on 1 May. One support agent on leave half the month.

**Output:**

```markdown
# KPI summary — May

**Headline:** MRR passed target at 182,000, but logo churn rose to 2.9% against a 2% target.

| KPI | This month | Last month | Change | Target | Status |
|---|---|---|---|---|---|
| MRR | 182,000 | 171,000 | +11,000, +6.4% | 180,000 | On track |
| New customers | 41 | 38 | +3, +7.9% | 50 | Off track (18% below) |
| Logo churn | 2.9% | 1.8% | +1.1 pts | under 2% | Off track |
| First response (hours) | 5.2 | 3.1 | +2.1, +68% | 4 | Off track |

## What moved and why
- **MRR:** +6.4% — the 1 May price increase for new customers likely contributed [check: split of MRR growth between price and new customers]
- **New customers:** +3, below target — reason not given
- **Logo churn:** up 1.1 points — reason not given
- **First response:** slower — one agent on leave for half the month

## 3 things to act on
1. Logo churn: pull the list of May cancellations with reasons — owner to assign
2. First response: cover support leave in June — owner to assign
3. New customers: check whether the price increase hurt conversion — owner to assign

## Gaps and questions
- Why did churn rise? Were churned accounts on the old or new price?
- Why were new customers 9 short of target?

**Data notes:** churn assumed to be logo churn, customers lost ÷ customers at start of month.
```

## Checks before you send

- [ ] Every number in the summary appears in the input or is computed from it.
- [ ] Changes and gaps to target are computed correctly, with direction flipped for lower-is-better KPIs.
- [ ] Every "why" points at a fact in the input, or says "reason not given".
- [ ] The headline is one sentence with a specific result.
- [ ] No more than 3 actions.
- [ ] Gaps are listed, not filled.

## Common mistakes

- Writing "driven by strong demand" with no evidence. That's a guess.
- Showing percent change for rates (churn 1.8% → 2.9% is +1.1 points, not +61% unless you say so).
- Burying an off-track KPI under 4 on-track ones.
