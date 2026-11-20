---
name: unit-economics-check
description: Checks a startup's unit economics from the user's own numbers. Recomputes CAC, LTV, LTV to CAC ratio, CAC payback months, and gross margin with every formula shown, and flags definitional mistakes such as revenue-based LTV instead of gross-margin LTV, blended CAC hiding paid CAC, or churn on the wrong base. Use when someone shares CAC, LTV, payback, or margin figures, a pitch deck metrics slide, or a SaaS metrics sheet and asks to check the math or "are our unit economics good".
---

# Unit economics check

Unit economics are only useful if they're defined the way investors and operators read them. Recompute each metric from the raw inputs, show the formula, and point out where a definition inflates the result. Benchmarks are reference points, not verdicts.

## When to use

- Before a fundraise, when a metrics slide shows LTV:CAC or payback.
- When marketing and finance report different CAC numbers.
- Before raising ad spend, to check paid acquisition pays back.
- Not for a full model review: use model-assumptions-review.

## What you need

- Acquisition: sales and marketing spend for the period (and what's included: salaries, ads, tools, agencies), new customers in the same period, split by paid vs organic if known.
- Revenue: average revenue per customer per month (or ARPA), and gross margin % (revenue minus cost to serve, such as hosting, support, payment fees).
- Retention: monthly customer or revenue churn, and how it was calculated.
- Their own stated CAC, LTV, payback, if they have them, so you can compare.
- Anything missing is "[check: ...]". Never fill in an industry-average churn or margin.

## Steps

1. **Recompute CAC.** CAC = sales and marketing spend ÷ new customers, same period. Show what spend was included. If only ad spend is included, call it "paid media CAC", not CAC. If paid and organic are mixed, also compute paid CAC = paid spend ÷ paid-acquired customers if the split is given.
2. **Recompute gross margin.** Gross margin % = (revenue − cost of revenue) ÷ revenue. Check that hosting, third-party software in the product, payment fees, and customer support are in cost of revenue. If not, flag that margin is overstated.
3. **Recompute LTV on gross margin.** Customer lifetime (months) = 1 ÷ monthly churn rate. LTV = ARPA per month × gross margin % × lifetime. If their LTV uses revenue without margin, flag it and show both. If churn is under 1% per month or based on fewer than 6 months of data, flag that lifetime is likely overstated.
4. **Compute LTV:CAC.** LTV ÷ CAC. Reference point: a ratio above 3 is often cited for SaaS, and that guide assumes gross-margin LTV. State the ratio; don't call it good or bad without the user's own target.
5. **Compute CAC payback.** Payback (months) = CAC ÷ (ARPA per month × gross margin %). Reference points: under 12 months is commonly cited as healthy for SaaS; 5 to 7 months is strong. Enterprise sales often run longer.
6. **List definitional issues.** Check each: revenue LTV vs margin LTV; blended CAC hiding paid CAC; spend and customers from different periods; churn as a share of end-of-period customers instead of start; annual contracts counted as monthly; expansion revenue inside new-customer ARPA. Each issue gets the effect on the number.
7. **Summarize.** Their figure vs your recomputed figure for each metric, and the 1 or 2 issues that matter most.

## Output format

```markdown
# Unit economics check — [company], [period]

## Results
| Metric | Their figure | Recomputed | Formula | Note |
|---|---|---|---|---|
| CAC | [n] | [n] | [spend ÷ new customers] | [what's included] |
| Gross margin | [%] | [%] | [(revenue − COGS) ÷ revenue] | |
| Lifetime (months) | | [n] | [1 ÷ monthly churn] | |
| LTV | [n] | [n] | [ARPA × GM% × lifetime] | |
| LTV:CAC | [x] | [x] | [LTV ÷ CAC] | reference: above 3 often cited |
| CAC payback (months) | [n] | [n] | [CAC ÷ (ARPA × GM%)] | reference: under 12 often cited |

## Definitional issues
1. **[Issue]:** [what was done] → [effect on the number]

## What matters most
- [1–2 bullets]

## Missing
- [Inputs not given]
```

## Example

**Input:**

> Brisa (B2B SaaS), Q2. Sales and marketing spend 180,000 (ads 90,000, 2 SDR salaries 60,000, tools 30,000). New customers 120 (paid ads brought 50). ARPA 400 per month. Gross margin 78% (hosting only in COGS; support team 9,000 per month not included). Monthly logo churn 1.5%. Deck says LTV 26,667 and LTV:CAC 17.8.

**Output (excerpt):**

```markdown
# Unit economics check — Brisa, Q2

## Results
| Metric | Their figure | Recomputed | Formula | Note |
|---|---|---|---|---|
| CAC | 1,500 [inferred: 26,667 ÷ 17.8] | 1,500 | 180,000 ÷ 120 | all S&M included |
| Paid CAC | | 1,800 | 90,000 ÷ 50 | ads only; excludes SDR time |
| Gross margin | 78% | [check: revenue to include support] | | support not in COGS |
| Lifetime (months) | | 66.7 | 1 ÷ 0.015 | |
| LTV | 26,667 | 20,800 | 400 × 0.78 × 66.7 | theirs is revenue-based (400 × 66.7) |
| LTV:CAC | 17.8 | 13.9 | 20,800 ÷ 1,500 | reference: above 3 often cited |
| CAC payback (months) | | 4.8 | 1,500 ÷ (400 × 0.78) | |

## Definitional issues
1. **Revenue-based LTV:** 400 × 66.7 = 26,667 ignores margin → overstates LTV by 28% (26,667 vs 20,800).
2. **Support outside COGS:** 9,000 per month of support isn't in cost of revenue → gross margin, LTV, and payback are all better than reality [check: quarterly revenue to recompute margin].
3. **Lifetime of 66.7 months:** at 1.5% churn this assumes 5+ years; [check: how many months of churn data?].

## What matters most
- Restate LTV on gross margin before the deck goes out: 20,800, ratio 13.9.

## Missing
- Total revenue for Q2, to put support into gross margin.
```

## Checks before you send

- [ ] Every recomputed metric shows its formula and the input numbers.
- [ ] LTV uses gross margin, and any revenue-based LTV is flagged.
- [ ] CAC spend and new customers come from the same period.
- [ ] Benchmarks are labelled as reference points, not verdicts.
- [ ] No churn, margin, or ARPA appears that isn't in the input; gaps are "[check: ...]".

## Common mistakes

- Taking a very low churn from a few months of data and getting a 10-year lifetime.
- Leaving salaries out of CAC because they're "fixed".
- Comparing a margin-based LTV:CAC to a revenue-based one from another company.
