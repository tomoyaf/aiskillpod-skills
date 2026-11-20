---
name: durable-advantage-check
description: Checks whether a business has a durable competitive advantage by testing each claimed moat for both a benefit (better cash flow than rivals) and a barrier (why capable rivals can't take it away), sorting it into one of seven types - scale economies, network economies, counter-positioning, switching costs, branding, cornered resource, process power - and matching it to the company's stage. Use when someone asks "do we have a moat", "what is our competitive advantage", "7 Powers analysis", "is this defensible", for an investor memo's moat section, or before betting the roadmap on a claimed advantage.
---

# Durable advantage check

A business earns more than its rivals over time only if two things are both true: something gives it better cash flow (a benefit), and something stops capable, motivated competitors from copying or competing it away (a barrier). A benefit with no barrier is good execution, and competitors will match it. A barrier with no benefit protects nothing. This test, and the seven types of advantage it sorts claims into, come from Hamilton Helmer's book 7 Powers: The Foundations of Business Strategy (2016). Helmer is a strategy consultant and investor who taught business strategy at Stanford; he calls a benefit-plus-barrier pair a "Power". The book also argues that each type tends to become available at a particular stage of a company's life. This skill applies the test to one business and ends with what to build now and what to stop calling a moat.

## When to use

- Someone says "our moat is..." and nobody has asked what stops a rival.
- Writing the competitive-advantage section of an investor memo, board deck, or strategy doc.
- Choosing where a young company should invest so an advantage exists when growth slows.
- A competitor just matched something you thought was unique.
- Not for an inventory of every resource the company owns (use vrio-analysis). Not for judging how profitable the whole industry is (use five-forces-analysis). Not for a first-pass list of strengths and threats (use swot-tows-analysis).

## What you need

- What the business sells, to whom, and the 2 to 5 rivals or alternatives customers compare it with.
- The claimed advantages, in the user's words.
- Evidence for each: prices against rivals, unit costs at different volumes, churn and what customers lose when they leave, how value changes as users grow, contracts, patents, how long rivals have tried to copy.
- The company's stage: still finding its product, growing fast, or growing slowly in a settled market. If unclear, ask once.
- Never invent numbers or competitor facts. Mark gaps "[check: ...]".

## Steps

1. **Set the frame.** Write the business, the market, the named rivals, and the stage in one line. Name the stage as one of three: origination (before the business takes off), take-off (rapid growth, market still shifting), or stability (growth has slowed, positions are settled). The book uses these three phases.
2. **Write each claim as a benefit.** For every claimed advantage, state how it improves cash flow: a higher price for the same thing, a lower cost, or less investment needed. If no cash-flow effect can be named, the claim is not an advantage yet; note it and move on.
3. **Classify the claim into one of the seven types.** Use the definitions below. A claim that fits none is usually operational excellence, which is valuable but copyable.
   - **Scale economies:** unit cost falls as volume grows, so the biggest player has the lowest cost.
   - **Network economies:** each customer gets more value as more customers join.
   - **Counter-positioning:** a new business model that an incumbent won't copy because copying would damage its existing business.
   - **Switching costs:** a customer would lose money, time, data, or work by moving to a rival.
   - **Branding:** buyers pay more for an objectively similar offer because of what years of consistent history make them believe about it.
   - **Cornered resource:** preferential access, on good terms, to something valuable: a patent, a license, a person, a site, a supply.
   - **Process power:** ways of working built into the organization that give lower cost or a better product, and that rivals can't copy quickly even when they can see them.
4. **Test the barrier.** For each claim, name the strongest rival and write why it can't simply copy or outspend the benefit. Typical barriers: for scale and network economies, the cost of winning share from the leader; for counter-positioning, the damage copying would do to the incumbent's own business; for switching costs, what a rival would have to pay or give up to win the customer; for branding and process power, the years it takes; for cornered resource, the contract or ownership. If the honest answer is "they could, they haven't tried yet", there is no barrier.
5. **Check materiality.** A benefit has to be large enough to matter in profit, not a rounding error. Compare its size with the gap to rivals using the user's numbers, or mark "[check: size]".
6. **Match to the stage.** The book's power progression ties each type to a phase. Counter-positioning and cornered resource are usually secured at origination. Scale economies, network economies, and switching costs are won during take-off, while the market is still moving. Branding and process power come once the business is stable, because they take years to build; a young company rarely has them. Flag claims that don't fit the stage (a two-year-old company claiming branding) and the type the current stage makes possible but the company isn't building.
7. **Give each claim a verdict.** One of: **Power** (benefit and barrier both shown), **Benefit only** (good execution; expect it to be matched), **Barrier only** (protects nothing yet), **Not yet** (possible at a later stage, with what it would take), or **Not supported** (no evidence).
8. **Decide actions.** For each Power, what keeps the barrier high. For each "Benefit only" item, stop calling it a moat in decks and plans. For the stage's open window, the one type to build now, with the first step, an owner, and a date. List the evidence still needed and who can get it.

## Output format

```markdown
# Durable advantage check: [business]
**Market:** [what, to whom] · **Rivals:** [names] · **Stage:** [origination / take-off / stability] · **Date:** [date]

## Claims tested
| Claim (user's words) | Type | Benefit (cash-flow effect, evidence) | Barrier (why [strongest rival] can't take it) | Material? | Verdict |
|---|---|---|---|---|---|
| [claim] | [one of seven, or none] | [higher price / lower cost / less investment: evidence] | [barrier, or "none found"] | [Yes/No/check] | [Power / Benefit only / Barrier only / Not yet / Not supported] |

## Stage fit
[2–3 sentences: which types this stage makes available, which claims are early or late, the window that is open now.]

## Decisions
- **Keep the barrier high:** [Power] — [action] — [owner] — [date]
- **Stop calling it a moat:** [claim] — [why]
- **Build now:** [type] — [first step] — [owner] — [date]

## Evidence still needed
- [check: ...] — who can get it: [name]
```

## Example

**Input:** "Do we have a moat? We're Ledgerline, monthly bookkeeping for independent restaurants, 2 years old, about 600 restaurants, adding roughly 8% a month. We charge a flat monthly fee; receipts and invoices are read by software and checked by a small team. Main alternatives: local accounting firms that bill by the hour, and two software-only bookkeeping apps (TallyPal, Booksy). Our claims: (1) accounting firms can't copy our flat fee because their partners are paid on billable hours; (2) once we have 12+ months of a restaurant's books, they don't want to move mid-year; churn after month 12 is under 1% a month vs about 4% before; (3) network effects: more restaurants train our categorization model; (4) customers love us, NPS 61. Unit cost per restaurant has dropped from $90 to $55 a month as we grew from 200 to 600 restaurants."

**Output:**

```markdown
# Durable advantage check: Ledgerline
**Market:** monthly bookkeeping for independent restaurants · **Rivals:** local hourly-billing accounting firms; TallyPal; Booksy · **Stage:** take-off (2 years old, ~8% monthly growth) · **Date:** [date]

## Claims tested
| Claim (user's words) | Type | Benefit (cash-flow effect, evidence) | Barrier (why the strongest rival can't take it) | Material? | Verdict |
|---|---|---|---|---|---|
| Firms can't copy our flat fee | Counter-positioning | Lower cost to serve than hourly firms [check: cost comparison]; [check: whether customers choose Ledgerline to avoid hourly bills] | Hourly firms would cut their own billable revenue and partner pay by copying | [check: share of new customers who came from hourly firms] | Barrier only against hourly firms until the benefit is shown; Power if the checks hold. Not a barrier against the apps [check: TallyPal and Booksy pricing] |
| 12+ months of books, they don't move | Switching costs | Churn under 1% a month after month 12 vs about 4% before | A rival must rebuild a year of categorized history and win the restaurant mid-year | Yes: churn drops by about three quarters | Power, for customers past month 12 |
| More restaurants train our model | Not network economies: one restaurant's value doesn't rise because others join. Possibly scale economies in data | [check: does categorization accuracy or cost improve with volume?] | [check: could TallyPal or Booksy reach similar accuracy with their own volume?] | [check] | Not supported yet |
| Customers love us, NPS 61 | None of the seven: satisfaction, not branding | No evidence of a price premium over TallyPal or Booksy | None found: rivals can also serve customers well | — | Benefit only (good execution) |
| Unit cost fell from $90 to $55 as volume tripled | Scale economies | Lower cost per restaurant at higher volume | Rivals with less volume have higher unit cost [check: rivals' volume] | [check: cost gap vs TallyPal and Booksy] | Benefit only [check: rivals' volume] |

## Stage fit
Ledgerline is in take-off, the window when scale economies and switching costs can be secured. Counter-positioning fits its origin story, and its barrier against hourly firms holds, but its benefit is not shown yet [check: cost comparison]; whether it works against the software-only apps depends on their pricing [check]. Branding is not available at two years; the NPS is good execution.

## Decisions
- **Keep the barrier high:** switching costs — make the year-end close and tax-ready reports depend on the history Ledgerline holds — [owner] — [date]
- **Stop calling it a moat:** "customers love us" — no price premium, and rivals can match service
- **Stop calling it a moat:** "network effects" — until accuracy or cost is shown to improve with volume
- **Build now:** scale economies — measure unit cost against TallyPal and Booksy and decide whether to spend on growth to widen the volume lead — [owner] — [date]

## Evidence still needed
- [check: unit cost vs TallyPal and Booksy] — who can get it: finance lead
- [check: categorization accuracy by volume] — who can get it: ML lead
- [check: share of new customers coming from hourly firms] — who can get it: sales lead
```

## Checks before you send

- [ ] Every claim names its benefit as a cash-flow effect, with evidence or a "[check: ...]" mark.
- [ ] Every barrier names the strongest rival and why it can't copy or outspend the benefit.
- [ ] Each claim is in one of the seven types or marked "none", with a reason.
- [ ] The stage is named and the stage fit is stated.
- [ ] At least one "Build now" decision with an owner and a date.
- [ ] No numbers or competitor facts were invented.

## Common mistakes

- Calling any improvement a moat. Better onboarding, faster support, and good design are benefits; without a barrier, rivals match them.
- Labeling data or users as "network effects" when one customer's value doesn't rise as others join.
- Mistaking satisfaction for branding. Branding shows up as a price premium for a similar offer, and it takes years.
- Checking the barrier against the weakest rival. Test against the strongest one.
- Claiming a type the stage can't support yet, and missing the type the current stage makes possible.
