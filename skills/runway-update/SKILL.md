---
name: runway-update
description: Writes a cash runway update from bank balances and monthly cash flows, with cash on hand, net burn as a 3-month average, runway in months, a base, downside, and upside scenario, and the levers that extend runway, with every formula spelled out. Use when a founder or finance lead asks "how much runway do we have", for a burn rate or cash runway update, a cash-out date, or before a board meeting, fundraise, or hiring decision.
---

# Runway update

A runway update answers one question: on current plans, in which month does the cash run out, and what would change that. Show the formula next to every number so anyone can check it, use an average burn rather than one noisy month, and never put a number in that isn't in the input.

## When to use

- Monthly, after the books close.
- Before a fundraise, a hiring plan, or a big spend decision.
- When cash dropped faster than expected.
- Not for a full financial model review: use model-assumptions-review.

## What you need

- Cash on hand at month end, across all accounts. If only some accounts are given, say which.
- Cash in and cash out for each of the last 3 months (or net burn per month). If fewer than 3 months are given, use what you have and say so.
- Known changes ahead: hires with start dates and cost, contracts, a raise closing, big one-off payments or receipts.
- Anything not in the input is "[check: ...]". Don't estimate revenue growth, hiring costs, or a raise.

## Steps

1. **State cash on hand.** As of the last day of the month, from the input. Exclude money that isn't usable (deposits held, restricted cash) if the input says so.
2. **Compute net burn.** Net burn = cash out − cash in, per month. Gross burn = cash out. Use the 3-month average of net burn as the default; show the 3 months. If net burn is negative (cash grew), say the company is cash-flow positive and runway is not limited by burn.
3. **Compute runway.** Runway (months) = cash on hand ÷ average monthly net burn. Round down to one decimal. Cash-out month = the month that many months after the balance date.
4. **Build 3 scenarios.** Base: average burn plus only the changes the input confirms (signed hires, signed contracts). Downside: base plus a stated risk from the input (a customer churns, a raise slips); if none is given, use "revenue flat at last month" and say so. Upside: base plus one stated upside. Show each scenario's burn and runway with its formula. When burn changes partway, step month by month: cash after each month = cash before − that month's net burn.
5. **List the levers.** 3 to 5 actions that extend runway, each with the monthly saving or cash it adds if the input gives the amount, otherwise "[check: amount]". Typical ones: delay a hire, cut a tool, collect overdue invoices, annual prepay from customers, cut a vendor.
6. **Write the headline.** One sentence: runway in months, the cash-out month, and the direction vs last month if given.

## Output format

```markdown
# Runway update — [month year]

**Headline:** [runway] months of runway at current burn; cash runs out in [month year]. [vs last month]

## Cash
Cash on hand at [date]: [amount] ([accounts included])

## Burn
| Month | Cash in | Cash out | Net burn |
|---|---|---|---|
| [month] | [n] | [n] | [n] |
| **3-month average** | | | **[n]** |

Net burn = cash out − cash in. Average = sum of 3 months ÷ 3.

## Runway
Runway = cash ÷ average net burn = [cash] ÷ [burn] = **[x] months** → cash out in [month year]

## Scenarios
| Scenario | What changes | Monthly net burn | Runway | Cash out |
|---|---|---|---|---|
| Base | [confirmed changes] | [n] | [x] | [month] |
| Downside | [stated risk] | [n] | [x] | [month] |
| Upside | [stated upside] | [n] | [x] | [month] |

## Levers
| Lever | Effect per month | Runway gained |
|---|---|---|
| [Action] | [amount or "[check: amount]"] | [months] |

## Not included
- [Items left out and why: unconfirmed raise, unsigned deals]
```

## Example

**Input:**

> Ferro Labs. Cash at 31 Aug: 1,240,000.
> Jun: in 95,000, out 205,000. Jul: in 102,000, out 214,000. Aug: in 98,000, out 228,000.
> Signed: 1 engineer starts 1 Oct, 11,000 per month all-in. Risk: largest customer (18,000 per month) may not renew in Nov. Possible: annual prepay offer to 5 customers, amount not known.

**Output:**

```markdown
# Runway update — August

**Headline:** 9.7 months of runway in the base case; cash runs out in June next year.

## Cash
Cash on hand at 31 August: 1,240,000 (all accounts given)

## Burn
| Month | Cash in | Cash out | Net burn |
|---|---|---|---|
| June | 95,000 | 205,000 | 110,000 |
| July | 102,000 | 214,000 | 112,000 |
| August | 98,000 | 228,000 | 130,000 |
| **3-month average** | | | **117,333** |

## Runway
Runway = 1,240,000 ÷ 117,333 = **10.5 months** → cash out in mid-July next year

## Scenarios
| Scenario | What changes | Monthly net burn | Runway | Cash out |
|---|---|---|---|---|
| Base | Engineer from 1 Oct (+11,000) | 128,333 from Oct | 9.7 | June next year |
| Downside | Base + largest customer lost from Nov (+18,000) | 146,333 from Nov | 8.7 | May next year |
| Upside | Base + annual prepay | [check: prepay amount] | [check] | [check] |

## Levers
| Lever | Effect per month | Runway gained |
|---|---|---|
| Delay the October hire by 3 months | 11,000 for 3 months | about 0.3 months |
| Annual prepay offer | [check: amount] | [check] |

## Not included
- August burn rose 18,000 vs July; reason not given [check: one-off or ongoing?]
```

## Checks before you send

- [ ] Net burn = cash out − cash in for each month, and the average uses the months shown.
- [ ] Runway = cash ÷ average net burn, with the formula and numbers visible.
- [ ] Scenarios include only changes stated in the input; the rest is "[check: ...]".
- [ ] The headline's runway and cash-out month match the base scenario.
- [ ] Every number is from the input or computed from it.

## Common mistakes

- Using gross burn for runway when there's revenue. That understates runway; show both if asked, label which is which.
- Using the best recent month as the burn. Average 3.
- Counting a raise that hasn't closed. List it under "Not included".
