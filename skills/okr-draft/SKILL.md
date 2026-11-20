---
name: okr-draft
description: Drafts quarterly OKRs from a strategy, goals, or planning notes - 1 to 3 objectives, 2 to 4 measurable key results each that measure outcomes rather than tasks, with a baseline, a target, one owner per KR, and a quality check that flags tasks posing as key results. Use when a founder, manager, or team asks to write OKRs, set quarterly goals, turn a strategy into objectives and key results, or review draft OKRs.
---

# OKR draft

Good OKRs tell a team what to stop doing. An objective says where we want to be; a key result is a number that proves we got there, not a list of things we'll ship. If a key result can be "done" without anything changing for a customer or the business, it's a task. OKRs are also not a performance evaluation: don't tie them to anyone's rating.

## When to use

- Turning a strategy doc, board goals, or planning notes into quarterly OKRs.
- Reviewing a draft set of OKRs before a planning meeting.
- Cascading company OKRs into one team's OKRs.
- Not for a project plan or task list: OKRs sit above that. Use quarterly-planning for the full plan.

## What you need

- The strategy or goals for the period (company OKRs, a strategy memo, or a founder's notes).
- The team and quarter the OKRs are for.
- Current numbers for anything you'll measure. If a baseline is missing, write "[baseline: to measure in week 1]" and make measuring it the owner's first action. Never invent a baseline.
- Who is on the team, so each KR gets one owner.

## Steps

1. **Pick 1 to 3 objectives.** Our default for a startup team is 3 at most; Google's re:Work guide says to pick 3 to 5 and warns that more can over-extend teams and diffuse effort. Each objective is a qualitative endpoint a team member could repeat from memory ("Make onboarding something customers finish on day 1"), never ongoing activity ("keep hiring"). If the input has 5 goals, rank them by impact, keep the top 3, and list the rest under "Not this quarter".
2. **Write 2 to 4 key results per objective.** Our default; re:Work suggests around 3 per objective. Each KR is a metric moving from a baseline to a target by a date: "Day-1 onboarding completion from 34% to 60%". Use the form "[metric] from [baseline] to [target]". Key results must be measurable and verifiable at the end of the quarter.
3. **Test each KR: outcome or output?** Ask "If we did this and nothing else changed, would we celebrate?" "Launch the new onboarding flow" fails: it's an output. Rewrite it as the change the launch should cause. Move outputs to an "Initiatives" list under the objective.
4. **Set ambition.** Mark each KR as committed (expected to be fully met) or aspirational, also called stretch (the path isn't known yet), the two types What Matters describes. Google's re:Work guide grades OKRs from 0.0 to 1.0, puts the sweet spot at 60 to 70%, and says someone who consistently fully attains their objectives isn't setting them ambitiously enough. If every KR is committed, say so; if every KR is stretch, nobody knows what's promised.
5. **Give each KR one owner.** A person, never a team. The owner reports progress; they don't have to do all the work.
6. **Check for gaps and conflicts.** A KR that can be gamed needs a counter-metric (raise trial sign-ups → watch trial-to-paid). Two KRs that pull against each other get a note on which wins.
7. **Run the quality check** in the output and fix every failed line before sending.

## Output format

```markdown
# OKRs — [team], [quarter]

## Objective 1: [qualitative, memorable sentence]
Why now: [one line linking to the strategy]

| KR | Baseline | Target | Type | Owner |
|---|---|---|---|---|
| 1.1 [metric] | [number or "to measure in week 1"] | [number] by [date] | committed / stretch | [person] |

Counter-metric: [metric that must not get worse, if a KR can be gamed]
Initiatives (outputs, not KRs): [project], [project]

## Not this quarter
- [Goal left out] — [why]

## Quality check
- [ ] 3 objectives or fewer, 2–4 KRs each
- [ ] Every KR is a number with a baseline and target
- [ ] No KR is a task ("launch", "build", "hire", "write")
- [ ] Every KR has one named owner
- [ ] Mix of committed and stretch
```

## Example

**Input:** "Growth team, Q3. Strategy: we're losing trials because setup is confusing. Goals: improve activation, launch new onboarding, hire a lifecycle marketer, get more trial sign-ups, start a referral program. Activation (connected first data source in 7 days) is 31%. Trial sign-ups ~900/month. Team: Mina (PM), Joel (lifecycle), Ana (eng lead)."

**Output:**

```markdown
# OKRs — Growth, Q3

## Objective 1: New trials reach their first result in the first week
Why now: confusing setup is the main reason trials don't convert.

| KR | Baseline | Target | Type | Owner |
|---|---|---|---|---|
| 1.1 Trials that connect a data source within 7 days | 31% | 50% by 30 Sep | committed | Mina |
| 1.2 Median time from sign-up to first connected source | [baseline: to measure in week 1] | under 1 day by 30 Sep | stretch | Ana |
| 1.3 Setup-related support tickets per 100 trials | [baseline: to measure in week 1] | half of baseline by 30 Sep | committed | Joel |

Counter-metric: trial-to-paid rate must not drop below current.
Initiatives (outputs, not KRs): new onboarding flow, setup emails rewrite.

## Objective 2: More of the right people start a trial

| KR | Baseline | Target | Type | Owner |
|---|---|---|---|---|
| 2.1 Monthly trial sign-ups | ~900 | 1,150 by Sep | stretch | Joel |

Counter-metric: share of sign-ups that activate (KR 1.1) must not fall.
Initiatives: referral program pilot.

## Not this quarter
- "Hire a lifecycle marketer" — a task, not an outcome; tracked in the hiring plan.

## Quality check
- [ ] 3 objectives or fewer, 2–4 KRs each — not yet: Objective 2 has 1 KR; add a second or merge it into Objective 1.
- [x] Every KR is a number with a baseline and target (2 baselines measured in week 1)
- [x] No KR is a task — "launch new onboarding" moved to initiatives
- [x] Every KR has one named owner
- [x] Mix of committed and stretch
```

## Checks before you send

- [ ] No KR starts with launch, build, ship, hire, write, or complete.
- [ ] Every baseline comes from the input or is marked "to measure in week 1".
- [ ] Every KR has exactly one named person as owner.
- [ ] Each objective has 2 to 4 KRs, or the gap is flagged in the quality check.
- [ ] Goals left out are listed under "Not this quarter" with a reason.

## Common mistakes

- Writing the team's project list as KRs. That's a roadmap.
- Targets with no baseline ("increase NPS to 50"). Nobody can tell if 50 is ambitious.
- 5 objectives. That's a list of everything, which tells the team nothing about priority.
