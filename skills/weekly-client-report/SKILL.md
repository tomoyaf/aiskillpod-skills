---
name: weekly-client-report
description: Writes a one-screen weekly status report for a client of an agency, consultancy, or services team - headline status (on track, at risk, off track) with the reason, done this week, next week, metrics against target, and blockers with what the client must do. Use when someone asks for a weekly client update, status report, client recap, or "send the client where we are" from notes, a task list, or a tracker export.
---

# Weekly client report

A good weekly report lets a busy client read the first line and know whether to worry, then find in under a minute what they must do. Write it as an inverted pyramid: status and the ask first, the work list as supporting evidence, so a reader who stops after 2 lines still has the point.

## When to use

- Every week (or sprint) on a retainer or project for an outside client.
- When the account lead dumps notes, a task board export, or a Slack thread and asks "turn this into the client update".
- Before a status call, so the call can spend its time on blockers.
- Not for an internal team update (use weekly-3p-update) or a quarterly business review (use qbr-prep).

## What you need

- What got done this week and what is planned next week (notes, tickets, or a tracker export).
- The project's goal or milestones and the targets for any metrics reported. If targets are missing, report the number without a judgment and mark "[target to confirm]".
- Blockers, and anything waiting on the client (approvals, assets, access, feedback).
- The client's name and the reporting week. If the deadline of the next milestone is missing, ask once.

## Steps

1. **Pick the headline status.** The 3 levels follow the red-amber-green delivery confidence scale the UK Infrastructure and Projects Authority uses for major projects. On track (green): delivery on time, budget and quality looks highly likely and no major open issue threatens it. At risk (amber): delivery looks feasible but significant issues need attention now; they look fixable if handled promptly, so name the fix and its date. Off track (red): the milestone looks unachievable as planned; give the new date or say it's not set. Our default: never pick "on track" while a client-side blocker is open and older than 3 working days.
2. **Write the reason in one sentence.** The reason names the cause and the consequence: "At risk: product photos arrived 4 days late, so the launch page moves from 12 to 15 May unless copy is approved by Friday." No softening words like "slightly".
3. **Put the client's asks right under the status.** Each ask: what, by when, and what happens if it's late. Max 3 asks; if there are more, the top 3 go here and the rest go under Blockers.
4. **List done this week as outcomes, not activity.** "Checkout page live on staging" beats "worked on checkout". Max 6 bullets; merge small items. Leave out internal chores the client doesn't pay for.
5. **List next week as commitments.** Max 5 bullets, each something the client could check on next week's report.
6. **Report metrics against target.** Number, target, and direction since last week. Only the 3-5 metrics in the agreement or that the client asked for. If a number is from an unfinished period, say "to date".
7. **Cut to one screen.** Our default is about 250 words. If it's longer, the done list is too long.

## Output format

```markdown
**[Client] — weekly report, week of [date]**

**Status: [On track / At risk / Off track]** — [one-sentence reason with cause and consequence]

**What we need from you**
- [Ask] — by [date]. [What happens if it's late.]

**Done this week**
- [Outcome]

**Next week**
- [Commitment]

**Metrics**
| Metric | This week | Target | vs last week |
|---|---|---|---|
| [Metric] | [value] | [target or "[target to confirm]"] | [up / down / flat] |

**Blockers and risks**
- [Blocker] — owner: [name], since [date]

Next milestone: [milestone] on [date].
```

## Example

**Input:** Notes from Dana (Brightfield Studio) for client Nordlys Coffee: "homepage design approved Mon. built product listing + cart on staging. photos for the 24 products still not here, promised last Wed (28 May). if they don't arrive by Wed 4 June, launch moves to 24 June at the earliest. email signup form done. next: checkout, mobile QA. sessions on old site 8,210 (target 9,000, last wk 7,900). launch 20 June."

**Output:**

```markdown
**Nordlys Coffee — weekly report, week of 2 June**

**Status: At risk** — product photos are 5 days late, so the 20 June launch slips unless they arrive by Wednesday 4 June.

**What we need from you**
- Product photos for all 24 items — by Wednesday 4 June. After that, launch moves to 24 June at the earliest.

**Done this week**
- Homepage design approved (Monday).
- Product listing and cart working on staging.
- Email signup form built.

**Next week**
- Checkout working on staging.
- Mobile QA done.

**Metrics**
| Metric | This week | Target | vs last week |
|---|---|---|---|
| Sessions on current site | 8,210 | 9,000 | up (7,900) |

**Blockers and risks**
- Product photos not received — owner: Nordlys, since 28 May.

Next milestone: launch on 20 June.
```

## Checks before you send

- [ ] The first line states a status and a reason with a cause and a consequence.
- [ ] Every ask to the client has a date and the cost of missing it.
- [ ] Status is not "on track" while a client-side blocker is more than 3 working days old.
- [ ] Every metric has a target or "[target to confirm]"; no number is made up.
- [ ] Done items are outcomes the client can see, not activity.
- [ ] It fits on one screen (about 250 words).

## Common mistakes

- Burying the ask in the last paragraph. Clients read the top and stop.
- Reporting "on track" to avoid an awkward week, then "off track" the next. Flag risk early.
- Listing 15 tasks to look busy. The client pays for outcomes.
