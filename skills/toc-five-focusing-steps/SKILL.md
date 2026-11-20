---
name: toc-five-focusing-steps
description: Finds the one constraint that limits how much a team or business delivers, then works through the Theory of Constraints five focusing steps - identify, exploit, subordinate, add capacity, and repeat without letting inertia set in - and ends with a dated action list and the measures to watch (throughput, inventory, operating expense). Works for factories and for sales teams, support queues, content pipelines, and agencies. Use when someone asks for a bottleneck analysis, "where is our bottleneck", the five focusing steps, Theory of Constraints, TOC, The Goal by Goldratt applied to their work, drum-buffer-rope, or why work piles up even though everyone is busy.
---

# Theory of Constraints: five focusing steps

Every system that turns work into results has one step that limits the whole flow. The Theory of Constraints says to find that step, get the most out of it, make everything else serve it, and only then spend money to widen it. Eliyahu M. Goldratt created the method; it was popularized in The Goal (1984), his business novel with Jeff Cox about a plant manager saving his factory. The five focusing steps apply just as well to a sales team, a support queue, or a content pipeline: anywhere work waits in a line.

## When to use

- Work piles up, deadlines slip, and everyone is busy, but output doesn't grow.
- A team wants to hire or buy tools to go faster and needs to know where extra capacity would actually help.
- Several teams each "optimize" their own step and the end result doesn't move.
- Not for choosing which projects or features to do at all: use feature-prioritization. Not for a one-off incident review: use retrospective.

## What you need

- The goal of the system in one line, and how it is measured (for example, "paid orders shipped per week", "tickets closed within 24 hours", "articles published per month").
- The steps work passes through, in order, with who does each.
- For each step, what you know: weekly capacity, how much work waits in front of it, and how long it waits. If numbers are missing, ask once; then work from what the user says and mark gaps "[check: ...]". Never invent capacities or queue sizes.
- Optional: money per unit of output (price minus truly variable cost), the costs of running the team, and planned hires or purchases.

## Steps

1. **Define the goal and the flow.** Write the system's goal and the one measure of output. List the steps from first input to delivered result. Translate Goldratt's three measures into the user's terms: throughput (the rate at which the system makes money through sales, or the output that counts toward the goal), inventory (money and work tied up inside the system: open deals, unanswered tickets, drafts), and operating expense (what it costs to run the system).
2. **Identify the constraint.** Look for the step with the biggest queue in front of it, the longest waits, and the step whose idle hour costs the whole system an hour. Compare capacity with demand at each step if numbers exist. Name one constraint. If the limit is outside the team (not enough demand, a policy, a supplier), say so: a market or policy constraint is common and needs different actions from a capacity constraint.
3. **Decide how to exploit it.** Get more out of the constraint with what you already have, before spending. Typical moves: stop it from ever waiting for input, take low-value tasks off it, check quality before work reaches it so it never processes items that will be rejected, put only the highest-value work through it, and cover breaks so it never sits idle. Write each as a concrete change with an owner.
4. **Subordinate everything else to that decision.** Set the pace of every other step by what the constraint can absorb. Release new work only as fast as the constraint finishes work. Keep a small buffer of ready work in front of it so it never starves. Say plainly that other steps will sometimes be idle, and that this is correct. In a factory this is drum-buffer-rope: the constraint is the drum that sets the pace, the buffer protects it, and the rope ties the release of new work to the drum.
5. **Add capacity at the constraint only if steps 3 and 4 are not enough.** This is the fourth focusing step. Now consider adding capacity: a hire, a tool, outsourcing, a second shift. Estimate the gain in throughput against the added operating expense. Mark costs the user didn't give as "[check: ...]".
6. **Plan the repeat.** Once the constraint gains capacity, another step may become the limit. Name the likely next constraint. Set a review date, and list the old rules (batch sizes, approval steps, utilization targets) that were built around the old constraint and must be re-checked so inertia doesn't become the new constraint.
7. **Close with decisions and measures.** List the actions in order with owners and dates. Name the 3 measures to watch weekly: throughput, inventory waiting in front of the constraint, and operating expense. Say what result in 30 days would show the plan is working.

## Output format

```markdown
# Constraint review: [system name]

**Goal:** [one line] · **Output measure:** [unit per week/month] · **Owner:** [name] · **Date:** [date]

## The flow
| # | Step | Who | Capacity per [week] | Waiting in front | Typical wait |
|---|---|---|---|---|---|
| 1 | [step] | [team] | [n or check] | [n or check] | [time or check] |

## The constraint
**[Step name]** limits the system because [evidence: queue, waits, capacity vs demand].
Type: [capacity / market / policy / supplier]

## Measures in our terms
- **Throughput:** [what counts as output, and money per unit if known]
- **Inventory:** [work and money tied up inside the system]
- **Operating expense:** [what it costs to run, if known]

## 1. Exploit (no new spend)
| Change | Owner | By |
|---|---|---|

## 2. Subordinate
- Release rule: [new work enters only when ...]
- Buffer: [how much ready work sits in front of the constraint]
- Other steps: [what they stop doing or slow down]

## 3. Add capacity (only if 1 and 2 fall short)
| Option | Added capacity | Added cost | Decide by |
|---|---|---|---|

## 4. Repeat
- Likely next constraint: [step]
- Rules to re-check: [list]
- Review date: [date]

## Watch weekly
| Measure | Now | Target in 30 days |
|---|---|---|
```

