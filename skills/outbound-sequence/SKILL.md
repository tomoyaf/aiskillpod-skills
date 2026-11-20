---
name: outbound-sequence
description: Writes a 4 to 7 touch multi-channel outbound sequence for one buyer persona - email, LinkedIn, and phone steps with the day of each touch and ready-to-use copy per step, each touch adding something new. Use when a rep, founder, or SDR asks for an outbound sequence, cadence, prospecting sequence, multi-touch campaign, follow-up steps for cold prospects, or copy for Outreach, Apollo, Salesloft, or HubSpot sequences.
---

# Outbound sequence

A good sequence gives the prospect a new reason to reply at every touch, not the same ask louder. Follow-ups bring in a large share of replies (42% in one 2026 benchmark), but only when each adds something. Write for one persona and one problem, keep each email under 80 words, and stop after the breakup touch. "Just bumping this up" is not a touch.

## When to use

- Starting outbound to a new persona or segment.
- Rebuilding a sequence with reply rates below the 3.43% average reported in one 2026 cold email benchmark.
- Loading copy into a sequencing tool (Outreach, Apollo, Salesloft, HubSpot).
- Not for one hand-researched first email: use cold-outreach-email. Not for following up after a call: use follow-up-email.

## What you need

- The persona: role, company type and size, and the one problem you solve for them.
- Proof: a customer result, a number, or a named customer type. If none is given, ask once; without it, use a specific observation instead and never invent a result.
- The ask: a 15-minute call, a reply, a resource. One ask per sequence.
- Channels available: email only, or email plus LinkedIn and phone. Default to all 3.
- Optional: personalization fields your tool supports. Write them as [first_name], [company], [observation].

## Steps

