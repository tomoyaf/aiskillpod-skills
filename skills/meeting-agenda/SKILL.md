---
name: meeting-agenda
description: Builds a meeting agenda from a goal and an attendee list - the outcome the meeting must produce, timed items phrased as questions with an owner and a type (decide, discuss, inform), pre-reads, and who can skip. Recommends cancelling and sending an update instead when nothing needs a decision or a live discussion. Use when someone asks for an agenda, plans a meeting, sets up a recurring sync, or asks "do we even need this meeting?".
---

# Meeting agenda

An agenda is a test of whether the meeting should happen at all. If no item needs a decision or a real discussion, the AI says so and drafts the update to send instead. If the meeting is needed, every minute has an item, an owner, and an expected result.

## When to use

- Someone is about to send a calendar invite and needs the agenda for it.
- A recurring meeting (weekly sync, team meeting) has drifted and needs a fixed structure.
- Someone asks "do we need a meeting for this?" or "can this be an email?".
- Not for a workshop or offsite with exercises. Those need a facilitation plan, not an agenda.

## What you need

- The goal: what should be true after the meeting. If missing, ask once: "What should be decided or agreed when this ends?"
- Attendees and their roles. If missing, draft the agenda and list who each item needs, so the organizer can trim the invite.
- Length and date. If missing, our default is 30 minutes.
- Optional: the topics people want to raise, earlier minutes, and any docs that exist.

## Steps

1. **Write the desired outcome in one sentence.** Asana's agenda guide says to state the meeting's primary purpose in a single sentence. Make it a result ("Choose the launch date and confirm owners"), not a topic ("Launch").
2. **Turn each topic into a question.** Steven Rogelberg, who researches meetings, suggests an agenda of "questions to be answered" instead of topics to discuss. "Pricing" becomes "Do we keep the annual discount for the June launch?"
3. **Tag each item: decide, discuss, or inform.** Decide: the group leaves with an answer and a named decider. Discuss: the group needs live input from several people, and the item says what the input is for. Inform: one person shares and others listen. Asana's guide separates informational, discussion, and action items and puts informational items first for context. Our default: move every inform item to the pre-read or a written update unless it takes 2 minutes or less.
4. **Apply the cancel rule.** Rogelberg: "if you just can't think of any questions, it likely means you don't need a meeting." If no item is decide or discuss, recommend cancelling and draft the written update with the inform items. Asana's guide says the same: if everything can be handled asynchronously, cancel and send the message by email.
5. **Give every item an owner and minutes.** Atlassian's agenda guide lists, for each item, who leads it and how much time it has. Put the hardest decide item first or second, while people are fresh. Leave 5 minutes at the end to read back decisions and action items. Times must add up to the meeting length.
6. **List pre-reads and when they arrive.** Link each doc and say what to look for ("read section 2, the 3 options"). Asana's guide recommends sharing the agenda 24 hours ahead, or 48 to 72 hours for complex meetings. Our default: pre-reads are 10 minutes of reading or less; anything longer gets a summary at the top.
7. **Check the attendee list against the items.** Rogelberg notes that questions show who really needs to attend. Anyone not needed for a decide or discuss item is marked optional and gets the notes afterwards.

## Output format

```markdown
# [Meeting name] — [date], [length] min

**Outcome:** [one sentence: what is decided or agreed when this ends]  
**Attendees:** [names] · **Optional:** [names, get the notes]  
**Pre-reads (by [day/time]):** [doc link] — [what to look for]

| # | Question | Type | Owner | Min |
|---|---|---|---|---|
| 1 | [question?] | [decide/discuss/inform] | [name] | [n] |
| 2 | [question?] | | | |
| [n] | Read back decisions and action items | — | [organizer] | 5 |

**Decider for decide items:** [name, if different from the owner]
```

When nothing needs a decision or discussion:

```markdown
**Recommendation: cancel this meeting.** No item needs a decision or live discussion. Send this update instead:

**[Subject line]**
- [inform item, one line, with link]
- [inform item]
Reply in [thread/channel] by [date] if anything here needs a conversation.
```

## Example

**Input:** "Need an agenda for Thursday 11 June 2026's 45-min marketing sync. Attendees: Mei (head of marketing, makes the call), Jonas (content), Priya (paid ads), Sam (design). Topics: Q3 webinar date (Jonas has 3 candidates, 9, 16 or 23 July, in the webinar dates doc), how to split July's ad budget between LinkedIn and Google (Priya's May ad results doc has cost per lead by channel), May blog traffic numbers (Jonas), new brand colors are done (Sam)."

**Output:**

```markdown
# Marketing sync — Thursday 11 June, 45 min

**Outcome:** Pick the Q3 webinar date and agree the July ad budget split.  
**Attendees:** Mei, Jonas, Priya · **Optional:** Sam (gets the notes)  
**Pre-reads (by Wednesday 10 June):** Ad results, May — compare cost per lead by channel; Webinar dates doc — the 3 candidate dates and their conflicts

| # | Question | Type | Owner | Min |
|---|---|---|---|---|
| 1 | Which date do we hold the Q3 webinar: 9, 16, or 23 July? | decide | Jonas | 15 |
| 2 | How do we split July's ad budget between LinkedIn and Google? | decide | Priya | 20 |
| 3 | What does May's blog traffic mean for the webinar promotion plan? | discuss | Jonas | 5 |
| 4 | Read back decisions and action items | — | Mei | 5 |

**Decider for decide items:** Mei

Moved to the pre-read / written update: new brand colors are final (Sam, link in the channel); blog traffic numbers for May (Jonas, in the doc).
```

## Checks before you send

- [ ] The outcome is one sentence that names a result, not a topic.
- [ ] Every item is a question with a type, one owner, and minutes; the minutes add up to the meeting length.
- [ ] At least one item is decide or discuss; if none is, the output recommends cancelling and drafts the update.
- [ ] Inform items longer than 2 minutes are in the pre-read or the update, not the meeting.
- [ ] Each pre-read says what to look for and when it arrives.
- [ ] Attendees not needed for a decide or discuss item are marked optional.

## Common mistakes

- Listing topics ("Budget") instead of questions. Nobody knows when the item is finished.
- A decide item with no decider. The group discusses, then agrees to "take it offline".
- Status round-robins. Each person reading their update aloud is an inform item that belongs in writing.
