---
name: one-on-one-prep
description: Prepares a manager's 1:1 with a direct report - the report's own agenda first, their updates, a win to recognize, one piece of feedback in SBI form, a career or growth question, blockers to clear, and last time's commitments checked off. Use when a manager asks to prep a 1:1, one-on-one, check-in, or weekly sync with someone on their team, or wants talking points before meeting a report.
---

# One-on-one prep

A 1:1 is a recurring, private conversation for feedback, career development and trust, not a status update. Our default: the report's agenda comes first, the manager brings 3 items or fewer, and the report leaves with a blocker cleared, a clear signal on how they're doing, and one thing the manager will do for them.

## When to use

- Before a weekly or biweekly 1:1 with a direct report.
- Before a first 1:1 with someone new to the team (use the first-meeting variant in step 6).
- When a manager has scattered notes (Slack threads, last 1:1 notes, project updates) and wants talking points.
- Not for a performance warning or a hard conversation: use difficult-conversation-prep.

## What you need

- The report's name and role, and how long you've managed them.
- Last 1:1's notes, especially commitments either of you made. If missing, ask once; otherwise write "no notes from last time" and skip the check-off.
- Recent signals: project updates, Slack messages, wins, misses, peer comments.
- Anything the report already put on the shared agenda. If none, add a prompt asking them to add items.

## Steps

1. **Put the report's agenda first.** Copy their items in their order. If they added nothing, open with one question: "What's the most useful thing we could talk about today?" Never move their items below yours.
2. **Check last time's commitments.** List each commitment with its owner and mark it done, not done, or changed. A manager's missed commitment goes first in this list and gets named plainly ("I said I'd get you budget sign-off; I haven't").
3. **Pick one win to recognize.** Choose a specific behavior from the last 2 weeks with its effect ("Your migration checklist meant support had zero tickets on launch day"). If there is no clear win, skip it rather than inventing praise.
4. **Pick at most one piece of feedback.** Write it with the Center for Creative Leadership's Situation–Behavior–Impact model, then add a request (our addition): a specific time and place, only what was observable, and the effect it had. Only behavior you saw or have direct evidence of. If you have more than one, keep the one with the biggest impact and save the rest.
5. **Pick one growth question.** Rotate through (our default list): what energizes them, the skill they want next, the role they want in 2 years, what they'd change about their job. If last time's growth question got a real answer, follow up on it instead of asking a new one.
6. **List blockers and what you will do.** Each blocker gets one manager action and a date, or "need more info" with the question to ask. For a first 1:1, replace steps 3 and 4 with questions like Lara Hogan's: how they like feedback (the medium, such as chat, email or in person; in 1:1s or as it happens), whether they like recognition in public or private, what makes them grumpy and how you'll know, and what makes 1:1s valuable for them.
7. **Keep the manager's items to 3 (our default).** Org news, a decision they need to know, or a request. Anything else goes in a written note after the meeting.

## Output format

```markdown
# 1:1 with [name] — [date]

## Their agenda (first)
- [Their item, in their words] / or: "What's the most useful thing we could talk about today?"

## Last time's commitments
| Owner | Commitment | Status |
|---|---|---|
| [Manager] | [What I said I'd do] | [done / not done / changed: why] |
| [Report] | [What they said they'd do] | [done / not done / changed] |

## Recognize
- [Specific behavior] → [effect it had]

## Feedback (SBI)
- **Situation:** [when and where]
- **Behavior:** [what they did, observable]
- **Impact:** [effect on people, work, or customers]
- **Request:** [what to keep doing or change]

## Growth question
- [One question] (follow-up on: [last answer, if any])

## Blockers
| Blocker | What I'll do | By |
|---|---|---|
| [Blocker] | [Manager action] | [date] |

## My items (max 3)
- [Item]

## After the meeting
- Send notes with new commitments within 24 hours.
```

## Example

**Input:** "1:1 with Dana (CS lead, managed 8 months) tomorrow. Last time I promised to ask finance about her headcount request, haven't yet. She said she'd draft the renewal playbook, it's in Notion. She handled the Orbitly escalation Friday really well, customer emailed to thank her and the renewal call is back on. She talked over Ravi twice in Monday's standup; he stopped and never finished his billing-bug update. She hasn't added anything to our doc. Org news: Q3 planning starts next week."

**Output:**

```markdown
# 1:1 with Dana — tomorrow [check: date]

## Their agenda (first)
- Nothing added yet. Open with: "What's the most useful thing we could talk about today?"

## Last time's commitments
| Owner | Commitment | Status |
|---|---|---|
| Manager | Ask finance about the CS headcount request | not done: say so first, give a new date (Friday) |
| Dana | Draft the renewal playbook | done: in Notion, ask what feedback she wants on it |

## Recognize
- Friday's Orbitly escalation: you owned it end to end → the customer emailed to thank you, and the renewal call is back on.

## Feedback (SBI)
- **Situation:** Monday's standup.
- **Behavior:** You started speaking while Ravi was mid-sentence, twice.
- **Impact:** Ravi stopped and didn't finish his update on the billing bug, so we lost that detail.
- **Request:** Let people finish, then add your point. Can you try that this week?

## Growth question
- "Which part of the escalation did you enjoy most, and would you want more of that work?"

## Blockers
| Blocker | What I'll do | By |
|---|---|---|
| Headcount answer from finance | Email finance today, share the answer | Friday [check: date] |

## My items (max 3)
- Q3 planning starts next week: bring the CS team's top 3 priorities.

## After the meeting
- Send notes with new commitments within 24 hours.
```

## Checks before you send

- [ ] The report's agenda (or the open question) comes before anything the manager wants.
- [ ] Every past commitment has a status, and the manager's misses are named.
- [ ] Feedback is one item, in SBI form, about observed behavior, with no personality words ("rude", "lazy").
- [ ] Every blocker has a manager action and a date.
- [ ] The manager has 3 items or fewer.

## Common mistakes

- Turning the 1:1 into a project status review. Status belongs in a written update.
- Stacking 3 pieces of feedback. People remember one.
- Asking "any blockers?" and moving on. Name the ones you already know about.
