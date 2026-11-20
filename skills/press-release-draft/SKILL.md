---
name: press-release-draft
description: Drafts a news release with a headline, dateline, a lead paragraph that answers who, what, when and why, one quote, boilerplate, and a media contact, and flags when the announcement isn't news. Use when someone asks for a press release, news release, media announcement, or "something we can send to journalists" about a launch, funding round, partnership, hire, or milestone.
---

# Press release draft

A good release lets a reporter write a 3-sentence story from the first paragraph alone. Lead with the fact, not the adjectives; if the fact isn't news to an outsider, say so before writing anything.

## When to use

- A launch, funding round, partnership, key hire, acquisition, or public milestone that people outside the company could care about.
- When a founder wants "a press release" and you need to check first whether it should be one.
- Not for a product changelog, a blog post, or a customer email: those don't need a dateline or boilerplate.

## What you need

- The news in one sentence: who did what, and when.
- Why it matters to someone outside the company (a customer, an industry, a city). If missing, ask once; if still missing, flag it as the release's weakest point.
- A quote source: name and title. If no quote was given, draft one and mark it "[draft quote: needs approval from name]".
- Company boilerplate and a media contact. If missing, write "[boilerplate: to confirm]" and "[contact: to confirm]".
- Embargo date or release date, and city for the dateline.

## Steps

1. **Run the news test (our default).** It's news if at least one is true: it's new (first, only, largest in a named group), it has a number an outsider can check, it affects a named group of people, or a known name is involved. If none is true, stop and say "This isn't news yet" with 2 options: a blog post, or what would make it news (a customer number, a partner, a date).
2. **Write the headline.** 100 characters or fewer (PR Newswire's guidance), factual, active verb, present tense, subject first, one concrete fact: "Northbeam raises 8 million to ..." not "Northbeam announces exciting funding". No exclamation marks, no "announces" unless nothing else fits.
3. **Write the dateline and lead.** The dateline opens the first paragraph: CITY in caps, date, then a dash. The lead is 1 to 2 sentences, about 25 to 30 words, answering who, what, when, where, and why, so a reader who stops there has the story. Details go in paragraph 2.
4. **Add 1 to 2 supporting paragraphs.** Numbers, the customer problem, availability and price if a product. Every claim checkable; mark anything not in the input "[check: source]".
5. **Write one quote.** Quotes carry opinion and context; facts and numbers belong in the body. The quote gives a reason, a belief, or a stake a reporter can't paraphrase from the facts. Cut quotes that restate the headline ("We're thrilled to announce").
6. **Close with boilerplate and contact.** Boilerplate is the standard "About" paragraph, the same in every release: what the company does, for whom, where, and the website. Our default length: 2 to 3 sentences. Close the release with "###".
7. **Flag the risks.** List claims that need approval (superlatives, customer names, numbers, partner quotes) before it goes out.

## Output format

```markdown
**News check:** [News / Weak news / Not news] — [one-line reason]

FOR IMMEDIATE RELEASE [or: EMBARGOED UNTIL date, time, timezone]

# [Headline, 100 characters or fewer]
## [Optional subhead: one supporting fact]

**[CITY], [Month Day, Year]** — [Lead: who, what, when, where, why, about 25 to 30 words.]

[Paragraph 2: how, where, numbers, availability.]

[Paragraph 3: context or customer evidence.]

"[Quote with a reason or stake]," said [Name], [title] at [Company].

**About [Company]**
[2–3 sentence boilerplate]

**Media contact**
[Name], [email], [phone]

###

**Needs approval before sending**
- [Claim, quote, or name] — [who approves]
```

## Example

**Input:** "We're Larkspur Labs, scheduling software for dental clinics. We just signed our 500th clinic and launched a no-show predictor. Write a press release. Founder is Dana Okafor. We're in Leeds."

**Output:**

```markdown
**News check:** Weak news — "500th clinic" is a milestone only you care about; the no-show predictor is the news. Lead with it.

FOR IMMEDIATE RELEASE

# Larkspur Labs predicts dental no-shows before they happen
## The scheduling tool used by 500 clinics now flags likely missed appointments in advance

**LEEDS, [Month Day, Year]** — Larkspur Labs today launched a no-show predictor that flags dental appointments likely to be missed, giving clinics 48 hours [check: lead time, not in input] to refill the slot. It is available now to all Larkspur customers [check: availability].

The predictor scores each booking using the patient's past attendance and booking lead time [check: inputs used]. Clinics see flagged appointments on their daily schedule and can send a reminder or offer the slot to a waitlist [check: what clinics can do with a flag]. Larkspur is used by 500 clinics across the UK [check: all UK].

[Paragraph 3: one clinic's result, e.g. no-show rate before and after — check: needs a customer and a number.]

"An empty chair costs a clinic the same whether the patient forgot or never meant to come," said Dana Okafor, founder of Larkspur Labs. "We'd rather clinics know the day before than find out at 9 a.m." [draft quote: needs approval from Dana Okafor]

**About Larkspur Labs**
Larkspur Labs makes scheduling software for dental clinics. Founded in [check: year] and based in Leeds, it is used by 500 clinics.

**Media contact**
[contact: to confirm]

###

**Needs approval before sending**
- "48 hours ahead", the inputs the model uses, availability, and what clinics can do with a flag — product lead
- The 500-clinic figure as of release date — Dana Okafor
- The quote — Dana Okafor
```

## Checks before you send

- [ ] The lead paragraph alone answers who, what, when, where, and why, in about 30 words.
- [ ] The headline is 100 characters or fewer, has one concrete fact, and no "exciting", "innovative", or "leading".
- [ ] Every number and superlative is in the input or marked "[check: ...]".
- [ ] The quote gives a reason or stake, not a restatement of the headline.
- [ ] Boilerplate, contact, and dateline are present or marked to confirm.
- [ ] The news check result is stated at the top.

## Common mistakes

- Burying the news in paragraph 3 behind company history.
- Writing "the leading platform" with no source. Reporters delete it, and it can be a false claim.
- Quoting 3 executives. One quote, two at most when a partner is involved.
