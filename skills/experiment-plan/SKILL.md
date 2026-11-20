---
name: experiment-plan
description: Writes an A/B test brief before the test starts, with a falsifiable hypothesis, one primary metric and guardrail metrics, the minimum detectable effect, a sample size and duration estimate with the method shown, a sample ratio mismatch check, stop rules, and the decision rule written in advance. Use when someone plans an A/B test, split test, or experiment on a page, pricing, onboarding, or email and asks for a test plan, hypothesis, sample size, or how long to run it.
---

# Experiment plan

An experiment is only worth running if the team writes down, before it starts, what result will change what they do. Fix the sample size and the decision rule in advance; deciding after seeing the numbers turns noise into "wins". The plan should let someone else run the test and reach the same decision.

## When to use

- Before launching an A/B test on a page, flow, email, price, or feature.
- When someone asks "how long should we run this?" or "how many users do we need?".
- When a past test was called early and the team wants a stricter process.
- Not for reading results of a finished test without a plan. Not for qualitative research: use interview-guide.

## What you need

- The change to test and why the team believes it will help.
- The primary metric and its current baseline rate (for example, 4.0% sign-up rate). If the baseline is missing, ask once; without it you can't size the test, so mark the sample size "[open: needs baseline]".
- Weekly traffic or users who would enter the test. If missing, mark duration "[open]".
- Optional: the smallest lift worth acting on, and metrics that must not get worse.

## Steps

1. **Write a falsifiable hypothesis.** "Because [evidence], we believe [change] for [audience] will increase [primary metric]. We'll know it's true if [metric] rises by at least [MDE]." If there's no evidence, say so; the test is then exploratory.
2. **Pick one primary metric and 1 to 3 guardrails.** The primary metric decides the test. Guardrails are metrics that must not get worse, such as refunds, unsubscribes, page load time, or support tickets. Choose the primary metric closest to the outcome the change can move within the test window.
3. **Set the minimum detectable effect.** The MDE is the smallest change the test can reliably detect. Choose it from the business side: the smallest lift worth shipping. A smaller MDE needs a much larger sample.
4. **Estimate sample size and duration, and show the method.** Defaults: 5% significance (α) and 80% power, the common settings in tools like Statsig. For a conversion rate, Evan Miller's rule of thumb is n = 16 × p(1 − p) ÷ δ² per variant, where p is the baseline rate and δ the absolute MDE. Duration = (n × number of variants) ÷ weekly users in the test, rounded up to whole weeks so every weekday is covered. Confirm with a calculator before launch and name it.
5. **Write the stop rules.** Don't stop early because the result looks significant: Evan Miller shows that repeated peeking inflates false positives. Stop early only for harm: a guardrail breaking a threshold you set now, or a broken experience. Check for sample ratio mismatch (the observed split differs from the planned one) with a chi-square test before reading results; Microsoft's experimentation team requires every test to pass this check first.
6. **Write the decision rule before launch.** State what you'll do for each outcome: ship if the primary metric beats the MDE and no guardrail breaks; don't ship if a guardrail breaks; if the result is inconclusive, keep control and record what you learned. Name who decides.
7. **List risks and the readout date.** Novelty effects, seasonality, overlap with other tests, and tracking gaps. Set the readout date from the duration, not from a meeting.

## Output format

```markdown
# Experiment plan: [name]

**Owner:** [person] · **Decision maker:** [person] · **Start:** [date] · **Readout:** [date]

## Hypothesis
Because [evidence], we believe [change] for [audience] will increase [metric]. We'll know it's true if [metric] rises by at least [MDE].

## Variants
- **Control:** [current experience]
- **Variant B:** [change]
- **Split:** [e.g. 50/50] · **Audience:** [who enters, who is excluded]

## Metrics
| Metric | Role | Baseline | Threshold |
|---|---|---|---|
| [metric] | Primary | [rate] | MDE: [absolute and relative] |
| [metric] | Guardrail | [rate] | Stop if worse than [value] |

## Sample size and duration
- α = [0.05] · power = [80%] · baseline p = [rate] · absolute MDE δ = [value]
- Estimate: n = 16 × p(1 − p) ÷ δ² = [math] ≈ [n] per variant
- Weekly users in test: [n] → duration: [n] weeks
- Confirmed with: [calculator name, or "to confirm"]

## Stop rules
- No early stop for a positive result.
- Stop for harm if: [guardrail threshold] or [broken experience].
- Sample ratio check: chi-square on assignment counts before reading results; investigate before analysis if it fails.

## Decision rule
- **Ship** if: [condition]
- **Don't ship** if: [condition]
- **Inconclusive:** [what happens]

## Risks
- [risk] — [mitigation]
```

## Example

**Input:** "We want to test a shorter sign-up form (3 fields instead of 7). Sign-up rate is 4% of pricing-page visitors. About 6,000 visitors a week. We'd ship it if it adds a point."

**Output:**

```markdown
# Experiment plan: Short sign-up form

**Owner:** [person] · **Decision maker:** [person] · **Start:** [date] · **Readout:** start + 3 weeks

## Hypothesis
Because [check: evidence, e.g. form analytics showing drop-off at field 4], we believe a 3-field sign-up form for pricing-page visitors will increase sign-up rate. We'll know it's true if sign-up rate rises by at least 1 percentage point (4% to 5%).

## Variants
- **Control:** 7-field form
- **Variant B:** 3-field form (email, password, company name [to confirm])
- **Split:** 50/50 · **Audience:** new visitors to the pricing page; logged-in users excluded

## Metrics
| Metric | Role | Baseline | Threshold |
|---|---|---|---|
| Sign-up rate | Primary | 4.0% | MDE: +1.0 point (25% relative) |
| Activation within 7 days of sign-up | Guardrail | [open: baseline] | Stop if more than [value] below control |
| Spam sign-ups | Guardrail | [open: baseline] | Stop if doubled |

## Sample size and duration
- α = 0.05 · power = 80% · baseline p = 0.04 · absolute MDE δ = 0.01
- Estimate: n = 16 × 0.04 × 0.96 ÷ 0.01² = 6,144 per variant
- Weekly users in test: 6,000 → 12,288 ÷ 6,000 = 2.05 weeks → 3 weeks
- Confirmed with: to confirm in a sample size calculator before launch

## Stop rules
- No early stop for a positive result.
- Stop for harm if spam sign-ups double, or the form fails to submit.
- Sample ratio check before reading results.

## Decision rule
- **Ship** if sign-up rate is at least 1 point higher, statistically significant, and no guardrail breaks.
- **Don't ship** if activation drops past the threshold, even if sign-ups rise.
- **Inconclusive:** keep the 7-field form; test removing fields one at a time next.

## Risks
- Fewer fields may mean less data for sales follow-up — sales lead to confirm which fields they use.
- A holiday week in the window would skew traffic — check the calendar before start.
```

## Checks before you send

- [ ] The hypothesis names the change, the audience, the metric, and the MDE.
- [ ] There is exactly one primary metric and at least 1 guardrail with a stop threshold.
- [ ] The sample size math is shown with the inputs used; missing inputs are marked open.
- [ ] Duration is rounded up to whole weeks.
- [ ] The decision rule covers ship, don't ship, and inconclusive, and names who decides.
- [ ] No baseline, traffic number, or evidence appears that the user didn't give.

## Common mistakes

- Choosing the MDE after seeing traffic so the test "fits" in a week. Pick the MDE from what's worth shipping, then accept the duration.
- Running a test the traffic can't power. If duration exceeds about 8 weeks (our default), test a bigger change or a metric with a higher base rate.
- Adding guardrails after the results are in. They must be in the plan before launch.
