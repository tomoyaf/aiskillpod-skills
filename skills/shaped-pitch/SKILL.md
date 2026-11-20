---
name: shaped-pitch
description: Turns a raw feature request or project idea into a shaped pitch in the style of Shape Up, Ryan Singer's book on how Basecamp builds products - the problem, the appetite (a fixed time budget instead of an estimate), a rough solution at the right level of detail, rabbit holes, and no-gos - ready for a betting table to decide on for a six-week cycle. Use when someone asks for a Shape Up pitch, to shape a project, set an appetite, fixed time and variable scope, scope a feature for a six-week cycle, or replace a backlog with bets.
---

# Shaped pitch

Ryan Singer's Shape Up, published free online by Basecamp, describes how Basecamp shapes and builds product work. Work runs in six-week cycles, followed by a cool-down. Before a cycle, senior people shape projects: rough enough to leave room for the team, solved enough that the main elements are clear, and bounded by an appetite. The appetite is a time budget for a standard team, chosen before the design: a small batch of one or two weeks, or a big batch of six. Singer contrasts it with an estimate: an estimate takes a design and asks how long it will take, while an appetite takes a time budget and asks what design fits it. A shaped project goes into a pitch with five ingredients: problem, appetite, solution, rabbit holes and no-gos. A betting table then decides which pitches to bet on; there is no standing backlog. This skill writes the pitch.

## When to use

- A feature request is vague or keeps growing in discussion.
- A team wants to stop estimating and start deciding how much time a problem is worth.
- Before a planning meeting where projects compete for a cycle.
- Not for a full product requirements document: use prd-from-notes. Not for ranking many backlog items: use feature-prioritization.

## What you need

- The raw idea or request, and who asked for it.
- The problem behind it: a specific story of a customer or user who hit it.
- How much the problem is worth to the business, in time.
- The current product, enough to sketch where the change fits.
- If the problem story is missing, ask for one. Never invent customer stories.

## Steps

1. **Find the problem.** Write the specific situation where the current product fails someone, from a real story in the input. Separate it from the requested solution.
2. **Set the appetite.** Decide how much time the problem is worth: a small batch (one designer and one or two programmers, one or two weeks) or a big batch (the same team, six weeks). Say why. If the solution can't fit, narrow the problem rather than raise the appetite.
3. **Sketch the solution.** Describe the elements at the level of places, affordances and connections (Singer calls this breadboarding), or a fat-marker sketch in words. Leave visual design and details to the team.
4. **Find rabbit holes.** List the technical or design unknowns that could blow the appetite, and the decision that removes each one now ("use the existing calendar component, don't build a new one").
5. **List no-gos.** Write what is explicitly out of scope, so the team doesn't build it.
6. **Write the pitch.** Assemble the five ingredients in a short document a betting table can read in a few minutes.
7. **Check readiness.** The pitch is rough (room for the team), solved (main elements clear) and bounded (appetite, no-gos). Flag any of the three that is missing.

## Output format

```markdown
# Pitch: [name]

## Problem
[The specific story, and why it matters]

## Appetite
[Small batch: 1–2 weeks / Big batch: 6 weeks] — [why it's worth this much and no more]

## Solution
[Elements, places and flows; breadboard or fat-marker description]

## Rabbit holes
| Risk | Decision now |
|---|---|

## No-gos
- [out of scope]

## Readiness
**Rough:** [yes/no] · **Solved:** [yes/no] · **Bounded:** [yes/no] · **Open question for the betting table:** [if any]
```

## Example

**Input:** "Sales wants 'full recurring appointments' in our booking app for physiotherapists. A clinic owner, Marta, told us she books the same patient every Tuesday at 9 for 8 weeks and has to create 8 bookings by hand; last month she forgot one and the patient came to a full room. Engineering estimates full recurrence (any pattern, edits to the series, exceptions) at 3 months. Our cycles are six weeks."

**Output:**

```markdown
# Pitch: repeat a booking weekly

## Problem
Physios book the same patient at the same weekly time for a course of treatment. Marta creates 8 bookings by hand for an 8-week course; last month she missed one and the patient arrived to a full room. The problem is weekly courses, not every possible recurrence.

## Appetite
Big batch: 6 weeks. Weekly courses are common for physios [check: share of bookings], and missed bookings cost a visit and goodwill. Full recurrence at 3 months is beyond what this problem is worth now.

## Solution
- On the booking form: "Repeat weekly" with a number of weeks (2 to 12).
- On save: the app creates the bookings and lists any week where the slot is taken, so the physio picks another time for that week before confirming.
- Each booking is then independent: moving or cancelling one doesn't change the others.
- In the patient's record: the course shows as a list of dates.

## Rabbit holes
| Risk | Decision now |
|---|---|
| Editing the whole series at once | Not in scope; each booking stands alone |
| Clashes with existing bookings | Show clashes before confirming; don't auto-move |
| Reminders for many bookings at once | Use the existing reminder per booking [check: rate limits] |

## No-gos
- Patterns other than weekly (every 2 weeks, monthly, weekdays).
- "Edit all following" for a series.
- Recurring bookings created by patients online.

## Readiness
**Rough:** yes · **Solved:** yes · **Bounded:** yes · **Open question for the betting table:** whether every-2-weeks courses are common enough for a later small batch.
```

## Checks before you send

- [ ] The problem comes from a specific story in the input, separate from the requested solution.
- [ ] The appetite is set as a time budget with a reason, not an estimate.
- [ ] The solution is at the level of elements and flows, not pixel design.
- [ ] Each rabbit hole has a decision; no-gos are explicit.
- [ ] The readiness check names anything missing.

## Common mistakes

- Starting from the estimate. Fix the time, then shape the scope to fit.
- Wireframes too detailed. The team loses room to find the best design.
- Words too abstract. "Improve recurrence" isn't shaped; the elements must be clear.
- Leaving rabbit holes for the team to find mid-cycle. Shaping removes the big unknowns before the bet.
