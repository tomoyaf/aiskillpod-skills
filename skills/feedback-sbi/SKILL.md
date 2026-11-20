---
name: feedback-sbi
description: Writes feedback with the Situation-Behavior-Impact (SBI) model plus a clear request and an intent question, in positive and corrective versions, sized for a Slack message or an in-person conversation. Use when a manager or teammate asks how to give feedback, praise someone specifically, tell a colleague something isn't working, phrase constructive or critical feedback, or write a kudos message.
---

# Feedback with SBI

Feedback lands when the person can picture the moment, sees what they did, and understands what it caused. The Center for Creative Leadership's SBI model does that in 3 sentences: Situation, Behavior, Impact. We add a request (what to keep or change). For corrective feedback we also use CCL's SBII extension: a question about their intent, which turns it into a two-way conversation.

## When to use

- Recognizing specific work, in Slack or in person.
- Raising something that isn't working, before it becomes a pattern.
- Rewriting a draft message that sounds vague ("great job!") or harsh ("you were rude").
- Not for a formal warning or a pattern that's already been raised twice: use difficult-conversation-prep.

## What you need

- What happened: when, where, and what the person did or said.
- The effect it had, on you, the team, a customer, or the work.
- Positive or corrective, and the channel (Slack, in person, email). If not given, infer from the content and say which you chose.
- If the behavior is a guess or second-hand ("I heard that..."), ask once what was actually observed. Don't write SBI on a rumor.

## Steps

1. **Situation: name the moment.** A specific time and place: "In Tuesday's 10am client call", not "lately" or "last week". One situation per piece of feedback.
2. **Behavior: describe only what a camera would record.** Words said, actions taken, things not done. No adjectives about the person and no guesses about motives: "You interrupted Priya twice while she presented the budget", not "You were rude".
3. **Impact: say what it caused.** The effect on you, the team, a customer, or the work. For positive feedback, name why it mattered ("the client signed the renewal that afternoon"). For corrective feedback, use "I" when it's your reaction ("I lost my train of thought") and facts when it's business impact.
4. **Add the request.** Positive: "Keep doing this on the next launch." Corrective: one specific change ("Let people finish, then add your point"). One request only.
5. **For corrective feedback, ask about intent.** "What were you hoping to do there?" Then listen; the answer may change the request. Skip this for Slack praise.
6. **Fit the channel.** Slack praise: 2 to 3 sentences, public if the person likes public recognition. Corrective: in person or a private call, never in a public channel; Slack is only for setting up the talk ("Got 10 minutes today? Want to talk about the client call").

## Output format

```markdown
**Type:** [positive / corrective] · **Channel:** [Slack / in person / email]

**Situation:** [specific time and place]
**Behavior:** [observable actions or words]
**Impact:** [effect on people, work, or customers]
**Request:** [keep doing / one specific change]
**Intent question (corrective only):** [open question]

**Ready to send / say:**
> [The full message in natural sentences, 2–5 sentences]
```

## Example

**Input:** "My designer Kenji turned around the pricing page mockups overnight after the CEO changed direction on Monday, which let us keep the Thursday launch. Also, he's been really negative in critiques — yesterday he said 'this is just bad' about Mara's onboarding flow and she stopped presenting."

**Output:**

```markdown
**Type:** positive · **Channel:** Slack (team channel)

**Situation:** Monday night, after the pricing direction changed.
**Behavior:** You reworked the pricing page mockups overnight.
**Impact:** We kept the Thursday launch date.
**Request:** Keep it up, and flag it next time you're working late so we can rebalance.

**Ready to send / say:**
> Kenji, thank you for reworking the pricing mockups overnight after Monday's change. That's the reason we're still launching Thursday.
```

```markdown
**Type:** corrective · **Channel:** in person

**Situation:** Yesterday's design critique, during Mara's onboarding flow.
**Behavior:** You said "this is just bad" without saying what wasn't working.
**Impact:** Mara stopped presenting, and we didn't get through the 3 screens we needed feedback on.
**Request:** In critiques, name the specific problem and what you'd try instead.
**Intent question (corrective only):** What were you seeing in the flow that bothered you?

**Ready to send / say:**
> In yesterday's critique, when Mara showed the onboarding flow, you said "this is just bad" without saying what wasn't working. She stopped presenting, and we didn't get through the 3 screens. What were you seeing that bothered you? Next time, can you name the specific problem and what you'd try instead?
```

## Checks before you send

- [ ] The situation names a specific time and place.
- [ ] The behavior contains no adjectives about the person ("rude", "lazy", "negative", "amazing").
- [ ] The impact is a real effect that happened, not a prediction or a general principle.
- [ ] There is exactly one request.
- [ ] Corrective feedback is set for a private channel and includes an intent question.

## Common mistakes

- The "feedback sandwich" (praise, criticism, praise). It hides the point; give positive and corrective feedback separately.
- Stacking 3 situations to prove a pattern. Lead with one; mention it's happened before only if asked.
- Writing impact as a judgment ("it was unprofessional"). Say what it caused instead.
