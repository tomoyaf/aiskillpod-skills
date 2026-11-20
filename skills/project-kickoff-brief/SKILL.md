---
name: project-kickoff-brief
description: Writes a one-page project kickoff brief from a goal and rough notes - the goal and why it matters, one success measure, scope in and out, milestones with dates, roles in a RACI-lite table with one accountable owner, top risks with an owner each, and how the team communicates. Use when a project is starting, someone asks for a kickoff doc, project charter, or project brief, or a team needs to agree who does what before work begins.
---

# Project kickoff brief

A kickoff brief gets everyone to agree on why the project exists, what "done" looks like, and who owns what, before the work starts. It fits on one page. Anything that doesn't change what people do this month goes in a linked doc.

## When to use

- A new project, launch, migration, or client engagement is starting and people need one shared page.
- Someone asks for a "kickoff doc", "project charter", "project one-pager", or "pre-read for the kickoff meeting".
- A project is already running but people disagree about scope or who decides. Write the brief to reset.
- Not for a product spec or requirements doc. Use a PRD for what the product does; this brief covers how the project runs.

## What you need

- The goal and why it matters now. If missing, ask once: "What changes for the business or the customer when this is done?"
- The deadline or target date. If none, write "[no date set]" and list it as the first open question.
- The people involved and their roles. If roles are unknown, list the names and mark the RACI table "[draft, confirm at kickoff]".
- Optional: budget, known constraints, related projects, and anything that is already decided.

## Steps

1. **Write the goal in 1 or 2 sentences.** Say what will be different and why it matters now. Asana's kickoff guide calls aligning on "what you are working towards and why this work matters" the most important part of a kickoff.
2. **Pick one success measure.** A number and a date ("40 customers moved to the new plan by 30 June") or a yes/no test anyone can check. Atlassian's kickoff play calls these tests "a shared definition of 'done'". Our default: one primary measure, at most 2 guardrails (things that must not get worse).
3. **Split scope into in and out.** List 3 to 6 items in scope and at least 3 out of scope. Out-of-scope items are the ones someone will ask for halfway through; naming them early is how you prevent scope creep. If an item is unclear, put it under open questions, not in scope.
4. **Set 3 to 6 milestones.** Each one is a finished, checkable thing with a date and an owner ("pricing page live on staging"), not an activity ("work on pricing"). The last milestone is the success measure's date.
5. **Fill the RACI-lite table.** One row per workstream. Responsible does the work; Accountable signs off and owns the result; Consulted reviews before it moves on; Informed hears about progress. Asana's RACI guide: "There should be only one Accountable role per task." Our default: one Accountable for the whole project too, named at the top.
6. **List the top 3 to 5 risks.** For each: what could go wrong, how likely (high/medium/low), what you'll do now, and one owner. A quick way to find them is Atlassian's pre-mortem: the team silently writes down what could go wrong, then votes on the biggest threats and gives each top risk an action with an owner. A risk without an owner is a worry, not a plan.
7. **Say how the team communicates.** Where daily talk happens (channel), how progress is shared (a weekly written update, its day and author), when the group meets, and where decisions are written down. Asana's kickoff guide lists this as a standard part of the kickoff.
8. **List open questions and decided items.** Open questions get an owner and a date. Things already decided go in one line each, so the kickoff doesn't reopen them.

## Output format

```markdown
# [Project name] — kickoff brief

**Accountable owner:** [one name] · **Start:** [date] · **Target date:** [date or "no date set"]

## Goal
[1–2 sentences: what changes, for whom, and why now.]

## Success measure
- **Primary:** [number + date, or yes/no test]
- **Guardrails:** [what must not get worse, or remove]

## Scope
| In scope | Out of scope |
|---|---|
| [item] | [item] |

## Milestones
| Milestone (a finished thing) | Owner | Date |
|---|---|---|
| [milestone] | [name] | [date] |

## Roles (RACI-lite)
| Workstream | Responsible | Accountable | Consulted | Informed |
|---|---|---|---|---|
| [workstream] | [name] | [one name] | [names] | [names or group] |

## Risks
| Risk | Likelihood | What we do now | Owner |
|---|---|---|---|
| [risk] | [high/medium/low] | [action] | [name] |

## How we communicate
- **Day to day:** [channel]
- **Progress:** [written update, day, author]
- **Meetings:** [which, how often]
- **Decisions logged in:** [place]

## Already decided
- [decision, one line]

## Open questions
- [question] — [owner], by [date]
```

