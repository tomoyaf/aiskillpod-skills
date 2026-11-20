---
name: content-calendar
description: Builds a 4 to 8 week content calendar from goals and themes, one row per piece with channel, owner, publish date, the goal it serves, and how it gets repurposed. Use when someone asks for a content calendar, content plan, editorial calendar, posting schedule, or "what should we publish next month" for a blog, newsletter, LinkedIn, X, or YouTube.
---

# Content calendar

A calendar is a promise of who ships what by when. Every row serves a stated goal, has one named owner, and fits the team's real capacity; a plan the team can't ship by week 3 is worse than a shorter one they can.

## When to use

- Planning the next 4 to 8 weeks of blog, newsletter, and social content.
- After a strategy or launch date is set and you need it turned into dated pieces.
- Not for choosing the strategy itself (which audience, which channels): settle that first, then calendar it.

## What you need

- 1 to 3 goals with a number if possible (signups, demo requests, newsletter subscribers).
- Themes or topics, and any fixed dates (launches, events, holidays in the audience's market).
- Channels in use and who can produce content, with hours per week each. If capacity is missing, ask once; otherwise assume 1 person at 4 hours a week and mark it "[assumption]".
- Optional: past top performers, so the calendar repeats what worked.

## Steps

1. **Set the capacity budget.** Our default hour costs: long article 6 hours, newsletter 3 hours, LinkedIn post 1 hour, short video 4 hours, repurposed post 0.5 hours. Sum the hours per week; our default is to plan no more than 80% of stated capacity.
2. **Pick 1 anchor piece per week.** The anchor is the piece that costs most and serves a goal directly (an article, a guide, a webinar). If capacity can't fit one per week, make it one every 2 weeks.
3. **Repurpose before inventing.** Each anchor yields 2 to 4 smaller pieces (a LinkedIn post from its most specific point, a newsletter item, a short clip). New standalone pieces only fill gaps.
4. **Place fixed dates first.** Seasonal and brand dates go in before anything else. Launches and events get their pieces scheduled backwards (our default): teaser 1 week before, main piece on the day, follow-up within 3 days.
5. **Tie every row to a goal.** If a piece doesn't move a goal, cut it or say which goal it serves indirectly. Mix: at least half the anchors aim at the main goal.
6. **Assign one owner and a status per row.** The owner is the person who moves the piece through and approves it; a person, never "marketing". Status starts at "idea" and moves to drafting, review, scheduled, published. Draft due (our default): 3 working days before publish for anchors, 1 day for small posts.
7. **List open slots and risks.** Weeks short on capacity, pieces waiting on someone outside the team (a customer quote, legal review).

## Output format

```markdown
# Content calendar — [start date] to [end date]

**Goals:** [goal 1 with number], [goal 2]
**Capacity:** [hours/week, by person] — planned at [n] hours/week ([%] of capacity)

| Week | Publish date | Piece | Type | Channel | Owner | Draft due | Status | Goal | Repurpose into |
|---|---|---|---|---|---|---|---|---|---|
| [1] | [date] | [working title] | [anchor / repurposed / standalone] | [channel] | [name] | [date] | [idea / drafting / review / scheduled] | [goal] | [rows or "none"] |

## Fixed dates
- [date] — [event or launch] — [pieces tied to it]

## Risks and open slots
- [week] — [risk] — [what to do]
```

## Example

**Input:** "6 weeks starting Monday 6 April 2026. Goal: 120 demo requests this quarter, grow newsletter. Themes: month-end close, audit prep. We launch a bank-sync feature 28 April. Me (Rosa, 6 h/week) and Kenji (3 h/week, design and video). Blog, newsletter every 2 weeks, LinkedIn."

**Output (first 3 weeks):**

```markdown
# Content calendar — 6 April to 15 May

**Goals:** 120 demo requests this quarter; newsletter growth [assumption: no number given]
**Capacity:** Rosa 6 h, Kenji 3 h = 9 h/week — planned at 7 h/week at most (78%): week 1 6.5 h, week 2 6.5 h, week 3 7 h

| Week | Publish date | Piece | Type | Channel | Owner | Draft due | Status | Goal | Repurpose into |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Tue 7 Apr | A 5-day month-end close checklist | anchor | Blog | Rosa | Thu 2 Apr | drafting | Demo requests | Rows 2, 4 |
| 1 | Fri 10 Apr | Checklist as a 1-page image | repurposed | LinkedIn | Kenji | Thu 9 Apr | drafting | Newsletter | none |
| 2 | Tue 14 Apr | Newsletter #1: close checklist + 2 reader tips | standalone | Newsletter | Rosa | Fri 10 Apr | idea | Newsletter | none |
| 2 | Thu 16 Apr | "Day 3 is where closes stall" | repurposed | LinkedIn | Rosa | Wed 15 Apr | drafting | Demo requests | none |
| 3 | Tue 21 Apr | Bank sync teaser: 40-second clip | standalone | LinkedIn | Kenji | Mon 20 Apr | idea | Demo requests | none |
| 3 | Thu 23 Apr | What auditors ask for first | anchor | Blog | Rosa | Mon 20 Apr | idea | Demo requests | Week 4: newsletter item 28 Apr, LinkedIn post Thu 30 Apr |

## Fixed dates
- 28 Apr — bank-sync launch — teaser 21 Apr, launch post and newsletter 28 Apr, customer follow-up by 1 May

## Risks and open slots
- Anchors run every 2 weeks (weeks 1, 3, 5): an article takes 6 h, all of Rosa's week, so it never shares a week with a newsletter.
- Week 2 — Kenji's teaser clip takes about 4 h and he has 3 h a week: he makes it in week 2 (3 h) and finishes it in week 3 (1 h).
- Customer follow-up on 1 May needs a customer quote — Rosa to ask by 20 Apr.
```

## Checks before you send

- [ ] Planned hours are 80% of stated capacity or less, with the sum shown.
- [ ] Every row has one named owner, a publish date, a draft-due date, and a status.
- [ ] Every row names the goal it serves.
- [ ] Each anchor lists what it's repurposed into, and those rows exist.
- [ ] Fixed dates are scheduled with a before, on-the-day, and after piece.
- [ ] Dates fall on real weekdays for the stated year.

## Common mistakes

- Planning 5 posts a week for a team that has shipped 1. Start from the hours.
- Rows like "LinkedIn post" with no topic. Every row needs a working title.
- Forgetting the draft-due date, so everything is written the night before.
