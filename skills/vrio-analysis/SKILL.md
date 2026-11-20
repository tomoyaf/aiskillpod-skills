---
name: vrio-analysis
description: Runs a VRIO analysis of a company's resources and capabilities - lists them, tests each for Value, Rarity, Imitability, and Organization with evidence, and gives each a competitive implication (disadvantage, parity, temporary advantage, sustained advantage, or unused advantage), then turns the verdicts into actions with owners. Use when someone asks for a VRIO analysis, a VRIO framework example, a resource-based view of their business, "what is our real competitive advantage", "which of our strengths can competitors copy", or an internal analysis before a strategy review.
---

# VRIO resource analysis

VRIO asks four questions about each thing a company has or does well: is it Valuable, is it Rare, is it costly to Imitate, and is the company Organized to use it? Only a resource that passes all four gives an advantage that lasts. The method comes from Jay Barney's resource-based view. His 1991 article "Firm Resources and Sustained Competitive Advantage" (Journal of Management) judged resources on value, rareness, imitability, and substitutability (often shortened to VRIN). His 1995 article "Looking Inside for Competitive Advantage" (Academy of Management Executive) framed the tests as the VRIO questions, with Organization as the fourth, and his textbooks, including Strategic Management and Competitive Advantage with William Hesterly, use VRIO throughout. Barney's outcome table runs from disadvantage to sustained advantage; for a resource that passes the first three tests but isn't organized, some texts say the advantage stays temporary and others call it unexploited. This skill names that row "unused advantage". It applies the questions to one business and ends with what to protect, fix, and stop.

## When to use

- Before a strategy review, to find out which strengths will still be strengths in three years.
- When a team says "our people" or "our quality" is the advantage and nobody has tested it.
- When choosing where to invest: which capability to deepen, which to buy or outsource.
- After a competitor copies something you thought was unique.
- Not for judging how attractive an industry is (use five-forces-analysis). Not for checking whether an advantage is defended by a specific barrier such as network effects or switching costs (use durable-advantage-check). Not for a quick list of strengths and weaknesses next to market changes (use swot-tows-analysis).

## What you need

- The business or unit being analyzed, and what it sells to whom.
- The competitor set to compare against: 3 to 6 named rivals or alternatives customers actually consider. If missing, ask once; without it, rarity can't be judged.
- The resources and capabilities the team thinks matter, with any evidence: win/loss notes, customer quotes, cost or margin data, patents, contracts, tenure, data assets.
- How the company is run around each resource: who owns it, which process or incentive uses it.
- Never invent market data, competitor facts, or numbers. Mark gaps "[check: ...]".

## Steps

1. **Frame the question.** Write one line: the business, the market it competes in, the named competitor set, and the decision this analysis feeds (for example, "where to invest next year"). VRIO verdicts only mean something against a named set of rivals.
2. **List resources and capabilities, specifically.** Aim for 6 to 12 items across tangible assets (cash, sites, equipment), intangible assets (brand, data, patents, contracts, relationships), and capabilities (what the company can do repeatedly, such as onboarding a client in two days). Rewrite vague items: "great team" becomes "four engineers who built the integrations with the three largest practice systems". Ask the user to add or cut before testing.
3. **Test Value.** For each item, name the customer need, opportunity, or threat it serves, and the evidence that it moves revenue, cost, or retention. If the user can't point to evidence, mark the verdict "[check: evidence of value]" rather than Yes. A No here ends the test for that item.
4. **Test Rarity.** Count how many of the named competitors have the same thing at a similar level. Name them. If most have it, it is not rare. Rare does not have to mean unique; it means few in this competitor set have it.
5. **Test Imitability.** Estimate what it would cost a competitor in time and money to build it, buy it, or reach the same result another way. Look for what makes copying hard: a history that can't be replayed (years of data, a contract won early), causes nobody can see clearly from outside, relationships and culture that take people and years to build, and legal protection. Include substitutes: if a rival can get the same result by a different route, the item is not costly to imitate. Write the estimate with its basis, or "[check: ...]".
6. **Test Organization.** Ask whether the company is set up to capture the value: an owner, a process that uses the resource, incentives that reward using it, and a way to see the results. A resource the company owns but no process uses fails this test.
7. **Read the implication.** Apply the table in Output format: not valuable means disadvantage; valuable but common means parity; valuable and rare but easy to copy means temporary advantage; valuable, rare, and costly to imitate but not organized means unused advantage; all four means sustained advantage. When value can't be judged without a fact the user doesn't have, write "Not rated [check: ...]" instead of guessing. Don't soften a verdict because the team is proud of the item.
8. **Turn verdicts into actions.** For each sustained advantage, what protects it. For each unused advantage, the organizing change (owner, process, incentive) that would put it to work. For each temporary advantage, how to use the lead before it closes or how to make it harder to copy. For parity items, the minimum spend to stay level. For disadvantages, fix, buy, partner, or stop. Every action gets an owner and a date.
9. **State the gaps and the next review.** List each "[check: ...]" with who can answer it, and set a date to re-run the analysis, sooner if a competitor moves.

## Output format

