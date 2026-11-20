---
name: account-plan
description: Builds an expansion plan for an existing customer - a stakeholder map, how they use the product today, whitespace (teams, use cases, or seats not yet bought), risks to the renewal, and 90-day plays with owners and dates. Use when an account manager, CSM, or founder asks for an account plan, expansion plan, upsell or cross-sell plan, key account review, or "how do we grow this customer".
---

# Account plan

An account plan says who matters at the customer, where more value is, and what you'll do in the next 90 days to get there. Protect the renewal before you pitch expansion: an upsell into an unhappy account speeds up the churn.

## When to use

- For your top accounts by revenue, once a quarter.
- 3 to 6 months before a renewal, or after a new executive joins the customer.
- When usage shows a team or use case growing on its own.
- Not for a deal that hasn't closed yet: use deal-review. Not for a quarterly business review deck: use qbr-prep.

## What you need

- Account basics: current plan, seats or usage, annual value, renewal date.
- Contacts you know, with titles and how engaged each is.
- Usage data or notes: which teams use it, for what, and trends.
- Recent support tickets, complaints, or praise.
- If org structure or usage is missing, ask once; otherwise mark each gap "[unknown]" and make finding it a play.

## Steps

1. **Check renewal health first.** A health score reads usage, support history, engagement, and sentiment: a low score calls for intervention, a strong one shows the customer is ready to grow. Score it green, yellow, or red. Our default: red if any of: usage down over 20% in 90 days, sponsor left, an open escalation, or no contact with the buyer in 60 days. If red, the first 2 plays fix health, not expansion.
2. **Map stakeholders.** For each person: role, what they care about, their stance (champion, supporter, neutral, skeptic), and your last contact. Mark the economic buyer, any blocker, and any gap: a team that uses the product with no named contact is a gap. If you know only 1 person, say so as a risk: won deals involve 67% more contacts than lost ones in Gong's data.
3. **Describe current use in their terms.** Which teams, which use cases, what outcome they've seen. If you have a number they've said ("cut invoice time by half"), use it; don't invent one.
4. **Find whitespace.** Map their business units against your products; the empty cells are whitespace. List teams, use cases, or plan features they don't use yet. For each: who would own it, the evidence it's needed (a ticket, a request, a similar customer), and rough value. Rank by evidence, not by size.
5. **List risks.** Champion leaving, budget cuts, a competitor in another team, low adoption, a known product gap. Each with a mitigation.
6. **Write 3 to 5 plays for the next 90 days (our default horizon).** Each: goal, first action, owner (a named person), date, and how you'll know it worked. One play must reach a stakeholder you haven't met.
7. **Set the measure.** One number for the 90 days: expansion value, seats, or a renewal signed early. State today's value.

## Output format

```markdown
# Account plan: [customer] — [date]

**Plan / value / renewal:** [plan] / [annual value] / [date]
**Renewal health:** [green / yellow / red] — [reason]
**90-day goal:** [one number, from today's value to target]

## Stakeholders
| Name | Role | Cares about | Stance | Last contact |
|---|---|---|---|---|
| [name] | [role] | [goal] | [champion/supporter/neutral/skeptic] | [date] |

Gaps: [teams or roles with no contact]

## Current use
- [team]: [use case] — [outcome, in their words]

## Whitespace
| Opportunity | Owner at customer | Evidence | Rough value |
|---|---|---|---|
| [team or use case] | [name or unknown] | [ticket, request, similar customer] | [value or "to size"] |

## Risks
- [risk] — [mitigation]

## 90-day plays
| # | Goal | First action | Owner | By | Success looks like |
|---|---|---|---|---|---|
| 1 | [goal] | [verb-first action] | [name] | [date] | [observable result] |
```

## Example

**Input:** Brightline Logistics, Team plan, 40 seats, 24,000 a year, renews 31 March. Contacts: Omar Diaz (ops director, sponsor, met monthly), Lena Fox (finance manager, raised 2 tickets about exports, neutral). Usage: ops team only, up 15% this quarter. Omar mentioned the warehouse team (about 60 people) still uses spreadsheets. Customer success lead: Priya Shah.

**Output:**

```markdown
# Account plan: Brightline Logistics — 4 November

**Plan / value / renewal:** Team, 40 seats / 24,000 / 31 March
**Renewal health:** green — usage up 15%, sponsor engaged monthly
**90-day goal:** 40 seats to 100 seats, by a warehouse team rollout

## Stakeholders
| Name | Role | Cares about | Stance | Last contact |
|---|---|---|---|---|
| Omar Diaz | Ops director | Fewer manual handoffs | Champion | October |
| Lena Fox | Finance manager | Clean exports for month-end | Neutral | 2 tickets, October |

Gaps: no contact in the warehouse team; economic buyer above Omar [unknown].

## Current use
- Ops team: shipment handoffs — usage up 15% this quarter.

## Whitespace
| Opportunity | Owner at customer | Evidence | Rough value |
|---|---|---|---|
| Warehouse team (about 60 people) | [unknown] | Omar: still on spreadsheets | About 60 seats, to price |
| Finance exports | Lena Fox | 2 export tickets | Retention, not new revenue |

## Risks
- Lena's export issues could make finance push back at renewal — fix the export problem before the renewal talk.
- Only one champion — meet a second stakeholder this quarter.

## 90-day plays
| # | Goal | First action | Owner | By | Success looks like |
|---|---|---|---|---|---|
| 1 | Turn finance neutral to supporter | Call Lena to walk through the export fix | Priya Shah | 15 November | Lena confirms month-end export works |
| 2 | Meet the warehouse lead | Ask Omar for an intro to the warehouse manager | Priya Shah | 20 November | Meeting booked |
| 3 | Pilot in the warehouse | Propose a 10-person, 30-day pilot | Priya Shah | 15 December | Pilot running with weekly use |
| 4 | Find the economic buyer | Ask Omar who approved the original purchase | Priya Shah | 20 November | Name and role known |
```

## Checks before you send

- [ ] Renewal health is scored with a stated reason, and a red account leads with health plays.
- [ ] Every play has a named owner, a date, and an observable success signal.
- [ ] At least one play reaches a stakeholder not yet met.
- [ ] Whitespace items each cite evidence; none is a guess presented as a need.
- [ ] No usage number or value appears that isn't in the input.

## Common mistakes

- Planning expansion with only one contact. If the champion leaves, the plan and the renewal go with them.
- Listing every product feature as whitespace. Only list what the customer has shown a need for.
- Plays with no date. A 90-day plan without dates is a wish list.
