---
name: case-study-writer
description: Writes a customer case study from interview notes or a call transcript - situation, problem, why they chose you, what changed with numbers, and a customer quote - and lists every item the customer must approve before it's published. Use when someone shares customer interview notes, a success story, or a testimonial call and asks for a case study, customer story, success story, or reference write-up.
---

# Customer case study

A case study sells when a prospect sees their own situation in it and a number they can believe. Write it from the customer's side, in their words, and never publish a claim the customer hasn't approved. In the US, the FTC's Endorsement Guides treat a customer quote as an endorsement: it "must reflect the honest opinion of the endorser", and if their result isn't what customers generally get, the page must say what is typical.

## When to use

- After a customer interview or success call, to turn notes into a publishable story.
- When sales needs proof for a specific segment or objection.
- When a happy customer email or review deserves a fuller story.
- Not for an anonymous stats roundup across many customers: that's a report, not a case study.

## What you need

- Interview notes or a transcript with the customer. Without one, ask for it; a case study from internal notes alone reads as an ad.
- The customer's name, role, company, size, and industry. Missing ones become "[confirm: ...]".
- Before and after numbers (time, cost, revenue, errors). If none exist, ask once; then write the change in concrete non-numeric terms and flag "no metric" in the approval list.
- Optional: the segment or objection this story should answer.

## Steps

1. **Find the before state in their words.** What they did before, what it cost them, and the moment they decided to change. Quote their phrasing; "we were drowning in spreadsheets" beats "they faced inefficiencies".
2. **Name why them, why you.** What else they considered (including doing nothing) and the 1 to 2 reasons they picked you. A prospect comparing options needs this section most.
3. **Pull the numbers.** Every before/after metric with its period: "from 6 hours a week to 40 minutes, over 3 months". If a number came from your team, not the customer, mark it for approval. Never round up, never extrapolate a year from a month. If this customer did unusually well, add a line on what results are typical or flag it "[check: typical results]" (FTC Endorsement Guides).
4. **Pick 1 to 2 quotes.** Quotes that state a result or a feeling, not a feature list. Light edits for grammar are fine if the meaning stays; mark edited quotes for approval. Don't invent or merge quotes: an endorsement can't misrepresent the endorser's experience.
5. **Write the headline from the result.** "[Customer] cut [X] by [number]" or "How [customer] [result]". If there's no number, use the concrete change.
6. **Structure for skimmers.** Result first (NN/g's inverted pyramid): a 3-line summary box (customer, challenge, result) on top, then sections: situation, problem, why [company], what changed, what's next. Our default: 400 to 700 words when the interview gives that much; if the notes are thin, write it shorter rather than pad it. Product features appear only where they caused a result.
7. **List approval items.** Every quote, number, the customer's name and logo, any competitor named, and anything that could be confidential (revenue, headcount, tools). If the customer got anything for taking part (a discount, credit, a free month) or knew they might, the page discloses it (FTC Endorsement Guides). The customer signs off on all of it before publishing.

## Output format

```markdown
# [Headline with the result]

| Customer | [Company, industry, size] |
|---|---|
| Challenge | [one line] |
| Result | [one line with the number] |

## The situation
[2–3 short paragraphs]

## The problem
[what it cost them, in their words]

## Why [company]
[alternatives considered, 1–2 reasons]

## What changed
- [metric: before → after, period]

> "[Quote]" — [Name, role, company]

## What's next
[1 short paragraph]

---
## For approval by [customer contact] before publishing
- [ ] Quote: "[...]" [edited / verbatim]
- [ ] Number: [...] — [source: customer / our data]
- [ ] Name, role, and logo use
- [ ] Anything given for taking part: [none / what, disclosed on the page]
- [ ] [Confidential or competitor items]
```

## Example

**Input:** Interview with Tomás Reyes, operations lead at Greenline Couriers (60 drivers, regional delivery). Before: dispatch done on a whiteboard and group chat, "every morning was chaos, 2 hours just assigning routes". Tried a big fleet suite, too complex. Picked Routelyn for the phone app drivers already understood. After 2 months: route assignment takes 20 minutes; missed deliveries down from about 30 a week to 8 (from Routelyn's dashboard). Quote: "My drivers stopped calling me at 7 a.m."

**Output:**

```markdown
# Greenline Couriers cut morning dispatch from 2 hours to 20 minutes

| Customer | Greenline Couriers, regional delivery, 60 drivers |
|---|---|
| Challenge | Routes assigned by hand on a whiteboard and group chat |
| Result | Dispatch takes 20 minutes; missed deliveries fell from about 30 to 8 a week |

## The situation
Greenline Couriers runs 60 drivers across the region. Before Routelyn, every route was planned on a whiteboard and sent out in a group chat.

## The problem
"Every morning was chaos," says Tomás Reyes, operations lead. Assigning routes alone took 2 hours.

## Why Routelyn
Greenline first tried a full fleet management suite and found it too complex. It chose Routelyn because its drivers already understood the phone app.

## What changed
- Route assignment: 2 hours → 20 minutes a morning, after 2 months
- Missed deliveries: about 30 → 8 a week, after 2 months

> "My drivers stopped calling me at 7 a.m." — Tomás Reyes, Operations Lead, Greenline Couriers

## What's next
[confirm: Greenline's plans, not covered in the interview]

---
## For approval by Tomás Reyes before publishing
- [ ] Quote: "Every morning was chaos" (verbatim)
- [ ] Quote: "My drivers stopped calling me at 7 a.m." (verbatim)
- [ ] Number: 2 hours → 20 minutes — source: customer
- [ ] Number: about 30 → 8 missed deliveries a week — source: Routelyn dashboard
- [ ] Name, role, and logo use
- [ ] Anything given for taking part: none stated in the interview [confirm: none]
- [ ] Mention that a fleet suite was tried first (unnamed)
- [ ] [check: typical results] — are these results typical for Routelyn customers?
```

## Checks before you send

- [ ] The headline states the result, with a number if one exists.
- [ ] Every metric has a before, an after, and a period.
- [ ] Every quote appears in the notes; edited ones are marked.
- [ ] The approval list covers every quote, number, name, and logo.
- [ ] Nothing in the story is missing from the input; gaps are "[confirm: ...]".
- [ ] An unusually good result says what is typical, or is flagged "[check: typical results]".

## Common mistakes

- Writing it as a feature tour. Features appear only where they caused a result.
- Skipping "why us". Prospects comparing vendors read that section first.
- Publishing a number from your own dashboard without the customer's sign-off.
