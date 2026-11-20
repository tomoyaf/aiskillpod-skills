---
name: feedback-themes
description: Analyzes NPS comments, survey answers, app store reviews, or other open-text customer feedback into themes with counts, representative quotes, sentiment, and suggested actions, and computes NPS when scores are given. Use when someone shares survey results, NPS responses, reviews, or a feedback export and asks "what are customers saying", for themes, a voice-of-customer summary, or what to fix first.
---

# Feedback themes

A theme analysis tells a team what customers say most, how strongly, and what to do about it. Read every comment, code it, count it, and quote it: counts without quotes feel abstract, and quotes without counts let the loudest comment win.

## When to use

- An NPS or CSAT survey closed and you have the comments.
- You exported app store, G2, or marketplace reviews.
- Before roadmap planning, to bring the customer's words into the room.
- Not for one-on-one interview transcripts: use user-interview-synthesis. Not for turning tickets into an FAQ: use faq-from-tickets.

## What you need

- The comments, one per row. Scores (0 to 10 for NPS) and segments (plan, region, tenure) help.
- The time period and how the survey was sent, for the header.
- If there are fewer than 30 comments, still do it, but say counts are small and avoid percentages.

## Steps

1. **Compute the score if given.** NPS = % promoters (9 to 10) minus % detractors (0 to 6); passives (7 to 8) count in the total only. Report it as a number from -100 to 100, with the response count. Our default: under 30 responses, say the sample is small.
2. **Read everything once, then code.** Give each comment 1 to 3 codes: short labels for what it's about ("slow load", "price", "support helpful"). One comment can carry a positive and a negative code.
3. **Group codes into 5 to 10 themes.** A theme is a specific topic a team can act on ("Reports load slowly"), not a category ("Performance"). Merge themes with fewer than 3 mentions into "Other" unless they concern data loss, security, or billing errors.
4. **Count and tag sentiment.** For each theme: number of comments, share of all comments, and sentiment (positive, negative, mixed). If scores exist, show how many mentions came from detractors vs promoters.
5. **Pick 2 quotes per theme.** Choose quotes that are typical, not the most extreme. Quote exactly; trim with "…" but never change words. Remove names and emails.
6. **Suggest an action per negative theme.** One concrete next step and who would own it (team, not person, is fine here). If a theme needs more data before action, say what data.
7. **Write the headline.** 3 bullets: the biggest negative theme, the biggest positive theme, and anything new or rising vs last period if a prior period was given.

## Output format

```markdown
# Feedback themes — [source], [period]

**Responses:** [N] · **NPS:** [score] ([promoters]% promoters, [passives]% passives, [detractors]% detractors) [or "no scores given"]

## Headline
- [Biggest negative theme, with count]
- [Biggest positive theme, with count]
- [New or rising, or "no prior period given"]

## Themes
| Theme | Mentions | Share | Sentiment | From detractors / promoters |
|---|---|---|---|---|
| [Theme] | [n] | [%] | [+/–/mixed] | [n / n] |

### [Theme]
- "[Quote]"
- "[Quote]"
**Suggested action:** [step] — [owner team]

## Other ([n] comments)
- [One-line summary of small topics]

## Notes on the data
- [Sample size, segments missing, how comments were coded]
```

## Example

**Input (8 of 112 responses, excerpt):**

> 3 — "Exports take forever, I gave up on the weekly report"
> 9 — "Support team is great, Ana fixed my issue in minutes"
> 5 — "Price went up and nothing changed"
> 10 — "Love the templates"
> 2 — "Export timed out again"
> 8 — "Good but the mobile app is clunky"
> 6 — "too expensive for a team our size"
> 9 — "Support is fast"

**Output (excerpt):**

```markdown
# Feedback themes — NPS survey, Q3

**Responses:** 112 · **NPS:** 14 (41% promoters, 32% passives, 27% detractors)

## Headline
- Slow or failing exports: 23 mentions, almost all detractors.
- Fast, friendly support: 31 mentions, the top reason promoters give.
- No prior period given, so no trend.

## Themes
| Theme | Mentions | Share | Sentiment | From detractors / promoters |
|---|---|---|---|---|
| Support is fast and helpful | 31 | 28% | + | 2 / 24 |
| Exports slow or time out | 23 | 21% | – | 19 / 1 |
| Price too high for value | 17 | 15% | – | 12 / 0 |

### Exports slow or time out
- "Exports take forever, I gave up on the weekly report"
- "Export timed out again"
**Suggested action:** Measure export times for large accounts and fix timeouts first — engineering

## Notes on the data
- Support quotes name an agent; names removed in the shared version.
```

## Checks before you send

- [ ] NPS, if shown, uses 9–10 minus 0–6 and states the response count.
- [ ] Every theme has a count, and counts are from actual coded comments.
- [ ] Quotes are exact and typical, with names and emails removed.
- [ ] Themes are specific enough that a team knows what to fix.
- [ ] Each negative theme has one suggested action.
- [ ] Small samples are labelled; no percentages from fewer than 30 comments.

## Common mistakes

- Themes like "UX" or "Product". Say what about it.
- Quoting the angriest comment as typical.
- Counting a long comment with 4 complaints as one theme. Code each point.
