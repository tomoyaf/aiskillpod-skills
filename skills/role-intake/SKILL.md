---
name: role-intake
description: Runs the hiring-manager intake meeting (recruiter intake, kickoff for a new hire) and turns it into a role scorecard - why the role exists, 3 to 5 measurable outcomes, must-have skills, level, deal breakers, the interview loop, a sourcing plan, pay range and timeline. Use when a manager says we need to hire someone, before writing a job post, or when a search is stuck because nobody agreed what good looks like.
---

# Role intake and scorecard

Most bad hires start with a vague role: "a strong marketer". The intake turns the manager's picture into outcomes, a short list of must-haves, and a plan everyone signs off on. The scorecard it produces drives the job post, the interview questions and the debrief.

## When to use

- A hiring manager asks for a new role or a backfill.
- Before writing a job post or booking any interviews.
- A search has run for weeks and the team keeps disagreeing about candidates.
- Not for deciding whether to hire at all (budget, headcount plans); bring that decision made.

## What you need

- The manager's notes or the meeting transcript. If there's no meeting yet, produce the agenda and question list from Step 1 and stop.
- Budget: the pay range the company has approved. If missing, write "[range needed from finance]" and flag it as a blocker.
- Where the role can be based (office, remote, countries). If missing, ask; it changes pay rules and sourcing.
- Optional: an old job description, the team's org chart, names of people who did the role well.

## Steps

