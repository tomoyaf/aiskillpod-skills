---
name: interview-questions
description: Writes structured interview questions (behavioral and situational) mapped to a role's competencies, each with prepared follow-up probes and what strong and weak answers sound like, plus a list of questions never to ask, such as age, family plans, religion, national origin, or health before an offer. Use when you prepare an interview, need questions for a competency, or want to check a question list for illegal or useless questions.
---

# Structured interview questions

Every candidate for the role gets the same questions, in the same order, with the same follow-ups, so answers can be compared. Two kinds work: behavioral questions ask what the candidate did before, situational questions ask what they would do in a job-related scenario (Google re:Work; Canada's Public Service Commission). Brainteasers and personal questions are not tied to the job, so our default is to leave them out.

## When to use

- Before an interview stage, once the competencies for the role are set.
- An interviewer asks "what should I ask?" or keeps improvising.
- You want an existing question list checked for bias, legal risk, or questions that predict nothing.
- Not for user research or customer interviews; use interview-guide for those.

## What you need

- The competencies for this stage and what "good" looks like (from the role scorecard or interview-scorecard). If missing, ask for the role's 3 outcomes and derive 4 competencies, marked "[assumption]".
- The stage length. If missing, assume 45 minutes: 4 questions, about 8 minutes each with probes, and 10 minutes for the candidate's questions and the close (our default).
- The candidate's level. The Public Service Commission recommends behavioral questions when applicants have relevant experience; for people with little of it, lean on situational questions (our default).

## Steps

1. **Write one main question per competency.** Behavioral: "Tell me about a time you…" with a specific, job-like situation. Situational: a short scenario from the real job and "What would you do?". Our default: 2 behavioral and 1 to 2 situational per stage. No hypotheticals about the candidate's personal life.
2. **Prepare 3 follow-up probes for each.** Probes dig into the same answer: "What did you do yourself?", "What did you decide not to do, and why?", "What was the result, and how do you know?". re:Work describes predetermined follow-ups designed to understand the candidate's thought process; the Public Service Commission recommends writing probes at the same time as the questions and says probing should not introduce new topics.
3. **Describe strong and weak answers.** Strong: a specific situation, the candidate's own actions ("I", not only "we"), a reasoned trade-off, and a result. Weak: general statements ("I always…"), no example, blame without action, or no result. Tie each to the 1–4 anchors if a scorecard exists.
4. **Cut questions not tied to the job.** Remove brainteasers, "Where do you see yourself in 5 years?", "What's your biggest weakness?" and anything not tied to a competency (our default). The Public Service Commission calls questions unrelated to job performance, such as hobbies, social activities or political beliefs, inappropriate; remove them.
5. **Check against the never-ask list.** Remove any question that asks directly or indirectly about a protected characteristic. The EEOC says pre-hire questions should be limited to what's essential to judge qualification, prohibits pre-offer disability questions, and treats questions about marital status, children, child care arrangements or future childbearing plans as possible evidence of discrimination. GOV.UK says UK employers must not ask about protected characteristics, whether a candidate is married, single or in a civil partnership, or whether they have or plan to have children; health questions are allowed only in narrow cases, such as asking whether a candidate needs help with the interview. Elsewhere [check: local law / HR]. Replace with the job-related version (see table).
6. **Order and time the set.** Open with an easy behavioral question, keep the same order for every candidate, and leave about 10 minutes for the candidate's questions and the close (our default). Before the interview, tell candidates the format, what will be assessed and how long it takes, so they can ask for adjustments; the Public Service Commission advises this.

## Output format

```markdown
# Interview questions — [role], [stage], [length]

**Competencies at this stage:** [list]  
Ask every candidate the same questions, in this order. Use only the probes listed.

## 1. [Competency] — [behavioral / situational]
**Ask:** "[question]"  
**Probes:**
- [probe]
- [probe]
- [probe]
**Strong answer:** [specific signs]  
**Weak answer:** [specific signs]

[Repeat for each question]

## Candidate's questions — [minutes]

## Never ask
| Don't ask | Why | Ask instead (if job-related) |
|---|---|---|
| [question] | [protected characteristic it touches] | [job-related version] |

## Removed from the draft
- "[question]" — [reason]
```

## Example

**Input:** Stage: peer interview (45 minutes) with Sofia, support lead at Lumen Ledger, for a Customer Onboarding Manager. Competencies: customer communication, process building. Manager's draft questions: "Are you a parent? Our launches run late", "What's your biggest weakness?", "How many golf balls fit in a plane?"

**Output:**

```markdown
# Interview questions — Customer Onboarding Manager, peer interview, 45 minutes

**Competencies at this stage:** customer communication, process building  
Ask every candidate the same questions, in this order. Use only the probes listed.

## 1. Customer communication — behavioral
**Ask:** "Tell me about a time you had to explain a complicated setup step to a customer who wasn't technical."  
**Probes:**
- What exactly did you say or send?
- How did you know they understood?
- What would you change next time?
**Strong answer:** names the customer type and the step; describes plain wording, an example or screenshot, and a check ("I asked her to do it while I watched"); result stated.  
**Weak answer:** "I'm a great communicator"; no example; blames the customer.

## 2. Customer communication — situational
**Ask:** "An accountant emails: 'Your import broke my client's ledger, I'm moving to a competitor.' You find it was a user error. What do you write back?"  
**Probes:**
- What do you say first?
- How do you handle the user error without blaming them?
- Who else do you tell?
**Strong answer:** acknowledges the impact, fixes or offers to fix first, explains the cause neutrally, offers a call, logs it for the product team.  
**Weak answer:** leads with "this was your error"; no next step.

## 3. Process building — behavioral
**Ask:** "Tell me about a process you created that other people used without you."  
**Probes:**
- What problem did it solve, and how did you know?
- What did the first version get wrong?
- Who uses it now?
**Strong answer:** a real document or checklist, why it was needed, a revision after feedback, evidence of use.  
**Weak answer:** describes a process their manager wrote; no evidence anyone used it.

## 4. Process building — situational
**Ask:** "Every onboarding at our company is done differently by whoever runs it. In your first month, what do you do?"  
**Probes:**
- What do you look at first?
- What do you standardise, and what do you leave alone?
- How do you get support to use it?
**Strong answer:** reviews recent onboardings, finds common steps, drafts a short playbook, tests with one teammate, measures go-live time.  
**Weak answer:** writes a long manual alone; no test or measure.

## Candidate's questions — 10 minutes

## Never ask
| Don't ask | Why | Ask instead (if job-related) |
|---|---|---|
| Are you a parent? / Do you plan to have children? | Family status; EEOC and GOV.UK guidance | "Some launches run late into the evening [confirm how often and how late]. Can you work that schedule?" |
| How old are you? / When did you graduate? | Age | Nothing; ask about the relevant experience |
| Where are you from originally? | National origin | "Do you have the right to work in the UK?" [check: local law / HR] |
| Do you have any health conditions? | Disability; no pre-offer questions in the US | "Do you need any adjustments for this interview?" |
| What religion are you? / What holidays do you observe? | Religion | Nothing |

## Removed from the draft
- "Are you a parent? Our launches run late" — family status; replaced by the schedule question asked of everyone.
- "What's your biggest weakness?" — not tied to a competency.
- "How many golf balls fit in a plane?" — brainteaser; not tied to any competency.
```

## Checks before you send

- [ ] Every question maps to one named competency.
- [ ] Each question has 3 prepared probes that stay on the same topic.
- [ ] Strong and weak answers are described as observable signs, not adjectives.
- [ ] No question touches age, sex, pregnancy or family, race, national origin, religion, disability or health, or marital status, directly or indirectly.
- [ ] Schedule or travel questions are asked of every candidate, worded the same.
- [ ] The order and timing fit the stage length.

## Common mistakes

- Asking the parent question only of women. The EEOC calls asking such questions of women and not men clearly discriminatory; don't ask it of anyone.
- Improvising follow-ups that change the topic. Then candidates answer different interviews.
- "What would you do?" for every question. Mix in past behavior for candidates who have it.
