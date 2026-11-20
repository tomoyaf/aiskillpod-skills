---
name: churn-risk-note
description: Writes a churn-risk note on one customer account from usage data, support tickets, and call notes. Gives a risk level backed by evidence, a root-cause hypothesis, a save plan with an owner and date for each step, and what to tell the customer. Use when an account looks at risk of cancelling, a renewal is coming up, usage dropped, a champion left, or someone asks for an "account health" or "churn risk" write-up.
---

# Churn-risk note

A churn-risk note gets the right person to act on one account this week. It states the risk level, shows the evidence behind it, names the most likely cause, and assigns each save step to a named person with a date. Evidence beats feeling: every risk claim points at a number, a ticket, or a quote.

## When to use

- Usage dropped, a champion left, or a renewal is within 90 days and something feels off.
- Before a save call or an escalation to a manager.
- During a weekly at-risk account review.
- Not for a portfolio-wide churn analysis across many accounts: use feedback-themes for the voice-of-customer side.

## What you need

- Usage data: logins, active users, key feature use, ideally the last 3 months against the 3 before.
- Recent tickets and their status.
- Call or meeting notes, emails with the customer.
- Account facts: plan, seats, contract value, renewal date, main contact and champion.
- If one is missing, proceed and write "[missing: ...]" in the evidence. Don't infer usage from tickets or tickets from usage.

## Steps

1. **List the signals.** Pull every signal from the input into one list, each with its source: "Active users 42 → 18 (usage, Jul vs Apr)". Common ones: active users down 30% or more, a key feature unused for 30 days, 3 or more open tickets, an unresolved ticket older than 14 business days, champion left, budget or competitor mentioned, a missed meeting, a seat downgrade request.
2. **Set the risk level with our default rubric.** Edit it to your team's health score if you have one. High: 2 or more strong signals (champion left, competitor or cancel mentioned, usage down 50% or more) or renewal within 60 days with any strong signal. Medium: 1 strong signal or 3 or more weak ones. Low: weak signals only. State which signals set the level.
3. **Write a root-cause hypothesis.** One sentence: what changed for the customer, not what we see. "Their ops lead who ran the rollout left in June; nobody owns the tool now." Add the evidence for it and what would prove it wrong. If 2 causes fit, list both and say which you'd test first.
4. **Plan the save.** 2 to 5 steps. Each has one owner (a person, never "CS"), a date, and what done looks like. The first step happens within 5 business days. Match the step to the cause: a lost champion needs a new sponsor, not a feature demo.
5. **Write what to tell the customer.** 2 to 4 sentences for the next message or call opening: name what you noticed in their terms, offer one concrete thing, ask one question. Never say "we noticed your usage dropped" as an accusation; say what you want to help with.
6. **State the stakes.** Contract value and renewal date from the input. If missing, write "[check: value]". Don't estimate.

## Output format

```markdown
# Churn risk: [Account] — [date]

**Risk:** [High / Medium / Low] — [one line: the signals that set it]
**Renewal:** [date] · **Value:** [amount or "[check: value]"] · **Owner:** [account owner]

## Evidence
| Signal | Source | Detail |
|---|---|---|
| [Signal] | [usage / ticket / call / email] | [number, date, or quote] |

## Root-cause hypothesis
[One sentence.] Evidence: [...]. Would be wrong if: [...].

## Save plan
| Step | Owner | Due | Done when |
|---|---|---|---|
| [Verb-first step] | [Name] | [Date] | [Observable result] |

## What to tell the customer
> [2–4 sentences]

## Missing
- [Data not provided that would change the call]
```

## Example

**Input:**

> Today: Wednesday 9 September 2026. Account: Brightwell Clinics, 25 seats, renews 30 November, 18,000 per year. Usage: weekly active users 21 → 7 (August vs May). Scheduling feature: no use since 12 August. Tickets: 2 open about calendar sync, oldest 19 business days. Call notes 2 Sept: "Our practice manager Joel left; Hana is covering." Hana asked if the plan can drop to 10 seats.

**Output:**

```markdown
# Churn risk: Brightwell Clinics — 9 September

**Risk:** High — champion left, usage down 67%, seat downgrade asked, renewal in 82 days
**Renewal:** 30 November · **Value:** 18,000 per year · **Owner:** [account owner]

## Evidence
| Signal | Source | Detail |
|---|---|---|
| Champion left | Call, 2 Sept | "Our practice manager Joel left; Hana is covering." |
| Active users down 67% | Usage | 21 → 7 weekly, May vs August |
| Key feature unused | Usage | Scheduling: no use since 12 August |
| Stale tickets | Tickets | 2 open on calendar sync, oldest 19 business days |
| Downgrade asked | Call, 2 Sept | Hana asked about 10 seats |

## Root-cause hypothesis
Joel ran scheduling; since he left, the calendar sync issue blocks Hana and nobody is driving use. Evidence: scheduling has been unused since 12 August and his exit was reported on 2 Sept [check: when Joel left]; both open tickets are on sync. Would be wrong if: usage fell before Joel left.

## Save plan
| Step | Owner | Due | Done when |
|---|---|---|---|
| Fix or work around calendar sync and close both tickets | [support lead] | 11 Sept | Hana confirms sync works |
| 30-minute setup call with Hana to re-run scheduling | [account owner] | 16 Sept | Scheduling used again that week |
| Ask Hana who owns the tool long term | [account owner] | 16 Sept | A named owner |
| Review seat count with usage after 3 weeks | [account owner] | 7 Oct | Seat number agreed on data |

## What to tell the customer
> Hana, thanks for picking this up after Joel's move. The calendar sync problem is on us; we're fixing it this week and I'll confirm when it's done. Could we take 30 minutes next week to get scheduling running for your team again? Then we can size seats on what you actually use.

## Missing
- Usage before May, to confirm the drop started after Joel left.
- Joel's leaving date, to compare with 12 August.
```

## Checks before you send

- [ ] The risk level names the signals that set it, using the rubric.
- [ ] Every evidence row has a source and a number, date, or quote.
- [ ] The hypothesis says what would prove it wrong.
- [ ] Every save step has one named owner and a date; the first is within 5 business days.
- [ ] No contract value, date, or usage number appears that isn't in the input.
- [ ] The customer message offers help, not an accusation about usage.

## Common mistakes

- Calling an account High because it "feels quiet". Show the signal or lower the level.
- A save plan of discounts. Price is rarely the cause; fix the cause first.
- "CS to follow up" as an owner. Name the person.
