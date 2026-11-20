---
name: wardley-map
description: Builds a Wardley map of a business or product - the user and their need as the anchor, the value chain of components below it ordered by visibility to the user, each component placed on the evolution axis (genesis, custom-built, product or rental, commodity or utility) with the evidence for that placement, movement and inertia, and the moves that follow (build, buy, rent, outsource, open, watch). Output is a component table, a plain-text sketch of the map, and a list of moves with owners. Use when someone asks for a Wardley map, value chain mapping, build vs buy across a stack, where to differentiate, what to outsource, or how a market or technology will evolve.
license: CC BY-SA 4.0. The method is Simon Wardley's (Wardley Maps, CC BY-SA 4.0).
---

# Wardley map

A Wardley map shows what a business is made of and how mature each part is, so a team can see where to build, where to buy, and what is about to change. Simon Wardley developed the method and wrote it up in his book Wardley Maps, published openly on Medium under the Creative Commons Attribution-ShareAlike 4.0 license. A map starts from a user and their need, lists the components that meet that need in a chain from visible to invisible (the vertical axis), and places each component on an evolution axis from genesis through custom-built and product to commodity (the horizontal axis). Components drift right over time through supply and demand competition. This skill is our step-by-step summary of the method for an AI working with a business user: a component table, a text sketch, and the moves. It is licensed CC BY-SA 4.0 like the source; see LICENSE.txt.

## When to use

- Deciding what to build in-house and what to buy, rent, or outsource across a product or operation.
- Finding where a company should differentiate and where it is spending effort on solved problems.
- Checking a strategy or roadmap against how the market and its technologies are evolving.
- Explaining a complex stack to non-technical decision makers on one page.
- Not for judging industry profitability (use five-forces-analysis) or listing internal activities by cost (use value-chain-analysis). For choosing among strategy methods, use strategy-approach-picker.

## What you need

- The scope: which business, product, or service, and for whom.
- The users and their needs. If unclear, ask once; the map is anchored on them, not on the company's goals.
- The components: what the company does, runs, or buys to meet the need (activities, practices, data, knowledge, and technology). The user's team usually knows these; the AI proposes a draft list and asks.
- Evidence for evolution: how many suppliers exist, whether it is sold as a product or metered utility, how standardized it is, how fast it is changing. Never place a component from a guess presented as fact; mark it "[check: evidence]".
- The decision the map should inform, if any.

## Steps

1. **Fix the anchor.** Name the user (one or a few types) and their need in their terms. Put them at the top. A company goal like "grow revenue" is not a user need.
2. **Build the value chain.** List the components needed to meet the need, then what each of those depends on, until you reach basic infrastructure. Order them by visibility: what the user sees directly near the top, what they never see near the bottom. Write the dependencies as "A needs B".
3. **Place each component on the evolution axis.** Use 4 stages: genesis (new, rare, uncertain, changing fast), custom-built (understood by a few, built for one case), product, including rental (several competing offerings, increasingly well defined), and commodity, including utility (standard, widely available, bought as a utility or volume item). Write one line of evidence for each placement. The same component can be at different stages in different markets; place it for this market today.
4. **Mark movement and inertia.** For each component, note whether it is moving right and how fast, from the evidence. Note inertia: where the company, its suppliers, or its customers resist a component moving (contracts, skills, past investment, habit).
5. **Draw the map.** Produce the component table and a plain-text sketch: evolution stages as columns left to right, visibility as rows top to bottom, arrows for dependencies, and ">" for expected movement. Keep the sketch readable in a chat window; the table is the source of truth.
6. **Read the map for method mismatches.** Check each component against how it is handled: building in-house what is a commodity, outsourcing or over-specifying what is genesis, running product-stage work with no standard. Wardley's doctrine includes "focus on user needs" and "use appropriate methods"; this step applies both.
7. **Choose the moves.** For each component, one move: build and explore (genesis), build or contract custom (custom-built), buy or rent (product), consume as a utility (commodity), and where useful open it, partner, or watch it. Then pick 2 to 4 strategic moves: where to differentiate, what to industrialize or hand to a supplier, what change to prepare for, and what inertia to remove. Each move names an owner and a first step.
8. **List assumptions and how to test them.** Every "[check: ...]" placement and every expected movement becomes a question with who will answer it. Maps are for discussion; invite the team to argue placements.

## Output format

````markdown
# Wardley map: [scope] · [date]
**User:** [user] · **Need:** [need] · **Decision this informs:** [decision]

## Components
| Component | Visibility (1 = top) | Depends on | Evolution stage | Evidence | Movement / inertia |
|---|---|---|---|---|---|

## Sketch
```text
             Genesis      Custom-built    Product (+rental)   Commodity (+utility)
Visible   [user need]
   |      ...
Invisible ...
```

## What the map shows
- [Method mismatches, differentiators, threats]

