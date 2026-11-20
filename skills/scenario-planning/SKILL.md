---
name: scenario-planning
description: Runs a scenario planning exercise for one decision - writes the focal question, lists the key factors and driving forces, separates predetermined elements from critical uncertainties, crosses the two most important uncertainties into four scenarios, tests the decision in each, picks signposts to watch, and ends with robust moves to make now and contingent moves tied to signposts. Use when someone asks for a scenario planning template or example, how to plan under uncertainty, what could happen to the business in 5 to 10 years, a 2x2 scenario matrix, a stress test of a long-term bet, or Shell-style scenarios.
---

# Scenario planning

Scenario planning prepares a decision for several futures instead of betting on one forecast. You write a few distinct, plausible stories about how the outside world could unfold, check how a decision holds up in each, and decide what to do now and what to watch. Pierre Wack developed the approach at Royal Dutch/Shell with Ted Newland in the early 1970s and described it in two Harvard Business Review articles in 1985, "Scenarios: Uncharted Waters Ahead" (September) and "Scenarios: Shooting the Rapids" (November). Peter Schwartz, a former member of Shell's planning group, set out a step-by-step method in The Art of the Long View (Doubleday/Currency, 1991). This skill follows Schwartz's steps, and builds the scenarios with the common 2×2 approach: two critical uncertainties crossed into four worlds.

## When to use

- Before a long, hard-to-reverse commitment: a lease, a plant, a hire plan, an acquisition, a new country.
- When the team argues about one forecast and the honest answer is "it depends".
- An annual strategy review in a market where regulation, technology, or demand could shift.
- Testing whether the current strategy survives a bad but plausible future.
- Not for estimating next quarter's numbers (use a forecast or quarterly-planning), not for choosing among growth routes in a known market (use ansoff-growth-options), and not for a quick list of strengths and threats (use swot-tows-analysis).

## What you need

- The decision or question the scenarios must serve, and its time horizon. If missing, ask once: "What decision will these scenarios help you make, and how far ahead does it commit you?"
- What the user knows about the outside world: trends, regulation, technology, customers, competitors, costs, with sources if any.
- The current plan or the options being considered.
- Who will use the scenarios (owner, board, team), so the stories speak to their worries.
- Never invent trends, statistics, or forecasts. Every fact comes from the user or is marked "[check: ...]". Scenarios are stories built from stated forces, not predictions.

## Steps

1. **Write the focal question.** One sentence naming the decision and the horizon, such as "Should we sign an eight-year lease for a second site?". A vague question ("what is the future of retail?") gives vague scenarios. Ask for the decision if the user gave only a topic.
2. **List the key factors.** Write the local factors that decide whether the decision succeeds: customers' demand, prices, costs, competitors, staff, suppliers. Keep them close to the business.
3. **List the driving forces.** For each key factor, write the wider forces behind it: social, economic, political, environmental, and technological. Use only forces the user named or that follow directly from their facts; ask about any area left empty.
4. **Separate predetermined elements from critical uncertainties.** A predetermined element will happen in every scenario, because it is already under way (people already born, a law already passed, a contract already signed). A critical uncertainty is both important to the decision and genuinely open. Rank the forces on importance and uncertainty, and pick the two that score highest on both.
5. **Build four scenarios from two axes.** Make each critical uncertainty an axis with two clear end states. The four combinations are the scenarios. Give each a short, memorable name and a paragraph describing that world at the horizon, with every predetermined element present in all four. Check that each is internally consistent and plausible; if one combination makes no sense, say so and explain the three that remain.
6. **Test the decision in each scenario.** For each scenario, write how the decision and the current plan fare: what goes well, what breaks, and what the company would wish it had done. A decision that works in only one scenario is a gamble; name it as one.
7. **Choose signposts.** For each scenario, pick 1 to 3 observable signals that would show the world is moving toward it, with where to watch and how often. Prefer signals that appear early and that someone will actually check.
8. **Sort the moves.** Robust moves make sense in all or most scenarios: do them now. Contingent moves make sense only in some: prepare them, and tie each to the signpost that triggers it. Name any move to avoid because it fails badly in a plausible scenario.
9. **End with the decision and next actions.** Answer the focal question in one paragraph, list the robust moves with owners, the signposts with who watches them, and a date to review the scenarios.

## Output format

```markdown
# Scenarios: [focal question]
**Horizon:** [year] · **Prepared for:** [name or team] · **Date:** [date]

## Focal question
[One sentence: the decision and the horizon.]

## Key factors and driving forces
| Key factor | Driving forces behind it | Source |
|---|---|---|

## Predetermined elements
- [Element]: [why it is already settled] ([source or "[check: ...]"])

## Critical uncertainties
| Uncertainty | End state A | End state B | Why it matters to the decision |
|---|---|---|---|
| [axis 1] | | | |
| [axis 2] | | | |

## Four scenarios
| | [Axis 2: end state A] | [Axis 2: end state B] |
|---|---|---|
| **[Axis 1: end state A]** | [Scenario name] | [Scenario name] |
| **[Axis 1: end state B]** | [Scenario name] | [Scenario name] |

### [Scenario name]
[One paragraph: what this world looks like at the horizon.]

## The decision in each scenario
| Scenario | How the decision fares | What breaks | What we'd wish we had done |
|---|---|---|---|

## Signposts
| Scenario | Signal | Where to watch | How often | Who |
|---|---|---|---|---|

## Moves
- **Robust (do now):** [move], [owner]
- **Contingent:** [move], triggered by [signpost]
- **Avoid:** [move], because [scenario where it fails]

## Decision
[One paragraph answering the focal question.] Review the scenarios on [date].
```

## Example

