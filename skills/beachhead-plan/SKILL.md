---
name: beachhead-plan
description: Picks one beachhead segment for a new product that has early fans but stalls with mainstream buyers, using the chasm idea from Geoffrey A. Moore's Crossing the Chasm - scores candidate segments, names the target customer and their compelling reason to buy, lists the whole-product gaps to close before selling hard, drafts a positioning line, and names the next adjacent segments. Use when someone asks for a beachhead market, a go-to-market focus, which niche to target first, crossing the chasm, early adopters versus early majority, a whole-product plan, or why sales stalled after the first enthusiastic customers.
---

# Beachhead segment plan

Early adopters buy a new product for its promise and put up with gaps. Mainstream buyers, the pragmatists, want proof that people like them already use it, and a complete solution. Geoffrey A. Moore called the gap between those two groups the chasm, in Crossing the Chasm (1991; 3rd edition 2014). His answer is to pick one narrow segment of pragmatists with an urgent problem, give them everything they need to solve it, win most of that segment, and use those customers as references to move into the segments next door. The book (3rd edition, HarperBusiness 2014) compares this to the D-Day landings: take one beach with everything you have, then push inland.

## When to use

- A product has a handful of keen early customers, and sales to everyone else are slow and custom.
- The team chases every lead and can't say who the product is for.
- Before a launch, a hire plan, or a marketing budget, to decide where to focus first.
- Not for analyzing a whole industry's profitability: use five-forces-analysis. Not for writing full positioning: use positioning-statement after choosing the beachhead. Not for testing whether anyone wants the product at all: use build-measure-learn.

## What you need

- What the product does today, and what it doesn't do yet.
- The current customers: who they are, why they bought, what they use it for, and how they found you. This matters most; if missing, ask once and mark claims "[assumption]".
- Candidate segments the team is considering (industry, role, use case, size, region), and any facts about each: number of reachable buyers, budget, how they buy, who they talk to.
- What the company is unusually good at, and what partners it has.
- Never invent segment sizes, budgets, or win rates; mark gaps "[check: ...]".

## Steps

1. **Place the product on the adoption curve.** Moore's life cycle runs from innovators and early adopters (visionaries who buy the promise) to the early majority (pragmatists who buy proven solutions), then the late majority and laggards. From the current customers, say who has bought so far and whether the stall looks like the chasm: wins come from enthusiasts and one-off projects, not from repeat buyers in one niche.
2. **List 3 to 8 candidate segments.** Define each narrowly enough that its members know each other and talk: a role in a type of company in a region, with one use case. "Healthcare" is not a segment; "billing managers at independent dental clinics in Ontario" is.
3. **Score each candidate.** Use a 1 to 5 scale on: urgency of the problem (do they have a compelling reason to buy now?), whether they have budget and a clear buyer, whether you can deliver a whole product for them soon, whether you can reach them, whether the segment talks within itself (references spread), size (a segment you can lead that is still worth winning), whether strong rivals already own it, and whether it opens doors to other segments. Show the scores in a table, and mark any guessed score "[check]".
4. **Choose one beachhead.** Pick the highest-scoring segment with an urgent problem, and say why the runner-up lost. Write one line on the target customer: who they are, what goes wrong today, and what they do about it. Write the compelling reason to buy in their words: the cost of doing nothing.
5. **List the whole-product gaps.** List everything the target customer needs to get the result, not just the core product: setup, integrations, training, support, data migration, templates, compliance, a partner who installs it. Mark each as have, partner, build, or drop, with an owner. Pragmatists won't assemble the missing pieces themselves.
6. **Draft the positioning line.** Moore's book gives a fill-in statement covering the target customer, their problem, the product's category, its key benefit, the main alternative they'd use instead, and how you differ. Write one for the beachhead, in the customer's words. Then hand off to positioning-statement for the full version.
7. **Name the next segments and the decisions.** List the 2 or 3 adjacent segments that share either the customer or the use case with the beachhead, in order. Close with what the team stops doing (leads outside the beachhead get a polite no or a waitlist), the first actions with owners and dates, and a share-of-segment target that would show the beachhead is won.

## Output format

