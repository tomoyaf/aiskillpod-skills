---
name: strategy-kernel
description: Writes a one-page strategy kernel in Richard Rumelt's sense - a diagnosis of the critical challenge, a guiding policy that says how to deal with it, and a short set of coherent actions that reinforce each other - then runs a bad-strategy test for fluff, failure to face the challenge, goals mistaken for strategy, and bad strategic objectives. Use when someone asks to write or fix a strategy, check whether a strategy is any good, turn a list of goals or initiatives into a real strategy, or mentions the strategy kernel, Good Strategy Bad Strategy, diagnosis guiding policy coherent action, or Rumelt.
---

# Strategy kernel

A strategy is a way through a difficulty, not a list of ambitions. Richard Rumelt argues that every good strategy has the same core, which he calls the kernel. In plain terms: say what the real problem is and why it is hard (the diagnosis), pick one way of attacking it (the guiding policy), and commit to a few steps that back each other up (coherent actions). He set this out in "The perils of bad strategy" (McKinsey Quarterly, June 2011) and in his book Good Strategy Bad Strategy (2011), which also names the signs of bad strategy: fluff, failure to face the challenge, mistaking goals for strategy, and bad strategic objectives. This skill drafts the kernel on one page and then tests the draft, or an existing strategy, against those signs.

## When to use

- A team has goals and a list of initiatives but can't say what problem the plan solves.
- A leader asks "is this strategy any good?" about a deck, a plan, or a board paper.
- Starting a strategy for a company, a product, a function, or a team.
- Before setting OKRs or a quarterly plan, so the goals follow from a strategy.
- Not for choosing how to plan in a given environment (use strategy-style-selector), and not for the full set of linked choices from aspiration to management systems (use strategy-choice-cascade).

## What you need

- The situation: what is happening, what changed, the numbers the user has (revenue, share, churn, costs), and the obstacle they think matters most.
- The current strategy or plan, if one exists, in its own words.
- Resources and constraints: people, money, time, what can't change.
- Who the strategy is for (company, unit, team) and who decides.
- Never invent facts, market data, or numbers. Ask once for what is missing; then mark it "[check: ...]". If the user has no view of the main obstacle, the first draft says so and the diagnosis is the open question.

## Steps

1. **Collect the facts and the existing plan.** Restate the situation in a few lines, with numbers and their sources. If there is an existing strategy, quote its stated goals and initiatives as they are written; you will test them in step 6.
2. **Write the diagnosis.** Name the one or two aspects of the situation that matter most and explain why they are the obstacle. Leave out the side issues; the reader should finish it knowing which part of the problem to push on. Write it as a judgment, not a list of every problem. If two diagnoses are plausible, write both and say what evidence would decide between them.
3. **Write the guiding policy.** State the overall approach to the obstacle in one or two sentences. It should rule things out: name what the organization will not do because of it. A guiding policy is a method, not a goal; "grow 20%" is not one, "win back renewals by owning onboarding for small accounts" is.
4. **Write three to five coherent actions.** Each action is a concrete commitment of people, money, or time that carries out the policy. Then check coherence: for each pair, say how one supports the other. Drop actions that don't connect to the policy, even if they are good ideas.
5. **Add a near-term objective.** Pick one objective the organization can actually reach soon with what it has, that moves it through the obstacle. Give it an owner and a date.
6. **Run the bad-strategy test.** Check the draft, and any existing strategy, for the four signs. Fluff: impressive-sounding words that say nothing a reader didn't already know. Failure to face the challenge: the plan never says what is standing in the way. Mistaking goals for strategy: targets and ambitions with no account of how to get there. Bad strategic objectives: a long wish list with no order, or objectives that leave the team no closer to an answer than before. For each sign, mark Pass or Fail with the line that fails and a rewrite.
7. **End with decisions and next actions.** What the decider must agree to, what to stop doing because of the policy, and the facts still to check.

## Output format

