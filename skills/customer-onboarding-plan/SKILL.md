---
name: customer-onboarding-plan
description: Writes an onboarding plan for a new customer account with success criteria in the customer's terms, milestones to first value with owners and dates, a kickoff call agenda, a check-in cadence, and the risks to watch. Use when a deal closes and the account moves to customer success, when someone asks for an onboarding plan, a kickoff agenda, a "mutual success plan", an implementation plan, or a time-to-value plan for a new customer.
---

# Customer onboarding plan

Onboarding ends when the customer gets the result they bought, not when the setup checklist is done. The plan starts from that result, works back to the fewest milestones that reach it, and gives every milestone an owner on each side and a date.

## When to use

- A deal just closed and the account is handed to customer success or onboarding.
- Before a kickoff call with a new customer.
- An existing customer is re-launching after a failed rollout.
- Not for onboarding a new employee: use employee-onboarding-plan.

## What you need

- Why they bought: the problem, the goal, and how they'll measure it, from sales notes or the contract. If no measurable goal is given, propose one and mark it "[assumption: confirm at kickoff]".
- Who's involved: their sponsor, day-to-day owner, users; your CSM and anyone else.
- What's in scope: plan, seats, integrations, data to import, start date, any deadline they mentioned.
- Your product's usual setup steps. If not given, ask once, then write steps as "[setup step]".

## Steps

1. **Write success criteria in the customer's terms.** 1 to 3 outcomes, each measurable and dated: "Support team answers 80% of chats inside the tool by 30 April". Not "Product is set up". Take the measure from the sales notes; if you made it up, mark it as an assumption.
2. **Define first value.** The first moment the customer sees the outcome in small form: the first report sent, the first campaign live, the first invoice paid through the tool. Aim to reach it in the fewest steps; our default target is within 30 days of kickoff, sooner for small accounts.
3. **Plan milestones back from first value.** 3 to 6 milestones, each a result, not an activity ("Contacts imported and checked", not "Import call"). Each gets a customer owner, a vendor owner, a due date, and what done looks like. Put anything that needs their IT, legal, or security team first: those take the longest.
4. **Write the kickoff agenda.** 30 to 45 minutes: introductions and roles, their goal in their words, confirm success criteria, walk the milestone plan, agree the cadence and the communication channel, list open questions and access needed. Send it before the call.
5. **Set the cadence.** Our default: a weekly 30-minute check-in until first value, then every 2 weeks until success criteria are met, then a monthly or quarterly review. Name the channel (email, shared Slack) and who sends the recap.
6. **List the risks.** 2 to 5 risks with an early sign and a response: no named day-to-day owner, data not ready, IT approval slow, users not invited, sponsor absent from kickoff. If the sponsor won't attend kickoff, flag it as the first risk.

## Output format

```markdown
# Onboarding plan: [Customer] — [start date]

**Their goal:** [one sentence in their words]
**Sponsor:** [name, role] · **Day-to-day owner:** [name] · **Our CSM:** [name]

## Success criteria
| Outcome | Measure | By |
|---|---|---|
| [Outcome] | [Number or observable result] | [Date] |

**First value:** [the moment] — target [date]

## Milestones
| # | Milestone (result) | Their owner | Our owner | Due | Done when |
|---|---|---|---|---|---|
| 1 | [...] | [Name] | [Name] | [Date] | [...] |

## Kickoff agenda ([length] minutes)
1. [Item] — [minutes]

## Cadence
- [Meeting, frequency, length, who sends the recap, channel]

## Risks
| Risk | Early sign | Response |
|---|---|---|
| [...] | [...] | [...] |

## Open questions
- [Question] — [who answers]
```

## Example

**Input:**

> Closed: Northpoint Dental Group, 6 clinics, 40 seats of our scheduling tool. Sponsor: Rui Tan (COO). Day-to-day: Beth Owusu (ops manager). Sales notes: they want to cut no-shows using SMS reminders; "no-shows are around 12%, we'd love under 8% by summer". Need to import patient calendars from their old system. Start 3 March. CSM: Arjun.

**Output:**

```markdown
# Onboarding plan: Northpoint Dental Group — 3 March

**Their goal:** Cut no-shows from about 12% to under 8% with SMS reminders.
**Sponsor:** Rui Tan, COO · **Day-to-day owner:** Beth Owusu · **Our CSM:** Arjun

## Success criteria
| Outcome | Measure | By |
|---|---|---|
| Fewer no-shows | No-show rate under 8% across 6 clinics | 30 June [assumption: confirm "summer" at kickoff] |
| Clinics live | All 6 clinics booking in the tool | 4 April |

**First value:** First clinic sends SMS reminders for a full week — target 21 March

## Milestones
| # | Milestone (result) | Their owner | Our owner | Due | Done when |
|---|---|---|---|---|---|
| 1 | Export from old system received | Beth | Arjun | 7 March | File checked, no missing fields |
| 2 | Pilot clinic calendars imported | Beth | Arjun | 12 March | Beth confirms 1 week of bookings match |
| 3 | SMS reminders on at pilot clinic | Beth | Arjun | 14 March | First reminders sent |
| 4 | Remaining 5 clinics imported and live | Beth | Arjun | 4 April | All 40 users logged in |
| 5 | No-show baseline and first read | Rui | Arjun | 2 May | Report compares April to the 12% baseline |

## Kickoff agenda (45 minutes)
1. Introductions and roles — 5
2. Your goal in your words; confirm the 8% target and date — 10
3. Walk the milestone plan — 15
4. Data export: format and who sends it — 5
5. Cadence and channel — 5
6. Open questions and access needed — 5

## Cadence
- Weekly 30-minute check-in, Beth and Arjun, until 21 March; Arjun sends the recap by email the same day.
- Every 2 weeks after that until 30 June; Rui joins monthly.

## Risks
| Risk | Early sign | Response |
|---|---|---|
| Old-system export slow | No file by 7 March | Arjun offers a call with their old vendor |
| Clinics don't adopt | Fewer than 5 users active in a clinic after a week | Short training at that clinic |
| Baseline unclear | Nobody can confirm the 12% | Measure March in the tool as the baseline |

## Open questions
- Does "by summer" mean 30 June? — Rui
- Which clinic pilots first? — Beth
```

## Checks before you send

- [ ] Every success criterion is measurable and dated, and assumptions are marked.
- [ ] First value is a moment the customer sees, with a target date.
- [ ] Every milestone is a result with an owner on each side and a due date.
- [ ] The kickoff agenda fits the stated length.
- [ ] Risks have an early sign someone can notice, not just a name.
- [ ] No goal, number, or date appears that isn't in the input or marked as an assumption.

## Common mistakes

- Milestones that are meetings ("Training session"). Name the result the meeting should produce.
- Only vendor owners. If the customer owns nothing, the plan slips the first time they're busy.
- Setting success as "fully adopted". Use their number.
