---
name: bezos-style-door-check
description: Sorts a pending decision, or a list of them, into one-way doors (consequential and hard or impossible to reverse) and two-way doors (reversible), then matches the process to the door - careful deliberation for the first, a quick call by one person or a small group for the second - and checks the information level, any disagree-and-commit, and whether a deadlock needs escalating, following decision-making principles Jeff Bezos described in the Amazon shareholder letters. Use when a team is stuck on a decision, when every choice goes through the same heavy approval, when someone asks whether a decision is reversible, one-way or two-way door, Type 1 or Type 2, or how much information is enough to decide.
---

# Bezos-style one-way or two-way door check

These are principles Jeff Bezos has described publicly in the Amazon shareholder letters for 2015 (Type 1 and Type 2 decisions) and 2016 (Day 1 and high-velocity decision making). Not affiliated with or endorsed by Jeff Bezos or their companies. The skill classifies each decision by how reversible and how consequential it is, says what process it deserves, and flags decisions that are slowed by the wrong process or stuck in a disagreement.

## Ground rules

- Do not attribute quotes or opinions to Jeff Bezos beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Jeff Bezos; review the user's material against the principles below.
- Classify from the facts the user gives: what it would cost, in money, time and trust, to undo the decision. Where that is unknown, write [check: cost to reverse].
- The 70% figure is a rough guide from the 2016 letter ("somewhere around"), not a threshold to compute. Never invent a percentage of information the user has.
- Reversible doesn't mean free. Say what reversing would cost and who would notice.
- Legal, safety, money-moving and data-deletion decisions get flagged for the owner's own judgement and any required review, whatever their door.

## The principles

1. **No one-size-fits-all process.** Bezos names one-size-fits-all decision making as a common pitfall that hurts speed and inventiveness in large organizations. Source: 2015 letter to shareholders, "Invention Machine".
2. **One-way doors (Type 1).** Some decisions are consequential and irreversible or nearly irreversible; if you walk through and don't like what you see, you can't get back. These should be made methodically, carefully and slowly, with deliberation and consultation. Source: 2015 letter.
3. **Two-way doors (Type 2).** Most decisions are changeable and reversible; a poor one can be undone by going back through the door. These can and should be made quickly by individuals with high judgement or small groups. Source: 2015 letter.
4. **Watch for the heavy process creeping in.** As organizations grow, they tend to use the heavy Type 1 process on most decisions, including many Type 2 ones, which leads to slowness, unthoughtful risk aversion, too little experimentation and less invention. The opposite mistake, a light process for Type 1 decisions, is addressed in the letter's footnote: companies that habitually do that die out before they grow large. Source: 2015 letter and its footnote.
5. **Decide with about 70% of the information you wish you had.** Waiting for 90% is, in most cases, probably slow. Either way, be good at recognizing and correcting bad decisions quickly; if you can course-correct, being wrong may cost less than being slow. Source: 2016 letter to shareholders, "High-Velocity Decision Making".
6. **Disagree and commit.** When there is conviction about a direction but no consensus, ask the others to commit anyway; the letter says this applies to the boss too, who can disagree and commit to the team's choice. Source: 2016 letter.
7. **Escalate real misalignment early.** When teams have different objectives and no number of meetings will align them, escalate immediately; otherwise the decision goes to whoever has more stamina. Source: 2016 letter.
8. **Why it matters: Day 1.** The 2016 letter lists high-velocity decision making as one of four essentials for staying a Day 1 company, alongside customer obsession, a skeptical view of proxies and the eager adoption of external trends. Day 2 companies, it says, make high-quality decisions slowly. Source: 2016 letter.

## When to use

- A decision has been in discussion for weeks.
- Every change, small or large, goes through the same approval chain.
- A team wants to just try something and nobody can say whether that is safe.
- Two teams disagree and the meeting keeps getting rescheduled.
- Not for writing the case for one big decision (use decision-memo once you know it is a one-way door), and not for recording a decision already made (use decision-record).

## What you need

