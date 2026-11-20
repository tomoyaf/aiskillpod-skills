---
name: automation-opportunity-scan
description: Scans a team's task list or a typical week to find where AI could save time - scores each task on frequency, minutes per run, how rule-based it is, and the risk of a mistake - ranks them, and picks the top 3 with a first small experiment, an owner, and a success measure for each. Use when a manager or team asks where to start with AI, what to automate, which tasks AI can take over, how to save time with ChatGPT or Claude, or wants an AI opportunity assessment.
---

# Automation opportunity scan

The best first AI project is boring: a task done often, taking real minutes each time, following clear rules, where a mistake is cheap to catch. Time saved compounds with frequency (xkcd's "Is it worth the time?" chart makes the point: shaving 1 minute off a daily task is worth about a day of effort over 5 years). So the scan scores every task on those four factors and starts with the simplest thing that could work, usually a prompt or a skill before an agent.

## When to use

- A team wants to start using AI and doesn't know where.
- A manager has a list of recurring work and wants to know what to try first.
- After a first AI pilot, to pick the next ones.
- Not for mapping one workflow in depth (use fde-workflow-discovery on the winner) or writing the AI policy (use ai-use-policy-draft).

## What you need

- The task list: recurring tasks with who does them. A calendar export, a time log, or a quick survey ("list everything you did more than once last week") works.
- For each task, roughly how often and how long. If missing, ask the person once; otherwise estimate and mark "[estimate]".
- Any data rules: what can't go into an AI tool (customer data, health data, contracts).

## Steps

1. **List tasks at the right size.** One row per task that has a clear input and output: "Write weekly client status email", not "client management". Split big jobs into tasks; merge duplicates across people.
2. **Score each task 1 to 5 on four factors (our default scale).** Frequency: 1 = yearly, 3 = weekly, 5 = several times a day. Time per run: 1 = under 2 minutes, 3 = 15 to 30 minutes, 5 = over 2 hours. Rule clarity: 1 = judgment every time, 3 = a pattern with exceptions, 5 = clear rules or a template. Risk (inverted, so higher is safer): 1 = a mistake reaches customers, money, or legal terms unchecked, 3 = a mistake is caught in review, 5 = a mistake is harmless and obvious.
3. **Compute the score.** Score = frequency × time × rule clarity × risk; the maximum is 625. Also compute hours per month: runs per month × minutes ÷ 60. Rank by score; use hours per month to break ties.
4. **Rule out what shouldn't go first.** Drop or defer tasks involving data that can't go into AI tools, decisions about people (hiring, performance), or anything legally binding without a human approval step. Note why.
5. **Pick the top 3 and choose the simplest approach.** For each: a saved prompt or a shared skill (most cases), an AI step inside an existing tool, or an automated workflow. Use an agent that acts on its own only when the output can be checked automatically and errors are cheap. A person reviews the output in every first experiment.
6. **Design a first experiment for each.** 2 weeks, one owner, a baseline (minutes per run today), a success measure (e.g., under half the time with the same quality), and a stop rule. Our default: if quality drops on more than 1 in 10 runs, stop and fix before continuing.

## Output format

```markdown
# AI automation scan — [team], [date]

## Scored tasks
| Task | Who | Freq (1–5) | Time (1–5) | Rules (1–5) | Risk (1–5, 5 = safe) | Score | Hours/month |
|---|---|---|---|---|---|---|---|
| [task] | [role] | | | | | | |

## Ruled out for now
- [Task] — [reason: data / people decision / legal]

## Top 3
### 1. [Task] — score [n], ~[n] hours/month
- **Approach:** [prompt / skill / tool feature / workflow]
- **Experiment:** [what, 2 weeks]
- **Owner:** [name]
- **Baseline → target:** [min per run] → [target]
- **Human check:** [who checks what]
- **Stop if:** [rule]
```

## Example

**Input:** "Agency account team, 4 people: Jo (lead), Sam and Priya (account managers), Alex (coordinator). Tasks: weekly client status emails (AMs, 8 clients, 25 min each), meeting notes to action items (everyone, ~15 meetings/week, 15 min each), monthly performance reports (AMs, 8 clients, 3 hours each), contract renewals (lead, 2/month, 1 hour, legal terms), replying to client Slack questions (everyone, all day, 3 min each), quarterly strategy decks (lead, 8/quarter, 6 hours)."

**Output:**

```markdown
# AI automation scan — Account team, 4 Nov

## Scored tasks
| Task | Who | Freq (1–5) | Time (1–5) | Rules (1–5) | Risk (1–5, 5 = safe) | Score | Hours/month |
|---|---|---|---|---|---|---|---|
| Meeting notes to action items | All | 4 | 3 | 4 | 4 | 192 | ~16 |
| Monthly performance reports | AMs | 2 | 5 | 4 | 3 | 120 | ~24 |
| Weekly client status emails | AMs | 3 | 3 | 4 | 3 | 108 | ~14 |
| Client Slack replies | All | 5 | 2 | 2 | 2 | 40 | [estimate] ~20 |
| Quarterly strategy decks | Lead | 1 | 5 | 1 | 3 | 15 | ~16 |

## Ruled out for now
- Contract renewals — legal terms; keep human, revisit with a review step.

## Top 3
### 1. Meeting notes to action items — score 192, ~16 hours/month
- **Approach:** shared skill (meeting-minutes) used on transcripts
- **Experiment:** every internal and client meeting for 2 weeks
- **Owner:** Jo
- **Baseline → target:** 15 min → 5 min per meeting
- **Human check:** meeting owner checks owners and dates before sending
- **Stop if:** more than 1 in 10 notes has a wrong owner or date

### 2. Monthly performance reports — score 120, ~24 hours/month
- **Approach:** prompt that drafts the narrative from the exported metrics
- **Experiment:** 3 clients' reports this month
- **Owner:** Sam
- **Baseline → target:** 3 hours → 1.5 hours per report
- **Human check:** AM checks every number against the dashboard
- **Stop if:** any number in a sent report is wrong

### 3. Weekly client status emails — score 108, ~14 hours/month
- **Approach:** shared skill (weekly-client-report) fed with the project board
- **Experiment:** 4 clients for 2 weeks
- **Owner:** Priya
- **Baseline → target:** 25 min → 10 min per email
- **Human check:** AM edits and sends
- **Stop if:** a client flags an error
```

## Checks before you send

- [ ] Every task has an input and output clear enough to describe in one line.
- [ ] Every score uses the defined 1–5 scales, and estimates are marked.
- [ ] Tasks with restricted data, people decisions, or legal terms are ruled out or have a human approval step.
- [ ] Each top-3 item has an owner, a baseline, a target, a human check, and a stop rule.
- [ ] The approach is the simplest that works (prompt or skill before agent).

## Common mistakes

- Starting with the most impressive task instead of the most frequent one. Wins on daily work build trust.
- Scoring "AI could probably do it" instead of rule clarity. If the person can't explain the rules, the AI can't follow them.
- Skipping the baseline. Without minutes-before, "it saves time" can't be shown.