## Moves
| Component or area | Move | Why (from the map) | Owner | First step |
|---|---|---|---|---|

## Assumptions to check
- [check: placement or movement] — who answers: [name]
````

## Example

**Input:** "Map our business. We run an online math tutoring service for high-school students in one country. Users: parents who pay, students who attend. The parent's need: the child passes the end-of-year math exam. We match students with tutors (our own matching rules, built in-house last year), book lessons (we use an off-the-shelf booking product), run lessons over a video-call service we pay per minute, take card payments through a payment provider, host on a cloud provider. We vet tutors with our own interview and test, which parents mention in reviews. We send parents a weekly progress report written by tutors by hand; few competitors do this, and we're still changing the format every month. We built our own whiteboard tool 3 years ago, and 2 engineers maintain it; several whiteboard products exist now. Some competitors have started testing AI practice tutors. Decision: where to spend our 4 engineers next year."

**Output:**

````markdown
# Wardley map: online math tutoring · next-year engineering plan
**User:** parent (pays), student (attends) · **Need:** the child passes the end-of-year math exam · **Decision this informs:** where 4 engineers spend next year

## Components
| Component | Visibility (1 = top) | Depends on | Evolution stage | Evidence | Movement / inertia |
|---|---|---|---|---|---|
| Weekly progress report | 1 | Tutor notes | Custom-built (early) | Few competitors offer it; format still changes monthly | [check: movement] |
| Tutor vetting | 2 | Interview and test | Custom-built | Own process; parents cite it in reviews | [check: movement] |
| Tutor matching | 2 | [check: dependency] | Custom-built | Own rules, built last year | [check: are matching products available?] |
| Lesson booking | 3 | [check: dependency] | Product | Bought off the shelf | [check: movement] |
| Whiteboard | 3 | [check: dependency] | Product | Several whiteboard products exist | Inertia: own tool, 2 engineers maintain it |
| Video calls | 4 | Video-call service | Commodity (+utility) | Paid per minute | [check: movement] |
| Card payments | 4 | Payment provider | Commodity (+utility) | Bought from a payment provider | [check: movement] |
| Cloud hosting | 5 | Cloud provider | Commodity (+utility) | Bought from a cloud provider | [check: movement] |
| AI practice tutor | 2 | [check] | Genesis | Competitors testing, not established | Moving right [check: speed] |

## Sketch
```text
             Genesis        Custom-built          Product (+rental)    Commodity (+utility)
Visible    Parent: child passes the exam
   |                        Progress report  
   |       AI tutor >       Vetting   Matching
   |                                              Booking    Whiteboard*
   |                                                                   Video calls  Payments
Invisible                                                              Cloud hosting
* own build of a product-stage component
```

## What the map shows
- The differentiators parents see are custom-built: vetting and the progress report.
- The whiteboard is a product-stage component built and maintained in-house: 2 of 4 engineers sit on a solved problem.
- AI practice tutors are in genesis; if they move right, they touch the same need the progress report serves.

## Moves
| Component or area | Move | Why (from the map) | Owner | First step |
|---|---|---|---|---|
| Whiteboard | Replace with a product | Product stage; frees 2 engineers | [owner: to confirm] | Trial 2 whiteboard products with 6 tutors for 30 days |
| Progress report | Invest: build and standardize | Visible differentiator, still custom | [owner: to confirm] | Fix one format; measure parent renewals [check: renewal data] |
| AI practice tutor | Explore cheaply and watch | Genesis; uncertain | [owner: to confirm] | A small experiment with a few students |
| Tutor vetting | Keep in-house | Differentiator parents cite | [owner: to confirm] | Write the process down |

## Assumptions to check
- Whether matching products exist for tutoring — who answers: [name]
- How fast AI practice tutors are spreading among competitors — who answers: [name]
- What current lessons would lose if we move off the in-house whiteboard — who answers: [name]
````

## Checks before you send

- [ ] The anchor is a user and a need in their terms, not a company goal.
- [ ] Every component has a visibility position, dependencies, an evolution stage, and one line of evidence or "[check: ...]".
- [ ] The evolution stages use the 4 names: genesis, custom-built, product (+rental), commodity (+utility).
- [ ] Movement and inertia are noted where the input supports them.
- [ ] Moves follow from the map (stage and visibility), not from a list of initiatives brought in.
- [ ] Each move has an owner and a first step.
- [ ] Credit to Simon Wardley and the CC BY-SA 4.0 license stays with the skill if it is shared or changed.

## Common mistakes

- Mapping the org chart or a process flow; a map is components ordered by visibility and evolution.
- Placing components by how important they feel instead of how evolved the market for them is.
- Treating the map as finished. Its value is in the argument about placements, so revise it with the team.
- One move for everything ("build our own platform"). Different stages need different methods.
- Ignoring inertia, including the company's own.