## Example

**Input:** "We're moving our 120 active customers from the old billing tool (Billwise) to Stripe. Kickoff is 7 April; Billwise gets cancelled on 30 June. Dana runs it, Marco does the integration, Aisha handles customer emails, finance (Lena) needs to sign off on the new invoice template by 2 May. CEO Tom wants it done before the price change on 1 July. Marco's plan: 5 internal test accounts billing correctly in Stripe test mode by 25 April, all customers live by 13 June. Aisha sends the notice by 16 May, then a reminder 1 week before each customer moves, and phones the top 20 accounts. Not doing: cancelled customers' history, a self-serve billing portal, accounting system changes. Worries: saved cards might not transfer; someone billed twice in the switch month. Failed payments must not go up. We talk in #billing-migration, Dana writes a Friday update, we meet 20 minutes on Tuesdays, decisions go in the project doc. We already decided no price changes during the migration. Lena wants to know if we keep Billwise read-only for a month after cancelling."

**Output:**

```markdown
# Billing migration to Stripe — kickoff brief

**Accountable owner:** Dana · **Start:** 7 April · **Target date:** 30 June

## Goal
Move all customers from Billwise to Stripe before the price change on 1 July, so the new prices go live on one system and Billwise can be cancelled.

## Success measure
- **Primary:** 120 of 120 active customers billed through Stripe by 30 June.
- **Guardrails:** No customer is charged twice or missed in any month; failed payments stay at or below the current monthly level.

## Scope
| In scope | Out of scope |
|---|---|
| Moving active subscriptions and saved cards | Price changes (decided: none during migration) |
| New invoice template approved by finance | Moving cancelled customers' history |
| Customer emails before and after the move | A new self-serve billing portal |
| Cancelling Billwise | Changes to the accounting system |

## Milestones
| Milestone (a finished thing) | Owner | Date |
|---|---|---|
| Stripe test mode billing 5 internal accounts correctly | Marco | 25 April |
| Invoice template signed off | Lena | 2 May |
| Customer notice email sent | Aisha | 16 May |
| All 120 customers live on Stripe | Marco | 13 June |
| Billwise cancelled | Dana | 30 June |

## Roles (RACI-lite) [draft, confirm at kickoff]
| Workstream | Responsible | Accountable | Consulted | Informed |
|---|---|---|---|---|
| Integration and data move | Marco | Dana | Lena | Tom |
| Invoices | Marco | Lena | Dana | Aisha |
| Customer emails | Aisha | Dana | Lena | Tom |

## Risks
| Risk | Likelihood | What we do now | Owner |
|---|---|---|---|
| Saved cards don't transfer and customers must re-enter them | Medium | Proposed: ask Billwise support whether a card export to Stripe is supported | Marco |
| A customer is billed in both systems in the switch month | Medium | Proposed: turn off each Billwise subscription the same day it starts in Stripe | Marco |
| Customers ignore the notice and miss the change | High | Send the notice by 16 May and a reminder 1 week before each move; Aisha phones the top 20 accounts | Aisha |

## How we communicate
- **Day to day:** #billing-migration
- **Progress:** written update every Friday by Dana
- **Meetings:** 20-minute check-in Tuesdays
- **Decisions logged in:** the "Decisions" section of the project doc

## Already decided
- No price changes during the migration.

## Open questions
- Do we keep Billwise read-only for a month after cancelling? — Lena, by [date to set at kickoff]
```

## Checks before you send

- [ ] The goal says why now, and the success measure is a number with a date or a yes/no test.
- [ ] Out of scope has at least 3 items that someone could plausibly ask for.
- [ ] Every milestone is a finished thing with one owner and a date.
- [ ] Each RACI row has exactly one Accountable, and the project has one named owner at the top.
- [ ] Every risk has an action taken now and one owner.
- [ ] No name, date, or number appears that isn't in the input; gaps are marked "[no date set]" or listed as open questions.
- [ ] It fits on one page.

## Common mistakes

- Writing a success measure nobody can check ("improve billing"). Ask what number or test would prove it.
- Leaving out-of-scope empty. That's where the arguments start in week 4.
- Two Accountable people on one row. If two people must both agree, make one Accountable and the other Consulted.
