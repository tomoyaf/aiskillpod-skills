---
name: retrospective
description: Runs a team retrospective from notes, sticky notes, or a survey - what went well, what didn't, recurring patterns, root causes with a short 5 whys, and 1 to 3 experiments with an owner and a date each - in Start/Stop/Continue, 4Ls, or went well/didn't format. Use when a team asks to run or write up a retro, sprint retrospective, post-project review, lessons learned, or "what should we change next time".
---

# Team retrospective

A retro is worth the hour only if the next sprint or project runs differently. The Scrum Guide puts it as planning "ways to increase quality and effectiveness". So the output is not a list of feelings; it's 1 to 3 changes the team will try, each with an owner and a date, and last retro's changes checked first.

## When to use

- At the end of a sprint, a project, a launch, or a quarter.
- When a team has raw input (survey answers, sticky notes, a Slack thread) and needs it grouped into themes and actions.
- To prepare a facilitator's plan before running the session live.
- Not for a single incident with customer impact: write an incident review with a timeline instead.

## What you need

- The raw input: notes, survey responses, or a board export. If there is none, produce the facilitation plan and the empty template.
- The period or project covered, and who took part.
- Last retro's actions, if any. If missing, say "no previous actions on record".
- Format preference. If none, use went well / didn't go well / try next (our default; it's the plainest).

## Steps

1. **Check last retro's actions first.** Each one: done, not done, or dropped, with one line on what happened. If more than half weren't done, the first experiment this time is fewer, smaller actions.
2. **Pick the format.** Went well / didn't / try next for most teams. Start / Stop / Continue when the team needs behavior changes. The 4Ls (loved, loathed, learned, longed for) when the period had a lot of learning, such as a first launch. Don't mix formats in one retro.
3. **Group the input into themes.** Merge duplicates and count how many people raised each theme. Look for patterns that recur, not one-time events. Keep the participants' words in quotes for the top themes; anonymize names unless the input is already attributed.
4. **Find the root cause of the top 2 problems.** Ask "why?" until you reach something the team can change. The Lean Enterprise Institute, which traces the method to Taiichi Ohno at Toyota, says the number 5 is not the point. Stop at a cause outside the team's control and say so. Never stop at a person ("Sam forgot"): ask why the process let it be forgotten.
5. **Pick 1 to 3 experiments.** Each is a specific change for the next period, small enough to try, with one owner (a person), a date to review it, and how we'll know it worked. If the team proposes 8 actions, keep the 3 with the biggest expected effect and park the rest.
6. **Plan the session if it's live.** For 60 minutes, Atlassian's Team Playbook splits it: set the tone (5), gather input (15), find patterns (20), choose actions (15), close (5). Remind the room the goal is improvement, not blame.

## Output format

```markdown
# Retro — [team / project], [period]

**Format:** [went well / didn't / try next | Start/Stop/Continue | 4Ls]
**Participants:** [names or count]

## Last retro's actions
| Action | Owner | Status | What happened |
|---|---|---|---|
| [action] | [name] | done / not done / dropped | [one line] |

## What went well
- [Theme] — raised by [n] — "[representative quote]"

## What didn't go well
- [Theme] — raised by [n] — "[representative quote]"

## Root causes
**[Problem 1]**
- Why? [answer] → Why? [answer] → Why? [answer] → root cause: [something the team can change]

## Experiments for next [sprint / project]
| Experiment | Owner | Review on | We'll know it worked if |
|---|---|---|---|
| [specific change] | [name] | [date] | [observable signal] |

## Parked
- [Ideas not chosen this time]
```

## Example

**Input:** "Platform team, Sprint 14 retro, 6 people (PM: Lina), survey answers: 'Demo went great' (3), 'Pair programming on the importer helped' (2), 'Too many last-minute scope changes' (4), 'QA got the build on Thursday, no time to test' (3), 'Standups run 25 min'. Last retro action: 'Ana to set up a staging env' — done, live since day 3. From the discussion: stories were finished in the last 2 days; late scope changes restarted 2 stories; requests after planning go straight to developers."

**Output:**

```markdown
# Retro — Platform team, Sprint 14

**Format:** went well / didn't / try next
**Participants:** 6

## Last retro's actions
| Action | Owner | Status | What happened |
|---|---|---|---|
| Set up a staging environment | Ana | done | Live since day 3 |

## What went well
- The sprint demo — raised by 3 — "Demo went great"
- Pairing on the importer — raised by 2

## What didn't go well
- Late scope changes — raised by 4 — "Too many last-minute scope changes"
- QA squeezed at the end — raised by 3 — "QA got the build on Thursday, no time to test"
- Long standups — raised by 1

## Root causes
**QA squeezed at the end**
- Why? The build reached QA on Thursday → Why? Stories were finished in the last 2 days → Why? Late scope changes restarted 2 stories → Why? Requests after planning go straight to developers → root cause: no rule for changes after sprint planning.

## Experiments for next sprint
| Experiment | Owner | Review on | We'll know it worked if |
|---|---|---|---|
| Changes after planning go through the PM, who swaps something out | Lina (PM) | Sprint 15 retro | Zero stories restarted mid-sprint |
| QA gets the build at least 2 days before the sprint ends | Ana | Sprint 15 retro | QA reports 2+ days to test |

## Parked
- Shorter standups (raised once; revisit if it comes up again)
```

## Checks before you send

- [ ] Last retro's actions have a status before any new action is listed.
- [ ] 3 experiments or fewer, each with one named owner, a review date, and a success signal.
- [ ] Every root-cause chain ends at something the team can change, not a person's name.
- [ ] Theme counts match the input; nothing is quoted that wasn't said.
- [ ] Individual comments are anonymous unless the input was attributed.

## Common mistakes

- Ending with "communicate better". Name the change: who does what differently, starting when.
- Writing 10 actions. Teams finish 1 to 3; the rest erode trust in the retro.
- Skipping what went well. It tells the team what to protect when they change things.
