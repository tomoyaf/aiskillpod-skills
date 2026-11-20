---
name: saas-spend-review
description: Reviews a list of SaaS subscriptions and software tools with owners, seats used vs seats paid, overlapping tools, renewal dates and notice deadlines, and a cancel, downgrade, or keep recommendation for each with the savings. Never invents prices or usage. Use when someone shares a software list, card statement, or SaaS inventory and asks for a SaaS audit, a software spend review, "what can we cut", unused licenses, or renewals coming up.
---

# SaaS spend review

A SaaS review ends with a short list of decisions and a calendar: what to cancel, downgrade, or keep, how much each saves, and the date by which each must be acted on before it auto-renews. Every tool gets one owner, and every saving is computed from the prices and seat counts in the input.

## When to use

- Quarterly, or before budget planning.
- Renewals are coming up and nobody knows who uses what.
- Card statements show tools nobody recognizes.
- Not for choosing a new vendor: use vendor-comparison.

## What you need

- The list: tool, plan, price and billing period, seats paid, renewal date, who pays (card or invoice).
- Usage: active seats or last login per tool, from admin consoles. If usage is missing for a tool, write "[check: usage]" and don't recommend cutting seats on it.
- Owners: who asked for each tool. If unknown, "[owner: unknown]" — finding one is the first action.
- Contract terms: auto-renewal and the notice period for opting out. If missing, "[check: notice period]".

## Steps

1. **Normalize the list.** One row per tool: annual cost (monthly price × 12 if billed monthly; show it), seats paid, seats active, renewal date, notice period, owner. Group duplicate subscriptions for the same tool (2 teams each paying for it).
2. **Compute seat use.** Seat use = active seats ÷ seats paid. Our default: flag a tool under 70% use, and treat a seat with no login in 90 days as inactive. Unused seats × price per seat = the possible saving.
3. **Find overlaps.** Group tools by job (video calls, project tracking, file storage, e-signature, design). Two or more tools doing the same job is an overlap; name which one most people use, from the usage data.
4. **Set the action deadline.** Deadline = renewal date − notice period. Sort the whole list by this date. Anything with a deadline within 30 days goes to the top.
5. **Recommend per tool.** Cancel: no owner after asking, or near-zero use, or fully covered by another tool. Downgrade: seats or plan tier above use. Keep: used, owned, no overlap. Saving = the cost difference, from input prices only; if the lower plan's price isn't given, write "[check: lower plan price]".
6. **Write the action list.** Each action has an owner and the deadline from step 4. Cancelling a tool also needs its data exported and its sign-ins removed; add that as part of the action.
7. **Total the savings.** Total confirmed annual savings, and separately the savings that depend on a "[check: ...]".

## Output format

```markdown
# SaaS spend review — [date]

**Total annual spend reviewed:** [amount] across [n] tools
**Savings:** [amount] confirmed + [amount] pending checks

## Act before these dates
| Deadline | Tool | Action | Saving per year | Owner |
|---|---|---|---|---|
| [date] | [tool] | [cancel / downgrade to X / keep] | [amount] | [name] |

## All tools
| Tool | Owner | Annual cost | Seats paid / active | Use | Renews | Notice | Recommendation |
|---|---|---|---|---|---|---|---|
| [tool] | [name] | [amount] | [n / n] | [%] | [date] | [days] | [action and why] |

## Overlaps
- **[Job]:** [tools] — keep [tool] because [usage reason]; move [n] users from [tool]

## Checks needed
- [Tool]: [what's missing]
```

## Example

**Input:**

> Today: 2 September. Tools:
> - Zoomly Pro, 18 seats × 15 per month, monthly, renews 1st of each month, owner Lina, active seats 7
> - MeetSpace Business, 25 seats × 12 per month billed annually (3,600), renews 15 Oct, 30-day notice, owner unknown, active 22
> - Taskboard Team, 30 seats × 10 per month billed annually (3,600), renews 20 Sept, 60-day notice, owner Ravi, active 29
> - SignFast, 1 seat, 40 per month, monthly, owner Lina, last used 5 months ago

**Output:**

```markdown
# SaaS spend review — 2 September

**Total annual spend reviewed:** 10,920 across 4 tools
**Savings:** 480 confirmed + up to 3,240 pending [check: cost of 4 added MeetSpace seats]

## Act before these dates
| Deadline | Tool | Action | Saving per year | Owner |
|---|---|---|---|---|
| Passed (22 July) | Taskboard | Keep; renews 20 Sept | 0 | Ravi |
| 15 Sept | MeetSpace | Find an owner; keep | 0 | [owner: unknown] |
| 1 Oct (next billing) | Zoomly Pro | Cancel; export its data, move 7 users to MeetSpace | up to 3,240 [check: minus 4 MeetSpace seats] | Lina |
| 1 Oct (next billing) | SignFast | Cancel; export signed documents first | 480 | Lina |

## All tools
| Tool | Owner | Annual cost | Seats paid / active | Use | Renews | Notice | Recommendation |
|---|---|---|---|---|---|---|---|
| Zoomly Pro | Lina | 3,240 (15 × 18 × 12) | 18 / 7 | 39% | monthly | [check: notice] | Cancel: overlaps MeetSpace |
| MeetSpace | [owner: unknown] | 3,600 | 25 / 22 | 88% | 15 Oct | 30 days | Keep: most-used video tool |
| Taskboard | Ravi | 3,600 | 30 / 29 | 97% | 20 Sept | 60 days | Keep |
| SignFast | Lina | 480 (40 × 12) | 1 / 0 | 0% | monthly | [check: notice] | Cancel: unused 5 months |

## Overlaps
- **Video calls:** Zoomly Pro and MeetSpace — keep MeetSpace (22 active vs 7); MeetSpace has 3 free seats, so 4 more are needed for Zoomly's 7 users [check: price of 4 added MeetSpace seats, subtract from saving]

## Checks needed
- MeetSpace: who owns it? Deadline to opt out is 15 Sept.
- SignFast: does anyone still need e-signature? If yes, which tool replaces it?
```

## Checks before you send

- [ ] Every annual cost shows how it was computed from the input price.
- [ ] Seat use = active ÷ paid, and no seat cut is recommended without usage data.
- [ ] Every tool has an owner or "[owner: unknown]".
- [ ] Action deadlines are renewal date minus notice period, sorted soonest first.
- [ ] Savings use only prices in the input; the rest is "[check: ...]".
- [ ] Every cancel action includes exporting data.

## Common mistakes

- Missing the notice window. A tool renews for a year if the opt-out date passed.
- Cutting a tool used by a few people for a critical job (payroll, e-signature) because use is low.
- Counting the full cost of a cancelled tool as saved when users must move to paid seats elsewhere.
