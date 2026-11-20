---
name: candidate-summary
description: Summarizes a candidate's interview notes, scorecards and CV into a one-page debrief brief - evidence per competency with who saw it, rating spread, concerns, open questions to resolve, and a recommendation kept separate from the evidence - with no inferences about age, family, health, origin or other protected characteristics. Use when you prepare a hiring debrief, write up a candidate for a decision, or compare interviewers' notes.
---

# Candidate summary for a debrief

The debrief should argue about evidence, not impressions. This summary puts every interviewer's evidence under the competency it supports, shows where they disagree, and lists what nobody found out. The recommendation comes last, in its own section, so readers can check it against the evidence.

## When to use

- After the interview loop, before the debrief meeting.
- A hiring manager asks "give me the case for and against".
- Interviewers' notes are scattered across docs and the ATS.
- Not for the rejection or offer message; use rejection-email or offer-email.

## What you need

- Each interviewer's scorecard or notes, with ratings. If a scorecard is missing, list that interviewer under "Missing" and don't guess their view.
- The role scorecard: competencies, must-haves, and the hire/no-hire rule. If no rule exists, write "[no rule agreed]" and don't apply one.
- The CV or application. Use it only for job-related facts (roles, dates, work done).
- Optional: work sample results and reference notes.

## Steps

1. **Collect ratings before reading opinions.** List each interviewer's rating per competency as they submitted it. Ratings should be made independently right after each interview; Canada's Public Service Commission advises this, then a consensus discussion. If a rating was changed after the interviewers talked, note it.
2. **Put the evidence under each competency.** For each one: what the candidate said or did, quoted or close to it, and who saw it. Notes should record what the candidate said, not the interviewer's judgement of it (Public Service Commission). Drop adjectives without evidence ("seemed sharp") or list them under "Unsupported impressions".
3. **Strip anything not job-related.** Remove comments on age, looks, accent, family, health, religion, nationality, or how someone "would fit" demographically, and any guess at these from the CV (graduation year, gaps, names, photos). The EEOC calls race, sex, national origin, age and religion irrelevant to hiring decisions. Note "[removed: not job-related]" with a count, not the content.
4. **Flag disagreements and gaps.** A spread of 2 or more points on one competency is a disagreement to discuss first (our default). A must-have competency nobody assessed is a gap, not a pass.
5. **List concerns and open questions.** A concern names the competency and the evidence behind it. An open question says how to answer it: a reference question, a follow-up call, a work sample.
6. **Apply the rule, then write the recommendation.** Check the ratings against the agreed hire/no-hire rule and state the result. Then give a recommendation in its own section, citing only evidence above. If evidence and rule disagree, say so; don't bend the rule.

## Output format

```markdown
# Candidate summary — [name], [role]

**Loop:** [stages and interviewers] · **Prepared:** [date] · **Missing:** [scorecards not in, or "none"]

## Ratings
| Competency | Must-have? | [Interviewer 1] | [Interviewer 2] | [Interviewer 3] | Spread |
|---|---|---|---|---|---|
| [name] | [yes/no] | [1–4/N/A] | | | [max–min] |

## Evidence by competency
### [Competency]
- [What the candidate said or did] — [who saw it, stage]
- [Counter-evidence, if any] — [who]

## Disagreements to discuss first
- [Competency]: [ratings] — [what each side's evidence is]

## Concerns
- [Competency]: [concern] — evidence: [quote or fact]

## Open questions
- [Question] — how to answer: [reference / call / task]

## Not used
- Unsupported impressions: [list or "none"]
- [removed: not job-related] × [count]

---
## Rule check
[Hire/no-hire rule] → [met / not met / "[no rule agreed]"], because [ratings].

## Recommendation
[Hire / No hire / Hold for open questions] — [2–3 lines citing evidence above]
```

## Example

**Input:** Notes on Ana Ruiz for Customer Onboarding Manager at Lumen Ledger. Dev (manager): project ownership 3 ("6 accounts in March, one slipped 4 days, re-planned"), judgment 4 ("ranks by contract date and revenue, escalates same day"). Sofia (peer): customer communication 2 ("explained imports in jargon at first, then fixed when I pushed"), process building 3 ("wrote a go-live checklist her old team still uses"), also "lovely, probably has young kids so may not do late launches". Case study (Dev): process building 3. References not yet taken. Prepared 14 November. Rule: every must-have 3 or higher across the loop, no 1, at least one 4. Must-haves: project ownership, customer communication, judgment.

**Output:**

```markdown
# Candidate summary — Ana Ruiz, Customer Onboarding Manager

**Loop:** manager interview (Dev), peer interview (Sofia), case study (Dev) · **Prepared:** 14 November · **Missing:** references not yet taken

## Ratings
| Competency | Must-have? | Dev | Sofia | Case study | Spread |
|---|---|---|---|---|---|
| Project ownership | yes | 3 | N/A | N/A | — |
| Customer communication | yes | N/A | 2 | N/A | — |
| Process building | no | N/A | 3 | 3 | 0 |
| Judgment under pressure | yes | 4 | N/A | N/A | — |

## Evidence by competency
### Project ownership
- "6 accounts in March, one slipped 4 days, re-planned" — Dev, manager interview

### Customer communication
- "Explained imports in jargon at first, then fixed when I pushed" — Sofia, peer interview

### Process building
- "Wrote a go-live checklist her old team still uses" — Sofia, peer interview
- Case study rated 3 — Dev, case study

### Judgment under pressure
- "Ranks by contract date and revenue, escalates same day" — Dev, manager interview

## Disagreements to discuss first
- None with 2 or more points; customer communication was assessed by one interviewer only.

## Concerns
- Customer communication: default to jargon — evidence: Sofia's note; corrected when pushed.

## Open questions
- Does she write plainly for customers without prompting? — how to answer: ask for a customer email she wrote, or a reference question to her last manager.

## Not used
- Unsupported impressions: "lovely"
- [removed: not job-related] × 1

---
## Rule check
Every must-have 3 or higher, no 1, at least one 4 → not met, because customer communication is 2.

## Recommendation
Hold for open questions — project ownership meets the bar (3) and judgment is strong (4), but the rule isn't met on customer communication (2). Resolve with a writing sample before deciding.
```

## Checks before you send

- [ ] Every rating comes from a submitted scorecard; missing ones are listed, not guessed.
- [ ] Every evidence line names who saw it and is a fact or quote, not an adjective.
- [ ] Nothing refers to or guesses at age, family, health, origin, religion, sex, race or other protected characteristics.
- [ ] Must-haves nobody assessed are shown as gaps.
- [ ] The rule check uses the rule agreed before interviews.
- [ ] The recommendation sits below the evidence and cites only it.

## Common mistakes

- Leading with the recommendation. Readers anchor on it and stop checking the evidence.
- Passing on the content of a removed comment "for context". Remove it and count it; raise the conduct with HR if needed.
- Treating "not assessed" as a pass. It's an open question.
