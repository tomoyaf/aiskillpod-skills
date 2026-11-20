---
name: ai-pilot-plan
description: Writes a short AI pilot plan for one team - the one or two tasks to try, who takes part, the baseline measured before the pilot, four weeks of steps (a kick-off week, two weeks of use, a measuring week), the rules that apply, success and stop criteria agreed up front, and the decision to take at the end. Use when a manager or founder asks for an AI pilot plan, an AI proof of concept, a generative AI PoC plan, a trial of ChatGPT or Claude for a team, or how to test AI before rolling it out.
---

# AI pilot plan

A pilot answers one question: should this team keep using AI for this task, the way we tried it? It needs a task that repeats, a number measured before the pilot starts, a fixed end date, and success and stop criteria written down before anyone sees results. Microsoft and LinkedIn's 2024 Work Trend Index found 59% of leaders worried about quantifying AI's productivity gains; a baseline taken before the pilot is what makes the gain measurable.

## When to use

- A team wants to try ChatGPT, Claude or another AI tool on real work before buying seats for everyone.
- A manager has to justify an AI budget with evidence.
- An earlier "let's all try AI" effort faded without a result.
- Not for building an AI product or choosing between AI vendors: use a vendor comparison for that.

## What you need

- The team, and the tasks it repeats every week, with rough minutes per task.
- The AI tool and plan that would be used, and the company's AI rules.
- Who can take part, and for how long.
- Who decides at the end.

## Steps

1. **Pick one or two tasks.** Weekly or more often, 20 minutes or more each time, easy to check, no data the rules forbid. One task beats five.
2. **Name the people.** Three to six people who do the task, at least one sceptic, one owner who runs the pilot.
3. **Measure the baseline first.** For one week before the pilot, record minutes per task and one quality signal people already track (rework, errors, reply rate). No baseline, no pilot.
4. **Write the success and stop criteria.** Agreed before the start: for example, at least 30% less time with no drop in quality = continue; any confidential data in a personal account = stop. Use the team's numbers.
5. **Plan the weeks.** Week 1: shared instructions for the task and a 45-minute kick-off. Weeks 2 to 3: use it on real work, log minutes and problems. Final week: measure the same way as the baseline.
6. **State the rules.** Which account, what never goes in, who reads output before it leaves the company.
7. **Set the decision.** Date, who decides, and the three possible outcomes: roll out, change and re-test, or stop. Write what each would mean for seats and budget.

## Output format

```markdown
# AI pilot: [team] · [task]
Owner: [name] · Decides: [name] · Dates: [start] to [end]

## Tasks
| Task | How often | Minutes now | Quality signal |
|---|---|---|---|

## People
[names and roles; the sceptic]

## Success and stop criteria (agreed [date])
- Continue if: [criteria]
- Stop if: [criteria]

## Weeks
| Week | What happens | Measured |
|---|---|---|

## Rules
- Account: [tool, plan] · Never paste: [list] · Reads before sending: [who]

## Decision on [date]
| Outcome | What it means |
|---|---|
| Roll out | |
| Change and re-test | |
| Stop | |
```

## Example

**Input:** "Customer support team, 6 people, answers about 300 emails a week, average 6 minutes each. Want to try Claude Team for first drafts. Support lead Rina runs it; COO decides. Rules: no customer payment details in any AI."

**Output (start):**

```markdown
# AI pilot: Customer support · first drafts of email replies
Owner: Rina · Decides: COO · Dates: 1 Dec to 26 Dec

## Tasks
| Task | How often | Minutes now | Quality signal |
|---|---|---|---|
| Reply to a customer email | ~300 a week | 6 | Reopened tickets (now 8%) |

## Success and stop criteria (agreed 28 Nov)
- Continue if: 4 minutes or less per reply in the final week, and reopened tickets at 8% or lower.
- Stop if: payment details go into any AI tool, or reopened tickets rise above 10%.
```

## Checks before you send

- [ ] One or two tasks only, each repeated weekly.
- [ ] A baseline is measured before the pilot starts.
- [ ] Success and stop criteria use numbers and were agreed before the start.
- [ ] The rules name the account and the data that never goes in.
- [ ] There's a decision date, a decider, and what each outcome means.

## Common mistakes

- No baseline, so nobody can say whether it worked.
- Ten tasks at once, so no task gets enough use to judge.
- Criteria written after the results, which turns the pilot into a debate.
