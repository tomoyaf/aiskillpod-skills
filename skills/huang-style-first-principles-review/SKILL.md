---
name: huang-style-first-principles-review
description: Reviews a plan, process or product against ideas Jensen Huang described publicly in his April 2024 Stanford GSB View From The Top conversation - going back to first principles to ask how you would redo something given today's conditions and tools, creating a market where none exists yet, showing others how you reason instead of only handing down answers, and an organization flat enough that information reaches many people - and returns a redo design, market-creation steps and a reasoning write-up to share. Use when someone asks how to apply first-principles thinking to an existing process, whether to enter a market that doesn't exist yet, how Jensen Huang or NVIDIA think about strategy, or how a leader can share reasoning with a team.
---

# Huang-style first-principles review

These are principles Jensen Huang has described publicly in his conversation at Stanford Graduate School of Business's View From The Top series (published April 25, 2024). Not affiliated with or endorsed by Jensen Huang or their companies. The skill reviews the user's plan against the ideas in that conversation and returns findings; it does not speak for him or for NVIDIA.

## Ground rules

- Do not attribute quotes or opinions to Jensen Huang beyond the cited sources.
- Never imitate him or write in his voice; review the user's material against the principles below.
- NVIDIA's history is used only as the source describes it; add no claims about the company.
- Use the user's facts. Never invent market sizes, costs or results; mark gaps "[check: ...]".

## When to use

- A process or product works the way it always has, and the team suspects it could be redone.
- The team is considering a market that doesn't exist yet.
- A leader wants to explain a decision so the team learns how it was reasoned, not just what was decided.
- Not for testing whether a rival will disrupt you: use disruption-threat-check. Not for stripping a design to physics-level constraints in the five-step order: use musk-style-five-step-algorithm.

## The principles

1. **Learn how it's done, then redo it from first principles.** In the conversation, Huang describes learning how something is done, then going back to first principles and asking how he would redo it given today's conditions, motivation, tools and changes. Source: GSB interview, April 2024, opening.
2. **Create the technology and the market.** He describes NVIDIA's founding as the meeting of a technology that was hard to make cheap and a market that didn't exist yet (he describes the videogame market of the time as "zero billion dollars"), and says the company creates technology and creates markets, which is why it was early in several fields. Source: same, founding story.
3. **Show how you reason.** He says that when he reviews someone's work, he shows how he reasoned through it, because seeing someone reason through something ambiguous or scary empowers people. Source: same, on his leadership style.
4. **Information reaches many people.** The interviewer describes his flat organization with many direct reports and an invitation to send him the top five things on their mind; Huang links his approach to the view that no task is beneath him. Source: same.

## What you need

- The process, product or plan, as it works today, and why it works that way.
- What has changed since it was designed: tools, costs, customers, rules.
- For a new market: who would use it, what stops them today, and what you would have to build besides the product.
- Who needs to understand the decision.
- If what changed is unknown, ask once, then mark it "[check]".

## Steps

1. **Describe how it's done today.** Write the current way in steps, and the reasons each step exists.
2. **List what changed.** For each reason, note whether today's conditions, tools or costs still support it.
3. **Redo it from first principles.** Ignoring the current design, write how you'd do it today with today's tools, in steps. Mark each step kept, changed or new.
4. **Check the market.** If the redo creates something new, ask whether the market exists. If not, list what must exist for someone to buy it (tools, partners, skills, content, standards) and who would build each.
5. **Write the reasoning to share.** A short note that walks through steps 1 to 4 in order: the facts, the reasoning and the uncertain parts, so others can follow and challenge it.
6. **Plan the information flow.** Name who needs to see this, and how people closest to the work can send what they're seeing back to the decider.
7. **Recommend.** The next step, its owner, and what evidence would show the redo is wrong.

## Output format

```markdown
# First-principles review (Huang-style): [plan]

These are principles Jensen Huang has described publicly at Stanford GSB's View From The Top (April 2024). Not affiliated with or endorsed by Jensen Huang or their companies.

## How it's done today
| Step | Why it exists | Still true today? |
|---|---|---|

## Redone from first principles
| Step | Kept / changed / new | Why |
|---|---|---|

## The market
**Exists?** [yes / partly / no] · **What must exist for people to buy:** [list, with who builds each]

## The reasoning, to share
[Short note: facts → reasoning → uncertain parts]

## Information flow
[Who sees it; how people close to the work report back]

## Recommendation
**Next step:** [action, owner, date] · **Would show it's wrong:** [evidence]
```

## Example

**Input:** "We run a chain of 6 language schools in Lisbon. Placement works as it did in 2005: a new student books a 45-minute paper test with a teacher, the teacher marks it by hand, and the student waits up to a week for a class. 30% of people who book the test never enrol [our CRM]. Teachers spend about 20 hours a week on tests across the chain. Since then: students book online, we have speaking-practice software, and our teachers say most of the test's grammar section could be scored automatically."

**Output:**

```markdown
# First-principles review (Huang-style): student placement

These are principles Jensen Huang has described publicly at Stanford GSB's View From The Top (April 2024). Not affiliated with or endorsed by Jensen Huang or their companies.

## How it's done today
| Step | Why it exists | Still true today? |
|---|---|---|
| Book a 45-minute paper test with a teacher | only teachers could judge level | partly: grammar can be scored automatically, say the teachers |
| Teacher marks it by hand | no other way to score in 2005 | no for grammar; yes for speaking |
| Wait up to a week for a class | classes started weekly | [check: whether classes could start more often] |

## Redone from first principles
| Step | Kept / changed / new | Why |
|---|---|---|
| Online grammar check at booking, scored automatically | new | removes the paper test and the marking |
| 10-minute speaking check with a teacher | changed | teachers judge what software can't [check: time needed] |
| Placement within a day, and a trial class | changed | 30% never enrol after booking the test [check: whether waiting is the reason] |

## The market
**Exists?** Yes: students already come to the schools. Nothing new must be built outside the school.

## The reasoning, to share
We designed placement in 2005 around paper tests marked by teachers. Two reasons for that have changed: grammar can be scored automatically, and students book online. Teachers spend about 20 hours a week on tests, and 30% of people who book one never enrol. We don't know yet whether the wait causes the drop-off; that is the uncertain part.

## Information flow
Share the note with all teachers and front-desk staff; ask each school to send weekly what new students say about placement.

## Recommendation
**Next step:** run the online check and the 10-minute speaking check at one school for 4 weeks [check: owner]. · **Would show it's wrong:** enrolment after booking doesn't rise at the trial school, or teachers find the placements wrong.
```

## Checks before you send

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every "still true today?" answer cites the input or is marked "[check]".
- [ ] The redo is written from today's tools, not as small edits to the old steps.
- [ ] The reasoning note shows the uncertain parts.
- [ ] Nothing is presented as Jensen Huang's opinion of the user's plan, and no claim about NVIDIA goes beyond the source.

## Common mistakes

- Calling a small tweak a first-principles redo. Start from the goal and today's tools.
- Assuming a market will appear. If it doesn't exist, list what must be built for it.
- Sharing only the decision. People learn from seeing the reasoning.
- Speaking for him. The skill applies what he said in one public conversation.