- The decision or decisions, each in one sentence.
- For each: what it would take to undo it (money, time, contracts, customers who would notice, data that can't be recovered).
- What is known and what is still missing.
- Who is deciding now, and who is consulted.
- Any disagreement: who holds which view, and whether they share the same objective.

## Steps

1. **List the decisions.** One line each. Split a bundled decision (for example, launching in a new country with a new pricing model) into its parts; the parts may be different doors.
2. **Test reversibility (principles 2, 3).** For each: if we do this and don't like the result, can we go back? What would it cost, and how long would it take? Who outside the team would notice?
3. **Test consequence (principle 2).** How big is the downside if it goes wrong and we can't fully undo it? A reversible decision with a large, lasting side effect (customer trust, a public commitment) moves toward one-way.
4. **Assign the door and the process (principles 1 to 4).** One-way: name the deliberation it needs (a written memo, the people to consult, a date). Two-way: name one person or a small group who decides, and a short deadline. Flag any two-way door currently going through a one-way process, and any one-way door being decided casually.
5. **Check the information level (principle 5).** What do we know, what would we wish to know, and would waiting get it? For a two-way door, say how we would notice a wrong call and how fast we could correct it.
6. **Check for disagreement (principles 6, 7).** Is it a genuine disagreement about a shared objective? Suggest disagree and commit, with the person who disagrees saying so openly and then committing. Are the objectives themselves different? Then it is misalignment: escalate now, and name to whom.
7. **Write the next action for each decision.** Who decides, by when, and what would make us revisit it.

## Output format

```markdown
# Door check: [topic] ([date])
These are principles Jeff Bezos has described publicly. Not affiliated with or endorsed by Jeff Bezos or their companies.

## Decisions
| # | Decision | Undo cost and time | Downside if wrong | Door | Process now | Process it needs |
|---|---|---|---|---|---|---|
| 1 | | | | One-way / Two-way | | |

## Mismatches
- [Decision n]: two-way door in a one-way process. [What to drop]
- [Decision n]: one-way door decided casually. [What to add]

## Information
| # | Known | Wish we knew | Would waiting get it? | How we'd notice a wrong call |
|---|---|---|---|---|

## Disagreements
- [Decision n]: shared objective, different view -> disagree and commit. [Who commits to what]
- [Decision n]: different objectives -> escalate to [name] by [date].

## Next actions
| # | Decider | By | Revisit if |
|---|---|---|---|

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We're a 12-person online language school. Pending: (1) move from monthly to annual-only plans; (2) change the homepage headline; (3) sign a three-year lease for a studio to record lessons; (4) test a new onboarding email. All four wait for the Thursday leadership meeting, which has pushed (2) and (4) twice. Marketing and finance disagree on (1): marketing wants more sign-ups, finance wants cash up front."

**Output (excerpt):**

```markdown
These are principles Jeff Bezos has described publicly. Not affiliated with or endorsed by Jeff Bezos or their companies.

## Decisions
| # | Decision | Undo cost and time | Downside if wrong | Door | Process now | Process it needs |
|---|---|---|---|---|---|---|
| 1 | Annual-only plans | Hard: customers already on annual can't easily be moved back; refunds [check: refund terms] | Lost sign-ups, complaints | One-way (nearly) | Thursday meeting | A written memo, finance and marketing consulted, decide by [date] |
| 2 | Homepage headline | Minutes | Small | Two-way | Thursday meeting | Marketing lead decides this week |
| 3 | Three-year studio lease | Break fee [check: lease terms] | Years of rent | One-way | Thursday meeting | Memo, read the lease, consult [check: legal adviser] |
| 4 | Onboarding email test | Stop the test | Small | Two-way | Thursday meeting | Product lead decides; check opens and replies after two weeks |

## Mismatches
- 2 and 4: two-way doors waiting on a one-way process; they have slipped twice. Take them off the Thursday agenda.

## Disagreements
- 1: marketing and finance have different objectives (sign-ups versus cash), so a discussion won't settle it. Escalate to the founder, with both views in one memo, by [date].
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every decision has an undo cost or a [check].
- [ ] Bundled decisions are split.
- [ ] Every two-way door has one named decider and a short deadline.
- [ ] Every one-way door has a named deliberation step (memo, consultation, date).
- [ ] Disagreements are sorted into disagree-and-commit or escalation, not left open.
- [ ] No invented percentages of information.

## Common mistakes

- Calling a decision two-way because it is technically reversible, when reversing it would break a promise to customers.
- Running every decision through the same meeting.
- Using disagree and commit to silence a real misalignment of objectives.
- Waiting for certainty on a decision that can be undone next week.
