---
name: inamori-style-unit-profit-review
description: Reviews how a company or department is split into small profit units and how each unit's results are measured, against the small-unit profit management that Kazuo Inamori described for Kyocera (known as Amoeba Management) - independent small units with their own leader and plan, results tied to the market, added value per hour, maximum sales with minimum expenses, pricing as a management decision, and participation by everyone. Use when a founder or manager asks to split a team into profit units, design a unit profit report, make each team's numbers visible, or check whether "everyone thinks like an owner" is real.
---

# Inamori-style small-unit profit review

These are principles Kazuo Inamori described publicly on the Kazuo Inamori website that Kyocera runs. Not affiliated with or endorsed by Kazuo Inamori or their companies. The method is known as Amoeba Management (アメーバ経営); this skill uses its publicly described principles to review your own units, their numbers and their leaders, and says where your setup departs from them.

## Ground rules

- Do not attribute quotes or opinions to Kazuo Inamori beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Kazuo Inamori; review the user's material against the principles below.
- Never invent numbers. A missing sales, expense or hours figure is written "[check: ...]".
- This is a review against the published principles, not an implementation of Kyocera's system; the cited sources don't give its detailed operating rules, so say so when the user needs that level.
- Say plainly when a principle doesn't fit the case (for example, a 4-person company doesn't need several profit units).

## The principles

1. **Small units run as independent profit centres.** A large organisation is divided into small groups, each run on its own profit and loss, each with an appointed leader who runs it almost like a partner in the business. Source: "Amoeba Management", Kazuo Inamori website (Kyocera).
2. **The leader makes and runs the unit's plan.** Within company policy, the leader draws up the unit's business plan and carries it out with the approval of their superior; this is how people with little experience grow a manager's sense of ownership. Source: same page.
3. **Everyone takes part.** Members set their own goals under the leader and work toward them, which the site calls management by all (全員参加経営). The three stated aims are a profit system by department tied directly to the market, developing people with a manager's mindset, and management by everyone. Source: same page.
4. **Added value per hour.** Inamori devised the Hourly Efficiency system in 1965 as a management accounting indicator: the added value created through work divided by total working hours. Source: Inamori Library exhibition page, "2F Technology and Management" (Kyocera).
5. **Maximise sales, minimise expenses.** Article 5 of his Twelve Management Principles. Article 6 says pricing is management (値決めは経営). Source: "Twelve Management Principles" (経営12カ条), Kazuo Inamori website.

## When to use

- Splitting a company or a department into units that each see their own profit.
- Designing a monthly unit report that a team leader can read and act on.
- Checking whether team leads really own a plan, or only receive targets.
- Comparing units that do very different work with one common number.
- Not for statutory accounts or tax; not a replacement for a management accountant. Use budget-variance-note for a variance explanation and unit-economics-check for per-customer economics.

## What you need

- The organisation: teams, their leaders, what each sells or delivers (to customers or to other teams).
- For each unit, if available: sales (or internal transfer revenue), expenses, and total hours worked in the period.
- How work and money move between units today (who "buys" from whom, at what internal price).
- Who sets each unit's plan and who approves it.
- The question the user is trying to answer.

## Steps

1. **Map the units.** List each unit with its leader, what it produces, its customer (external or another unit), and headcount. Flag any unit that has no clear output to sell or hand over: it can't show a result of its own.
2. **Check each unit against principle 1.** Can it be measured on its own revenue and expenses? Is it small enough for the leader to know every member's work? Is it tied to the market (its revenue moves when customers buy more or less)? Mark each yes, no, or [check].
3. **Check who owns the plan (principle 2).** For each unit: does the leader write the plan, or does it arrive from above? Is there an approval step? A leader who only receives targets fails this principle.
4. **Compute added value per hour (principle 4).** For each unit: added value = revenue minus the expenses the unit's work uses; divide by total hours worked. Show the formula with the user's own expense lines, state which expenses you included, and mark the choice "[decide: which expenses count]" when the input doesn't say. Compare units on this number, and month to month.
5. **Look for sales and expense levers (principle 5).** For each unit, name the largest lever to raise sales and the largest expense to cut, from the user's numbers only. Flag pricing decisions that sit with nobody in particular: under principle 5's companion article, pricing is a management decision.
6. **Check participation (principle 3).** Do members see the unit's numbers, set their own goals, and know how their work moves the number? Note what the user would have to change for that to be true.
7. **Name the risks.** Common ones: units competing instead of cooperating, internal prices that cause disputes, leaders gaming hours, and too much reporting for a small team. Give each a guard.
8. **Recommend the smallest next step.** Usually: one pilot unit, one monthly report, one meeting where the leader presents it.

