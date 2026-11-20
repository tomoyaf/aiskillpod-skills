---
name: decision-bias-review
description: Reviews a pending decision for the judgment errors Daniel Kahneman describes in Thinking, Fast and Slow - fast intuitive answers taken as fact, anchoring, judging only from the evidence in view, the planning fallacy, loss aversion and narrow framing - then adds an outside view from a reference class and a pre-mortem, and states what would change the call. Use when someone asks to check a decision for bias, run a pre-mortem, get an outside view, sanity-check a forecast or estimate, review a hiring, pricing or investment call, or apply Thinking Fast and Slow.
---

# Decision bias review

Daniel Kahneman's Thinking, Fast and Slow (2011) describes two modes of thinking. System 1 is fast, automatic and intuitive; System 2 is slow, effortful and deliberate. Most judgments come from System 1, and System 2 often accepts them without checking. The book collects the errors that follow, many from Kahneman's research with Amos Tversky. This skill takes a decision that is about to be made, looks for the errors that most often distort business decisions, and adds two corrections the book recommends: the outside view (start from how similar cases turned out) and the pre-mortem (a technique Kahneman credits to Gary Klein).

## When to use

- Before a decision that is hard to reverse: a hire, a price change, an investment, a launch date, a large contract.
- When a forecast or estimate feels confident but rests on one story.
- When a team agreed quickly and nobody argued.
- Not for writing the decision up for others: use decision-memo after this review. Not for weighing whether the decision can be reversed: use bezos-style-door-check.

## What you need

- The decision, the options considered, and the option the team leans toward.
- The estimates it rests on (cost, time, revenue, probability), and where each number came from.
- Who was involved and how the discussion went, if known.
- Any record of similar past decisions or projects, inside or outside the company.
- If the source of a number is missing, mark it "[check: source]". Never invent base rates; ask for them or say where to find them.

## Steps

1. **State the decision and the intuitive answer.** Write the question, the leading option, and the one-sentence reason people give for it. That reason is often System 1's answer.
2. **Trace each key number.** For every estimate, note where it came from. Flag numbers that started from a figure someone mentioned first (anchoring), from a single vivid case (availability), or from the plan with no comparison (planning fallacy).
3. **Check what you see is all there is.** Kahneman's phrase for judging only from the evidence in view. List the information that would matter but isn't in the input: failure cases, the customers who didn't reply, the costs nobody estimated.
4. **Check the framing.** Restate the choice as a gain and as a loss. If the preference flips, loss aversion or framing is at work. Check whether the decision is judged alone when it is really one of many similar bets (narrow framing).
5. **Take the outside view.** Name a reference class: similar projects, hires, launches or deals. Give the typical outcome (time, cost, success rate) if the input has it, or say where to get it. Adjust the team's estimate from that base rate, not the other way round.
6. **Run a pre-mortem.** Imagine it is a year later and the decision has failed. Write the 3 to 5 most plausible reasons, each with an early warning sign.
7. **Recommend.** Say whether to proceed, proceed with changes, gather one more piece of evidence, or stop. Name what evidence would change the call, and who decides.

## Output format

```markdown
# Decision bias review: [decision]

**Date:** [date] · **Decider:** [name]

## Decision and intuitive answer
**Question:** [question] · **Leaning toward:** [option] · **Reason given:** [one sentence]

## Where the numbers come from
| Estimate | Value | Source | Risk |
|---|---|---|---|

## What isn't in view
- [missing information that would matter]

## Framing check
**As a gain:** [restated] · **As a loss:** [restated] · **Does the preference change?** [yes/no and why]

## Outside view
**Reference class:** [similar cases] · **Typical outcome:** [base rate or where to find it] · **Adjusted estimate:** [value]

## Pre-mortem: it failed because
1. [reason] — early sign: [signal]

## Recommendation
[Proceed / proceed with changes / get one more piece of evidence / stop] — [why]
**Would change the call:** [evidence] · **Decides:** [name, date]
```

## Example

**Input:** "We plan to open a second café in March. Our manager says fit-out will take 6 weeks and cost 60,000 euros, because the first one took 6 weeks. Daily sales should hit 900 euros by month two; our first café does 1,100 now, after three years. The landlord offered a 10-year lease and said the rent is 20% below market. Everyone in the meeting agreed. Our contractor's last two jobs for other clients both ran about 4 weeks late."

**Output:**

```markdown
# Decision bias review: opening a second café in March

**Date:** [date] · **Decider:** [check: owner]

## Decision and intuitive answer
**Question:** sign the 10-year lease and open in March? · **Leaning toward:** yes · **Reason given:** the first café works, so a second will too.

## Where the numbers come from
| Estimate | Value | Source | Risk |
|---|---|---|---|
| Fit-out time | 6 weeks | the first café | Planning fallacy: one case, and the contractor's last two jobs ran about 4 weeks late |
| Fit-out cost | 60,000 euros | the manager [check: quote] | No written quote in the input |
| Sales by month two | 900 euros a day | anchored on today's 1,100 | The first café reached 1,100 after three years [check: its month-two sales] |
| Rent | 20% below market | the landlord | The other side of the deal set the anchor [check: comparable rents] |

## What isn't in view
- The first café's sales in its first months.
- Footfall at the new site.
- What it costs to leave the lease early.

## Framing check
**As a gain:** a second café adds sales. · **As a loss:** if sales stay below [check: break-even], the lease locks in losses for up to 10 years. · **Does the preference change?** Likely: the loss frame shows the lease length matters more than the opening date.

## Outside view
**Reference class:** second sites opened by single-site cafés, and this contractor's recent jobs. · **Typical outcome:** the contractor's jobs ran about 4 weeks late; for café ramp-up, [check: industry or bank data]. · **Adjusted estimate:** about 10 weeks of fit-out, so plan for April or later.

## Pre-mortem: it failed because
1. Fit-out ran late and the café opened after the spring season — early sign: no fixed contractor date by [check].
2. Sales ramped like the first café's early months, not like today's — early sign: below [check: break-even] in month two.
3. The rent wasn't below market — early sign: comparable rents within 10%.

## Recommendation
Proceed with changes: get the first café's first-year sales and two comparable rents, plan fit-out at about 10 weeks, and ask for a break clause.
**Would change the call:** early sales and comparable rents that support 900 euros a day by month two. · **Decides:** [check: owner, date]
```

## Checks before you send

- [ ] Every key number has a source, or is marked "[check: source]".
- [ ] At least one reference class is named, with a base rate from the input or where to find one.
- [ ] The pre-mortem has specific reasons and early signs, not generic risks.
- [ ] Biases are named only where the input shows them, each tied to a number or statement.
- [ ] It ends with a recommendation, what would change it, and who decides.

## Common mistakes

- Listing every bias in the book. Name the ones the input shows.
- Treating the review as a veto. The aim is a better estimate and a clearer call.
- Inventing base rates. A wrong base rate is another anchor.
- Citing individual studies from the book as settled. Some priming results it reports have failed to replicate, and Kahneman acknowledged this; the decision tools here don't depend on them.