**Input:** "We run Harbourline English, an English school for adults in Fukuoka: one site, 16 classrooms, about 700 students, 60% of revenue from individuals and 40% from company contracts (employers paying for staff lessons). Our landlord offers a second site near Hakata station on an eight-year lease, which we must sign or decline within two months. Facts: the city's population of people aged 20 to 39 has been falling for years and our planning assumes it keeps falling [check: city statistics]. Machine translation is improving fast, and we don't know whether that will make people want lessons less or want real conversation practice more. Since 2023, 30% of new individual students choose our online classes; the rest still come in person. Two of our company clients cut their training budgets this year; three others increased theirs. A national rule now requires companies of a certain size to report on staff training [check: exact rule], which our sales lead thinks will keep company budgets up."

**Output:**

```markdown
# Scenarios: Should Harbourline sign an eight-year lease for a second site near Hakata station?
**Horizon:** eight years (the lease term) · **Prepared for:** Harbourline English · **Date:** [date]

## Focal question
Should we sign the eight-year lease for a second site near Hakata station, decision due within two months?

## Key factors and driving forces
| Key factor | Driving forces behind it | Source |
|---|---|---|
| Number of individual students | Fewer people aged 20 to 39 in the city; better machine translation | User; [check: city statistics] |
| In-person vs online demand | Online share of new students (30% since 2023); comfort with online learning | User |
| Company contracts | Training budgets; national training reporting rule | User; [check: exact rule] |

## Predetermined elements
- Fewer people aged 20 to 39 in Fukuoka over the horizon: the fall has run for years and the plan treats it as settled ([check: city statistics]).
- Machine translation keeps improving; its effect on demand is the uncertainty, not the improvement.

## Critical uncertainties
| Uncertainty | End state A | End state B | Why it matters to the decision |
|---|---|---|---|
| How adults want to learn | Most choose in person | Most choose online | A second site only pays if people come in |
| Company training budgets | Grow (the reporting rule pushes them up) | Shrink (translation tools replace training) | Company contracts are 40% of revenue and fill daytime rooms |

## Four scenarios
| | Company budgets grow | Company budgets shrink |
|---|---|---|
| **Most choose in person** | Full Rooms | Evening Crowd |
| **Most choose online** | Screens at Work | Quiet Station |

### Full Rooms
Machine translation keeps improving, but adults still want a teacher in the room, and companies spend more on training to meet the reporting rule. There are fewer young adults in the city, yet both sites fill during the day with company groups and in the evening with individuals.

### Evening Crowd
Individuals keep coming in person for conversation practice as machine translation improves, but company contracts shrink. Daytime rooms sit empty; evenings are busy. Fewer young adults means each year's intake is smaller.

### Screens at Work
Machine translation keeps improving; companies keep paying, but staff take lessons online at their desks. Fewer young adults means a smaller individual intake. Classrooms are used less; the online timetable is full.

### Quiet Station
Learners move online and companies cut training as translation tools spread. A smaller pool of young adults shrinks individual demand too. Classroom space is a cost with little use.

## The decision in each scenario
| Scenario | How the decision fares | What breaks | What we'd wish we had done |
|---|---|---|---|
| Full Rooms | Good: the second site fills | Nothing major | Signed early |
| Evening Crowd | Weak: half-empty days | Daytime revenue | Taken a smaller or evening-only space |
| Screens at Work | Poor: rent for rooms few use | Classroom economics | Put the money into online teaching |
| Quiet Station | Bad: eight years of rent on an empty site | Cash | Declined the lease |

The lease works well in one of the four scenarios, so signing now is a gamble on Full Rooms.

## Signposts
| Scenario | Signal | Where to watch | How often | Who |
|---|---|---|---|---|
| Full Rooms | Company clients adding classroom hours | Contract renewals | Quarterly | Sales lead |
| Evening Crowd / Quiet Station | More company clients cutting budgets | Renewals and cancellations | Quarterly | Sales lead |
| Screens at Work / Quiet Station | Online share of new students rising above 30% | Enrolment data | Monthly | [owner] |

## Moves
- **Robust (do now):** grow online classes and sell them to company clients, since they are useful in both online scenarios and cheap to keep in the other two; ask company clients how the reporting rule affects their plans, [owner].
- **Contingent:** take extra classroom space on a short lease or by the hour, triggered by company clients adding classroom hours for two quarters in a row.
- **Avoid:** an eight-year commitment while both uncertainties are open.

## Decision
Decline the eight-year lease, or ask the landlord for a shorter term or a break clause [check: whether the landlord would agree]. Grow online teaching now, and watch company renewals and the online share each quarter. Review the scenarios in six months.
```

## Checks before you send

- [ ] The focal question names a decision and a horizon, not just a topic.
- [ ] Predetermined elements are separated from critical uncertainties, and they appear in every scenario.
- [ ] The two axes are important to the decision and genuinely uncertain, each with two clear end states.
- [ ] Each scenario is plausible and internally consistent, and none is labelled "most likely".
- [ ] The decision is tested in every scenario, and a decision that works in only one is called a gamble.
- [ ] Every signpost is observable, with where to watch and who watches.
- [ ] Moves are split into robust, contingent (each tied to a signpost), and to avoid.
- [ ] Every fact comes from the input or is marked "[check: ...]".

## Common mistakes

- Starting from a topic ("the future of AI") instead of a decision, so nothing changes after the exercise.
- Making a best case, a worst case, and a middle case. That is one forecast with error bars, not different worlds.
- Picking axes that are uncertain but don't matter to the decision, or that matter but are already settled.
- Treating a predetermined element as uncertain, or the other way round.
- Writing rich stories and skipping the implications, signposts, and moves, which are the point.
- Quietly choosing a favourite scenario and planning only for it.
