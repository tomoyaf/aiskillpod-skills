---
name: bullseye-channel-plan
description: Picks the customer acquisition channel to focus on with the Bullseye framework from Gabriel Weinberg and Justin Mares's Traction - brainstorm one idea for every traction channel, rank them into promising and possible rings, run cheap parallel tests on the top few, and focus on the one that works - with test budgets, success numbers and a stop rule. Use when someone asks how to get customers, which marketing channel to try, the Bullseye framework, Traction by Weinberg, growth channels for a startup, or why marketing efforts are scattered.
---

# Bullseye channel plan

Gabriel Weinberg, founder of DuckDuckGo, and Justin Mares wrote Traction, which collects the channels through which a startup can get customers and the way to choose among them. Weinberg described the Bullseye framework in a 2015 excerpt as three steps around a target. In the outer ring, brainstorm at least one realistic idea for each traction channel, including ones that seem unusual for the business. In the middle ring, pick the most promising few and run cheap tests on them at the same time. In the inner ring, focus on the one channel that tests show works, until it stops growing. The book counts 19 channels. This skill runs the three rings with the team's facts.

## When to use

- A product works for early customers, and the team needs a repeatable way to get more.
- Marketing effort is spread thin across many channels with no clear winner.
- A channel that worked has stopped growing.
- Not for writing ads or posts in one channel: use ad-copy-variants or social-post-from-article. Not for designing funnel stages: use funnel-stage-design.

## What you need

- The product, the customer, the price and what a customer is worth (revenue or margin per customer).
- Channels tried so far, with spend and results.
- Budget and team time available for tests.
- How customers found you so far.
- Never invent channel results or costs; mark guesses "[estimate]" and tests will replace them.

## Steps

1. **Set the traction goal.** Write the number of customers (or users) needed by a date, and the most the business can pay per customer. Every channel is judged against these.
2. **Brainstorm the outer ring.** Write one specific idea for each of the 19 channels: targeting blogs, publicity, unconventional PR, search engine marketing, social and display ads, offline ads, search engine optimization, content marketing, email marketing, viral marketing, engineering as marketing, business development, sales, affiliate programs, existing platforms, trade shows, offline events, speaking engagements and community building. One line each, specific to this product.
3. **Rank into rings.** For each idea, estimate how many customers it could bring, cost per customer and time to learn. Put the 3 most promising in the middle ring ("promising") and the next few in "possible". Mark estimates "[estimate]".
4. **Design cheap tests for the middle ring.** For each, a test that costs little and runs in weeks, with a budget, a duration and the numbers that would count as success: cost per customer and volume.
5. **Run the tests in parallel.** Record results in the same table, side by side, so channels are compared with real numbers.
6. **Pick the inner ring.** Choose the one channel that beat its success numbers. Focus most of the effort there, and set a stop rule: the signal that it has stopped growing, when the team goes back to the outer ring.
7. **Plan the next cycle.** Note what each failed test taught, and which "possible" ideas move up next time.

## Output format

```markdown
# Bullseye channel plan: [product]

**Traction goal:** [customers by date] · **Most we can pay per customer:** [amount]

## Outer ring: one idea per channel
| Channel | Specific idea | Customers it could bring | Cost per customer | Time to learn |
|---|---|---|---|---|

## Middle ring: tests
| Channel | Test | Budget | Duration | Success if |
|---|---|---|---|---|

## Results
| Channel | Spent | Customers | Cost per customer | Beat target? |
|---|---|---|---|---|

## Inner ring
**Focus on:** [channel] — [why]
**Stop rule:** [signal it has stopped growing]

## Next cycle
- [what we learned, what moves up]
```

## Example

**Input:** "We sell a booking app for dog groomers in Australia, 49 AUD a month. 60 customers, mostly from a groomers' Facebook group where the founder posts. Customers stay about 2 years on average. We have 3,000 AUD and 10 hours a week for marketing over the next 6 weeks. Google Ads last year cost 400 AUD per customer. We want 150 customers by June."

**Output:**

```markdown
# Bullseye channel plan: groomer booking app

**Traction goal:** 150 customers by June (90 more) · **Most we can pay per customer:** [check: margin; revenue is about 1,176 AUD over 2 years at 49 AUD a month]

## Outer ring: one idea per channel
| Channel | Specific idea | Customers it could bring | Cost per customer | Time to learn |
|---|---|---|---|---|
| Community building | Run a weekly tips thread in the groomers' Facebook group | [estimate] | low [estimate] | 4 weeks |
| Business development | Partner with a grooming supplies wholesaler to include us in orders | [estimate] | [estimate] | 6+ weeks |
| Trade shows | A stand at [check: national pet trade show] | [estimate] | [estimate] | the show date |
| Engineering as marketing | A free no-show cost calculator for groomers | [estimate] | [estimate] | 3 weeks |
| Search engine marketing | Google Ads, tighter keywords | 400 AUD last year | 400 AUD | known |
| Sales | Call groomers listed in [check: a directory] | [estimate] | [estimate] | 2 weeks |
| Affiliate programs | Pay current customers for referrals | [estimate] | [estimate] | 4 weeks |
| [the other 12 channels] | [one idea each] | | | |

## Middle ring: tests
| Channel | Test | Budget | Duration | Success if |
|---|---|---|---|---|
| Affiliate programs | Offer 1 free month for each referral that stays 2 months | 600 AUD [estimate] | 6 weeks | 10+ customers at under 150 AUD each |
| Sales | 100 calls to groomers from a directory | 10 hours a week | 4 weeks | 8+ customers |
| Engineering as marketing | Build the calculator, share it in the group and to groomer blogs | 800 AUD | 6 weeks | 300 uses and 6+ customers |

## Results
| Channel | Spent | Customers | Cost per customer | Beat target? |
|---|---|---|---|---|
| [fill in after the tests] | | | | |

## Inner ring
**Focus on:** [the channel that beats its target]
**Stop rule:** cost per customer rises above [check: limit] for 4 weeks, or new customers fall for a month.

## Next cycle
- If none beats its target, move the trade show and the wholesaler partnership up.
```

## Checks before you send

- [ ] All 19 channels appear in the outer ring, each with a specific idea or "not applicable" and why.
- [ ] Each middle-ring test has a budget, a duration and success numbers set before it starts.
- [ ] Tests fit inside the stated budget and time.
- [ ] Past results come from the input; estimates are marked "[estimate]".
- [ ] One inner-ring channel and a stop rule are named, or the output says the tests haven't run yet.

## Common mistakes

- Skipping the brainstorm and testing only familiar channels. The point of the outer ring is to find the overlooked one.
- Testing one channel at a time. Parallel tests compare channels on the same numbers.
- Expensive first tests. A test should answer "is this promising?" cheaply.
- Staying in the inner ring after it stops growing. Channels saturate; return to the outer ring.
