---
name: ai-training-plan
description: Plans short AI training for a company's staff - three 45-minute sessions built on each team's own tasks (the rules and a first real task, the team's shared instructions, checking AI output), homework between sessions, the exercises with planted errors, and an attendance record. Use when a manager, HR or ops lead asks for an AI training plan, generative AI training for employees, an AI literacy programme, an AI workshop agenda, or how to teach staff to use ChatGPT or Claude.
---

# AI training plan

Training that changes how people work is short, uses their own tasks, and teaches the company's way of using AI rather than AI in general. In Microsoft and LinkedIn's 2024 Work Trend Index, only 39% of people who use AI at work had received AI training from their company. In the EU, Article 4 of the AI Act asks companies that use AI to take measures for their staff's AI literacy; the European Commission says no certificate is needed and an internal record of training is enough.

## When to use

- A company or team is rolling out ChatGPT, Claude or Copilot and wants people to use it well and safely.
- People already use AI, each differently, and results vary.
- Someone needs an AI literacy record for the EU AI Act or a customer questionnaire.
- Not for teaching engineers to build AI products, and not a replacement for the company's AI rules: write those first.

## What you need

- The AI tools and plans the company uses.
- The company's AI rules (approved tools, data that never goes in, who checks output). If there are none, say so; the plan's first step will be to write them.
- The teams to train and 3 tasks each team repeats every week.
- Who runs the sessions and when people are free.

## Steps

1. **Check the rules exist.** If there are no written AI rules, make writing a one-page version the first item, before any session. Training without rules teaches habits you'll undo.
2. **Pick 3 tasks per team.** Tasks done weekly, that take 20 minutes or more, and that the person can check. Use the team's words for them.
3. **Plan session 1: rules and a first task (45 min).** 10 minutes on the rules with one real example of what not to paste; 35 minutes where each person does one of their tasks with AI, briefing it like a new colleague. Homework: the same task 3 times, timed.
4. **Plan session 2: the shared instructions (45 min).** Walk through the team's shared instructions for its 3 tasks; everyone runs each once on yesterday's real case. Homework: use them for a week and note where they're wrong. If shared instructions don't exist yet, list who writes each and by when.
5. **Plan session 3: checking AI output (45 min).** Prepare 5 real AI drafts, each with one realistic planted error: a wrong number, an invented fact, a confidential detail, the wrong tone, a promise nobody made. People find them in pairs. Homework: suggest one fix to a shared instruction.
6. **Schedule.** Three sessions a week apart, small groups by team, at times people are free.
7. **Set the record.** Date, attendees, topics covered, kept by a named person. Add new hires to the same three sessions in their first month.

## Output format

```markdown
# AI training plan: [Company]
Tools: [tools and plans] · Rules: [exist / to write by date] · Record kept by: [name]

## Tasks by team
| Team | Task 1 | Task 2 | Task 3 |
|---|---|---|---|

## Session 1: rules and a first task (45 min) · [date]
- 10 min: rules, with [example]
- 35 min: [task per team]
- Homework: [task] 3 times, timed

## Session 2: shared instructions (45 min) · [date]
- [instructions to walk through, owner of each]
- Homework: [what to note]

## Session 3: checking AI output (45 min) · [date]
| Draft | Planted error | What it teaches |
|---|---|---|

## Record
| Date | Session | Attendees | Covered |
|---|---|---|---|

## New hires
Same three sessions within [30] days of starting.
```

## Example

**Input:** "Property management company, 22 people: lettings (8), accounts (5), maintenance coordinators (6), managers (3). We just bought Claude Team. We have a one-page AI policy. Ops director runs it, Thursday mornings work."

**Output (start):**

```markdown
# AI training plan: Brookfield Property Management
Tools: Claude Team · Rules: one-page policy (exists) · Record kept by: ops director

## Tasks by team
| Team | Task 1 | Task 2 | Task 3 |
|---|---|---|---|
| Lettings | Reply to a repair request | Viewing follow-up email | Listing description |
| Accounts | Summarize an invoice dispute | Arrears reminder letter | Monthly landlord statement note |
| Maintenance | Brief a contractor | Tenant update on a repair | Weekly job summary |

## Session 3: checking AI output (45 min) · Thu 27 Nov
| Draft | Planted error | What it teaches |
|---|---|---|
| Repair reply | Promises a repair "within 24 hours" | Never state a time the contractor hasn't confirmed |
| Arrears letter | Wrong amount owed | Check every number against the ledger |
```

## Checks before you send

- [ ] Every session uses tasks from the trainees' own jobs, by team.
- [ ] The rules are written before session 1, or writing them is the first item.
- [ ] Session 3 has 5 drafts with one realistic planted error each.
- [ ] Each session has homework on a real task.
- [ ] A named person keeps a dated attendance record.
- [ ] Nothing about law is stated as fact for the reader's country; say "check" where it depends on where they operate.

## Common mistakes

- A long general course on how AI works. People forget it by Monday.
- Training before rules exist, so people learn to paste what they shouldn't.
- One session for everyone. Sales and accounts don't repeat the same tasks.
