---
name: funnel-stage-design
description: Designs or audits a B2B revenue process split into specialized roles - marketing, inside sales, field sales, customer success - with an owner, an entry criterion, a handoff definition, a conversion metric, a time metric, and capacity for every stage, then finds the bottleneck stage and proposes 3 fixes with owners. Use when someone asks to set up or fix a sales funnel, define MQL and SQL or lead handoff rules, split sales into inside sales and field sales, set KPIs per sales stage, work backward from a revenue target to leads, or asks for THE MODEL style division of labor (ザ・モデル, 分業, 営業プロセス, KPI 設計).
---

# Sales funnel roles and stage metrics

This skill lays out a B2B revenue process as a chain of specialized stages, where each stage's output is the next stage's input, and measures every stage the same way: how much comes in, what share moves on, and how long it takes. The Japanese B2B classic on this design is Yasutaka Fukuda's THE MODEL (Shoeisha, 2019), written from his years building the business at Salesforce's Japan unit and then running Marketo's Japan unit. It splits the work into marketing, inside sales, field sales, and customer success, and its subtitle calls the result a 共業 (working together) process rather than a plain division of labor, which suggests the split works only when the teams share definitions and numbers. Salesforce Japan calls the process model used there "The Model" and describes it with a base, a success rate, and a goal for each department. Aaron Ross and Marylou Tyler's Predictable Revenue (2011) makes the related case for separating prospecting from closing. This skill builds the stage table, finds the bottleneck, and proposes fixes.

## When to use

- A company is moving from "everyone sells" to specialized roles and needs stage definitions.
- Marketing says it sends enough leads and sales says the leads are bad.
- Revenue misses target and nobody can say at which stage.
- Planning headcount: how many inside sales or field sales people a target needs.
- Not for diagnosing one deal (use deal-review) or one account's plan (use account-plan). For the general method of working a constraint once it's found, see toc-five-focusing-steps.

## What you need

- The stages the company uses today and who owns each (a team or a named person). If there are no formal stages, ask what happens from first contact to renewal.
- Counts per stage for one recent period (a quarter is usual): visitors or contacts, leads, qualified leads handed to sales, opportunities, wins, renewals due and renewed. Use the CRM's numbers; never estimate a missing count. Mark it "[check: count]".
- Time per stage if available: time to first contact, sales cycle length, time to onboarding.
- Capacity: people per stage and how many leads, opportunities, or accounts one person handles in the period.
- The target: new wins or new revenue for the next period, and average deal size if revenue is the target.

## Steps

1. **List the stages and owners.** Use the company's own words, then map each to one of the four roles: marketing (creates leads), inside sales (qualifies and creates opportunities, by phone, email, or video), field sales (runs opportunities to a close), customer success (adoption and renewal). One owner per stage. If one person spans two stages, say so; it limits the split.
2. **Write entry and exit criteria as observable facts.** Each handoff is a definition both sides sign: "a marketing-qualified lead is a contact at a company of [size] in [segment] who [action]"; "an opportunity is a lead where [the buyer, the need, and a next meeting] are confirmed". Common labels are MQL (a lead marketing judges likely to buy) and SQL (a lead ready to talk to sales); use them only if the company does, and define them either way. Add what happens to rejected handoffs: returned with a reason, never dropped.
3. **Fill the stage table from the counts.** For each stage: count in, count out, conversion rate (out ÷ in), and the time metric. Compute every rate from the input; show the math once. Missing counts stay "[check: ...]" and the rate stays blank.
4. **Add capacity.** For each stage: people × what one person handles in the period = capacity. Compare with the volume that arrived. A stage where arrivals exceed capacity drops work silently; look for leads never contacted, opportunities without a next step, or renewals reached late.
5. **Work backward from the target.** Divide the target by each conversion rate, stage by stage, to get the volume each stage needs. Put needed volume next to actual volume and capacity.
6. **Name the bottleneck.** The bottleneck is the one stage that limits output most: where needed volume exceeds capacity, or where work is dropped or waiting longest. Pick one stage and give the evidence. Low conversion alone isn't proof; check whether the input to that stage changed first.
7. **Propose 3 fixes for the bottleneck.** One for the handoff definition or rule, one for capacity or time (who does what, response-time agreement), and one for measurement (what gets reported weekly). Each fix names the metric it should move, the owner, and when to check it. Don't invent benchmark rates from other companies; compare with the company's own history or target.
8. **Set the weekly review.** One shared table, reviewed by all stage owners together, with the handoff rejections and their reasons. The split works only if the teams look at the same numbers.

## Output format

```markdown
# Revenue process: [company] · [period]
**Target next period:** [wins or revenue] · **Average deal:** [amount or [check]]

## Handoff definitions
| Handoff | Definition (observable) | Who accepts | If rejected |
|---|---|---|---|

## Stage table
| Stage | Owner | Entry criterion | Exit / handoff | In | Out | Conversion | Time metric | Capacity |
|---|---|---|---|---|---|---|---|---|

## Working back from the target
| Stage | Needed | Actual | Capacity | Gap |
|---|---|---|---|---|

## Bottleneck
**Stage:** [stage] — [evidence in 2 to 3 sentences]

## Fixes
| # | Fix | Metric it moves | Owner | Check on |
|---|---|---|---|---|
| 1 | [handoff rule] | | | |
| 2 | [capacity or time] | | | |
| 3 | [measurement] | | | |

## Weekly review
[Who meets, the table they review, how rejections are logged]

## Gaps
- [check: missing count or definition]
```

