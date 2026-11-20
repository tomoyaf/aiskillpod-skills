---
name: win-loss-analysis
description: Analyses notes or interview transcripts from won and lost deals into the real reasons buyers chose or rejected you, the patterns across deals, and specific changes to make in product, pricing, messaging, or sales process. Use when someone shares closed-won or closed-lost notes, win-loss interviews, or CRM loss reasons and asks why we win, why we lose, a win/loss review, or what to change.
---

# Win-loss analysis

A win-loss analysis is worth doing only if it changes something. Find the reason the buyer gives in their own words, not the reason the rep logged, count how often it shows up, and end with changes that have an owner. Clozd, a win-loss vendor, reports that reps are wrong about why they win or lose more often than not, and that CRM loss reasons often say "price" when the real blocker was risk or indecision.

## When to use

- At the end of a quarter, over closed deals from the last 2 to 8 weeks; Clozd's playbook reaches buyers 2 to 6 weeks after the decision, while memory is fresh.
- After a run of losses to the same competitor or in the same segment.
- When you have buyer interviews and need them turned into decisions.
- Not for reviewing one open deal: use deal-review.

## What you need

- Notes or transcripts per deal: outcome (won or lost), size, segment, competitor if any, and what the buyer said.
- Who the source is for each note: buyer interview, rep's notes, or CRM field. Buyer words outweigh rep notes.
- Larger samples hold up better (Clozd's playbook targets 30 to 60 won and lost deals). If fewer than 5 deals are given, say the patterns are weak and proceed anyway, marking each one "[small sample]".
- Optional: the decisions the team is weighing, so the changes speak to them.

## Steps

1. **Tag each deal with its source.** Buyer interview, rep notes, or CRM reason. Weight buyer interviews highest: CRM reasons and rep debriefs carry recall bias and see only part of the buying committee. If the rep note and buyer words disagree, use the buyer's and note the gap: that gap is itself a finding.
2. **Find the primary reason per deal.** One reason per deal, the one that decided it. Write it as the buyer would: "Couldn't get IT to approve SSO in time", not "Security". Add up to 2 secondary reasons.
3. **Dig under price and "no decision".** If a loss says "price" or "budget", look for what else was said: value not proven, risk, wrong buyer, competitor bundled it, timing. Keep "price" only if the buyer compared a number and said yours was higher for the same thing. Count "no decision" (they bought nothing) as its own outcome, not as a loss to a competitor.
4. **Group reasons into themes.** Count deals per theme, separately for wins and losses. Our default: a theme needs at least 2 deals; single cases go under "One-offs worth watching".
5. **Cut by segment and competitor.** Check whether a theme clusters in one deal size, industry, or competitor. A pattern that's 4 of 5 losses to one competitor is a battlecard problem, not a product problem.
6. **Write changes, not observations.** Each change is verb-first, names the area (product, pricing, messaging, sales process, targeting), an owner role, a due date if known, and the evidence count behind it. Max 5 changes (our default), ranked by deals affected.
7. **Pull 3 to 5 buyer quotes.** Exact words, attributed by role and company type, not by name, so they can be shared internally.

## Output format

```markdown
# Win-loss analysis: [period or scope]

**Deals reviewed:** [n won] won, [n lost] lost. Sources: [n] buyer interviews, [n] rep notes, [n] CRM only.
**Headline:** [One sentence: the single biggest reason we win or lose.]

## Why we win
| Theme | Deals | Example in the buyer's words |
|---|---|---|
| [theme] | [n of won] | "[quote]" |

## Why we lose
| Theme | Deals | Example in the buyer's words |
|---|---|---|
| [theme] | [n of lost] | "[quote]" |

## Patterns by segment or competitor
- [Pattern with counts]

## Rep notes vs buyer words
- [Where they disagree, with count]

## Changes to make
| # | Change | Area | Owner | Evidence |
|---|---|---|---|---|
| 1 | [verb-first change] | [area] | [role] | [n deals] |

## One-offs worth watching
- [Single-deal reason]

## Quotes to share
- "[quote]" — [role, company type, won/lost]
```

## Example

**Input (summarized):** 9 deals, Q3. Sources: buyer interviews on 2 losses, rep notes on the other 7. Won 4: rep notes quote three buyers saying onboarding "took a day, not a month"; one won on price vs a spreadsheet. Lost 5: CRM says "price" on 3. The 2 interviews were on those: "We couldn't show our CFO the savings" and "Vendor X included it with our payroll tool". Two other losses: "No SSO, IT blocked it" (both over 200 seats). Who said what: the "took a day" buyer is an ops manager at a 40-person agency; the CFO quote is from an office manager at a 90-person firm.

**Output:**

```markdown
# Win-loss analysis: Q3

**Deals reviewed:** 4 won, 5 lost. Sources: 2 buyer interviews, 7 rep notes. [small sample]
**Headline:** We win on fast onboarding and lose large accounts on SSO; "price" losses are mostly a missing savings case.

## Why we win
| Theme | Deals | Example in the buyer's words |
|---|---|---|
| Fast onboarding | 3 of 4 | "Took a day, not a month." |

## Why we lose
| Theme | Deals | Example in the buyer's words |
|---|---|---|
| Logged as "price" | 3 of 5 | Interviews found other reasons on 2: "We couldn't show our CFO the savings."; "Vendor X included it with our payroll tool." 1 not interviewed. |
| No SSO | 2 of 5 | "No SSO, IT blocked it." |

## Patterns by segment or competitor
- Both SSO losses were accounts over 200 seats. [check: seat counts of the other 7 deals]

## Rep notes vs buyer words
- CRM logged "price" on 3 losses; the 2 interviewed buyers gave other reasons (savings case, bundling).

## Changes to make
| # | Change | Area | Owner | Evidence |
|---|---|---|---|---|
| 1 | Decide whether to build SSO before chasing deals over 200 seats | Product | Head of product | 2 deals |
| 2 | Give reps a one-page savings calculator the champion can send to finance | Sales process | Sales lead | 1–3 deals |
| 3 | Lead first calls with the "live in a day" onboarding story | Messaging | Marketing lead | 3 deals |
| 4 | Interview the third "price" loss before calling it price | Sales process | Sales lead | 1 deal |

## One-offs worth watching
- Savings not shown to the finance approver (1 confirmed loss).
- Bundling by a payroll vendor; watch for a second case.
- Won 1 deal on price against a spreadsheet workaround.

## Quotes to share
- "Took a day, not a month." — ops manager, 40-person agency, won
- "We couldn't show our CFO the savings." — office manager, 90-person firm, lost
```

## Checks before you send

- [ ] Each deal has exactly one primary reason, and the counts add up to the deals reviewed.
- [ ] No theme rests on 1 deal; single cases are under one-offs.
- [ ] Every "price" loss was checked for another reason, and the result is stated.
- [ ] Each change has an area, an owner role, and an evidence count.
- [ ] Quotes are exact and attributed by role, never by a person's name.

## Common mistakes

- Taking the CRM loss reason at face value. Reps pick "price" because it's nobody's fault.
- Listing 12 findings. Rank and cut to the 5 that the most deals point at.
- Skipping wins. Why you win tells marketing what to say and sales which deals to chase.