```markdown
# Strategy kernel: [organization or unit]
**Decider:** [name] · **Date:** [date] · **Scope:** [company / unit / team]

## Diagnosis
[2–4 sentences: what is going on, the critical obstacle, why it is hard. Facts with sources.]

## Guiding policy
[1–2 sentences: the overall approach.]
**We will not:** [what the policy rules out]

## Coherent actions
1. **[Action]** — [owner] — [resources]
2. **[Action]** — [owner] — [resources]
3. **[Action]** — [owner] — [resources]

**How they fit:** [one line per pair or chain: action 1 makes action 2 work because ...]

## Near-term objective
[One objective reachable with current resources] — [owner] — [date]

## Bad-strategy test
| Sign | Pass / Fail | Line that fails | Rewrite |
|---|---|---|---|
| Fluff | | | |
| Failure to face the challenge | | | |
| Mistaking goals for strategy | | | |
| Bad strategic objectives | | | |

## Decisions and next actions
- **Decide:** [what to approve]
- **Stop:** [what the policy ends]
- **Check:** [check: ...]
```

## Example

**Input:** "We run a meal-kit service in Osaka, 2,400 subscribers. Last year's strategy: 'Become Kansai's most customer-centric food platform. Goals: 30% subscriber growth, launch a corporate lunch line, add vegan boxes, open Kobe, build an app, improve NPS.' Subscribers grew only 4%. Our data: 55% of new subscribers cancel within their first 8 weeks; those who pass 8 weeks stay about 14 months on average. Exit surveys: most say cooking took longer than the 30 minutes we promise. Team of 18, including a head chef with two cooks in our test kitchen, an operations lead, a data lead, and a customer team of 2 led by our head of customer. Decider is the CEO, Mr. Tanaka."

**Output:**

```markdown
# Strategy kernel: Osaka meal-kit service
**Decider:** Mr. Tanaka (CEO) · **Date:** [date] · **Scope:** company

## Diagnosis
Growth is stuck because new subscribers leave before the habit forms: 55% cancel within 8 weeks, while those who stay past 8 weeks stay about 14 months. Exit surveys point to one cause: recipes take longer than the 30 minutes we promise. The problem is the first 8 weeks, not reach.

## Guiding policy
Make the first 8 weeks reliably easy, so more new subscribers reach the point where they stay.
**We will not:** open Kobe, launch the corporate lunch line, or build an app this year.

## Coherent actions
1. **Rebuild the first-8-week menu around recipes timed under 30 minutes in home tests** — head chef — two cooks, part of the test-kitchen budget [check: amount]
2. **Pre-cut the two most time-consuming ingredients in starter boxes** — operations lead — [check: added cost per box]
3. **Call or message every new subscriber in week 2 and week 5** — customer team (2 people) — [check: hours available]
4. **Report cancellations by week and reason every Monday** — data lead — existing tools

**How they fit:** Actions 1 and 2 remove the cause in the surveys. Action 3 catches the subscribers they don't reach, and its notes feed the menu changes. Action 4 shows within weeks whether 1 to 3 are working.

## Near-term objective
Cut first-8-week cancellations from 55% to [check: target the team believes] for subscribers who join next quarter — head of customer — end of next quarter

## Bad-strategy test
| Sign | Pass / Fail | Line that fails | Rewrite |
|---|---|---|---|
| Fluff | Fail | "Kansai's most customer-centric food platform" | "Make the first 8 weeks reliably easy" |
| Failure to face the challenge | Fail | Old plan never names early cancellations | Diagnosis above names the 8-week drop-off |
| Mistaking goals for strategy | Fail | "30% subscriber growth" with no account of how | Growth follows from more subscribers passing week 8 |
| Bad strategic objectives | Fail | Six unprioritized goals, including Kobe and an app | One near-term objective; Kobe, app, and lunch line stopped |

## Decisions and next actions
- **Decide:** approve the guiding policy and the four actions.
- **Stop:** Kobe opening, corporate lunch line, app build.
- **Check:** [check: added cost per pre-cut box], [check: test-kitchen budget], [check: target for 8-week cancellations]
```

## Checks before you send

- [ ] The diagnosis names a specific obstacle and the facts behind it.
- [ ] The guiding policy is a method, not a target, and says what it rules out.
- [ ] Every action carries out the policy, and the draft says how the actions support each other.
- [ ] There is one near-term objective the team can reach with what it has.
- [ ] The bad-strategy test marks each sign Pass or Fail with the failing line.
- [ ] No number is invented; gaps are marked "[check: ...]".

## Common mistakes

- Starting with goals and calling the result a strategy. Start with the obstacle.
- A diagnosis that lists every problem. Pick the one or two that explain the rest.
- A guiding policy so broad that nothing is ruled out.
- Keeping every initiative from the old plan. Coherence means dropping good ideas that don't fit.
- Writing the kernel in the language of a vision statement. If a sentence would fit any company, cut it.