## Example

**Input:** "We sell scheduling software to physiotherapy clinics. Last quarter: 6,000 site visitors, 260 sign-ups for a demo or guide, 200 of them matched our clinic profile and went to inside sales. Inside sales is 2 reps who also do outbound; each works about 55 inbound leads a quarter. They contacted 110 of the 200; median first contact 4 business days. From the 110 contacted, 40 became opportunities (buyer and need confirmed, demo booked). Field sales is 2 account executives: 40 opportunities, 12 wins, median cycle 38 days; each AE can run about 30 opportunities a quarter. Customer success is 1 CSM with 70 accounts; 24 renewals were due and 22 renewed. Target next quarter: 18 new wins."

**Output:**

```markdown
# Revenue process: physiotherapy scheduling · last quarter
**Target next period:** 18 new wins · **Average deal:** [check: amount]

## Handoff definitions
| Handoff | Definition (observable) | Who accepts | If rejected |
|---|---|---|---|
| Lead → inside sales | Sign-up from a clinic matching the profile [check: written profile] | Inside sales | Back to marketing nurture with a reason |
| Inside sales → field sales | Buyer and need confirmed, demo booked | Account executive | Back to inside sales with a reason |
| Field sales → customer success | Contract signed | CSM | [check: onboarding criteria] |

## Stage table
| Stage | Owner | Entry criterion | Exit / handoff | In | Out | Conversion | Time metric | Capacity |
|---|---|---|---|---|---|---|---|---|
| Marketing | [check: owner] | Site visit | Sign-up matching profile | 6,000 | 200 | 3.3% | [check] | n/a |
| Inside sales | 2 reps | Profile-matched lead | Opportunity | 200 | 40 | 20% (36% of contacted) | Median first contact 4 business days | 2 × 55 = 110 |
| Field sales | 2 AEs | Opportunity | Win | 40 | 12 | 30% | Median cycle 38 days | 2 × 30 = 60 |
| Customer success | 1 CSM | Win | Renewal | 24 due | 22 | 92% | [check] | 70 accounts [check: limit] |

Math: 40 ÷ 200 = 20%; 40 ÷ 110 = 36%; 12 ÷ 40 = 30%; 22 ÷ 24 = 92%.

## Working back from the target
| Stage | Needed | Actual | Capacity | Gap |
|---|---|---|---|---|
| Wins | 18 | 12 | | 6 short |
| Opportunities (÷ 30%) | 60 | 40 | 60 | at field sales capacity |
| Contacted leads (÷ 40/110) | 165 | 110 | 110 | 55 over capacity |
| Profile-matched leads | 165 or more | 200 | | enough |

## Bottleneck
**Stage:** inside sales. Marketing already sends 200 profile-matched leads, but only 110 are contacted, which equals the 2 reps' capacity, and first contact takes a median 4 business days. At the current 36% rate, contacting all 200 would give about 73 opportunities, more than the 60 the target needs.

## Fixes
| # | Fix | Metric it moves | Owner | Check on |
|---|---|---|---|---|
| 1 | Score leads; the top 110 by score go to inside sales the same day, the rest to an email nurture with a re-handoff rule | Share of handed-over leads contacted | Marketing lead and IS lead | End of month 1 |
| 2 | Move the 2 reps' outbound time to inbound for one quarter, or add one rep [check: budget]; agree first contact within 1 business day | Contacted leads; median time to first contact | Head of sales | Weekly |
| 3 | Add "not contacted after 5 business days" and rejection reasons to the weekly table | Leads dropped without contact | Sales ops [check: owner] | Weekly |

## Weekly review
Marketing, inside sales, field sales, and CS owners review the stage table every Monday, including returned leads and their reasons.

## Gaps
- Average deal size, for a revenue target.
- Field sales is at capacity once opportunities reach 60; plan the next hire before inside sales is fixed.
```

## Checks before you send

- [ ] Every stage has one owner, an entry criterion, and an exit criterion written as observable facts.
- [ ] Every rate is computed from the input, with the math shown; missing counts are "[check: ...]".
- [ ] Capacity is compared with arrivals for every stage.
- [ ] One bottleneck is named, with evidence beyond a low conversion rate.
- [ ] 3 fixes, each with a metric, an owner, and a check date.
- [ ] No benchmark rates from outside the company are presented as facts.
- [ ] Rejected handoffs go back with a reason.

## Common mistakes

- Fixing the stage with the worst-looking rate instead of the stage that limits output.
- Handoff definitions in adjectives ("hot lead", "qualified") instead of facts both sides can check.
- Measuring each team only on its own output, so marketing sends volume and sales complains about quality.
- Splitting roles before there's enough volume for each person; a specialist with too little work goes back to doing everything.
- Forgetting time: a lead contacted after a week is a different lead.
