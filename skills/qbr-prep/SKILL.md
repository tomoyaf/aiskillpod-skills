---
name: qbr-prep
description: Prepares a quarterly business review (QBR) or executive business review for a customer, with a slide-by-slide deck outline and talking points covering outcomes against their goals, usage, ROI from their own numbers, roadmap asks, a next-quarter plan, and expansion only when the results earn it. Use when a QBR, EBR, quarterly review, renewal review, or account review with a customer is coming up and someone asks for the deck, the agenda, or what to say.
---

# QBR prep

A QBR is a meeting about the customer's results, not a product demo. Show what they set out to achieve, what happened, and what you'll do together next quarter. Bring up expansion only when the results already make the case.

## When to use

- A quarterly or executive business review with a customer is on the calendar.
- A renewal is within 2 quarters and you want the value story in their numbers.
- A new executive sponsor joined the customer and needs to see what the tool does for them.
- Not for an internal account plan or forecast: use account-plan.

## What you need

- Their goals for the quarter, from the onboarding plan or last QBR. If none were set, say so on the first slide and propose goals for next quarter.
- Usage data for the quarter and the one before.
- Their business numbers that show impact (hours saved, revenue, tickets, conversion), if they shared them. Use only their numbers; if you have none, ROI becomes a question to ask, not a slide to fill.
- Tickets, feature requests, and anything that went wrong this quarter.
- Who attends from their side.

## Steps

1. **Start from their goals.** For each goal: target, result, status (met, partly, missed). Put a missed goal on the slide and say why and what changes. Hiding it costs more trust than the miss.
2. **Pick 3 usage facts that explain the outcomes.** Not every chart. Usage matters only as the cause of a result: "Reminders sent rose 40%, and no-shows fell". Compare to last quarter.
3. **Calculate ROI only from their numbers.** Show the formula on the slide: "Hours saved per week × hourly cost × weeks". If an input is missing, write "[ask: ...]" and plan the question for the meeting. Never use an industry average as their result.
4. **List what went wrong and what you did.** Incidents, open tickets, slow fixes. One line each with the current status.
5. **Collect roadmap asks.** Their top 3 requests, with what you can say about each: shipped, planned (only if the product team confirmed), not planned. Don't promise dates you weren't given.
6. **Propose next quarter's plan.** 2 to 3 goals with measures, and the actions on each side. Ask them to confirm or change the goals in the meeting. Send the agenda a few days before, book the next QBR before the call ends, and send a recap with action items within 24 hours.
7. **Decide on expansion with a rule.** Our default: raise more seats, a new team, or a higher plan only if at least one goal was met and the customer asked about it or usage hit a plan limit. Otherwise leave it out of the deck.

## Output format

```markdown
# QBR: [Customer] — [quarter] — [date]

**Attendees:** [their side] / [our side]
**What we want from this meeting:** [1–2 outcomes, e.g. "agree next quarter's goals"]

## Deck outline
1. **Agenda and goals for today**
2. **Your goals and results** — [goal: target → result, status]
3. **What drove it** — [3 usage facts vs last quarter]
4. **Value in your numbers** — [formula and result, or "[ask: ...]"]
5. **What went wrong and what we did** — [items]
6. **Your requests** — [request: shipped / planned / not planned]
7. **Next quarter** — [2–3 goals, actions each side]
8. **[Expansion — only if the rule is met]**

## Talking points
- Slide [n]: [what to say, 1–2 lines]

## Questions to ask
- [Question]

## Do not say
- [Promises or numbers we can't back]
```

## Example

**Input:**

> Customer: Tallis Freight, Q3. Goals set in Q2: cut average quote turnaround from 4 hours to 1 hour; get all 12 sales reps using templates. Usage: quotes created 1,150 (Q2: 700). Template use 9 of 12 reps. Their ops lead said turnaround is "about 90 minutes now" and the 3 reps not on templates still take the longest. Hourly cost not shared. Tickets: 1 outage on 8 Aug (2 hours). Requests: Excel export (planned for Q4, confirmed), SSO (not planned). They have not asked about more seats.

**Output (excerpt):**

```markdown
# QBR: Tallis Freight — Q3 — 14 October

**What we want from this meeting:** agree Q4 goals; get the hourly cost to size value

## Deck outline
1. **Agenda and goals for today**
2. **Your goals and results** — Quote turnaround: 1 hour target → about 90 minutes (partly met, from 4 hours). Templates: 12 reps target → 9 reps (partly met)
3. **What drove it** — Quotes created 700 → 1,150; 9 of 12 reps on templates; [third fact from usage data]
4. **Value in your numbers** — Time saved per quote about 2.5 hours × quotes × [ask: hourly cost of a rep]
5. **What went wrong and what we did** — 8 August outage, 2 hours; [check: cause and fix to state]
6. **Your requests** — Excel export: planned for Q4. SSO: not planned.
7. **Next quarter** — Turnaround under 1 hour; 12 of 12 reps on templates

## Talking points
- Slide 2: Turnaround fell from 4 hours to about 90 minutes. We're not at 1 hour yet; the 3 reps not on templates are the gap.
- Slide 5: Own the outage first, before they raise it.

## Questions to ask
- What does an hour of a rep's time cost you, roughly?
- What's stopping the last 3 reps from using templates?

## Do not say
- A date for Excel export beyond "Q4".
- Anything about more seats: no goal fully met and they haven't asked.
```

## Checks before you send

- [ ] Every goal from last quarter is on the deck, including missed ones.
- [ ] ROI uses only the customer's numbers, with the formula shown, or is a question.
- [ ] Roadmap items say only what the product team confirmed.
- [ ] Next quarter has 2 to 3 measurable goals.
- [ ] Expansion appears only if the rule in step 7 is met.
- [ ] No number appears that isn't in the input.

## Common mistakes

- Opening with a product update. Their results go first.
- A slide of 10 usage charts. Pick the 3 that explain the outcome.
- Pitching an upgrade in a quarter with a missed goal and an outage.
