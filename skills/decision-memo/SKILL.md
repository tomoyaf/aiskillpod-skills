---
name: decision-memo
description: Writes a short decision memo in the Amazon narrative style - the recommendation first, then context, 2 to 4 options with trade-offs, risks and mitigations, and the ask with a decider and a deadline - in full sentences, not bullet slides. Use when someone needs a decision from a founder, exec, or team and asks for a decision memo, a one-pager, a proposal, a recommendation doc, a narrative instead of slides, or "help me make the case for X".
---

# Decision memo

A decision memo gets a decision, not a discussion. Amazon doesn't use slide presentations: it writes narratively structured six-page memos, read silently at the start of the meeting (Bezos, 2017 shareholder letter). Our view is that full sentences expose fuzzy thinking that bullets hide. Ours is short (1 to 2 pages), puts the recommendation in the first paragraph, and ends with a named decider and a date.

## When to use

- A choice needs someone else's approval: a hire, a vendor, a price change, a reorg, a build-or-buy.
- A meeting keeps ending without a decision.
- Replacing a slide deck for a leadership review.
- Not for recording a decision already made (use decision-record), and not for a long strategy document.

## What you need

- The decision to be made, stated as a question.
- Who decides, and by when. If unknown, ask once; otherwise write "[decider: to confirm]".
- The options considered, and the facts for each: cost, time, effect. Never invent numbers; mark gaps "[check: ...]".
- Your recommendation. If the writer has none, draft the memo neutrally and say "no recommendation yet" in the first paragraph.

## Steps

1. **Write the question and the ask first.** One paragraph: the decision needed, the recommendation, the decider, the deadline, and the cost of not deciding by then. A reader who stops here can still act.
2. **Give only the context needed.** 1 to 2 paragraphs: what changed, why now, what we know (with numbers and their sources). Cut history the decider already knows.
3. **Lay out 2 to 4 real options.** Include "do nothing" when it's viable. For each: what it is, cost, time, what it gets us, what it gives up. Use a comparison table for the numbers, sentences for the reasoning.
4. **Make the trade-off explicit.** One paragraph on why the recommended option wins, naming what we give up by choosing it. If the choice is reversible, say so: Bezos's 2016 letter calls these "two-way doors" that can use a light-weight process.
5. **Name the risks.** Top 2 to 3 risks of the recommendation, each with a mitigation and an early warning sign.
6. **Close with the ask.** Exactly what you need: approve option B, a budget, a person. The decider, the deadline, and the first step after a yes.
7. **Write in sentences and cut.** Prose, not slide bullets, except the options table. Aim for under 2 pages. Remove adjectives that replace data ("significant", "massive").

## Output format

```markdown
# [Decision as a question]
**Decider:** [name] · **Decision needed by:** [date] · **Author:** [name] · **Date:** [date]

## Recommendation
[One paragraph: we recommend X because Y. If we don't decide by [date], [consequence].]

## Context
[1–2 paragraphs: what changed, why now, key facts with sources]

## Options
| | A: [name] | B: [name] | C: Do nothing |
|---|---|---|---|
| Cost | | | |
| Time | | | |
| Gets us | | | |
| Gives up | | | |

[A paragraph per option on the reasoning.]

## Why [recommended option]
[The trade-off in plain sentences, including what we give up. Reversible or not.]

## Risks
| Risk | Mitigation | Early warning sign |
|---|---|---|

## The ask
[Approve X / budget / person] by [date]. If yes, the first step is [action] by [owner] on [date].
```

## Example

**Input:** "Today is Tuesday 10 Nov 2026. Need CEO (Hana) to decide by Friday whether we move support from email to Zendesk. Email via shared Gmail, 2 support reps, ~600 tickets/month, we lose track of ~5% (customers chase us). Zendesk Suite quote: $[check] per agent. Alternative: Help Scout, cheaper, fewer features. Or stay. I want Help Scout — we don't need Zendesk's complexity. Migration ~2 weeks either way. January renewals are our peak. — Leo"

**Output:**

```markdown
# Should we move customer support from shared Gmail to a help desk tool?
**Decider:** Hana · **Decision needed by:** Friday 13 Nov · **Author:** Leo · **Date:** 10 Nov

## Recommendation
We recommend moving support to Help Scout. It fixes the lost-ticket problem at a lower cost and setup effort than Zendesk, which offers features we won't use at our size. If we decide by Friday, the move finishes before the January renewal peak; a later start runs into it.

## Context
Two support reps handle about 600 tickets a month in a shared Gmail inbox. About 5% of tickets (around 30 a month) get lost and are found only when a customer chases us. There's no way to see who owns a ticket or how long customers wait. Both tools would take about 2 weeks to migrate.

## Options
| | A: Help Scout | B: Zendesk Suite | C: Stay on Gmail |
|---|---|---|---|
| Cost | [check: quote] | [check: quote] per agent | $0 extra |
| Time | ~2 weeks | ~2 weeks | none |
| Gets us | Ownership, statuses, reporting [check: plan features] | Same, plus advanced routing and a bigger app ecosystem [check: plan features] | Nothing new |
| Gives up | Advanced routing we don't need yet | More setup and admin time | ~30 lost tickets a month continue |

Help Scout covers the 3 things we lack: assignment, status, and reporting. Zendesk adds routing and automation built for larger teams. Staying costs nothing in software but keeps losing about one ticket a day.

## Why Help Scout
We trade Zendesk's headroom for a simpler tool the 2 reps can run without an admin. The decision is reversible: if we outgrow Help Scout, the ticket history can be exported [check: export terms].

## Risks
| Risk | Mitigation | Early warning sign |
|---|---|---|
| Tickets lost during migration | Run both inboxes in parallel for 1 week | Customers replying to old threads |
| Reps resist the new tool | Reps choose the ticket statuses | Tickets still answered from Gmail after week 2 |

## The ask
Approve Help Scout and its annual cost [check: quote] by Friday 13 Nov. If yes, Leo starts the trial setup on Monday 16 Nov.
```

## Checks before you send

- [ ] The recommendation, decider, and deadline are in the first paragraph.
- [ ] There are 2 to 4 options, each with what it gives up, and "do nothing" if it's viable.
- [ ] Every number has a source in the input or is marked "[check: ...]".
- [ ] The memo says whether the decision is reversible.
- [ ] It ends with one specific ask and the first step after a yes.
- [ ] It fits in 2 pages.

## Common mistakes

- Building suspense: context for a page, recommendation at the end. Lead with it.
- A straw-man option list where only one choice is plausible. Deciders notice, and trust drops.
- Hiding the downside of the recommendation. Name what we give up; it's what the decider will ask about.
