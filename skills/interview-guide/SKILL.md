---
name: interview-guide
description: Writes a user interview guide for a research question, with a screener, warm-up, questions about past behavior in the style of The Mom Test (no hypotheticals, no leading questions, no pitching), follow-up probes, and a wrap-up. Use when someone plans customer interviews, discovery calls, or user research and asks for interview questions, a discussion guide, a script, or a screener.
---

# User interview guide

Good interviews collect facts about what people did last time, not opinions about what they might do. The guide follows the 3 rules of Rob Fitzpatrick's The Mom Test: talk about their life, not your idea; ask about specific past behavior, not hypotheticals; and look for real commitment of time, reputation, or money. Every question in the guide asks about a specific past event. If a question can be answered with "yes, I'd use that", it gets rewritten.

## When to use

- Before a round of user interviews, discovery calls, or customer research.
- When someone has a list of questions and wants them fixed so they don't lead.
- When you need a screener to recruit the right people.
- Not for usability tests of a prototype (those need tasks, not questions). Not for job interviews: use interview-questions.

## What you need

- The research question: what decision the interviews should inform. If missing, ask once; it's the one input you can't skip.
- Who to talk to: role, situation, company size. If missing, propose a profile and mark "[assumption]".
- Interview length. Default to 30 minutes.
- Optional: hypotheses the team holds, so the guide can test them without naming them.

## Steps

1. **Turn the research question into 3 to 5 learning goals.** Each is something you want to know about past behavior: "How do they handle late invoices today?", "What did they try before?". Drop any goal that is really "would they buy our idea?".
2. **Write a screener.** 4 to 6 questions that qualify people by recent behavior ("In the last month, how many times did you ...?"), not by self-description. Mark which answers qualify and which disqualify. Hide what you're testing so people don't answer to get in.
3. **Write a 3-minute warm-up.** Role, typical week, where the topic fits. No product talk.
4. **Write core questions about the last time.** Anchor each on a specific recent event: "Tell me about the last time you ...". NN/g recommends this form because a particular incident jogs memory better than a question about the general process. Ask what happened, what they did, what it cost them (time, money, stress), and what they tried before. Split the time left after the intro, warm-up and wrap-up evenly across the learning goals (our default): in 30 minutes that is about 23 minutes, 5 to 8 per goal.
5. **Remove bad questions.** Leading questions compromise the data (NN/g), and compliments and "I'd buy that" cost the speaker nothing. Rewrite any question that is hypothetical ("Would you ...?"), leading ("Don't you find ... frustrating?"), about the future ("How much would you pay?"), or yes/no. Replace with a past-behavior version: "How much did you spend on this last year?".
6. **Add probes under each question.** 2 to 3 short follow-ups: "Why was that?", "What happened next?", "Can you show me?", "How did you decide?". Add one probe for when they mention a workaround: "How did you set that up?".
7. **Write the wrap-up.** Ask what you should have asked, who else to talk to, and whether you may follow up. An intro to a colleague or a second meeting is a small commitment; note who agrees. Pitching, if at all, happens after the interview ends, never in the guide.

## Output format

```markdown
# Interview guide: [research question]

**Length:** [minutes] · **Who:** [profile] · **Decision this informs:** [decision]

## Learning goals
1. [goal]

## Screener
| Question | Qualifies | Disqualifies |
|---|---|---|
| [behavior question] | [answer] | [answer] |

## Intro (1 min)
[Script: who you are, that there are no wrong answers, you're not selling, recording consent.]

## Warm-up (3 min)
- [question]

## Core questions ([minutes])
### Goal 1: [goal]
- [Tell me about the last time ...]
  - Probe: [follow-up]
  - Probe: [follow-up]

## Wrap-up (3 min)
- What should I have asked that I didn't?
- Who else deals with this that I should talk to?
- May I follow up if I have a question?

## Questions we removed
- [bad question] → [rewritten version]
```

## Example

**Input:** "We're thinking of building auto reminders for late invoices. Who should we talk to and what do we ask? 30 minutes."

**Output:**

```markdown
# Interview guide: How do small service businesses get late invoices paid today?

**Length:** 30 min · **Who:** owners of agencies or freelancers who send 5 or more invoices a month [assumption] · **Decision this informs:** whether to build automatic payment reminders

## Learning goals
1. What do they do when an invoice goes past due?
2. How much time or money does chasing cost them?
3. What have they tried to make it easier?

## Screener
| Question | Qualifies | Disqualifies |
|---|---|---|
| How many invoices did you send last month? | 5 or more | Fewer than 5 |
| In the last 3 months, did a client pay you late? | Yes | No |
| Who chases late payments in your business? | Me, or someone I manage | An outside collections agency |
| What tools do you use to send invoices? | Any (record answer) | — |

## Intro (1 min)
Thanks for your time. I'm learning how people handle invoices, not selling anything. There are no wrong answers. May I record this for my notes?

## Warm-up (3 min)
- What does your business do, and who are your clients?
- Walk me through a normal week. Where does billing fit?

## Core questions (23 min)
### Goal 1: What they do when an invoice is late
- Tell me about the last invoice that was paid late.
  - Probe: When did you notice it was late?
  - Probe: What did you do first?
- How did you word the reminder?
  - Probe: Can you show me the message you sent?
  - Probe: How long after you sent it did they pay?

### Goal 2: What chasing costs
- How long did it take, from noticing to getting paid?
  - Probe: What else didn't get done in that time?
  - Probe: How many times did you follow up in that time?
- In the last year, how many invoices were never paid?
  - Probe: What did you do about them in the end?
  - Probe: What changed with that client afterwards?

### Goal 3: What they've tried
- What have you tried to make this easier?
  - Probe: How did you set that up?
  - Probe: Why did you stop, or why do you keep using it?

## Wrap-up (3 min)
- What should I have asked that I didn't?
- Who else deals with this that I should talk to?
- May I follow up if I have a question?

## Questions we removed
- "Would you use automatic reminders?" → "What have you tried to make this easier?"
- "Isn't chasing payments frustrating?" → "Tell me about the last invoice that was paid late."
- "How much would you pay for this?" → "How much did you spend on this last year, and on what?"
```

## Checks before you send

- [ ] No question starts with "Would you", "Do you think", or "How likely".
- [ ] Every core question is anchored on a specific past event or a real number.
- [ ] No question names the team's idea or feature.
- [ ] The screener qualifies by recent behavior, with qualify and disqualify answers.
- [ ] Timings add up to the stated interview length.
- [ ] Each core question has at least 2 probes.

## Common mistakes

- Asking people to predict their own behavior. They will be polite and wrong.
- Describing the idea halfway through "to get feedback". From then on, the answers are about the pitch.
- Writing 30 questions for 30 minutes. NN/g calls for a few well-designed, open-ended questions; our default is 1 or 2 core questions per learning goal, each with 2 to 3 probes.
