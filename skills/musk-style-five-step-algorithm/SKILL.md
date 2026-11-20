---
name: musk-style-five-step-algorithm
description: Reviews a process, product specification or workflow with the five-step order Elon Musk described on a 2021 Starbase tour and that Walter Isaacson's biography calls the algorithm - question each requirement and name the person behind it, delete parts and steps, only then simplify, then speed up, and automate last. Use when a process has grown slow or heavy, before automating or buying software for a workflow, when a specification has requirements nobody can explain, or when someone asks to apply the five-step algorithm, question every requirement, or cut steps from a process.
---

# Musk-style 5-step requirements algorithm

These are principles Elon Musk has described publicly in a 2021 Starbase tour interview with Tim Dodd (Everyday Astronaut), as Entrepreneur and Fortune report them, Fortune drawing on Walter Isaacson's 2023 biography. Not affiliated with or endorsed by Elon Musk or their companies. The skill walks one process or specification through the five steps in their order and returns what to question, delete, simplify, speed up and, last, automate.

## Ground rules

- Do not attribute quotes or opinions to Elon Musk beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Elon Musk; review the user's material against the principles below.
- Keep the order. Don't propose simplifying, speeding up or automating a step before it has been through questioning and deletion.
- A requirement that comes from law, safety or a signed contract is questioned by asking its owner, not deleted by the skill. Mark it [check: owner / clause] and say so.
- Never invent who owns a requirement or how long a step takes. Unknowns are marked [check: ...].
- Say when the method doesn't fit, for example a process that is already minimal and only needs capacity.

## The principles

1. **Question every requirement, whoever set it.** Musk said requirements are definitely dumb, no matter who gave them, since everyone is wrong some of the time, and that they are most dangerous when they come from a smart person, because you may not question them enough. Source: Starbase tour, Part 1, 2021 (video); Entrepreneur, 2021.
2. **Each requirement carries a person's name.** He said a requirement or constraint must come with the name of a person who takes responsibility for it, not a department, because a requirement can outlive the person who made it up. Source: Starbase tour, Part 1, 2021 (video).
3. **Try hard to delete the part or step.** He said the bias runs strongly toward adding a part or step in case it is needed, and that if parts and steps aren't being added back in at least 10 percent of the time, not enough is being deleted. Source: Starbase tour, Part 1, 2021 (video); Entrepreneur, 2021.
4. **Simplify or optimise only third.** He gave the reason for the order: a very common error of a smart engineer is to optimise something that should not exist. Source: same.
5. **Speed up fourth.** Go faster, but only after the first three steps; his image was that if you are digging your grave, the answer is to stop digging, not to dig faster. Source: same.
6. **Automate last.** He said he had made the mistake of going through the steps backwards, automating before deleting, on the Tesla Model 3. Fortune, reporting Isaacson's biography, lists the same five steps in the same order and describes the early Fremont plan to automate every task from the outset, later reversed. Source: Starbase tour, Part 1, 2021 (video); Fortune, 2023.

## When to use

- A process, form, approval chain or product specification has grown slow or heavy.
- Before automating a workflow or buying software for it.
- A specification has requirements nobody can explain.
- Not for finding the root cause of one failure (use ohno-style-five-whys), and not for sorting waste types across a whole value stream (use ohno-style-seven-wastes).

## What you need

- The process or specification, step by step or requirement by requirement.
- For each requirement: where it came from and who can speak for it, if known.
- Time per step and wait time between steps, if known.
- Any plan to automate or buy a tool.
- Constraints you know are fixed (law, safety, contract), with their source.

## Steps

1. **List requirements and steps.** One line each. Next to each, write the person who owns it (a name, not a team); if nobody can be named, write "no owner" (principle 2).
2. **Question each requirement.** For each, ask what would break if it were removed and how the owner knows. Mark it keep, change or delete candidate. Smart-sounding requirements get the same question (principle 1).
3. **Delete.** Remove every delete candidate from the plan. Note which deletions are reversible, and plan to add some back: if none comes back after trying the process, you probably didn't delete enough (principle 3).
4. **Simplify what's left.** Only now merge steps, cut handoffs, shorten forms and remove options (principle 4).
5. **Speed up.** Shorten cycle time on the simplified process: remove waits, batch less, decide faster (principle 5).
6. **Automate last.** List what is now stable enough to automate and what to leave manual. Flag any automation that was planned for a step you deleted (principle 6).
7. **Set the review.** Name an owner, a date to check what had to be added back, and the measure (cycle time, error rate, hours per week).

## Output format

```markdown
# Five-step review: [process or specification]
These are principles Elon Musk has described publicly. Not affiliated with or endorsed by Elon Musk or their companies.

## 1. Requirements and their owners
| # | Requirement or step | Owner (a person) | What breaks without it | Verdict |
|---|---|---|---|---|
| | | | | keep / change / delete |

## 2. Deleted
| Item | Reversible? | How we'll know if it must come back |
|---|---|---|

## 3. Simplified
- [Change]

## 4. Faster
- [Change, with expected cycle time]

## 5. Automate (last)
| Step | Automate now / later / never | Why |
|---|---|---|

## Fixed constraints we did not touch
- [Requirement] - [source] [check: owner]

## Review
Owner: [name] · Date: [date] · Measure: [metric]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "Our agency's client onboarding takes 9 working days. Steps: sales fills a 40-field intake form; account lead re-enters it in the CRM; a kickoff deck is built from scratch; finance runs a credit check on every client; legal reviews the standard contract; the client gets a welcome pack PDF; we were about to buy a tool to automate the intake-to-CRM copy. Nobody knows who wanted the credit check; it was added after one bad debt four years ago."

**Output (excerpt):**

```markdown
These are principles Elon Musk has described publicly. Not affiliated with or endorsed by Elon Musk or their companies.

## 1. Requirements and their owners
| # | Requirement or step | Owner (a person) | What breaks without it | Verdict |
|---|---|---|---|---|
| 1 | 40-field intake form | no owner | [check: which fields the kickoff uses] | change: keep fields someone reads |
| 2 | Re-entry into CRM | no owner | Nothing, if the form writes to the CRM | delete |
| 3 | Credit check on every client | no owner (added after one bad debt) | Risk on large unpaid invoices | change: only above a set contract value [check: finance lead] |
| 4 | Legal review of the standard contract | [check: legal] | [check] | fixed constraint: ask the owner |
| 5 | Welcome pack PDF | no owner [check] | [check: whether clients read it] | delete |

## 2. Deleted
| Item | Reversible? | How we'll know if it must come back |
|---|---|---|
| CRM re-entry | Yes | Kickoff finds missing client data |
| Welcome pack PDF | Yes | Clients ask the same setup questions |

## 5. Automate (last)
| Step | Automate now / later / never | Why |
|---|---|---|
| Intake-to-CRM copy tool | never | The step it automates was deleted |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every requirement has a named person or is marked "no owner".
- [ ] The steps were applied in order; nothing was automated before deletion.
- [ ] Deletions say whether they're reversible and how a needed one would show up.
- [ ] Legal, safety and contract requirements are flagged for their owner, not deleted.
- [ ] A review date, owner and measure are set.

## Common mistakes

- Starting with automation or a new tool because it's the visible fix.
- Polishing a step (a better form) that should have been deleted.
- Accepting "compliance needs it" without a person and a clause.
- Treating zero add-backs as success.
