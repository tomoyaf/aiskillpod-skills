---
name: reference-check
description: Prepares a reference call guide for one candidate and turns the call notes into a short summary with examples, the rehire answer, and red flags. Covers consent, verifying scope, behavioral questions tied to the role, and questions never to ask a reference. Use when you are about to check references, need reference check questions, want a script for a call with a former manager, or have notes from reference calls to summarize.
---

# Reference check

> Not legal advice. Rules on references differ by country and state; mark anything local "[check: local law / HR]".

A reference call is useful only when it produces examples of what the candidate actually did. Ask open questions tied to the role, let silences run, and write down what was said, not your impression of it.

## When to use

- A candidate is at the final stage and you want to speak to 2 or 3 people who worked with them.
- You need a call script for a former manager, peer, or direct report.
- You have notes from several reference calls and need one summary for the hiring decision.
- Not for background checks, credit checks, or criminal record checks. Those follow separate legal processes; send them to HR.

## What you need

- The role and the 3 to 5 things the job needs most (from the job post or scorecard). If missing, ask for them; without them the questions turn generic.
- The candidate's written permission and the referees they named. If permission is missing, stop and get it first.
- What the candidate said about each job: title, dates, scope, team size. You verify against this.
- Optional: concerns from the interviews you want to test. Turn each into an open question, never a leading one.

## Steps

1. **Get consent and pick referees.** Get the candidate's permission in writing before any call (Acas says to have the applicant's permission before requesting references), and don't contact a current employer without explicit permission. Acas advises asking for references at the final stage, when making a job offer, and making a conditional offer before contacting a current employer, so the candidate's search isn't exposed early "[check: local law / HR]". Our default is 3 referees, at least 1 a former manager. SHRM's article quotes a recruiter who asks for 3, favours supervisors, and prefers people who worked with the candidate daily in the last 5 to 7 years.
2. **Write the call guide.** Our default is 6 to 8 questions in 20 minutes. Use the same core questions for every candidate for the role, so answers compare. Every question must relate to the job.
3. **Verify scope first.** Confirm the relationship, dates, title, and what the candidate owned (team size, budget, results). A mismatch with what the candidate told you is a finding, not a verdict; note it and ask the candidate.
4. **Ask for examples.** Use open, behavioral questions ("How would you describe her performance on X? Can you give an example?"), not yes/no ones. SHRM's article recommends open-ended, behavioral questions, and quotes a recruiter who lets the question hang so the referee recalls specific instances.
5. **Ask the rehire question last.** "Would you hire or work with them again? Why or why not?" Write down the exact words and any pause or hedge.
6. **Stay inside the line.** Our default: treat a reference call like an interview. Never ask about age, race, religion, national origin, sex, pregnancy or family plans, marital status, disability, health or sick days, or genetic information. The EEOC says employers may not make pre-offer inquiries about disability, and calls race, sex, national origin, age and religion irrelevant to hiring decisions; don't ask a referee what you can't ask the candidate. Salary history and criminal record questions are restricted in many places: "[check: local law / HR]". If a referee volunteers such information, don't record it and move on.
7. **Read for red flags.** Patterns worth noting: answers that are general and not very positive, or neutral (SHRM's article says this can signal mediocre performance), and what the referee leaves unsaid; no example for a core skill; a hesitant or conditional rehire answer; scope that doesn't match the candidate's account; a referee who isn't who the candidate said. A former employer's no-comment policy is not a red flag; ask for another referee.
8. **Summarize.** One block per referee, then a combined read against the role's needs. Quote, don't paraphrase, for anything negative.

## Output format

```markdown
# Reference check — [candidate], [role]

_Consent received: [date, how]. Prepared for the hiring decision; not legal advice._

## Call guide (same for every referee)
1. How do you know [candidate], and when did you work together?
2. What was [candidate] responsible for? (team size, budget, results)
3. [Role need 1]: how did [candidate] do at this? Can you give an example?
4. [Role need 2]: tell me about a time it went well and a time it didn't.
5. What did you rely on [candidate] for? Where did they need support?
6. What should their next manager know to help them do their best work?
7. Would you hire or work with [candidate] again? Why or why not?

## Referee [n]: [name], [relationship], [dates]
- **Scope verified:** [matches / differs: what]
- **Examples:** [one line per example, quoted where possible]
- **Rehire:** "[exact words]"
- **Flags:** [pattern, or "none"]

## Combined read
| Role need | Evidence (referee) | Strength |
|---|---|---|
| [need] | [example] (R[n]) | [strong / some / none] |

**Follow-ups for the candidate:** [questions, or "none"]
```

## Example

**Input:** Hiring a customer success lead at Fernhill Analytics. Needs: owning renewals, calm escalations, coaching juniors. Candidate Dana Okafor gave written consent by email on 2 November. Her CV says she owned 40 accounts, about 1.1M ARR. Referee 1: Marcus Lee, her manager at Bluestem Software 2022–2025. Notes: "Owned 40 accounts, ~1.1M ARR. Saved the Arden account after an outage, ran daily calls for 2 weeks. Coaching: hmm, she mostly worked alone. Rehire? Yes, for an IC role, definitely." Referee 2, a former direct report, is not called yet.

**Output:**

```markdown
# Reference check — Dana Okafor, Customer success lead

_Consent received: 2 November, by email. Prepared for the hiring decision; not legal advice._

## Referee 1: Marcus Lee, former manager, Bluestem Software, 2022–2025
- **Scope verified:** Matches. 40 accounts, about 1.1M ARR.
- **Examples:** Kept the Arden account after an outage; "ran daily calls for 2 weeks".
- **Rehire:** "Yes, for an IC role, definitely."
- **Flags:** Rehire answer is conditional on an individual role; no coaching example ("she mostly worked alone").

## Combined read
| Role need | Evidence (referee) | Strength |
|---|---|---|
| Owning renewals | 40 accounts, 1.1M ARR (R1) | strong |
| Calm escalations | Arden outage, daily calls (R1) | strong |
| Coaching juniors | No example (R1) | none |

**Follow-ups for the candidate:** Ask Dana for a coaching example; ask the second referee (a former direct report) question 5.
```

## Checks before you send

- [ ] Written consent is recorded, and no current employer was called without it.
- [ ] Every question relates to the job; none touches a protected characteristic, health, or family.
- [ ] Each referee block has at least 1 example or says "no example given".
- [ ] The rehire answer is quoted word for word.
- [ ] Negative points are quoted, not paraphrased, and volunteered protected information is left out.
- [ ] Local rules on salary history and records are marked "[check: local law / HR]".

## Common mistakes

- Asking "Was she a good worker?" A yes tells you nothing. Ask for the example.
- Treating one lukewarm referee as a verdict. Look for the same pattern across 2 or more.
- Reading a company's no-comment policy as a warning sign.
