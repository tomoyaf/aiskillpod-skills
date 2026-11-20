---
name: meeting-minutes
description: Turns a meeting transcript or rough notes into minutes with decisions, action items (owner and due date each), and open questions, ready to paste into Slack, email, or a doc. Use when someone shares a transcript, call recording notes, or bullet notes and asks for minutes, a recap, a summary of a meeting, or "who's doing what".
---

# Meeting minutes with action items

Minutes exist so people who missed the meeting know what changed and who owes what by when. Write for them. Decisions and action items come first; the discussion comes last and short.

## When to use

- After any internal or client meeting with a transcript (Zoom, Meet, Teams, Otter) or someone's rough notes.
- When a thread asks "what did we decide?" or "who's doing that?".
- Not for a verbatim record (board minutes, legal hearings): those need the full wording.

## What you need

- The transcript or notes. Speaker names help; if they're missing, ask once, then write "[unknown speaker]".
- The meeting's date and title. If missing, take them from the transcript header or ask.
- Optional: the agenda, so you can flag items that were skipped.

## Steps

1. **Find the decisions.** A decision is something the group agreed and won't revisit without a reason: "We'll launch on the 14th", "Pricing stays as is". Proposals nobody agreed to are not decisions; they go under open questions.
2. **Find every action item.** Look for "I'll", "can you", "let's have X do", "by Friday", "next week". Each item gets one owner (a person, never "the team"), a verb-first task, and a due date. If no date was said, write "no date set" and add it to open questions.
3. **Collect open questions.** Anything raised but not settled, and anything waiting on someone outside the meeting.
4. **Summarize the discussion in 3 to 5 bullets.** One line each, only what explains a decision. Skip small talk, repeated points, and who said what unless it matters.
5. **Check against the agenda** if you have it. List agenda items that weren't covered under "Not covered".
6. **Write it in the format below.** Use the attendees' own words for names of projects, customers, and products. Don't add facts that aren't in the source.

## Output format

```markdown
# [Meeting title] — [date]

**Attendees:** [names]  
**Absent:** [names, if known]

## Decisions
- [Decision, one line. Why, in a few words, if it was stated.]

## Action items
| Owner | Task | Due |
|---|---|---|
| [Name] | [Verb-first task] | [Date or "no date set"] |

## Open questions
- [Question] — [who will answer, if anyone]

## Discussion
- [3 to 5 one-line bullets]

## Not covered
- [Agenda items skipped, or remove this section]
```

## Example

**Input (excerpt):** Onboarding email sync, Tuesday 3 March 2026

> Priya: So we're agreed, the onboarding email goes out Tuesday, not Monday.  
> Sam: Yes. I'll fix the subject line tonight.  
> Priya: Can someone ask legal about the discount wording?  
> Lee: I can, probably by Thursday.  
> Sam: Do we still want the webinar in March? Let's talk next week.

**Output:**

```markdown
# Onboarding email sync — Tuesday 3 March 2026

**Attendees:** Priya, Sam, Lee

## Decisions
- The onboarding email goes out Tuesday, not Monday.

## Action items
| Owner | Task | Due |
|---|---|---|
| Sam | Fix the email's subject line | 3 March (tonight) |
| Lee | Ask legal to approve the discount wording | Thursday 5 March |

## Open questions
- Do we still run the March webinar? — to discuss next week

## Discussion
- Tuesday was chosen over Monday; no reason was given in the call.
```

## Checks before you send

- [ ] Every action item has exactly one named owner and a due date or "no date set".
- [ ] Every decision was agreed in the source, not just suggested.
- [ ] No fact, number, or name appears that isn't in the transcript or notes.
- [ ] Someone who missed the meeting can act on it after reading only Decisions and Action items.
- [ ] It fits on one screen; the discussion is 5 bullets or fewer.

## Common mistakes

- Writing "Team to follow up". Name a person or list it as an open question.
- Turning a long debate into a decision because it ended. If nobody said "agreed" or equivalent, it's open.
- Copying the transcript's order. Group by decisions, then actions; the order of talk doesn't matter to the reader.
