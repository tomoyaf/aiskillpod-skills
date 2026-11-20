---
name: build-measure-learn
description: Turns a new product, feature, or business idea into a one-page experiment card in the build-measure-learn style from Eric Ries's The Lean Startup - the leap-of-faith assumption to test (value or growth hypothesis), the smallest test that could prove it wrong (an MVP), the metric and pass threshold set in advance, a decision date, and the pivot-or-persevere rule. Plans the loop in reverse: what to learn, then what to measure, then what to build. Use when someone asks for an MVP plan, how to validate an idea, a build-measure-learn loop, validated learning, innovation accounting, whether to pivot or persevere, or "what's the smallest thing we can build to test this".
---

# Build-measure-learn loop

A new product is a set of guesses. The build-measure-learn loop tests the riskiest guess first with the smallest thing you can put in front of real customers, measures what they do, and decides whether to keep going or change course. Eric Ries described the loop in The Lean Startup (2011). He calls the unit of progress validated learning: evidence from customer behavior, not features shipped. The book's advice is to run the loop forwards but plan it in reverse: decide what you need to learn, then what to measure, then what to build.

## When to use

- A team is about to spend weeks or months building something new and the core assumptions are untested.
- Someone asks "what's our MVP?" or "how do we validate this before we build it?".
- A product has been live a while, numbers are flat, and the team argues about whether to pivot.
- Not for testing a change on an existing product with enough traffic to split it: use experiment-plan for an A/B test with sample sizes. Not for interviews alone: use interview-guide or jtbd-switch-interview.

## What you need

- The idea in one or two sentences: for whom, what problem, what you'd offer.
- What the team already knows: interviews, sign-ups, sales calls, numbers. If there is no evidence, say so; the first card then tests the most basic assumption.
- How much time and money the team can put into one test, and who decides.
- The current baseline, if the product exists (for example, weekly active users, trial-to-paid rate). If missing, ask once; then mark it "[check: baseline]". Never invent baselines or market sizes.

## Steps

1. **List the leap-of-faith assumptions.** Write the beliefs the whole plan depends on. Sort them into the two kinds Ries names: the value hypothesis (customers get real value once they use it) and the growth hypothesis (new customers will find it and come). Add any other belief that, if false, ends the plan (they will pay this price, a partner will integrate).
2. **Pick the riskiest one.** Choose the assumption that is most likely to be false and most costly if it is. Test one per card. If two are tied, test the cheaper one first.
3. **Write what you need to learn.** One falsifiable sentence: "We believe [customer] will [behavior] because [reason]." Behavior beats opinion: paying, signing up, coming back, referring. "Would you use this?" answers don't count as learning.
4. **Choose the metric and set the threshold now.** One metric that shows the behavior, measured per cohort (the people who entered in the same period), not a running total. Set the pass line before the test starts: "at least [n] of [n] trial users do [behavior] within [days]". Write why that number: what result would make the business work. Avoid vanity metrics such as total sign-ups or page views, which rise whatever you do.
5. **Design the smallest test.** Pick the cheapest MVP that produces that metric with real customers: a landing page with a price and a sign-up, a manual service delivered by hand behind a simple front end, a demo video, a pre-order, a single-feature version. Ries defines the MVP as the version that gets the most validated learning for the least effort, so cut anything that doesn't feed the metric.
6. **Set the decision date and the rule.** Fix the end date and the minimum number of customers. Write the rule: persevere if the metric clears the threshold; pivot if it falls clearly short (name which part of the plan you would change: customer segment, problem, channel, price, or solution); if it lands in between, name the one change you'll test next. Name who decides.
7. **Plan the next loop.** Say what you will test next if this one passes, and schedule a regular pivot-or-persevere review (for example, every few weeks) so the decision is made on evidence, not mood.

## Output format

