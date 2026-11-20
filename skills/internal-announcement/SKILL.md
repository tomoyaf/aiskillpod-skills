---
name: internal-announcement
description: Writes an internal announcement email or Slack post for a change at work - bottom line up front (BLUF), what changes and what doesn't, why, when, who it affects, what each group must do and by when, and where to ask questions. Use when someone needs to announce a policy, process, tool, org, or schedule change to the team, asks for an all-hands email, a Slack announcement, or "how do I tell everyone about this?".
---

# Internal announcement

Our default assumption: many readers see only the first 2 lines and decide from them whether it concerns them. Put the change and the action in those lines. Everything after that is for the people who want detail.

## When to use

- A policy, process, tool, schedule, office, or team structure is changing and staff need to know.
- Someone asks for an all-hands email, a #general post, or a manager's note to their team about a change.
- A change was announced badly and needs a clear follow-up.
- Not for news to customers or the public. Use a customer notice or a launch announcement; this skill writes for people inside the company.

## What you need

- What is changing and when it takes effect. If either is missing, ask once; never guess a date.
- Who it affects. If unclear, write the draft for everyone and mark "[confirm who is affected]".
- What people must do, and by when. If nothing, say "No action needed" in the opening.
- Where to ask: a person, a channel, or a meeting. If missing, use the sender and mark "[confirm contact]".
- Optional: the reason for the change, what stays the same, a link to the full policy, and the channel (email or Slack).

## Steps

1. **Write the bottom line first.** BLUF means bottom line up front: the change and the action in the first 1 or 2 sentences. NN/g's inverted pyramid guidance says the same for web writing: "The story should start with the main point." The subject line or first bold line names the change and the date ("Expense reports move to Ramp on 1 March").
2. **Say what changes and what doesn't.** 2 to 5 bullets of what is different, in concrete terms. Add 1 or 2 bullets of what stays the same when people are likely to worry ("Your approval limit doesn't change").
3. **Give the reason in 1 to 3 sentences.** Prosci's ADKAR model starts with awareness: people need to "understand why the change is needed" before they support it. Give the real reason; skip slogans.
4. **State when.** The date it starts, any deadline before it, and any period when both the old and new way work. Use dates, not "soon" or "next week".
5. **Split actions by group.** If different groups do different things, give each group its own line ("Managers: approve pending reports by 28 February"). Each action starts with a verb and has a date. If a group needs to do nothing, say so.
6. **Say where to ask.** One person or channel, and any session where people can ask live. Our default: name a person, not only a channel.
7. **Fit the channel.** Our default lengths: email, subject line plus up to about 200 words, with a link to the full detail. Slack: bold first line, 3 to 8 short lines, link to detail, and ask people to reply in the thread. Our default: if the change affects pay, job roles, or working hours, managers tell affected people directly before the wide announcement; mark "[check: local law / HR]" for anything that touches employment terms.

## Output format

```markdown
**Subject:** [Change] — [date it takes effect]

[BLUF: 1–2 sentences. What changes, when, and what the reader must do, or "No action needed".]

**What changes**
- [concrete change]

**What stays the same**
- [only if people will worry; otherwise remove]

**Why**
[1–3 sentences.]

**When**
- [date]: [what happens]

**What you need to do**
- **[Group]:** [verb-first action] by [date]
- **Everyone else:** [action or "nothing"]

**Questions?** [Person] or [channel]. [Live session, if any.]

[Link to full details]
```

## Example

**Input:** "Tell the whole company (40 people) we're moving expense reports from spreadsheets to Ramp. Starts 1 March. Old spreadsheet closes 28 Feb, anything after goes through Ramp. Managers have to approve their team's pending spreadsheet reports by 28 Feb. Reason: finance spends 2 days a month chasing receipts. Approval limits don't change. Questions to Lucia in finance or #ask-finance. Lucia will do a 20-min demo on 25 Feb. Email."

**Output:**

```markdown
**Subject:** Expense reports move to Ramp on 1 March

From 1 March, submit all expenses in Ramp instead of the expense spreadsheet. Managers: approve your team's pending spreadsheet reports by 28 February.

**What changes**
- You submit expenses and receipts in Ramp.
- The expense spreadsheet closes on 28 February. Expenses from 1 March go through Ramp only.

**What stays the same**
- Your approval limits.

**Why**
Finance spends about 2 days every month chasing receipts. Moving to Ramp is meant to cut that time.

**When**
- 25 February: 20-minute demo with Lucia
- 28 February: spreadsheet closes
- 1 March: Ramp only

**What you need to do**
- **Managers:** approve your team's pending spreadsheet reports by 28 February.
- **Everyone:** submit expenses from 1 March in Ramp. [confirm: how people get Ramp access]

**Questions?** Lucia in finance, or #ask-finance. Bring them to the demo on 25 February.

[Link to the expense guide]
```

## Checks before you send

- [ ] The first 2 sentences say what changes, when, and what the reader must do (or "No action needed").
- [ ] Every date is a real date; no "soon" or "next week".
- [ ] Each affected group has a verb-first action with a deadline, or is told it needs to do nothing.
- [ ] One named person or channel is given for questions.
- [ ] The reason is stated plainly in 3 sentences or fewer.
- [ ] Nothing is stated that isn't in the input; open points are marked "[confirm]".

## Common mistakes

- Opening with background ("As you know, we've been reviewing..."). Readers stop before the change.
- One action list for everyone when managers and staff do different things.
- Announcing changes to pay, roles, or hours to the whole company before the affected people hear it from their manager.
