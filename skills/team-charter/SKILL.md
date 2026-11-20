---
name: team-charter
description: Drafts a team charter - mission, the customers the team serves, what it owns and explicitly doesn't, roles, working agreements, rituals and communication channels, how decisions are made and escalated, and the metrics it is judged on. Use when a manager or founder is forming a new team, splitting or merging teams, onboarding a new lead, fixing "who owns this?" confusion, or asks for a team charter, team mission, or working agreement.
---

# Team charter

A charter answers the questions new members and neighboring teams ask in their first week: what is this team for, what does it own, how does it work, and how do decisions get made. Notre Dame's Mendoza College of Business template names four key components (purpose, decision-making process, roles and responsibilities, working agreements); we add scope boundaries and metrics, because "who owns this?" is where startup teams lose the most time.

## When to use

- A new team forms, two teams merge or split, or a new manager takes over.
- Requests keep landing on the wrong team, or two teams think they own the same thing.
- A team wants to write down how it works before adding people.
- Not for a single project's plan (use project-kickoff-brief) or for one person's task (use delegation-brief).

## What you need

- The team's name, members, and manager.
- What the team is expected to achieve and for whom.
- What it currently does, and what other teams expect from it.
- How it works today: meetings, channels, tools. If unknown, propose defaults and mark them "[proposal]".

## Steps

1. **Write the mission in one sentence.** Who it serves and what changes for them: "Help new customers reach their first report within a day of sign-up." No values words without an outcome.
2. **Name the customers.** Internal and external, in priority order. If two customers conflict, the order says who wins.
3. **Draw the boundaries.** List what the team owns (systems, processes, decisions) and what it doesn't, with the team that does own it. Every "not ours" item names an owner, or is flagged "owner unknown".
4. **Set roles.** Named people for recurring roles (lead, on-call, facilitator, who answers requests from other teams). Measurable, not titles: "answers #team-requests within 1 working day".
5. **Write working agreements.** 5 to 8 specific norms: working hours and time zones, response times by channel, how feedback is given, meeting-free time, how conflict is raised. Each one is something a member could break, so it can be checked.
6. **Set rituals and channels.** Each meeting with purpose, cadence, length, and attendees; drop any meeting without a purpose. Each channel with what goes there. Say when async beats a meeting.
7. **Define decision-making.** Default method by decision type (one person decides after consulting, the team votes, consensus for the few decisions everyone must support), who has the final say, and the fallback if consensus fails. Add the escalation path.
8. **Pick 2 to 4 metrics.** What the team is judged on, with current value and target where known. Add when the charter is reviewed; our default is quarterly and whenever someone joins or leaves.

## Output format

```markdown
# [Team name] charter
**Members:** [names, roles] · **Manager:** [name] · **Last reviewed:** [date]

## Mission
[One sentence: who we serve and what changes for them]

## Who we serve (in priority order)
1. [Customer] — [what they need from us]

## What we own
- [System / process / decision]

## What we don't own
| Area | Owner |
|---|---|
| [area] | [team or "owner unknown"] |

## Roles
| Role | Person | Responsibility (measurable) |
|---|---|---|

## Working agreements
1. [Specific, checkable norm]

## Rituals and channels
| Meeting / channel | Purpose | Cadence / use | Who |
|---|---|---|---|

## How we decide
- [Decision type] → [method], final say: [person]
- If we can't agree: [fallback]
- Escalate to: [person], when [condition]

## Metrics
| Metric | Now | Target |
|---|---|---|

## Review
Next review: [date] · Also when someone joins or leaves.
```

## Example

**Input:** "New Lifecycle team: Mina (lead), Joel (email marketer), Sofia (data analyst). Job: get trials to convert. Today they send onboarding emails and nurture campaigns. Product team owns in-app onboarding. Sales sometimes asks them for one-off email blasts. Remote, EU and US East. Trial-to-paid is 11%."

**Output:**

```markdown
# Lifecycle team charter
**Members:** Mina (lead), Joel (email marketer), Sofia (data analyst) · **Manager:** Mina · **Last reviewed:** 4 Nov

## Mission
Turn more trial sign-ups into paying customers through the messages they get outside the product.

## Who we serve (in priority order)
1. Trial users — the right message at the right step
2. Sales — warm, qualified trials to follow up
3. Product — data on where trials drop off

## What we own
- Onboarding and nurture email sequences
- Trial-stage segmentation and reporting
- Decisions on email frequency for trial users

## What we don't own
| Area | Owner |
|---|---|
| In-app onboarding | Product |
| One-off sales email blasts | Sales (we advise on timing only) |
| Customer newsletters after purchase | owner unknown |

## Roles
| Role | Person | Responsibility (measurable) |
|---|---|---|
| Lead | Mina | Sets priorities; final say on sends to all trials |
| Requests owner | Joel | Answers #lifecycle-requests within 1 working day [proposal] |
| Reporting | Sofia | Weekly trial funnel report by Monday 12:00 CET [proposal] |

## Working agreements
1. Core overlap hours: 15:00–17:00 CET; meetings only in that window. [proposal]
2. Slack replies within 4 working hours; email within 1 working day. [proposal]
3. Every send to more than 1,000 people gets a second pair of eyes. [proposal]
4. Disagreements go to a 15-minute call, not a long thread. [proposal]
5. Feedback is given privately first, within a week of the event. [proposal]

## Rituals and channels
| Meeting / channel | Purpose | Cadence / use | Who |
|---|---|---|---|
| Planning | Pick the week's experiments | Monday, 30 min [proposal] | All |
| Funnel review | Read the numbers, decide changes | Thursday, 30 min [proposal] | All |
| #lifecycle-requests | Requests from other teams | Async [proposal] | Joel triages |

## How we decide
- Copy and timing → Joel decides after consulting the team [proposal]
- Changes to all-trial sequences → Mina decides after consulting Sofia's data [proposal]
- If we can't agree: Mina decides within 2 working days [proposal]
- Escalate to: Head of Growth [proposal], when another team disputes ownership

## Metrics
| Metric | Now | Target |
|---|---|---|
| Trial-to-paid | 11% | [proposal: 14% by end of Q1] |
| Trial email unsubscribe rate | [check: baseline] | [proposal: under 0.5% per send] |

## Review
Next review: 4 Feb · Also when someone joins or leaves.
```

## Checks before you send

- [ ] The mission is one sentence and names who is served.
- [ ] Every "don't own" item names an owner or says "owner unknown".
- [ ] Every working agreement is specific enough to notice when it's broken.
- [ ] Decision-making names who has the final say and the fallback when there's no consensus.
- [ ] Metrics have a current value or are marked to measure; targets not given are marked "[proposal]".

## Common mistakes

- A mission made of values ("excellence, ownership"). Say who it serves and what changes.
- Listing only what the team owns. The "don't own" list prevents most of the friction.
- Choosing consensus for every decision. Save it for the few decisions everyone must support.
