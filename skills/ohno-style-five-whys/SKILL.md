---
name: ohno-style-five-whys
description: Runs a 5 whys root-cause analysis on a problem the way Taiichi Ohno illustrated it for the Toyota Production System - state the problem as a gap from the standard, ask why at each answer until the cause that can be removed is reached (five is a guide, not a rule), check each link against facts, and fix the root cause rather than the symptom. Use when an incident, defect, missed deadline, customer complaint or repeated failure needs a root cause, when a team keeps patching the same symptom, or when someone asks for a 5 whys, a root-cause analysis or "why does this keep happening".
---

# Ohno-style 5 whys root-cause analysis

These are principles Taiichi Ohno described publicly in his book on the Toyota Production System, as the Lean Enterprise Institute's lexicon summarises them, and as Toyota describes his role. Not affiliated with or endorsed by Taiichi Ohno or their companies. The skill takes one problem, walks the chain of whys with evidence at each step, and ends with a countermeasure aimed at the root cause.

## Ground rules

- Do not attribute quotes or opinions to Taiichi Ohno beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Taiichi Ohno; review the user's material against the principles below.
- Every answer in the chain needs a fact behind it (a log, a record, an observation, a person who saw it). An answer without one is marked "[check: ...]" and the chain stops there until it is checked.
- Ask why about the process, not about a person. "Because Sam forgot" is never a root cause; ask why the process let it be forgotten.
- Never invent facts about the incident.

## The principles

1. **Ask why repeatedly.** Whenever a problem appears, ask why again and again to get beyond the obvious symptoms to the root cause. Source: Lean Enterprise Institute lexicon, "5 Whys".
2. **The number five is not the point.** Keep asking until the root cause is reached and eliminated. Source: same entry.
3. **Fix the cause, not the symptom.** Ohno's own example is a machine that stopped: an overload blew the fuse, because a bearing wasn't lubricated, because the pump wasn't pumping enough, because its shaft was worn, because no strainer kept metal scraps out. Replacing the fuse or the pump alone would let the failure recur. Source: same entry, citing Ohno's 1988 book, p. 17.
4. **Start from a gap from the standard.** The lexicon places the method within problem-solving that defines the problem specifically, sets a goal, analyses the root cause and sets countermeasures. Source: same entry.
5. **Context.** Toyota credits Ohno with helping establish the Toyota Production System, whose aim is to eliminate waste thoroughly and shorten lead times. Source: Toyota, "Toyota Production System".

## When to use

- An incident, outage, defect, or missed delivery needs a root cause.
- The same problem keeps coming back after it was "fixed".
- A customer complaint that points at a process, not a one-off.
- Not for a team retrospective on how a project went (use retrospective), and not for turning a support ticket into a bug report (use bug-report-from-ticket).

## What you need

- The problem: what happened, where, when, how often, and what should have happened (the standard).
- The facts you have: logs, timelines, records, who saw what.
- What has been tried already.
- Who can confirm facts you don't have.

## Steps

1. **State the problem as a gap.** "Orders shipped late: 12 of 140 last week, against a standard of same-day dispatch before 15:00." Specific, measured, with the standard (principle 4).
2. **Ask the first why.** Why did the gap happen? Write the direct, observable cause, with its evidence.
3. **Keep asking (principle 1).** Take each answer and ask why it happened. One line per step, each with its evidence. If an answer has two causes, branch and follow both.
4. **Check each link.** Read the chain backwards with "therefore": "No strainer, therefore metal got in, therefore the shaft wore ...". If a "therefore" doesn't hold, the chain is wrong at that step.
5. **Stop at the root (principle 2).** Stop when the next why leaves your control (the weather, the law) or when the cause found is one you can remove and that would stop the failure. That may be after three whys or seven.
6. **Set countermeasures (principle 3).** One for the root cause (the strainer), and, if needed, one for containment now (replace the fuse). Label them; containment alone is not a fix.
7. **Name an owner, a date and a check.** How will you know in two weeks that the problem doesn't recur?

## Output format

```markdown
# 5 whys: [problem in one line]
These are principles Taiichi Ohno described publicly. Not affiliated with or endorsed by Taiichi Ohno or their companies.

## Problem
**What happened:** [measured] · **Standard:** [what should happen] · **Since:** [date]

## The chain
| # | Why? | Because | Evidence |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

## Read back
[Root cause], therefore [...], therefore [the problem]. Holds: yes / no at step [n].

## Root cause
[One sentence, about the process]

## Countermeasures
| Type | Action | Owner | Date |
|---|---|---|---|
| Containment (now) | | | |
| Root cause | | | |

## How we'll know it worked
[Measure and date]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "Online shop. Last week 12 of 140 orders shipped a day late. We promise same-day dispatch for orders before 15:00. The packer says the label printer jammed several afternoons. Labels are printed in one batch at 14:30. The printer's last service was 18 months ago; the manual says every 6 months. Nobody owns the printer."

**Output (excerpt):**

```markdown
These are principles Taiichi Ohno described publicly. Not affiliated with or endorsed by Taiichi Ohno or their companies.

## The chain
| # | Why? | Because | Evidence |
|---|---|---|---|
| 1 | Why did 12 orders ship late? | Labels weren't printed in time | Packer's account |
| 2 | Why weren't labels printed in time? | The printer jammed during the 14:30 batch | Packer's account [check: printer error log] |
| 3 | Why did it jam? | It is 12 months past its service interval | Service record; manual says every 6 months |
| 4 | Why was the service missed? | Nobody owns the printer, so nobody books it | Input: "Nobody owns the printer" |

## Root cause
The label printer has no owner, so its maintenance never gets scheduled; a single 14:30 batch turns any jam into late orders.

## Countermeasures
| Type | Action | Owner | Date |
|---|---|---|---|
| Containment (now) | Service the printer this week | [name] | [date] |
| Root cause | Give the printer an owner and a 6-monthly service in the calendar | [name] | [date] |
| Root cause | Print labels in two batches, 12:00 and 14:30 | [name] | [date] |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] The problem is stated as a measured gap from a standard.
- [ ] Every step has evidence or is marked [check].
- [ ] The chain reads back with "therefore" without a gap.
- [ ] The root cause is about a process, not a person.
- [ ] There is a root-cause countermeasure, not only containment, with an owner and a date.

## Common mistakes

- Stopping at the first plausible answer ("the printer jammed").
- Forcing exactly five steps.
- Ending at a person's mistake.
- Writing a chain from opinion with no evidence at any step.
