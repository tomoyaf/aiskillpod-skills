---
name: swot-tows-analysis
description: Runs a SWOT analysis that ends in decisions - external opportunities and threats first, then strengths and weaknesses measured against named competitors, each item with evidence - and turns the strongest pairs into a TOWS matrix (SO, WO, ST, WT strategies, also called cross SWOT) with an owner, a first step, and a date for each chosen strategy. Use when someone asks for a SWOT analysis, a SWOT template, a TOWS matrix, cross SWOT, "strengths and weaknesses for our plan", or a situation analysis before a strategy, planning, or board meeting.
---

# SWOT and TOWS analysis

SWOT lists a company's internal Strengths and Weaknesses and the external Opportunities and Threats it faces. Used alone it often ends as four lists nobody acts on. The TOWS matrix fixes that: Heinz Weihrich, in "The TOWS Matrix: A Tool for Situational Analysis" (Long Range Planning, 1982), paired the internal and external items to produce four kinds of strategy: SO (use strengths to take opportunities), WO (overcome weaknesses to take opportunities), ST (use strengths to meet threats), and WT (reduce weaknesses and avoid threats). In Japan this pairing is widely called cross SWOT. SWOT's own origin is contested. It is often credited to work at the Stanford Research Institute in the 1960s, with Albert Humphrey's name attached; Harvard's Business Policy textbook (Learned, Christensen, Andrews and Guth, 1965) is also cited; a 2023 archival study by Puyt, Lie and Wilderom credits Robert F. Stewart's SOFT approach at SRI. This skill requires evidence for every item and ends with chosen strategies that have owners.

## When to use

- Before a planning cycle, offsite, or board meeting, to agree on the situation and pick a few moves.
- When a team has a SWOT already and nothing came of it.
- When a new market change (a regulation, a new competitor, a technology) needs a structured response.
- Not for testing which resources give a lasting advantage (use vrio-analysis). Not for judging the profitability of the whole industry (use five-forces-analysis). Not for choosing among growth directions such as new markets or new products (use ansoff-growth-options).

## What you need

- The unit being analyzed (company, product, team), the decision it feeds, and the time horizon (for example, next 12 months).
- 2 to 5 named competitors or alternatives, to judge strengths and weaknesses against.
- Facts for each item: numbers, customer quotes, win/loss notes, market reports with their source. If the user gives only opinions, keep them and mark "[check: evidence]".
- Who can own actions. If unknown, write "[owner: to confirm]".
- Never invent market data, competitor facts, or numbers.

## Steps

1. **Frame the analysis.** One line: the unit, the decision, the horizon, the competitors. Without a decision, a SWOT has no way to rank anything.
2. **List opportunities and threats first.** Weihrich's process starts with the external environment. Opportunities and threats are outside the company's control: customer demand, competitors' moves, technology, regulation, the economy. Each item gets its evidence and source. Write the condition, not the move: "studios outside Japan are asking for Japanese releases" is an opportunity; "launch a Japanese service" is a strategy and belongs later.
3. **List strengths and weaknesses against the competitors.** Internal items only: what the company has or does, compared with the named rivals. "Experienced team" is not a strength unless rivals' teams are weaker; say how. Each item gets evidence. Keep internal and external apart: a strength filed as an opportunity breaks the pairing.
4. **Cut to what matters.** Keep at most 5 items per quadrant, ranked by effect on the decision. Number them (S1, W1, O1, T1). Move items with no evidence to "To check" rather than keeping them silently.
5. **Pair items into TOWS strategies.** For each quadrant, write 1 to 3 strategies, each naming the items it combines:
   - **SO:** use S to take O.
   - **WO:** fix or work around W to take O (build, hire, partner, buy).
   - **ST:** use S to reduce T. Weihrich warns that meeting a threat head-on from strength can backfire; choose the response with care.
   - **WT:** defensive moves where weakness meets threat: shrink exposure, exit, partner, or fix.
6. **Choose.** Pick 3 to 5 strategies to act on, and say why these and not the others: size of the effect, cost, time, and fit with the decision. Name what is explicitly not being done.
7. **Make each chosen strategy actionable.** Owner, first step, date, and the measure that will show whether it works.
8. **Set the review.** External items change. Weihrich suggested drawing the matrix again at later points in time; set a date or trigger for the next one, and list which items are most likely to move.

## Output format

```markdown
# SWOT and TOWS: [unit]
**Decision:** [decision] · **Horizon:** [period] · **Compared with:** [competitors] · **Date:** [date]

## External
| # | Opportunity | Evidence (source) |
|---|---|---|
| O1 | [condition outside our control] | [fact, source] |

| # | Threat | Evidence (source) |
|---|---|---|
| T1 | [condition] | [fact, source] |

## Internal (against [competitors])
| # | Strength | Evidence |
|---|---|---|
| S1 | [item] | [fact] |

| # | Weakness | Evidence |
|---|---|---|
| W1 | [item] | [fact] |

## TOWS matrix
| | Opportunities (O1–On) | Threats (T1–Tn) |
|---|---|---|
| **Strengths** | **SO:** [strategy] (S1×O2) | **ST:** [strategy] (S2×T1) |
| **Weaknesses** | **WO:** [strategy] (W1×O1) | **WT:** [strategy] (W2×T1) |

## Chosen strategies
| Strategy | Pair | Owner | First step | By | Measure |
|---|---|---|---|---|---|

**Not doing now:** [strategies set aside, and why]

## To check
- [check: ...] — who can answer: [name]

**Next review:** [date or trigger]
```