## Output format

```markdown
# Unit profit review: [company or department]
**Period:** [month] · **Prepared for:** [name]
These are principles Kazuo Inamori described publicly. Not affiliated with or endorsed by Kazuo Inamori or their companies.

## Summary
[2-3 sentences: is the current setup close to the principles, the biggest gap, the next step]

## Units
| Unit | Leader | Output and customer | Own P&L possible? | Leader owns the plan? |
|---|---|---|---|---|

## Added value per hour
| Unit | Revenue | Expenses counted | Added value | Hours | Added value per hour |
|---|---|---|---|---|---|
Expenses counted: [list]. [decide: ...] where the input didn't say.

## Levers
| Unit | Biggest sales lever | Biggest expense to cut | Who sets the price |
|---|---|---|---|

## Participation
[What members see and decide today; what would have to change]

## Risks and guards
| Risk | Guard |
|---|---|

## Next step
[One pilot, one report, one owner, one date]

## Principles used
[Numbered list with the source of each]
```

## Example

**Input:** "We're a 22-person web agency. Three teams: Design (7), Build (9), Account management (4), plus 2 in admin. Last month: revenue 9.6M yen, all billed by account management. Design spent 0.3M on fonts and stock, Build 0.5M on hosting and tools, Accounts 0.2M on travel. Hours: Design 1,150, Build 1,500, Accounts 640. Leads get a revenue target from me each quarter. Nobody but me sees the numbers. I want each team to think like it runs its own shop."

**Output (excerpt):**

```markdown
These are principles Kazuo Inamori described publicly. Not affiliated with or endorsed by Kazuo Inamori or their companies.

# Unit profit review: the agency
**Period:** last month · **Prepared for:** founder

## Summary
The teams are close to natural units, but only Accounts touches revenue, so Design and Build can't see a result of their own. The leads receive targets rather than writing plans, and no member sees the numbers. Next step: pilot an internal price between Accounts and Build for one month.

## Units
| Unit | Leader | Output and customer | Own P&L possible? | Leader owns the plan? |
|---|---|---|---|---|
| Design | [lead] | Designs, handed to Build and Accounts | Only with an internal price | No: target from founder |
| Build | [lead] | Sites, handed to Accounts | Only with an internal price | No |
| Accounts | [lead] | Billed projects to clients | Yes | No |
| Admin | [lead] | Support to all | No: a cost centre | n/a |

## Added value per hour
Revenue can't be split by team from the input. [check: project revenue by team, or an internal price per design and build hour]. With all revenue at the company level: (9.6M - 1.0M) / 3,290 hours = about 2,614 yen per hour for the three teams together.

## Next step
Agree an internal price for Build's work with Accounts, run it for one month starting [check: start date], and have the Build lead present Build's own added value per hour at the monthly meeting.
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every unit has a leader, an output and a customer, or is flagged.
- [ ] Added value per hour shows the formula and which expenses were counted.
- [ ] Every number comes from the input or is marked [check] or [decide].
- [ ] Each principle used is listed with its source.
- [ ] The next step is one pilot with an owner and a date.

## Common mistakes

- Treating the method as a cost-cutting tool only; the stated aims include developing leaders and participation by everyone.
- Splitting units so small that the reporting costs more than it teaches.
- Setting internal prices nobody agreed to; disputes then replace improvement.
- Comparing units on revenue alone; units that do different work compare fairly only on added value per hour.
