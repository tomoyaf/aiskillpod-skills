---
name: capture-clarify-review
description: Runs a weekly review of a person's or small team's open loops with the five steps David Allen describes in Getting Things Done - capture everything, clarify what each item means (actionable or not, next action, project), organize into lists, reflect weekly, and engage - turning a messy brain dump, inbox or task list into projects with next actions, waiting-for items, someday items and reference. Use when someone asks for a weekly review, Getting Things Done or GTD, a brain dump to sort, next actions, an overflowing to-do list or inbox, or how to get organized.
---

# Capture and clarify weekly review

David Allen's Getting Things Done (2001; revised 2015) is a method for managing commitments so they live in a trusted system instead of in your head. His site describes five steps: capture what has your attention; clarify what it means (is it actionable? if so, what's the next action, and is it part of a project, meaning anything that needs more than one action; if not, trash, reference or on hold); organize reminders where they belong; reflect by reviewing often; and engage by choosing what to do with confidence. The book's two-minute rule says that if a next action takes less than two minutes, do it now. Its weekly review keeps the system current. This skill takes a brain dump, an inbox or a task list and runs the clarify, organize and reflect steps.

## When to use

- A to-do list is long, vague and stressful.
- After a holiday, a busy launch or a role change, to get back in control.
- Every week, as the review.
- Not for planning a team's quarter: use quarterly-planning. Not for writing a weekly status update to others: use weekly-3p-update.

## What you need

- Everything that has the person's attention: tasks, emails to answer, ideas, worries, commitments to others. A raw list is fine.
- Their calendar for the next two weeks, if available.
- The contexts where they work (computer, phone, office, errands, with a named person).
- If an item's meaning is unclear, ask once or mark it "[clarify]". Never invent deadlines.

## Steps

1. **Capture.** List every item from the input as one line. Ask: "Anything else on your mind: work, home, people waiting on you?" Add what comes back.
2. **Clarify each item.** Decide whether it is actionable. If not, mark it trash, reference or someday/maybe. If it is, write the next physical, visible action, starting with a verb ("Call Rosa about the lease", not "Lease"). If it needs more than one action, also write the project's outcome.
3. **Apply the two-minute rule.** Mark actions that take under two minutes "do now".
4. **Organize.** Sort into lists: projects (with outcome), next actions by context, waiting for (who, what, since when), calendar (only things that must happen on a date), someday/maybe, and reference.
5. **Reflect.** Check that every project has at least one next action, every waiting-for item has a follow-up date, and the next two weeks of calendar are covered. Flag stale items.
6. **Engage.** Suggest what to do first given time, energy and context, starting with "do now" items and dated commitments.

## Output format

```markdown
# Weekly review: [name], [date]

## Do now (under two minutes)
- [action]

## Projects
| Project (outcome) | Next action | Context |
|---|---|---|

## Next actions by context
**@computer:** · **@phone:** · **@errands:** · **@[person]:**

## Waiting for
| What | From whom | Since | Follow up on |
|---|---|---|---|

## Calendar (date-specific only)
- [date]: [item]

## Someday / maybe
- [item]

## Reference (no action)
- [item]

## Trash
- [item]

## Review flags
- [project without a next action, stale item, uncovered date]

## Start with
1. [action]
```

## Example

**Input:** "Brain dump, Monday: Q3 budget. Email from Priya asking for the vendor contract. Dentist. Office move in September. Idea: start a team newsletter. Waiting on legal's review of the NDA (sent 2 weeks ago). Board deck due Thursday. Read that article on pricing. Reply to Tom: yes to Friday lunch. Old flyer for the 2023 conference. Car insurance renews 30 June."

**Output:**

```markdown
# Weekly review: [name], Monday [date]

## Do now (under two minutes)
- Reply to Tom: yes to Friday lunch.
- Forward Priya the vendor contract [check: where it's stored].

## Projects
| Project (outcome) | Next action | Context |
|---|---|---|
| Q3 budget submitted [check: due date] | Pull Q2 actuals into the budget sheet | @computer |
| Office move in September done | Email facilities to ask for the move plan and my part in it | @computer |
| Board deck sent by Thursday | Outline the deck's 5 sections | @computer |
| Car insurance renewed before 30 June | Get two quotes to compare | @phone |

## Next actions by context
**@computer:** Pull Q2 actuals; email facilities; outline the deck · **@phone:** Book the dentist; get two car insurance quotes · **@errands:** — · **@[person]:** —

## Waiting for
| What | From whom | Since | Follow up on |
|---|---|---|---|
| NDA review | Legal | 2 weeks ago | Today: it's stale |

## Calendar (date-specific only)
- Thursday: board deck due
- 30 June: car insurance renews
- Friday: lunch with Tom

## Someday / maybe
- Start a team newsletter

## Reference (no action)
- Article on pricing (to read when there's time) [or someday/maybe]

## Trash
- 2023 conference flyer

## Review flags
- NDA review waiting 2 weeks: follow up today.
- Q3 budget has no due date [clarify].

## Start with
1. The two "do now" replies.
2. Follow up with legal on the NDA.
3. Outline the board deck (due Thursday).
```

## Checks before you send

- [ ] Every captured item lands in exactly one list.
- [ ] Every next action starts with a verb and is a physical, visible step.
- [ ] Every project has an outcome and at least one next action.
- [ ] Only date-specific items are on the calendar.
- [ ] No deadline is invented; unclear items are marked "[clarify]".

## Common mistakes

- Writing projects as tasks ("Budget"). Without a next action, nothing moves.
- Putting wishes on the calendar. The calendar is for what must happen that day.
- Skipping the weekly review. Lists go stale and the mind stops trusting them.
- Keeping some items in your head. The system works only if everything is captured.
