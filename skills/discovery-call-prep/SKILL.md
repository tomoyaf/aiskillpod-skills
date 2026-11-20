---
name: discovery-call-prep
description: Builds a one-page prep sheet for a sales discovery call from the prospect's website, LinkedIn, and notes - hypotheses about their problem, 8 questions ranked by what they reveal, what to learn to qualify the deal, and red flags to listen for. Use when someone has a discovery call, first meeting, intro call, or sales call coming up and asks to prep, research the prospect, or write call questions.
---

# Discovery call prep

Good discovery tests a few sharp guesses about the buyer's problem instead of running a questionnaire. The prep sheet fits on one page, ranks the questions so the most important ones get asked even if the call runs short, and says what you must learn to know whether this is a real deal. Gong's analysis of 519,000 calls found success peaked at 11–14 targeted questions, with questions about the buyer's business issues, goals, and concerns most linked to success.

## When to use

- Before a first meeting or discovery call with a prospect.
- When a call was booked by someone else (SDR, inbound form) and you need context fast.
- Before a second call with a new stakeholder in an existing deal.
- Not for a demo script or a negotiation: this is for learning, not presenting.

## What you need

- The prospect's company website or a description of what they do.
- The attendee's name, title, and LinkedIn summary if available. If missing, ask once; otherwise prepare for the likely role and mark it "[assumption]".
- Anything already known: inbound form answers, SDR notes, emails.
- What you sell, in one line, and who it's usually for.
- Call length. If not given, assume 30 minutes.

## Steps

1. **Write a 3-line snapshot.** What the company does, size and stage if visible, and the one fact most relevant to what you sell (a hiring push, a launch, a new market, a complaint in reviews). Cite where each fact came from.
2. **Form 2–3 hypotheses.** Each is a guess about their problem you can confirm or kill: "Because they're opening 3 new warehouses, inventory counts are likely manual and slow." Rank by how likely and how costly. A hypothesis without a reason from the research doesn't go on the sheet.
3. **Write 8 questions, ranked.** 8 prepared questions plus follow-ups lands in Gong's 11–14 range; beyond 14, success fell back to average. Spread them through the call, not all up front: Gong found top reps spread questions evenly while average reps front-load them. Order: 2 to confirm the top hypothesis, 2 on impact (what it costs, who feels it), 1 on what they've tried, 1 on timeline or trigger, 1 on how they decide and who signs, 1 open closer ("What would make this call worth it for you?"). Open questions only; no "Do you..." questions. If the call is 30 minutes, mark the first 5 as must-ask.
4. **Define what you must learn to qualify.** 4–5 items, each a yes/no you can tick after the call, built on BANT as Salesforce defines it (budget, authority, need, timing): pain confirmed in their words, a cost or number, who signs, a date or trigger, current alternative. Name the minimum to book a next step.
5. **List red flags.** 3–5 things that would mean this isn't a deal now: no problem owner, "just researching" with no trigger, a signed contract with a competitor until next year, a budget frozen until a named date, a company outside your target size.
6. **Plan the opening and the close.** Opening: 1 sentence to set the agenda and confirm time. Close: the next step you'll propose if it's qualified, and the one if it isn't.
7. **Keep it to one page.** Under 350 words (our default). Cut background that won't change a question.

## Output format

```markdown
# Discovery prep: [company] — [attendee, title] — [date, length]

## Snapshot
- [What they do, size, stage] ([source])
- [Most relevant fact] ([source])
- [What's already known from form/notes]

## Hypotheses
1. [Guess] — because [evidence]
2. [Guess] — because [evidence]

## Questions (ranked; first 5 must-ask)
1. [Question] — tests H1
2. ...
8. [Open closer]

## To qualify, learn
- [ ] [Item]
Minimum for a next step: [items]

## Red flags
- [Flag]

## Open and close
- Open: "[agenda line]"
- If qualified: [next step to propose]
- If not: [graceful exit or nurture]
```

## Example

**Input:** Call Thursday, 30 minutes, with Rosa Lindqvist, Head of People at Northwind Clinics (website: 22 physiotherapy clinics in Sweden and Norway; careers page lists 31 open roles). Inbound form: "We need a better way to onboard new staff." We sell Onboardly, onboarding checklists and e-signing for multi-site teams.

**Output:**

```markdown
# Discovery prep: Northwind Clinics — Rosa Lindqvist, Head of People — Thu, 30 min

## Snapshot
- 22 physiotherapy clinics, Sweden and Norway (website)
- 31 open roles (careers page)
- Form: "We need a better way to onboard new staff."

## Hypotheses
1. Each clinic onboards its own way and start dates slip — 22 sites, 31 open roles.
2. Contracts and licence checks are chased by email — clinical roles need licence proof before day 1 [assumption].
3. Swedish and Norwegian documents drift out of sync — they hire in both countries.

## Questions (ranked; first 5 must-ask)
1. Walk me through what happens between a signed offer and someone's first day at a clinic.
2. How does that differ between clinics?
3. What happened the last time onboarding went wrong?
4. How many hours does a clinic manager spend on a new hire before day 1?
5. Who decides on a tool like this, and who else would weigh in?
6. What have you tried so far: templates, your HR system?
7. What made you fill in the form now?
8. What would make this call worth your 30 minutes?

## To qualify, learn
- [ ] Pain in her words (inconsistency, delays, compliance)
- [ ] A number: hours, delayed starts, or hires per month
- [ ] Who signs and whether IT must approve
- [ ] A trigger or date (new clinics, hiring season)
- [ ] What they use today
Minimum for a next step: pain in her words + who signs.

## Red flags
- Their HR system already does onboarding; they're just comparing features.
- Hiring freeze despite the open roles.
- No owner: "each clinic manager decides".

## Open and close
- Open: "I'd like most of our 30 minutes on how onboarding works today, then we decide together if a demo is worth it. Still have the full 30?"
- If qualified: a 45-minute demo with Rosa and one clinic manager next week.
- If not: send a checklist template; check in after their next hiring round.
```

## Checks before you send

- [ ] Every hypothesis cites a fact from the research.
- [ ] 8 questions, ranked, all open-ended, first 5 marked must-ask.
- [ ] The qualify list is yes/no items you can tick after the call.
- [ ] No fact about the prospect is invented; unknowns are marked "[assumption]".
- [ ] It fits on one page, under 350 words.

## Common mistakes

- 20 questions and no ranking. You'll run out of time before the important ones.
- Asking what the website already answers ("So what does Northwind do?").
- Hypotheses about your product's features instead of the buyer's problem.
