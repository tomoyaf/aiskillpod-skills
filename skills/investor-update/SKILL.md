---
name: investor-update
description: Writes a short, honest monthly investor update from the founder's notes and numbers, with a 2-to-3-sentence summary, KPIs with month-over-month change, highlights, lowlights with cause and fix, cash, burn and runway, and specific asks. Never invents numbers. Use when a founder asks for an investor update, a monthly update to investors or angels, a shareholder update, or a "what happened this month" email to backers.
---

# Investor update

An investor update keeps backers informed so they can help, and so bad news never arrives as a surprise. Keep it short, put the numbers and the asks near the top, report lowlights as plainly as highlights, and use only the numbers the founder gave.

## When to use

- Monthly at pre-seed and seed, or quarterly after a larger round.
- Before a fundraise, to show a consistent track record.
- When something went wrong and investors should hear it from the founder first.
- Not for the internal leadership report: use monthly-kpi-summary.

## What you need

- The founder's notes for the month: wins, problems, hires, launches, customers.
- KPIs for this month and last month, defined the same way as in past updates.
- Cash at month end, net burn, runway. If runway isn't given, compute it as cash ÷ average monthly net burn and show the formula; if burn is missing, write "[check: burn]".
- The asks: intros, hires, advice. If none are given, ask once; an update without asks wastes the readers.
- The last update, if any, to keep the same KPIs and format.

## Steps

1. **Write the summary first.** 2 to 3 sentences: the most important thing that happened, the main number, and the biggest problem. A reader who stops here knows how the month went.
2. **Show KPIs in a table.** 3 to 6 metrics, the same ones every month: this month, last month, change. Keep metrics that got worse. If a metric is new or its definition changed, say so.
3. **List 3 to 5 highlights.** Each is a fact with a number or name: "Signed Harlow Foods, 24,000 per year". No adjectives standing in for facts.
4. **List 1 to 3 lowlights, each with cause and fix.** "Lost our second-largest customer (budget cut); we're adding a lower tier to keep similar accounts." Never skip lowlights; a month with none reads as a month with something hidden.
5. **State cash, burn, and runway.** Cash at month end, net burn (cash out − cash in), runway in months with the formula. If runway is under 6 months, say so in the summary too.
6. **Make 1 to 3 specific asks.** Name the type of person or the company: "Intro to a head of operations at a 50 to 200 person logistics company." Not "intros to customers".
7. **Keep it under 400 words.** Our default: plain email, no attachments needed to understand it.

## Output format

```markdown
**Subject:** [Company] — [month] update: [one-line headline]

Hi all,

[Summary: 2–3 sentences]

**Asks**
1. [Specific ask]

**KPIs**
| Metric | [Month] | [Last month] | Change |
|---|---|---|---|
| [Metric] | [n] | [n] | [+/-] |

**Highlights**
- [Fact]

**Lowlights**
- [What happened] — cause: [cause]; fix: [fix]

**Cash**
Cash [amount] · net burn [amount]/month · runway [n] months ([cash] ÷ [burn])

Thanks,
[Founder]
```

## Example

**Input:**

> Tidewater (B2B scheduling). October. MRR 41,200 (Sept 37,900). Customers 88 (Sept 84). Logo churn 1 customer. Signed Harlow Foods 2,000 MRR. Launched SMS reminders. Lost Brightpath Clinics (1,100 MRR, budget cut). Hired Dev as first support lead. Cash 905,000. Net burn last 3 months: 78,000, 81,000, 84,000. Asks: intro to ops leaders at clinic chains of 10+ sites; advice on SOC 2 auditors.

**Output:**

```markdown
**Subject:** Tidewater — October update: MRR 41,200, up 8.7%

Hi all,

MRR grew 8.7% to 41,200, helped by signing Harlow Foods. We lost Brightpath Clinics to a budget cut. Runway is 11.2 months.

**Asks**
1. Intros to operations leaders at clinic chains with 10 or more sites.
2. Recommendations for a SOC 2 auditor you've seen work well with a small team.

**KPIs**
| Metric | October | September | Change |
|---|---|---|---|
| MRR | 41,200 | 37,900 | +3,300 (+8.7%) |
| Customers | 88 | 84 | +4 |
| Customers lost | 1 | [check: Sept churn] | |

**Highlights**
- Signed Harlow Foods, 2,000 MRR.
- Launched SMS reminders.
- Hired Dev as our first support lead.

**Lowlights**
- Lost Brightpath Clinics (1,100 MRR) — cause: budget cut; fix: [check: founder's planned response]

**Cash**
Cash 905,000 · net burn 81,000/month (3-month average) · runway 11.2 months (905,000 ÷ 81,000)

Thanks,
[Founder]
```

## Checks before you send

- [ ] The summary alone tells a reader how the month went, including the main problem.
- [ ] Every number is from the input or computed from it, with runway's formula shown.
- [ ] KPIs are the same as last update, including ones that got worse.
- [ ] Every lowlight has a cause and a fix, or a "[check: ...]".
- [ ] Asks are specific enough that an investor knows who to introduce.
- [ ] Under 400 words.

## Common mistakes

- Dropping a metric the month it gets worse. Investors notice.
- Asks like "intros to anyone relevant". Nobody acts on it.
- Writing the lowlight's fix yourself when the founder didn't give one. Mark it.
