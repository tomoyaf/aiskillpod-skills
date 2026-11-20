---
name: quarterly-planning
description: Builds a quarterly planning pack for a team - last quarter's review, real capacity after time off and run work, priorities ranked with an explicit cut line, dependencies on other teams, risks, and a split between committed work and stretch. Use when a manager, founder, or team lead asks for quarterly planning, Q1 to Q4 planning, a quarterly roadmap, capacity planning, "what can we actually do next quarter", or a planning doc for leadership.
---

# Quarterly planning pack

Planning is mostly deciding what not to do. The pack ranks every candidate, adds up real capacity, and draws a cut line: everything above it is committed, everything below is stretch or not this quarter. Like Shape Up's "fixed time, variable scope", the quarter's length is fixed and the scope is what moves.

## When to use

- Before a quarterly planning meeting, for one team or a small company.
- When a team has more requests than people and needs a defensible "no".
- To turn last quarter's results and a pile of ideas into a ranked plan.
- Not for writing the goals themselves (use okr-draft) or a single project plan.

## What you need

- Last quarter's goals and what happened (numbers if possible).
- The candidate work: projects, requests, goals, each with a rough size. If sizes are missing, ask once; otherwise use S/M/L with [assumption].
- The team: people, planned time off, recurring duties (on-call, support rotation).
- Known dependencies and dates (launches, contracts, events).

## Steps

1. **Review last quarter in 5 lines or fewer.** Each goal: hit, partly, missed, with the number and one reason. Carry over only unfinished work that still matters; re-rank it with everything else.
2. **Calculate real capacity.** Working weeks per person, minus time off and holidays, minus recurring duties. Then hold back a buffer for unplanned work. Our default is 20%; use the team's own history if it has one. Show the arithmetic.
3. **Rank every candidate in one list.** No ties. Rank by the quarter's goal first, then by cost of delay (what we lose by waiting a quarter). Mark anything with a fixed external date.
4. **Draw the cut line.** Walk down the ranking, adding sizes until planned capacity is used. Everything above the line is committed. The next 1 to 2 items are stretch: done only if committed work finishes early. Everything else is "not this quarter", listed by name.
5. **Map dependencies.** For each committed item, what it needs from another team or vendor, by when, and who confirmed. An unconfirmed dependency on a committed item is a risk.
6. **List the top risks.** 3 to 5, each with an owner and a trigger that means "act now". Typical ones: a key person leaving or on leave, an unconfirmed dependency, an estimate that is a guess.
7. **Write the summary.** 3 sentences: what we commit to, what we won't do, what we need from leadership.

## Output format

```markdown
# [Team] — [quarter] plan

## Summary
[What we commit to · what we won't do · what we need]

## Last quarter
| Goal | Result | Why |
|---|---|---|
| [goal] | hit / partly / missed: [number] | [one line] |

## Capacity
| Person | Weeks available | Minus time off | Minus run work | Net weeks |
|---|---|---|---|---|
**Total net:** [n] weeks · **Buffer ([n]%):** [n] · **Plannable:** [n] weeks

## Priorities
| Rank | Item | Size (weeks) | Running total | Why this rank |
|---|---|---|---|---|
| 1 | [item] | [n] | [n] | [goal / cost of delay] |
| | **Cut line: committed above, stretch below** | | | |
| [n] | [stretch item] | [n] | | |

## Not this quarter
- [Item] — [one-line reason]

## Dependencies
| Item | Needs | From | By | Confirmed? |
|---|---|---|---|---|

## Risks
| Risk | Owner | Act-now trigger |
|---|---|---|
```

## Example

**Input:** "Data team Q2. 3 people (Ana, Ben, Chloe), 13 weeks. Ana off 2 weeks. Ben does on-call 1 week in 4. Last Q: goal 'self-serve dashboards for sales' — shipped 3 of 5. Candidates: finish sales dashboards (4 wks), churn model (8 wks), migrate to new warehouse (12 wks, IT says warehouse contract ends 30 June), finance reporting automation (7 wks), marketing attribution (6 wks)."

**Output:**

```markdown
# Data team — Q2 plan

## Summary
We commit to the warehouse migration (contract ends 30 June), the remaining sales dashboards, and the finance reporting automation. The churn model is stretch and marketing attribution waits for Q3. We need IT to confirm the new warehouse access by 15 April.

## Last quarter
| Goal | Result | Why |
|---|---|---|
| Self-serve dashboards for sales | partly: 3 of 5 shipped | [check: reason not given] |

## Capacity
| Person | Weeks available | Minus time off | Minus run work | Net weeks |
|---|---|---|---|---|
| Ana | 13 | 2 | 0 | 11 |
| Ben | 13 | 0 | 3.25 (on-call 1 in 4) | 9.75 |
| Chloe | 13 | 0 | 0 | 13 |
**Total net:** 33.75 weeks · **Buffer (20%):** 6.75 · **Plannable:** 27 weeks

## Priorities
| Rank | Item | Size (weeks) | Running total | Why this rank |
|---|---|---|---|---|
| 1 | Warehouse migration | 12 | 12 | Fixed date: contract ends 30 June |
| 2 | Finish sales dashboards (2 left) | 4 | 16 | Carry-over; sales is waiting |
| 3 | Finance reporting automation | 7 | 23 | [assumption] saves finance time at every month-end |
| | **Cut line: committed above, stretch below** | | | |
| 4 | Churn model | 8 | 31 | Over plannable capacity by 4 weeks |

## Not this quarter
- Marketing attribution (6 weeks) — doesn't fit the 4 weeks left after committed work; first in line for Q3.

## Dependencies
| Item | Needs | From | By | Confirmed? |
|---|---|---|---|---|
| Warehouse migration | New warehouse access | IT | 15 April | no |

## Risks
| Risk | Owner | Act-now trigger |
|---|---|---|
| Migration overruns the 30 June contract end | Chloe | Less than 50% migrated by 20 May |
| Ana's 2 weeks off overlap the migration cutover | Ana | Cutover date set inside her leave |
```

## Checks before you send

- [ ] Capacity shows the arithmetic, including time off, run work, and the buffer.
- [ ] The ranking has no ties, and the cut line sits where the running total meets plannable capacity.
- [ ] Every item below the line is named as stretch or "not this quarter".
- [ ] Every committed item's dependency says whether it's confirmed.
- [ ] Sizes and numbers not in the input are marked "[assumption]" or "[check: ...]".

## Common mistakes

- Planning to 100% of capacity. Unplanned work always arrives; the buffer is what keeps commitments true.
- Carrying last quarter's unfinished work to the top by default. Re-rank it like everything else.
- Leaving "not this quarter" unstated. Stakeholders assume their item is in until told otherwise.
