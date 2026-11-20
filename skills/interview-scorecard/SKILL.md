---
name: interview-scorecard
description: Builds a structured interview scorecard (interview rubric, rating sheet) from a role scorecard or job post - 4 to 6 job-related competencies, behavioral anchors for ratings 1 to 4, evidence fields for what the candidate said, and a written hire or no-hire rule set before interviews. Use when you set up an interview loop, interviewers keep scoring on gut feel, or you want every candidate judged on the same scale.
---

# Structured interview scorecard

A scorecard makes interviewers rate the same things on the same scale, from what the candidate said. Google's re:Work guide and the US Office of Personnel Management (OPM) both describe the core: the same predetermined questions, one rating scale, and shared standards for what an acceptable answer looks like. re:Work says structured interviews result in increased predictive validity and decreased differences between demographic groups, citing academic research.

## When to use

- You're setting up interviews for a role and need one sheet every interviewer fills in.
- Debriefs end in "I liked her" vs "I didn't" with nothing written down.
- You want the decision rule agreed before anyone meets a candidate.
- Not for performance reviews of current staff; those rate work done, not interview answers.

## What you need

- The role scorecard (outcomes, must-haves, competencies) or a job post. If you only have a title, ask for the 3 outcomes the hire must deliver; without them, run role-intake first.
- The interview loop: stages and who interviews. If missing, make one scorecard covering all competencies and note "[assign stages]".
- Optional: the questions already chosen; otherwise pair this with interview-questions.

## Steps

1. **Choose 4 to 6 competencies.** Each comes from an outcome or must-have in the role scorecard and can be observed in an answer: "Prioritises under conflicting deadlines", not "Smart". Drop anything that is personality, background, or "fit" without a definition. Mark which interviewer owns each one.
2. **Write the 1–4 anchors.** Our default scale: 1 Poor, 2 Borderline, 3 Solid, 4 Outstanding (the levels re:Work's rubric uses). For each competency write what an answer at each level contains, as observable behaviour: "Names the trade-off, says what they dropped and why, gives the result." Level 3 is the bar for the role, not "average". No even-split middle option; a 4-point scale forces a side (our default).
3. **Add evidence fields.** Under each competency: the question asked, what the candidate said (close to verbatim, as Canada's Public Service Commission advises for interview notes), and the rating. Notes record what was said, not the interviewer's opinion of it.
4. **Set the scoring rules.** Each interviewer rates on their own, right after the interview, before talking to anyone: the Public Service Commission advises independent ratings shortly after the interview, then a group consensus. A rating with an empty evidence field doesn't count. "Not assessed" is allowed and is not a 1.
5. **Write the hire/no-hire rule before interviews.** Our default: hire only if every must-have competency is 3 or higher across the loop, with no 1 anywhere, and at least one 4. Any 2 on a must-have is a no-hire unless the debrief names evidence that resolves it. Adjust the rule to the role, then freeze it.
6. **Add a job-related-only note.** The sheet has no field for age, family, health, nationality, religion, or appearance, and interviewers write nothing about them. The EEOC advises avoiding questions that could reveal race, color, sex, national origin, religion, age, disability or ancestry, and says employers are explicitly prohibited from making pre-offer inquiries about disability. Outside the US [check: local law / HR].

## Output format

```markdown
# Interview scorecard — [role], [stage]

**Candidate:** [name] · **Interviewer:** [name] · **Date:** [date]  
Rate on your own, right after the interview, before any debrief. Write what the candidate said, not your impression. Job-related evidence only.

**Scale:** 1 Poor · 2 Borderline · 3 Solid (meets the bar) · 4 Outstanding · N/A Not assessed

## [Competency 1] — [must-have / nice-to-have]
| Rating | What the answer shows |
|---|---|
| 4 | [observable behaviour] |
| 3 | [observable behaviour, the bar] |
| 2 | [observable behaviour] |
| 1 | [observable behaviour] |

**Question asked:** [question]  
**Evidence (what they said):** [notes]  
**Rating:** [1–4 / N/A]

[Repeat for 4–6 competencies]

## Overall
**Hire/no-hire rule:** [rule, written before interviews]  
**My recommendation:** [Strong hire / Hire / No hire / Strong no hire]  
**Main reason, citing evidence above:** [one or two lines]
```

## Example

**Input:** Role scorecard for a Customer Onboarding Manager at Lumen Ledger. Competencies: project ownership, customer communication, process building, judgment under pressure; project ownership and judgment are must-haves. Stage: hiring manager interview with Dev Patel (owns project ownership and judgment). Candidate: Ana Ruiz, interviewed 12 November. Dev's notes: on a slipping onboarding she said "I had 6 accounts going live in March", built a shared plan per account with weekly dates, saw in week 2 that one customer's data export was 2 weeks late, moved their training earlier and the import later; that account went live on day 34 instead of 30, the other 5 on time. On 3 customers wanting the same go-live week with room for 2: ask each customer's deadline driver, rank by contract date and revenue, offer the third a date and a self-serve checklist, tell her manager the same day. Dev rates project ownership 3 and judgment 4.

**Output (two competencies shown, then the overall section):**

```markdown
# Interview scorecard — Customer Onboarding Manager, hiring manager interview

**Candidate:** Ana Ruiz · **Interviewer:** Dev Patel · **Date:** 12 November  
Rate on your own, right after the interview, before any debrief. Write what the candidate said, not your impression. Job-related evidence only.

**Scale:** 1 Poor · 2 Borderline · 3 Solid (meets the bar) · 4 Outstanding · N/A Not assessed

## Project ownership — must-have
| Rating | What the answer shows |
|---|---|
| 4 | Ran several customer projects with dates; spotted a slip early, changed the plan, and gives the measured result. |
| 3 | Ran a customer project end to end with a plan and dates; chased blockers; says how it ended. |
| 2 | Took part in projects but someone else set dates or chased blockers; result vague. |
| 1 | No example of owning a project, or describes the team's work only as "we". |

**Question asked:** Tell me about a customer onboarding you owned that was at risk of slipping.  
**Evidence (what they said):** "I had 6 accounts going live in March." Built a shared plan per account with weekly dates. Noticed one customer's data export was 2 weeks late in week 2; moved their training earlier and the import later. Went live on day 34 instead of 30; other 5 on time.  
**Rating:** 3

## Judgment under pressure — must-have
**Question asked:** Three customers want to go live the same week and you can support two. What do you do?  
**Evidence (what they said):** Would ask each customer's deadline driver, rank by contract date and revenue, offer the third a date and a self-serve checklist. Would tell her manager the same day.  
**Rating:** 4

## Overall
**Hire/no-hire rule:** every must-have 3 or higher across the loop, no 1, at least one 4.  
**My recommendation:** Hire  
**Main reason, citing evidence above:** owned 6 live accounts with dated plans (3); clear ranking rule and early escalation in the go-live clash (4).
```

## Checks before you send

- [ ] There are 4 to 6 competencies, each traced to an outcome or must-have.
- [ ] Every rating level has an observable description, and 3 is the bar.
- [ ] Each competency has a question, an evidence field, and a rating.
- [ ] The hire/no-hire rule is written and dated before the first interview.
- [ ] No field or anchor touches a protected characteristic or "fit" without a definition.
- [ ] The sheet tells interviewers to rate alone before the debrief.

## Common mistakes

- Anchors like "good communication". Describe what the candidate says or does at each level.
- Averaging scores into one number. A 4 on a nice-to-have doesn't cancel a 1 on a must-have.
- Changing the rule after meeting a candidate everyone liked. Change it for the next search, not this one.
