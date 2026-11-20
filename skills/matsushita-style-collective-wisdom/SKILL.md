---
name: matsushita-style-collective-wisdom
description: Plans and reviews how a team gathers everyone's knowledge before a decision, against the management by everyone with collective wisdom (衆知を集めた全員経営) that Konosuke Matsushita practised as Panasonic describes it - one person's wisdom has limits, so the knowledge people build in their own work is gathered and used in management - and the open mind (素直な心) he named as the condition for it. Use when a manager is about to decide something that affects many people, a team's ideas never reach decisions, a suggestion scheme has gone quiet, or a leader asks how to hear from the front line before committing.
---

# Matsushita-style collective-wisdom review

These are principles Konosuke Matsushita described publicly, as recorded by Panasonic and by the PHP Institute he founded. Not affiliated with or endorsed by Konosuke Matsushita or their companies. The skill designs or reviews the way a decision collects the knowledge of the people who do the work, and checks that the decider listens with an open mind before choosing.

## Ground rules

- Do not attribute quotes or opinions to Konosuke Matsushita beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Konosuke Matsushita; review the user's material against the principles below.
- Collecting views is not voting. The decider still decides and says why.
- Never invent what people said. Summaries of input name where they came from ("3 of 5 drivers said ...").
- Protect people who disagree: say how input stays safe to give.

## The principles

1. **One person's wisdom has limits.** However able, one person's knowledge is limited and relying on one person's judgment can invite mistakes; so the knowledge each employee builds while fully committed to their own work is gathered and used in management. Panasonic describes this as the "management by everyone with collective wisdom" (衆知を集めた全員経営) Matsushita practised throughout his life. Source: Panasonic Stories, 「パナソニックの歴史ものがたり Episode 10」.
2. **Make a mechanism for it.** Panasonic notes that a suggestion scheme was introduced in 1954 so that each person's ideas could be used in management. Source: same page.
3. **An open mind is the condition (素直な心).** Later in life he named the open, unbiased mind as essential to gathering collective wisdom. PHP describes it as a mind free of fixed views: the humility to listen to anyone and learn from everything, and the ability to see things as they are. Sources: Panasonic Stories Episode 10; "素直な心", 用語セレクション, 松下幸之助.com (PHP Institute).

## When to use

- Before a decision that changes many people's work: a new process, a price change, an office move, a reorganisation.
- A team whose ideas never reach decisions, or a suggestion box nobody uses.
- A leader who wants to hear from the front line without running a survey nobody reads.
- Not for collecting customer feedback (use feedback-themes) or running a retrospective (use retrospective).

## What you need

- The decision to be made and who decides it, by when.
- Who knows something about it: roles, teams, partners.
- What the decider believes today, stated honestly.
- How input is gathered today, if at all.

## Steps

1. **Write the decision and the decider.** One line each. If the decision is already made, say so: asking for input then is theatre, and people notice.
2. **Map who knows what (principle 1).** List the groups whose daily work gives them knowledge the decider lacks: the people who do the task, handle the complaint, run the machine, talk to the supplier. Note what each group probably knows that the decider doesn't.
3. **Write the decider's current view, then set it aside (principle 3).** State it in one sentence, then list what would change it. This makes room to hear contrary input.
4. **Pick the mechanism (principle 2).** Match it to the group: a short conversation on the floor, a two-question written form, a review of a draft, a standing suggestion channel. Each question asks for facts from their work, not opinions on the conclusion ("What goes wrong on Friday deliveries?").
5. **Make it safe and visible.** Say who sees the input, that disagreement is wanted, and when people will hear what was decided.
6. **Gather and sort.** Group what came in by theme, with counts and sources. Mark input that contradicts the decider's view first.
7. **Decide and close the loop.** The decider chooses, says which input changed the decision and which didn't and why, and thanks people by name where they agree to it.
8. **Review the mechanism.** After the decision: did anyone outside the usual voices contribute? If not, change the mechanism next time.

## Output format

```markdown
# Collective-wisdom plan: [decision]
**Decider:** [name] · **Decide by:** [date]
These are principles Konosuke Matsushita described publicly. Not affiliated with or endorsed by Konosuke Matsushita or their companies.

## What the decider thinks now
[One sentence] · **What would change it:** [list]

## Who knows what
| Group | What they likely know that the decider doesn't | How we ask | By when |
|---|---|---|---|

## Questions
[2-4 questions about facts from their work]

## Safety and follow-up
[Who sees input; disagreement wanted; when people hear the decision]

## After the input (fill in later)
| Theme | How many said it | Where from | Changes the decision? |
|---|---|---|---|

## Decision and reasons
[What was decided; which input changed it; which didn't and why]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "I run a 30-person home cleaning company. I want to switch all cleaners from fixed routes to app-assigned jobs to fill gaps. I'm fairly sure it's right. Decision by end of month. The cleaners, two dispatchers and our largest landlord client are affected."

**Output (excerpt):**

```markdown
These are principles Konosuke Matsushita described publicly. Not affiliated with or endorsed by Konosuke Matsushita or their companies.

## What the decider thinks now
App-assigned jobs will fill gaps in the schedule. · **What would change it:** evidence that fixed routes keep clients, or that travel time rises.

## Who knows what
| Group | What they likely know that the decider doesn't | How we ask | By when |
|---|---|---|---|
| Cleaners | Which clients expect the same person; real travel times | 10-minute talk at the weekly meeting, plus a two-question form | Day 7 |
| Dispatchers | Where gaps really come from (cancellations or sick days) | Review of last month's gaps with them | Day 5 |
| Landlord client | Whether unit turnover needs the same cleaner | Call by the account owner | Day 10 |

## Questions
1. Which of your clients would notice if someone else came? Why?
2. Where did you lose the most time between jobs last week?
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] The decider and the date are named, and the decision is still open.
- [ ] The decider's current view is written down with what would change it.
- [ ] Questions ask for facts from people's work, not votes.
- [ ] People hear what was decided and which input changed it.

## Common mistakes

- Asking only managers; the source's point is the knowledge built in each person's own work.
- Asking after deciding.
- Treating the count of opinions as the decision.