```markdown
# Experiment card: [name]

**Owner:** [name] · **Decider:** [name] · **Start:** [date] · **Decision date:** [date]

## Leap-of-faith assumptions
| Assumption | Type | Risk if false | Tested here? |
|---|---|---|---|
| [belief] | Value / Growth / Other | [what breaks] | Yes / Later |

## What we need to learn
We believe [customer] will [behavior] because [reason].

## Metric and threshold (set before start)
- **Metric:** [behavior, per cohort]
- **Baseline:** [number or "none yet"]
- **Pass threshold:** [at least n of n do X within n days]
- **Why this number:** [what it means for the business]

## Smallest test (MVP)
- **What we build:** [the minimum]
- **Who sees it:** [customers, how many, where they come from]
- **What we leave out:** [list]
- **Cost and time:** [budget, days]

## Decision rule
- **Persevere** if: [metric ≥ threshold]
- **Pivot** if: [metric clearly below] → change [segment / problem / channel / price / solution]
- **In between:** [the one change we test next]

## Next loop
- If it passes, next we test: [assumption]
- Pivot-or-persevere review: [cadence and date]
```

## Example

**Input:** "We run a small bookkeeping firm. Idea: a monthly flat-fee 'close your books in 3 days' service for online shops with 1–10 staff. We think shop owners hate doing books and will pay $240 a month. We talked to 8 shop owners; 6 said month-end is painful. We don't know if they'd switch from their current accountant. We can spend about 3 weeks and $600 on a test. Partner Ken decides."

**Output:**

```markdown
# Experiment card: Flat-fee 3-day close for online shops

**Owner:** [check: owner] · **Decider:** Ken · **Start:** [date] · **Decision date:** start + 3 weeks

## Leap-of-faith assumptions
| Assumption | Type | Risk if false | Tested here? |
|---|---|---|---|
| Shop owners with 1–10 staff will pay $240 a month for a 3-day close | Value | No business | Yes |
| They will switch from their current accountant | Value | Few customers even if they like it | Later (a paid first month gives a first sign) |
| We can reach shop owners cheaply online | Growth | Customer cost too high | Later |
| We can close books in 3 days at this price | Other | Margin | Later |

## What we need to learn
We believe owners of online shops with 1–10 staff will book a paid first month at $240 because month-end bookkeeping is painful (6 of the 8 owners we talked to said so).

## Metric and threshold (set before start)
- **Metric:** shop owners who pay for a first month, out of those who reach the offer page
- **Baseline:** none yet
- **Pass threshold:** [check: number of paid first months the partners need, e.g. at least 4 within 3 weeks]
- **Why this number:** [check: how many clients make the service worth running]

## Smallest test (MVP)
- **What we build:** one page with the offer, the price, and a "book your first month" payment link; the first clients' books are closed by hand
- **Who sees it:** the 8 owners interviewed, plus [check: channel, e.g. a shop-owner community]
- **What we leave out:** software, onboarding automation, multiple plans
- **Cost and time:** up to $600, 3 weeks

## Decision rule
- **Persevere** if paid first months reach the threshold → test the growth hypothesis next.
- **Pivot** if paid first months fall clearly below the threshold → change the segment or the price, and ask non-buyers what stopped them [check: what counts as "clearly below"].
- **In between:** keep the page, test a lower first-month price.

## Next loop
- If it passes, next we test: whether one channel brings shop owners at a cost that fits the fee
- Pivot-or-persevere review: every 3 weeks, Ken decides
```

## Checks before you send

- [ ] The card tests one assumption, and it is the riskiest one listed.
- [ ] The metric measures customer behavior, not opinion, and is not a running total.
- [ ] The threshold and the decision date were set before the test, with a reason.
- [ ] The MVP leaves out everything that doesn't feed the metric.
- [ ] The decision rule covers persevere, pivot, and in between, and names who decides.
- [ ] No baseline, market size, or price appears that the user didn't give.

## Common mistakes

- Building first and deciding what to measure later. Plan in reverse: learn, measure, then build.
- An MVP that is a smaller version of the full product. It should be the cheapest thing that answers one question.
- Counting compliments or survey "yes" answers as validation. Ask for money, time, or a commitment.
- Moving the threshold after the results arrive. Then any result passes.
- Persevering by default. Without a scheduled pivot-or-persevere review, flat numbers drift on for months.