1. **Pick one angle per touch.** Plan the sequence before writing: touch 1 the problem, touch 2 proof, touch 3 a different angle (cost of doing nothing, a peer's approach), touch 4 a useful resource, last touch the breakup. No two touches use the same angle.
2. **Set the timing.** Instantly's 2026 benchmark puts the sweet spot at 4 to 7 touches spaced 3 to 4 days apart. Our default is 6 touches over 17 days: day 1 email, day 4 LinkedIn connect (no pitch), day 7 email, day 10 call plus voicemail, day 14 email, day 17 breakup email. For 4 touches: days 1, 4, 8, 12. Never 2 touches on the same day in the same channel.
3. **Write email touches under 80 words.** The best-performing senders in that benchmark average under 80 words per first-touch email. Line 1 is about them, not you. One problem, one proof point, one ask, phrased as a yes/no question. Subject lines 2 to 5 words, lowercase, no clickbait. Follow-up emails reply in the same thread unless the angle changes completely.
4. **Write the LinkedIn note under 200 characters.** LinkedIn caps invitation notes at 200 characters, and members without Premium can add a note to only 3 requests a month, so skip the note for those senders. A connection reason, no pitch, no link. If they accept, the message after is one line referencing the email.
5. **Write the call script as 3 lines and a voicemail.** Opener with the reason for the call, one question about the problem, the ask. Voicemail under 20 seconds, says you'll send an email, and the email goes out that day.
6. **Write the breakup.** Short, polite, gives an easy out: "Should I close the loop?" or "Wrong person? Who should I talk to?" No guilt.
7. **Add the exit rules.** Stop the sequence on any reply, a meeting booked, or an unsubscribe; pause on an out-of-office over 7 days (our default). Gmail requires every sender to keep spam rates below 0.3%, and senders of more than 5,000 messages a day to offer one-click unsubscribe on marketing and subscribed messages and to set up SPF, DKIM and DMARC, so check the tool's unsubscribe link is on. Say this in the output so it gets set in the tool.

## Output format

```markdown
# Outbound sequence: [persona] — [problem]

**Ask:** [one ask] · **Length:** [n] touches over [n] days · **Proof used:** [proof]
**Exit rules:** stop on reply, meeting booked, or unsubscribe; pause on out-of-office over 7 days. Unsubscribe link on.

## Touch 1 — Day [n] — Email — Angle: [angle]
**Subject:** [2–5 words]
[Body under 80 words]

## Touch 2 — Day [n] — LinkedIn — Angle: [angle]
**Connection note:** [under 200 characters]
**If accepted:** [one line]

## Touch 3 — Day [n] — Call — Angle: [angle]
**Opener:** [line]
**Question:** [line]
**Ask:** [line]
**Voicemail:** [under 20 seconds]

## Touch [n] — Day [n] — Email — Breakup
**Subject:** [same thread or 2–5 words]
[Body under 60 words]
```

## Example

**Input:** Sender: Sam at Rosterly, which matches open shifts to available carers by text in minutes. Persona: head of operations at 50–200 person home-care agencies. Problem: shift scheduling done in spreadsheets, last-minute gaps. Most agencies that size fill sick calls by phone from the spreadsheet, so the gaps land on the ops lead at 6 a.m., and a gap filled at the last minute usually means overtime or agency staff at a higher rate. Proof: Maple Care cut unfilled shifts from 30 a month to 8 after moving off spreadsheets, and their ops lead stopped doing the 6 a.m. calls. Ask: 15-minute call. Channels: all 3. 6 touches.

**Output:**

```markdown
# Outbound sequence: head of operations, home-care agencies — unfilled shifts

**Ask:** 15-minute call · **Length:** 6 touches over 17 days · **Proof used:** Maple Care, 30 to 8 unfilled shifts a month
**Exit rules:** stop on reply, meeting booked, or unsubscribe; pause on out-of-office over 7 days. Unsubscribe link on.

## Touch 1 — Day 1 — Email — Angle: the problem
**Subject:** last-minute shift gaps
Hi [first_name], most agencies [company]'s size still fill sick calls by phone from a spreadsheet, which is why gaps land on the ops lead at 6 a.m. We match open shifts to available carers by text in minutes. Worth a 15-minute call to see if it fits how you schedule?

## Touch 2 — Day 4 — LinkedIn — Angle: connection
**Connection note:** I work with home-care ops leads on scheduling. Would be glad to connect.
**If accepted:** Thanks for connecting, [first_name]. I sent a short note about shift gaps by email, in case it's useful.

## Touch 3 — Day 7 — Email — Angle: proof
**Subject:** (same thread)
[first_name], one example: Maple Care went from 30 unfilled shifts a month to 8 after moving off spreadsheets. Their ops lead stopped doing the 6 a.m. calls. Open to 15 minutes to see if [company] could do the same?

## Touch 4 — Day 10 — Call — Angle: how they fill gaps today
**Opener:** Hi [first_name], it's Sam from Rosterly. I'm calling about how you fill last-minute shifts. Do you have 30 seconds?
**Question:** When a carer calls in sick at 6 a.m., what happens next at [company]?
**Ask:** Would a 15-minute call this week to compare notes be worth it?
**Voicemail:** Hi [first_name], Sam from Rosterly, about filling last-minute shifts. I'll send you a short email today. Thanks.

## Touch 5 — Day 14 — Email — Angle: cost of doing nothing
**Subject:** overtime from gaps
[first_name], a quick thought: every gap filled at the last minute is usually overtime or agency staff at a higher rate. If gaps are under control at [company], ignore this. If not, is a 15-minute call worth it?

## Touch 6 — Day 17 — Email — Breakup
**Subject:** (same thread)
[first_name], I haven't heard back, so I'll close the loop here. If shift scheduling is someone else's job at [company], who should I talk to?
```

## Checks before you send

- [ ] Each touch has a different angle, and none says only "bumping this up" or "following up".
- [ ] Every email body is under 80 words and has exactly one ask.
- [ ] Every proof point and number comes from the input.
- [ ] Timing has no 2 same-channel touches on one day, and the breakup is the last touch.
- [ ] Exit rules are stated.
- [ ] Personalization fields are written as [field] so they map to the tool.

## Common mistakes

- Pitching in the LinkedIn connection note. It lowers accept rates and burns the channel.
- Writing for "SMBs" or "decision makers". One persona, one problem per sequence.
- Adding touches 8 to 12. After the breakup, put them in a nurture list, not more follow-ups.
