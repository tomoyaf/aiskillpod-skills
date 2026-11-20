---
name: internal-faq-roundup
description: Collects the questions many employees are asking across Slack, email, and docs, and writes a short internal FAQ with answers drawn from official sources, flagging anything that needs a leader's answer. Use when someone asks for an internal FAQ, an all-hands Q and A prep, "what are people asking about", or answers to common questions after a reorg, launch, policy change, or fundraise.
license: Apache-2.0 (see LICENSE.txt). Adapted from anthropics/skills internal-comms.
---

# Internal FAQ roundup

When many people ask the same question, one clear written answer saves dozens of repeated replies and stops rumours. This skill finds the questions that affect a large part of the company and answers each in 1 to 2 sentences, from official sources only.

## When to use

- After a change people talk about: a reorg, new leader, launch, office move, policy or benefits change, fundraise.
- Before an all-hands, to prepare the questions leadership should answer.
- As a weekly or monthly roundup in a company channel.
- Not for answering one person's question: just answer it.

## What you need

- Where questions are asked: Slack channels, email threads, doc comments, the all-hands question form. If you can't read them, ask the user to paste the questions.
- The official sources for answers: announcements, policy docs, leadership emails, the handbook.
- The audience (whole company, one office, one department) and the period to cover.

## Steps

1. **Collect questions where the signal is strongest.** Questions with many replies or reactions, the same question asked by different people, questions under big announcements, and FAQs already written into docs or emails.
2. **Cluster and count.** Merge questions that ask the same thing in other words. Keep a count of how many people asked each. Drop ones that affect only one person or team, unless the audience is that team.
3. **Rank by reach.** Order by how many people the answer affects, then by how often it was asked. Keep the top 5 to 10.
4. **Answer from official sources only.** Each answer is 1 to 2 sentences and links the source it came from. If the sources don't settle it, write "Not decided yet" or "[needs an answer from: role]" instead of guessing.
5. **Flag what needs a leader.** Questions about pay, jobs, strategy, or anything sensitive go to the "Needs a leadership answer" list with who should answer.
6. **Write it in the format below**, in the company's usual tone: professional, plain, and approachable.

## Output format

```markdown
# Internal FAQ — [topic or period]
_Updated [date]. Answers come from the linked sources. Ask more in [channel]._

**Q: [Question in the words people used, 1 sentence]**
A: [1–2 sentence answer.] Source: [link or document name]

**Q: …**
A: …

## Needs a leadership answer
- [Question] — asked by about [n] people — suggested owner: [role]

## Not decided yet
- [Question] — what we know so far: [1 line]
```

## Example

**Input:** About 40 messages in #general after the announcement that the company moves to a 4-day office week from 1 May. Handbook updated 20 April. Nothing yet on parking.

**Output (excerpt):**

```markdown
# Internal FAQ — office week change
_Updated 22 April. Answers come from the linked sources. Ask more in #ask-people-ops._

**Q: Which days do we need to be in the office?**
A: Monday to Thursday from 1 May; Friday stays remote for everyone. Source: Handbook, "Office days" (updated 20 April)

**Q: Can I keep working remotely if I was hired as remote?**
A: Yes. Contracts that say remote don't change. Source: CEO email, 18 April

## Needs a leadership answer
- Will the commuting allowance go up? — asked by about 12 people — suggested owner: Head of People

## Not decided yet
- Parking — the office manager is reviewing options; nothing is confirmed.
```

## Checks before you send

- [ ] Every answer cites an official source or is marked "Not decided yet".
- [ ] No answer guesses at pay, jobs, or plans that a source doesn't state.
- [ ] Each question is worded the way employees asked it, not in management language.
- [ ] The list covers questions that affect many people, ranked by reach.
- [ ] Sensitive questions are in "Needs a leadership answer", with a suggested owner.

## Common mistakes

- Answering from what "everyone knows". If it isn't written down by someone who can decide, it isn't an answer.
- Softening an unwelcome answer until it says nothing. Say it plainly, and link the source.
- Writing 30 questions. Past 10, people stop reading; move the rest to a linked doc.

---

Adapted from the `internal-comms` skill (examples/faq-answers.md) in github.com/anthropics/skills, Copyright 2026 Anthropic, PBC, licensed under the Apache License, Version 2.0 (LICENSE.txt). Changed by Fluxenic Inc.: rewritten with clustering and ranking steps, a leadership-answer list, an example, and a checklist.