## Example

**Input:** "We're a 9-person content agency. Flow: sales books a client, a strategist writes the brief, 4 freelance writers draft, our one editor (Mia) edits, the client approves, we publish. Writers can do about 30 drafts a week between them. Mia edits about 18 a week. There are 26 drafts waiting for her right now and they wait about 8 days. About a third of drafts come back to writers for a rewrite after Mia reads them. Clients want 25 articles a week in total. Sales wants to sign 2 more clients. We're thinking of hiring a second editor."

**Output:**

```markdown
# Constraint review: content production

**Goal:** publish client articles on time · **Output measure:** articles approved per week · **Owner:** [check: owner] · **Date:** [date]

## The flow
| # | Step | Who | Capacity per week | Waiting in front | Typical wait |
|---|---|---|---|---|---|
| 1 | Brief | Strategist | [check] | [check] | [check] |
| 2 | Draft | 4 freelance writers | ~30 | [check] | [check] |
| 3 | Edit | Mia | ~18 | 26 drafts | ~8 days |
| 4 | Client approval | Client | [check] | [check] | [check] |
| 5 | Publish | [check] | [check] | [check] | [check] |

## The constraint
**Editing (Mia)** limits the system: clients want 25 a week, Mia edits about 18, and 26 drafts wait about 8 days for her. Writers produce more than she can absorb.
Type: capacity

## Measures in our terms
- **Throughput:** articles approved per week [check: fee per article]
- **Inventory:** 26 drafts waiting for edit, plus drafts in rewrite
- **Operating expense:** writer fees, Mia's and the strategist's time [check: amounts]

## 1. Exploit (no new spend)
| Change | Owner | By |
|---|---|---|
| A brief checklist and a writer self-edit checklist, so fewer drafts need a rewrite after Mia reads them (about a third do today) | Strategist | [date] |
| Mia edits only; [check: tasks Mia does besides editing] move to others | [check: owner] | [date] |
| Mia's queue sorted by client deadline and fee, not arrival order | Mia | [date] |

## 2. Subordinate
- Release rule: writers start a new draft only when Mia's queue is under [check: e.g. 6] drafts.
- Buffer: keep a few ready drafts in front of Mia so she never waits.
- Other steps: writers spend spare hours on rewrites and research, not new drafts. Their drafting capacity will sit partly idle, and that is correct: drafts beyond what Mia can edit only lengthen her queue. Sales confirms start dates for the 2 new clients with production before signing.

## 3. Add capacity (only if 1 and 2 fall short)
| Option | Added capacity | Added cost | Decide by |
|---|---|---|---|
| Second editor, part-time | [check] | [check] | after 30 days of steps 1–2 |
| Senior writer edits short pieces | [check] | [check] | after 30 days of steps 1–2 |

## 4. Repeat
- Likely next constraint: client approval or briefing, once editing speeds up.
- Rules to re-check: [check: draft targets for writers, if any]; new clients signed without checking production capacity.
- Review date: [date + 30 days]

## Watch weekly
| Measure | Now | Target in 30 days |
|---|---|---|
| Articles approved per week | [check] | [check: toward 25] |
| Drafts waiting for edit | 26 | [check] |
| Rewrite rate after edit | about 1 in 3 | [check] |
| Operating expense per week | [check] | [check: no rise beyond planned] |
```

## Checks before you send

- [ ] Exactly one constraint is named, with the evidence for it.
- [ ] Exploit and subordinate come before any spend, and each change has an owner and a date.
- [ ] The plan says which steps will slow down or sit idle, and why that's correct.
- [ ] Throughput, inventory, and operating expense are stated in the user's own terms.
- [ ] Every number comes from the input or is marked "[check: ...]".
- [ ] It names the likely next constraint and a review date.

## Common mistakes

- Improving every step at once. Gains away from the constraint add inventory, not output.
- Hiring first. Exploiting and subordinating often free capacity at no cost; do them first and measure.
- Keeping everyone 100% busy. Non-constraints that run flat out flood the constraint with work it can't absorb.
- Calling the slowest person the constraint without evidence. Look at queues and waits, not opinions.
- Forgetting the repeat. Rules built for the old constraint keep running after it's gone.