```markdown
# VRIO analysis: [business or unit]
**Market:** [what it sells, to whom] · **Compared with:** [competitor 1, 2, 3...] · **Feeds decision:** [decision] · **Date:** [date]

## Verdicts
| # | Resource or capability | Valuable? | Rare? | Costly to imitate? | Organized? | Implication |
|---|---|---|---|---|---|---|
| 1 | [specific item] | Yes/No: [evidence] | Yes/No: [who else has it] | Yes/No: [cost or time to copy, substitutes] | Yes/No: [owner, process] | [Disadvantage / Parity / Temporary advantage / Unused advantage / Sustained advantage] |

Implication rules: No on V = disadvantage. V only = parity. V + R = temporary advantage. V + R + I without O = unused advantage (our label; others say unexploited, or still temporary). V + R + I + O = sustained advantage. Value unknown = Not rated [check: ...].

## What this means
[2–4 sentences: where the real advantage is, what is only parity, and the biggest surprise.]

## Actions
| Item | Verdict | Action | Owner | By |
|---|---|---|---|---|
| [item] | [verdict] | [protect / organize / exploit then deepen / keep level / fix or stop] | [name] | [date] |

## Gaps to check
- [check: ...] — who can answer: [name]

**Next review:** [date or trigger]
```

## Example

**Input:** "Do a VRIO on us. We're Calla, 30 people, SaaS for booking and reminders at independent dental clinics, about 1,100 clinics on it. Competitors: DentiBook, SmileSlot, and the reminder module built into the practice-management systems. What we think we have: (1) two-way integrations with the 3 most-used practice-management systems, took us 5 years, DentiBook has one of them, SmileSlot none; (2) support answers within 2 hours, DentiBook and SmileSlot both advertise same-day; (3) 9 years of appointment and no-show history across our clinics, nobody else has that much; we don't use it in the product, it sits in the warehouse and nobody owns it; (4) about $3M in the bank; (5) our CEO sits on a regional dental association committee. Win/loss notes say integrations come up in most won deals. Deciding where to put next year's product budget."

**Output:**

```markdown
# VRIO analysis: Calla (booking and reminders for independent dental clinics)
**Market:** booking and reminder software for independent dental clinics · **Compared with:** DentiBook, SmileSlot, built-in reminder modules of practice-management systems · **Feeds decision:** next year's product budget · **Date:** [date]

## Verdicts
| # | Resource or capability | Valuable? | Rare? | Costly to imitate? | Organized? | Implication |
|---|---|---|---|---|---|---|
| 1 | Two-way integrations with the 3 most-used practice-management systems | Yes: win/loss notes cite integrations in most won deals | Yes: DentiBook has 1 of 3, SmileSlot none | Yes: took Calla 5 years; [check: whether the system vendors now offer open APIs that cut this time] | Yes, likely: [check: owner and process that keep them current] | Sustained advantage, if the check holds |
| 2 | Support replies within 2 hours | [check: evidence that reply time affects wins or retention] | No: both rivals advertise same-day support | — | — | Not rated [check: value] |
| 3 | 9 years of appointment and no-show history from ~1,100 clinics | Yes, likely: could predict no-shows and fill gaps [check: test with clinics] | Yes: no rival reported to have comparable history | Yes: years of history can't be bought or rebuilt quickly | No: unused in the product, no owner | Unused advantage |
| 4 | About $3M cash | Yes: funds product and sales | No: [check: rivals' funding]; cash is generally easy to raise or match | — | — | Parity |
| 5 | CEO's seat on a regional dental association committee | [check: any deals or referrals traced to it] | [check] | [check] | [check] | Not rated [check: evidence] |

## What this means
Calla's lasting advantage is its integrations, and it is in use. The largest opportunity is the no-show history: it passes the first three tests but nobody owns it, so it earns nothing today. Cash keeps Calla level with rivals and is not a reason clinics choose it. Fast support can't be rated until its value is shown, and even then it would be parity, since both rivals advertise same-day support.

## Actions
| Item | Verdict | Action | Owner | By |
|---|---|---|---|---|
| Integrations | Sustained, if the check holds | Confirm the owner; keep them current ahead of each vendor release; check vendors' API plans | [owner: integrations lead] | [date] |
| No-show history | Unused | Name an owner; test a no-show prediction with 10 clinics; budget next year's product work around the result | [owner: to confirm] | [date] |
| Support speed | Not rated [check: value] | Check whether reply time shows up in churn or win/loss before spending more on it | [owner: support lead] | [date] |
| Cash | Parity | No action from this analysis | — | — |
| Association seat | Not rated | Trace any referrals from it in the CRM | [owner: CEO] | [date] |

## Gaps to check
- [check: vendor API plans for the 3 practice-management systems] — who can answer: integrations lead
- [check: owner and process that keep the integrations current] — who can answer: integrations lead
- [check: evidence that support speed affects wins or retention] — who can answer: support lead
- [check: test a no-show prediction with clinics] — who can answer: [owner: to confirm]
- [check: rivals' funding] — who can answer: [name]
- [check: any deals or referrals traced to the association seat] — who can answer: CEO

**Next review:** [date], or sooner if DentiBook ships a second integration.
```

## Checks before you send

- [ ] The competitor set is named, and every rarity verdict names who else has the item.
- [ ] Every Yes has evidence or a "[check: ...]" mark; nothing rests on pride or assumption.
- [ ] Substitutes were considered under imitability, not only direct copying.
- [ ] Every row has exactly one implication from the five, applied by the rules, or "Not rated [check: ...]" when value can't be judged.
- [ ] At least one action per row that isn't parity, each with an owner and a date.
- [ ] No market data, competitor facts, or numbers were invented.

## Common mistakes

- Rating the company or a product instead of a resource or capability. "Our app" is not a resource; "two-way integrations with the three largest systems" is.
- Calling everything valuable and rare. Most real lists end with many parity items, and that is useful: it shows where not to over-spend.
- Forgetting substitutes. A rival doesn't need your asset if it can reach the same result another way.
- Skipping Organization. Resources that pass the first three tests often sit unused because no one owns them; that is the cheapest advantage to claim.
- Stopping at the table. The output is the action list, not the verdicts.