## Example

**Input:** "SWOT for Hikari Translation, 12 people, Japanese-English game translation. Decide next year's focus. Competitors: two bigger localization agencies (Locabridge, Nami Global) and freelancers. Facts: our 8 translators have credits on 40 released games; two studio clients are 60% of revenue; we don't offer linguistic QA (testing the translated game), and three clients asked for it this year; Locabridge and Nami do offer it. Studios increasingly run machine translation and pay us only to post-edit, at about half our full rate; that was 30% of our jobs this year vs 10% last year. A Tokyo studio association told members that overseas sales are a priority [check: source document]. We're good at keeping tone and jokes; clients say so in reviews."

**Output:**

```markdown
# SWOT and TOWS: Hikari Translation
**Decision:** next year's focus · **Horizon:** next 12 months · **Compared with:** Locabridge, Nami Global, freelancers · **Date:** [date]

## External
| # | Opportunity | Evidence (source) |
|---|---|---|
| O1 | Studios are asking for linguistic QA from their translation vendor | Three clients asked this year (Hikari's records) |
| O2 | Japanese studios are prioritizing overseas sales | Studio association statement [check: source document] |

| # | Threat | Evidence (source) |
|---|---|---|
| T1 | Studios shift work to machine translation plus post-editing at about half the rate | 30% of jobs this year vs 10% last year (Hikari's records) |
| T2 | Larger agencies offer translation and QA as one package | Locabridge and Nami Global offer QA (user) |

## Internal (against Locabridge, Nami Global, freelancers)
| # | Strength | Evidence |
|---|---|---|
| S1 | Game-specific translators with a track record | Credits on 40 released games |
| S2 | Tone and humor that clients notice | Client reviews mention it [check: how many] |

| # | Weakness | Evidence |
|---|---|---|
| W1 | No linguistic QA service | Both larger agencies offer it; three clients asked |
| W2 | Revenue depends on two clients | 60% of revenue |

## TOWS matrix
| | Opportunities (O1–O2) | Threats (T1–T2) |
|---|---|---|
| **Strengths** | **SO:** pitch overseas-bound studios on story-heavy games where tone matters most (S1, S2×O2) | **ST:** price full translation for dialogue- and humor-heavy titles, where machine output needs most rework; accept post-editing only on menus and system text (S2×T1) |
| **Weaknesses** | **WO:** add linguistic QA, first by partnering with a testing studio, then in-house if demand holds (W1×O1) | **WT:** win new clients in QA and story-heavy work so no client exceeds a set share of revenue (W2×T1, T2) |

## Chosen strategies
| Strategy | Pair | Owner | First step | By | Measure |
|---|---|---|---|---|---|
| Add linguistic QA through a partner | W1×O1 | [owner: to confirm] | Shortlist 3 testing studios and price a pilot with one of the three clients who asked | [date] | Pilot signed; QA revenue next quarter |
| Full-rate offer for story-heavy titles | S2×T1 | [owner: to confirm] | Write a one-page comparison of machine output vs Hikari on a past title's dialogue [check: client permission] | [date] | Share of jobs at full rate |
| Reduce dependence on two clients | W2×T1, T2 | [owner: to confirm] | List 20 overseas-bound studios with story-heavy games | [date] | Largest client's share of revenue |

**Not doing now:** the broad overseas pitch (SO) until the association claim is checked and the QA pilot shows demand.

## To check
- [check: source document for the studio association statement] — who can answer: [name]
- [check: how many client reviews mention tone and humor] — who can answer: [name]

**Next review:** in 6 months, or sooner if post-editing passes 40% of jobs.
```

## Checks before you send

- [ ] Every item has evidence with a source, or sits under "To check".
- [ ] Opportunities and threats are conditions outside the company, not moves; strengths and weaknesses are internal and compared with named rivals.
- [ ] No quadrant has more than 5 items, and each is numbered.
- [ ] Every TOWS strategy names the pair (for example S1×O2) it comes from.
- [ ] 3 to 5 strategies are chosen, each with owner, first step, date, and measure, and what is not being done is stated.
- [ ] No market data or competitor facts were invented.

## Common mistakes

- Stopping at four lists. A SWOT without the TOWS step and chosen strategies changes nothing.
- Writing strategies as opportunities ("expand to Europe"). The opportunity is the condition; the expansion is a strategy.
- Strengths that every competitor also has. Compare against named rivals or drop the item.
- Long lists. Twenty items per quadrant hide the five that matter.
- Treating the matrix as fixed. External items move; redraw it on a schedule.
