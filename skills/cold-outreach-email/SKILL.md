---
name: cold-outreach-email
description: Writes a first-touch cold email to a prospect from your research - under 90 words, one specific observation, one problem, one low-friction ask - with 2 subject line options. Use when someone wants a cold email, prospecting email, first outreach, or intro email to a lead they haven't spoken to, and has a LinkedIn profile, company website, news item, or notes to work from.
---

# Cold outreach email

A cold email earns a reply when the first line could only have been written to this person, the problem is one they'd say out loud, and the ask takes 10 seconds to answer. Short beats clever. If you can't find a specific observation, don't send yet. In Gong's analysis of 304,174 emails, asking about interest was the best-performing call to action for cold emails, ahead of asking for a time.

## When to use

- First contact with a prospect you have researched but never spoken to.
- Rewriting a cold email template that gets no replies.
- Not for someone who already met you: use follow-up-email. For a multi-step cadence, use outbound-sequence.

## What you need

- Research on the person and company: role, a recent post, hire, launch, funding, job ad, review, or anything specific. If you have nothing specific, ask once for a link; without one, write the email but flag "[needs a specific observation]".
- What you sell, in one line, and the problem it solves.
- Optional: one proof point (a similar customer and a result). Use only proof that's given.
- The sender's name and role.

## Steps

1. **Pick one observation.** Choose the most specific, most recent fact that connects to the problem you solve. A job ad for 3 SDRs beats "I saw you're growing". Never open with a compliment about their company or "I hope this finds you well".
2. **Name one problem.** The problem that observation usually brings, stated the way the buyer would say it ("new reps take 3 months to book their first meeting"). One problem only; a list reads like a brochure.
3. **Add one line of credibility, if you have it.** A similar company and what changed, with a number. No proof given? Skip the line rather than invent one.
4. **Make one low-friction ask.** An interest question ("Worth a look?", "Is this on your list for Q1?") beats a meeting request: in Gong's data, specific-time asks in cold emails had a success rate of only 15%, behind interest asks. Never ask for 30 minutes in the first email.
5. **Cut to under 90 words.** Our default, inside the 50–125 word range where Boomerang's study of over 40 million emails found the most replies. Count the body only: not the greeting, not the signature. Delete adjectives, "I wanted to reach out", "just", and any sentence about your company's history.
6. **Write 2 subject lines.** 2–4 words: Boomerang found 3–4 word subjects got the most replies. Lowercase reads like a colleague (our default); no clickbait, no "quick question". One based on the observation, one on the problem.
7. **Read it as the prospect.** If the first line could be sent to 100 people unchanged, rewrite it. If any claim isn't in the research, remove it or mark it "[check]".
8. **Respect the list rules.** Send only to a person you researched, never a bought list: Gmail's sender guidelines say not to buy addresses and require every sender to keep the spam rate in Postmaster Tools below 0.3% (target below 0.1%). If the sender sends more than 5,000 messages a day to Gmail accounts, the bulk rules also apply: SPF, DKIM and DMARC, plus one-click unsubscribe on marketing messages. In the US, CAN-SPAM covers this email too, business-to-business included (the FTC's compliance guide): identify it clearly as an ad, with a line saying it's a sales message; include a valid physical postal address; and give a way to opt out, honored within 10 business days. For recipients in other countries, add "[check: local email rules]".

## Output format

```markdown
**To:** [name], [title] at [company]
**Subject option A:** [observation-based]
**Subject option B:** [problem-based]

Hi [first name],

[Observation: 1 sentence, specific to them]

[Problem: 1–2 sentences, in their words]

[Credibility: 1 sentence with a result, or omit]

[Ask: 1 short question]

[Sender name]
[Role, company]
[A line that it's a sales message] · [Postal address] · [How to opt out]

---
**Word count:** [n] (body only, without greeting and signature)
**Research used:** [the fact behind the first line + source]
**Flags:** [anything to confirm, or "none"]
```

## Example

**Input:** Prospect: Daniel Osei, Head of Sales at Quillsoft (B2B invoicing software, about 80 people). Research: LinkedIn post 5 days ago saying they're hiring 4 SDRs this quarter. We sell Rampkit, a practice tool where new reps rehearse calls with AI. Proof: Meridian HR cut new-rep time to first booked meeting from 9 weeks to 5.

**Output:**

```markdown
**To:** Daniel Osei, Head of Sales at Quillsoft
**Subject option A:** your 4 new sdrs
**Subject option B:** booked by week 5

Hi Daniel,

Saw your post about hiring 4 SDRs this quarter.

The usual catch: new reps spend their first 2 months practicing on real prospects, and the early calls burn good leads.

Meridian HR had their new reps rehearse with Rampkit first and cut time to first booked meeting from 9 weeks to 5.

Worth a look before the new hires start?

Ana Silva
Account Executive, Rampkit
A sales message from Rampkit · [postal address] · Reply "no thanks" and I won't email again.

---
**Word count:** 60 (body only, from "Saw" to "start?", without greeting and signature)
**Research used:** LinkedIn post, 5 days ago, hiring 4 SDRs
**Flags:** confirm the Meridian result is approved for outbound use
```

## Checks before you send

- [ ] Body is under 90 words.
- [ ] The first line names something specific to this person or company and couldn't go to 100 people unchanged.
- [ ] Exactly one problem and one ask.
- [ ] The ask is a yes/no or one-line answer, not a meeting request.
- [ ] Every fact and result comes from the research or proof given; anything else is flagged.
- [ ] 2 subject lines, each 2–4 words.
- [ ] The address came from research on this person, not a bought list.
- [ ] For US recipients: a line that it's a sales message, a postal address and a way to opt out.

## Common mistakes

- Opening with yourself: "I'm Ana from Rampkit and we help...". Open with them.
- Stacking 3 pain points to cover all bases. Pick the one the observation points to.
- Fake personalization ("I loved your recent post!") without saying what was in it.
