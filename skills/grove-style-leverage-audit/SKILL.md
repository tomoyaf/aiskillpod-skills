---
name: grove-style-leverage-audit
description: Audits how a manager spends a week against the output-based view of management Andy Grove set out in High Output Management - a manager's output counted as the output of their team plus the neighbouring teams they influence - by mapping each activity to whose output it raises, sorting performance gaps into training or motivation, matching how closely each person is managed to their experience with the task, and checking that the team's key results measure output. Use when a manager feels busy but the team's results don't move, is stuck doing individual work, asks where their time should go, wants to audit their calendar, or asks about managerial leverage, High Output Management or task-relevant maturity.
---

# Grove-style managerial leverage audit

These are principles Andy Grove described publicly in his book High Output Management, as quoted and summarised in Ben Horowitz's foreword to its 2015 edition, and in his OKR practice at Intel as John Doerr's What Matters site describes it. Not affiliated with or endorsed by Andy Grove or their companies. The skill takes a manager's actual week and shows which activities raise the team's output, which don't, and what to change first.

## Ground rules

- Do not attribute quotes or opinions to Andy Grove beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Andy Grove; review the user's material against the principles below.
- Grove is quoted only as the cited sources quote him (the foreword and What Matters). Anything about the book not in the sources below is left out, not guessed.
- Work from the manager's real calendar or a list of what they did, with hours. Never invent hours or results; missing ones are [check: ...].
- Talk about the work and the process, not a person's character. Can't and won't are hypotheses to check in a conversation, not labels.
- The classification of activities below (team output, neighbouring output, own work) is this skill's method for applying the principles, not a list from the book.

## The principles

1. **A manager's output is the team's output.** Horowitz's foreword says the book introduces management with this equation: "A manager's output = the output of his organization + the output of the neighboring organizations under his influence." Horowitz's gloss: a manager's skills and knowledge are valuable only when they get more leverage from the team. Source: Horowitz, foreword to High Output Management (a16z, 2015).
2. **Two reasons someone isn't doing the job.** The foreword quotes Grove: when a person isn't doing the job, either they can't do it or they won't, so the manager's two ways to raise an individual's output are training and motivation. Source: same foreword.
3. **Manage by task-relevant maturity.** Whether to be hands-on or hands-off depends on the person's maturity in the specific task: hands-on training for someone new to it, delegation for someone experienced. The foreword quotes Grove's warning about leaving a subordinate to learn from mistakes the customer pays for. Source: same foreword.
4. **Training is the boss's job.** The book's last chapter is titled "Why Training Is the Boss's Job"; the foreword summarises it as saying a manager who isn't training is neglecting half of what they can do for output. Source: same foreword.
5. **One-on-ones are a core tool.** The book's section on meetings begins with how to conduct a one-on-one. Horowitz adds his own view that the one-on-one may be a manager's best source of knowledge about the organization. Source: same foreword.
6. **Plan for the future gap, not today's.** The foreword quotes Grove: "today's gap represents a failure of planning sometime in the past." Source: same foreword.
7. **Measure output, quarterly, apart from pay.** What Matters describes Grove's OKRs at Intel as quarterly rather than annual, separate from compensation, graded simply as met or not met; when Grove first introduced OKRs at Intel, only aspirational OKRs existed; it quotes Grove: "Stressing output is the key to increasing productivity." Sources: What Matters, "OKR meaning", "Inputs vs. outputs", "Committed vs. aspirational OKRs".

## When to use

- A manager works long hours and the team's results don't move.
- A manager who was promoted from the team still does most of the hands-on work.
- Before planning next quarter's calendar, or after a team grows.
- When one person keeps missing and the manager doesn't know whether to coach or step in.
- Not for preparing one specific 1:1 (use one-on-one-prep), not for writing the team's OKRs (use okr-draft), and not for handing off one task (use delegation-brief).

## What you need

- One or two typical weeks of the manager's calendar, or a list of activities with hours.
- The team: who reports to the manager, what each one owns, and how long they've done it.
- The neighbouring teams the manager's work affects, and how.
- The team's goals or key results for this period, if any.
- Any current performance gaps: who, what, since when.

## Steps

