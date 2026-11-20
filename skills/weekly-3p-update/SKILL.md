---
name: weekly-3p-update
description: Writes a weekly Progress, Plans, Problems (3P) update for a team or project that a reader takes in within 60 seconds, from Slack threads, task lists, docs, or notes. Use when someone asks for a weekly update, status update, 3P, team update for leadership, or "what did we do this week".
license: Apache-2.0 (see LICENSE.txt). Adapted from anthropics/skills internal-comms.
---

# Weekly 3P update (Progress, Plans, Problems)

A 3P update tells leadership and neighbouring teams what moved, what's next, and what's in the way, in under a minute of reading. It is written for people with some context on the team but not a lot. Short, factual, and with numbers where the team has them.

## When to use

- The weekly team or project update to a manager, leadership, or a company channel.
- A status update for a client or partner who wants the short version.
- Not for a launch announcement or a long project review: those need more than three lines a section.

## What you need

- The team or project name and the period covered (usually the last 7 days for Progress and Problems, the next 7 for Plans). If either is missing, ask once.
- The raw material: Slack posts, closed tasks, docs, meeting notes, metrics. If you can read the team's tools, pull from them; otherwise ask the user to paste what to cover.
- Optional: last week's update, so Plans from last week can be checked against this week's Progress.

## Steps

1. **Set the scope.** Confirm the team name and dates. The bigger the team, the less granular the items: a squad reports "shipped the export button", a company reports "closed 4 new enterprise deals".
2. **Gather from where the work happened.** Prefer posts with many replies or reactions, docs many people opened, closed tasks, and non-recurring meetings that mattered (reviews, customer calls). Ignore routine chatter.
3. **Pick what matters.** Progress: things shipped, milestones hit, numbers moved. Plans: the 1 to 3 things that are top of mind for next week. Problems: what slows the team: blockers, missing people, a deal that fell through, a dependency on another team.
4. **Check last week's Plans.** Each plan from last week shows up as done in Progress, or as a Problem with the reason it slipped. Don't let a plan disappear silently.
5. **Write 1 to 3 sentences per section.** Matter-of-fact, no adjectives doing the work of numbers. Name the metric and its change ("trial sign-ups 120 → 145"), not "strong growth".
6. **Add one ask, if there is one.** If a Problem needs a decision or help from the reader, say who and what in the Problems line.

## Output format

Keep exactly this shape. One line of heading, then three labelled sections.

```markdown
[emoji that fits the week] [Team name] ([dates covered])
**Progress:** [1–3 sentences: shipped, achieved, measured]
**Plans:** [1–3 sentences: next week's top priorities]
**Problems:** [1–3 sentences: blockers and asks, or "None this week."]
```

## Example

**Input (notes):** Billing team, 10 to 14 March. Shipped annual plans on Wednesday; 18 customers switched so far. Refund flow redesign is in review. Next week: send the annual plan email to all monthly customers, start invoicing PDFs. Waiting on legal for the new refund wording since last Monday; we need their answer by Wednesday to ship the redesign next week. Last week's plan "fix VAT rounding" got done Tuesday.

**Output:**

```markdown
💳 Billing (10–14 March)
**Progress:** Annual plans went live on Wednesday and 18 customers have switched. The VAT rounding fix shipped Tuesday. The refund flow redesign is in review.
**Plans:** Send the annual plan email to all monthly customers and start work on invoice PDFs.
**Problems:** The new refund wording has waited on legal since 10 March; we need an answer by Wednesday to ship the redesign next week.
```

## Checks before you send

- [ ] The heading names the team and the dates.
- [ ] Each section has 3 sentences or fewer, and the whole update reads in under 60 seconds.
- [ ] Every claim of progress has a number, a date, or a named deliverable.
- [ ] Each of last week's Plans is accounted for in Progress or Problems.
- [ ] Every Problem that needs help names who should act and by when.
- [ ] No fact appears that isn't in the sources you read.

## Common mistakes

- Listing activity ("had 6 meetings about pricing") instead of outcomes ("agreed the new price; it ships 1 April").
- Hiding a slipped plan. Readers remember last week's update.
- Writing Problems as complaints with no ask. Say what would unblock it.

---

Adapted from the `internal-comms` skill (examples/3p-updates.md) in github.com/anthropics/skills, Copyright 2026 Anthropic, PBC, licensed under the Apache License, Version 2.0 (LICENSE.txt). Changed by Fluxenic Inc.: rewritten for non-engineering teams, with steps, a plan-carryover check, an example, and a checklist.