```markdown
# Beachhead plan: [product]

**Owner:** [name] · **Date:** [date] · **Decide by:** [date]

## Where we are on the adoption curve
[Who has bought so far, and why this looks or doesn't look like the chasm.]

## Candidate segments (1 = poor, 5 = strong)
| Segment | Urgent problem | Budget and buyer | Whole product soon | Reach | Talk to each other | Size fit | Rivals weak | Opens next | Total |
|---|---|---|---|---|---|---|---|---|---|

## The beachhead
**Segment:** [narrow definition]
**Target customer:** [who, what goes wrong today, what they do about it]
**Compelling reason to buy:** [the cost of doing nothing, in their words]
**Why not [runner-up]:** [reason]

## Whole-product gaps
| Need | Status (have / partner / build / drop) | Owner | By |
|---|---|---|---|

## Positioning line (draft)
For [target customer] who [problem], [product] is a [category] that [key benefit]. Unlike [main alternative], it [key difference].

## Next segments
1. [segment] — shares [customer / use case]
2. [segment] — shares [customer / use case]

## Decisions
- We stop: [what]
- First actions: [action, owner, date]
- The beachhead is won when: [share of segment, references]
```

## Example

**Input:** "We make scheduling software with automatic text reminders. 40 paying customers: 14 physio clinics, 9 hair salons, 8 dog groomers, 9 mixed. Physio clinics found us through one physio association newsletter, and they say no-shows cost them a lot because each slot is 45 minutes with one therapist. Salons churn often and compare us to free tools. Physios ask for insurance-claim notes and an integration with ClinicLink, their practice software; we have neither. Our strength: reminders that patients confirm by reply. We have 2 salespeople."

**Output:**

```markdown
# Beachhead plan: scheduling with text reminders

**Owner:** [check: owner] · **Date:** [date] · **Decide by:** [date]

## Where we are on the adoption curve
40 customers across several trades, with no segment won. Physio clinics came through one association's newsletter, so they share a channel [check: whether they refer each other]; the rest are scattered. This looks like the edge of the chasm.

## Candidate segments (1 = poor, 5 = strong)
| Segment | Urgent problem | Budget and buyer | Whole product soon | Reach | Talk to each other | Size fit | Rivals weak | Opens next | Total |
|---|---|---|---|---|---|---|---|---|---|
| Independent physio clinics | 5 | 4 [check] | 3 | 5 | 5 [check] | [check] | [check] | 4 [check] | [check] |
| Hair salons | 3 [check] | 2 [check] | 4 [check] | 3 [check] | 3 [check] | [check] | 2 [check] | 3 [check] | [check] |
| Dog groomers | 3 [check] | 3 [check] | 4 [check] | 2 [check] | 2 [check] | [check] | [check] | 2 [check] | [check] |

## The beachhead
**Segment:** independent physio clinics [check: region]
**Target customer:** a clinic owner whose 45-minute slots go empty when patients don't show; today they [check: what clinics do about no-shows now].
**Compelling reason to buy:** each no-show is a lost 45-minute slot of one therapist's time [check: whether a slot can be refilled at short notice].
**Why not hair salons:** salons compare us to free tools and churn often; the problem is less urgent.

## Whole-product gaps
| Need | Status | Owner | By |
|---|---|---|---|
| Reply-to-confirm reminders | have | — | — |
| ClinicLink integration | build or partner [check] | [check] | [check] |
| Insurance-claim notes | build [check: scope] | [check] | [check] |
| Setup help moving the existing patient list | [check] | [check] | [check] |

## Positioning line (draft)
For independent physio clinics who lose 45-minute slots to no-shows, [product] is appointment scheduling that gets patients to confirm by text reply. Unlike [check: what clinics do about no-shows now], it [check: measured effect on no-shows from current clinics].

## Next segments
1. Other one-therapist-per-slot clinics, such as chiropractors [check] — shares the use case
2. Larger physio groups [check] — shares the customer

## Decisions
- We stop: custom work for salons and groomers; new leads outside physio go to a waitlist.
- First actions: decide ClinicLink build vs partner ([check: owner, date]); ask the 14 clinics for references.
- The beachhead is won when: [check: share of reachable clinics in the region, number of referenceable clinics]
```

## Checks before you send

- [ ] Each candidate segment is narrow enough that its members talk to each other.
- [ ] Exactly one beachhead is chosen, with the reason the runner-up lost.
- [ ] The compelling reason to buy is a cost of doing nothing, not a feature.
- [ ] Every whole-product gap has a status and an owner.
- [ ] Scores, sizes, and budgets come from the input or are marked "[check]".
- [ ] It ends with what the team stops doing and the first actions.

## Common mistakes

- Picking the biggest segment. A large market you can't lead gives no references; pick one you can dominate.
- Picking two beachheads "to be safe". Splitting effort means winning neither.
- Selling the core product alone to pragmatists. Missing pieces stall the deal.
- Positioning against visionaries' wishes. Pragmatists buy against the alternative they use today.
- Staying in the beachhead forever. Once it's won, move to the adjacent segment.