1. **List the week.** Every activity with its hours: meetings, 1:1s, reviews, the manager's own hands-on work, email, hiring, training, firefighting. Mark hours as [check] if estimated.
2. **Map each activity to whose output it raises (principle 1).** Team output (it helps the people who report to you produce more or better), neighbouring output (it helps another team you influence), or own work (the manager doing a task a team member could do). Some activities touch none of these; mark them.
3. **Check the own-work hours against maturity (principle 3).** For each task the manager does personally: who on the team could do it, and how experienced are they in it? High maturity: delegate it. Low maturity: replace doing it with training someone to do it. Name the person.
4. **Sort each performance gap (principle 2).** For each gap: is it most likely "can't" (skills, knowledge, unclear standard) or "won't" (motivation, priorities, conflict)? Write the evidence and the next step: a training plan for can't, a conversation for won't. Mark the hypothesis [check in 1:1].
5. **Check training time (principle 4).** How many hours this week went to teaching or coaching? If none, name one thing only the manager knows that the team needs, and schedule it.
6. **Check one-on-ones (principle 5).** Who had one this period and who didn't? A gap is a gap in what the manager knows about the team. Use one-on-one-prep for each.
7. **Look ahead (principle 6).** What output gap will appear next quarter (a launch, a departure, growth) and what would close it if started now: hiring, training, a process?
8. **Check the measures (principle 7).** Do the team's key results measure output that can be graded met or not met? If they list activities, flag them and hand off to okr-draft. Note if any key result is tied to someone's pay.
9. **Pick the first three changes.** The changes that free the most own-work hours or raise the most team output, each with an owner and a date.

## Output format

```markdown
# Leverage audit: [manager, team] (week of [date])
These are principles Andy Grove described publicly. Not affiliated with or endorsed by Andy Grove or their companies.

## The week
| Activity | Hours | Raises | Note |
|---|---|---|---|
| | | Team / Neighbouring / Own work / None | |

**Totals:** team [h] · neighbouring [h] · own work [h] · none [h]

## Own work to hand over
| Task | Hours/week | Who could own it | Their experience with it | Delegate or train first |
|---|---|---|---|---|

## Performance gaps
| Person | Gap | Can't or won't (hypothesis) | Evidence | Next step |
|---|---|---|---|---|

## Training and one-on-ones
- Training hours this week: [h]. What to teach next: [topic, to whom, when]
- One-on-ones missed this period: [names]

## Next quarter's gap
[What will be short, and what to start now]

## Measures
[Key results that measure output / that list activities / tied to pay]

## First three changes
| Change | Owner | By |
|---|---|---|

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "I lead the support team at a 40-person software company: 5 agents. My week: 14h answering tickets myself, 6h in product meetings, 4h writing the help center, 3h weekly team meeting and queue review, 2h on hiring, 0h of 1:1s this month (too busy). Neha has handled billing tickets for two years; Sam joined last month and Sam's escalations are often wrong. The product team ships changes we hear about from customers first. Our goal is 'answer more tickets'."

**Output (excerpt):**

```markdown
These are principles Andy Grove described publicly. Not affiliated with or endorsed by Andy Grove or their companies.

## The week
| Activity | Hours | Raises | Note |
|---|---|---|---|
| Answering tickets | 14 | Own work | Mostly billing [check: share of billing tickets] |
| Product meetings | 6 | Neighbouring | Could prevent the surprise releases if support's needs are raised there |
| Help center writing | 4 | Team | Fewer repeat tickets for all agents |
| Team meeting and queue review | 3 | Team | The whole queue seen weekly [check: what changes after it] |
| Hiring | 2 | Team | Future team capacity |
| One-on-ones | 0 | Team (none held) | None this month: no view of what Sam and Neha need |

**Totals:** team 9h · neighbouring 6h · own work 14h · none 0h

## Own work to hand over
| Task | Hours/week | Who could own it | Their experience with it | Delegate or train first |
|---|---|---|---|---|
| Billing tickets | [check: about 8] | Neha | Two years | Delegate |

## Performance gaps
| Person | Gap | Can't or won't (hypothesis) | Evidence | Next step |
|---|---|---|---|---|
| Sam | Escalations often wrong | Can't (one month in the job) | Joined last month; escalations often wrong (input) | Two weeks of pairing on escalations; a written escalation checklist |

## Measures
"Answer more tickets" is an activity count. Hand to okr-draft: an output such as resolution on first reply [check: baseline].

## First three changes
| Change | Owner | By |
|---|---|---|
| Hand billing tickets to Neha | [manager] | [date] |
| Start 1:1s with all five agents | [manager] | This week |
| Ask product for release notes to support two days before release | [manager] | Next product meeting |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every activity has hours (or [check]) and a "raises" label.
- [ ] Own-work tasks each have a named person and a delegate-or-train call based on experience with that task.
- [ ] Performance gaps are hypotheses with evidence, not verdicts on people.
- [ ] Training hours and missed one-on-ones are stated.
- [ ] Key results are checked for output and for ties to pay.
- [ ] Only three changes, each with an owner and a date.
- [ ] Grove is quoted only as the cited sources quote him.

## Common mistakes

- Counting hours in meetings as team output without asking whose output the meeting changed.
- Delegating a task to someone new to it without training, or training someone who already knows it.
- Treating every gap as motivation.
- Dropping one-on-ones first when the week gets busy.