1. **Run the meeting with a fixed agenda.** 30 to 45 minutes (our default). Ask: Why are we hiring now, and is this new or a backfill? What are the top 3 things this person must deliver in the first 90 days, and what by the end of year 1? Which skills are required and which are nice to have? What would rule someone out, and why? How will we assess them? What's the range, the start date, the reporting line? All but the year-1 question come from Workable's intake question set; year 1 is our default.
2. **Write the mission in one sentence.** What the role exists to achieve, in words the manager would repeat: "Get our first 50 customers live within 30 days of signing."
3. **Turn duties into 3 to 5 outcomes.** Each has a verb, a measure and a date: "Cut onboarding time from 60 days to 30 by month 9". If the manager can't put a number on one, keep it and write "[measure to agree]".
4. **Cut the must-haves to 5 or fewer.** Keep a skill only if the manager would reject an otherwise strong candidate who lacks it and it can't be learned in the first 3 months (our default). Move the rest to nice-to-haves. Write skills, not years or degrees, and keep each tied to an outcome. The EEOC says pre-employment inquiries should be limited to those essential for determining if a person is qualified; we apply the same test to criteria (our default). Acas warns that wording such as "recent graduate" or "highly experienced" can discriminate against age.
5. **Set the level and deal breakers.** Level: scope, autonomy, who they manage, and the pay range. Deal breakers are job-related only (can't work the required shift, lacks a required licence). Never a protected characteristic, "culture fit" without a definition, or a proxy such as age, graduation year or family plans; if one comes up, take it out and note "[removed: not job-related]".
6. **Pick 4 to 6 competencies for the interviews.** Each must-have and outcome maps to at least one competency, and each competency to one stage of the loop. Google's re:Work guide describes the basis of structured interviewing: the same vetted questions for every candidate, one scale, and decisions against predetermined qualifications.
7. **Design the loop and sourcing plan.** Our default loop: recruiter screen, hiring manager interview, a work sample, a peer interview, and references, each owning named competencies and one interviewer. Sourcing: name at least 2 channels (Acas advises advertising in at least 2 ways or places), plus referrals and 10 to 20 named target profiles or companies. Set a timeline per stage.
8. **Get sign-off.** Send the scorecard to the manager and every interviewer. Changes to must-haves after interviews start need a written reason, because they move the bar mid-search.

## Output format

```markdown
# Role scorecard — [title], [team]

**Hiring manager:** [name] · **Recruiter:** [name] · **Signed off:** [date or "pending"]  
**Why now:** [new role / backfill, one line]  
**Level:** [level, scope, reports to, manages] · **Location:** [where] · **Pay range:** [range or "[range needed from finance]"]

## Mission
[One sentence.]

## Outcomes
| # | Outcome | Measure | By |
|---|---|---|---|
| 1 | [verb-first outcome] | [number or "[measure to agree]"] | [month] |

## Must-haves (max 5)
- [Skill] — needed for outcome [#]

## Nice-to-haves
- [Skill]

## Deal breakers (job-related only)
- [Item]

## Competencies and interview loop
| Competency | What good looks like | Stage | Interviewer |
|---|---|---|---|
| [Name] | [one line] | [stage] | [name] |

## Sourcing plan
- Channels: [at least 2]
- Referrals: [who to ask]
- Target profiles/companies: [list]

## Timeline
| Stage | Target date |
|---|---|

## Open items
- [Blockers, "[measure to agree]", "[removed: not job-related]" notes]
```

## Example

**Input (intake notes):** Dev Patel, VP Customer at Lumen Ledger (bookkeeping software, 70 people, London). "We need an onboarding manager. Customers take 60 days to go live, that's killing expansion. Someone who's done SaaS onboarding, can run projects, talks to accountants. Must have 5 years experience, a finance degree, and be a young energetic type who fits in. Budget £55–65k. Start in 8 weeks. Interviews: me, Sofia from support, a case study."

**Output:**

```markdown
# Role scorecard — Customer Onboarding Manager, Customer team

**Hiring manager:** Dev Patel · **Recruiter:** [name] · **Signed off:** pending  
**Why now:** new role; go-live takes 60 days and slows expansion  
**Level:** individual contributor, reports to VP Customer, manages no one · **Location:** London (hybrid) [assumption] · **Pay range:** £55,000–£65,000

## Mission
Get new customers live fast enough that they expand in their first year.

## Outcomes
| # | Outcome | Measure | By |
|---|---|---|---|
| 1 | Own every new customer's onboarding plan | 100% of new accounts have a dated plan | Month 2 |
| 2 | Cut time to go-live | 60 days to 30 | Month 9 |
| 3 | Build a repeatable onboarding playbook | Used by support for all accounts | Month 6 |
| 4 | Raise first-year expansion | [measure to agree] | Month 12 |

## Must-haves (max 5)
- Has run software onboarding or implementation projects for business customers — outcomes 1, 2
- Plans and tracks several customer projects at once — outcome 1
- Explains setup clearly to finance professionals — outcomes 2, 4

## Nice-to-haves
- Knows bookkeeping or accounting workflows.
- Has written a playbook others use.

## Deal breakers (job-related only)
- Can't be in the London office 2 days a week [assumption, confirm with Dev].

## Competencies and interview loop
| Competency | What good looks like | Stage | Interviewer |
|---|---|---|---|
| Project ownership | Sets dates, chases blockers, hits go-live | Manager interview | Dev Patel |
| Customer communication | Turns jargon into steps an accountant follows | Peer interview | Sofia |
| Process building | Writes a playbook from messy cases | Case study | Dev Patel |
| Judgment under pressure | Chooses what to drop when 3 launches collide | Manager interview | Dev Patel |

## Sourcing plan
- Channels: careers page and LinkedIn; one accounting-software community job board.
- Referrals: ask the support and sales teams.
- Target profiles/companies: onboarding or implementation managers at UK finance and HR software companies.

## Timeline
| Stage | Target date |
|---|---|
| Post live | Week 1 |
| Screens done | Week 3 |
| Offer | Week 6 |
| Start | Week 8 |

## Open items
- "5 years experience" became the experience itself; "finance degree" moved out (not needed for the outcomes).
- [removed: not job-related] "young energetic type": implies an age preference.
- "Fits in": define as a competency or drop.
- Outcome dates and the 30-day target are proposals; confirm with Dev.
- Add a reference check stage and an interviewer for it.
```

## Checks before you send

- [ ] Every outcome has a measure and a date, or "[measure to agree]".
- [ ] There are 5 must-haves or fewer, each linked to an outcome.
- [ ] No deal breaker or criterion refers to a protected characteristic or a proxy for one.
- [ ] Every competency has one stage and one named interviewer.
- [ ] The pay range is filled in or flagged as a blocker.
- [ ] The manager has a clear request to sign off.

## Common mistakes

- Copying the last job description. It lists duties, not outcomes, and nobody can score against duties.
- "Culture fit" as a criterion. Define the behaviour you mean or leave it out.
- Five interviewers all asking about the same thing. Give each stage its own competencies.
