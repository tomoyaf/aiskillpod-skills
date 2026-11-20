---
name: thiel-style-contrarian-check
description: Tests whether a startup thesis, strategy or product bet rests on a real non-consensus belief, using the contrarian question Peter Thiel puts in Zero to One (as Farnam Street quotes it) - state what most people believe, state what you believe instead, check that it isn't already widely agreed or just one side of a familiar debate, check whether it is new (0 to 1) or a copy (1 to n), and name the next concrete step. Use when writing or reviewing a strategy, pitch, thesis or product bet, when a plan sounds like everyone else's, or when someone asks what important truth few people agree with them on.
---

# Thiel-style contrarian truth check

These are principles Peter Thiel has described publicly in his book Zero to One (2014), as Farnam Street quotes it, and as his publisher describes the book. Not affiliated with or endorsed by Peter Thiel or their companies. The skill takes the user's thesis, forces it into the form the book recommends, tests whether it is truly non-consensus and important, and ends with what would have to be true and the next concrete step.

## Ground rules

- Do not attribute quotes or opinions to Peter Thiel beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Peter Thiel; review the user's material against the principles below.
- Being contrarian is not the test; being right and important is. A belief that is unpopular but has no evidence is marked [check: evidence] and is not called a truth.
- Never invent market facts, surveys or numbers to show what "most people" believe. Mark them [check: ...] with a way to find out.
- Keep the check to business, product and market beliefs. Don't take sides on politics or religion; if the user's thesis is one, say that the check doesn't fit and ask for a business claim.

## The principles

1. **The question.** Zero to One gives the question Thiel likes to ask when he interviews someone: "What important truth do very few people agree with you on?" Source: Zero to One, quoted by Farnam Street, "The Single Best Interview Question You Can Ask", 2015.
2. **It is hard on purpose.** The book says the question is intellectually hard because what everyone learns in school is by definition agreed upon, and psychologically hard because answering means saying something you know is unpopular. Source: same.
3. **Two kinds of bad answer.** The book's bad answers are statements many people already agree with, and statements that only take one side of a familiar debate. Source: same.
4. **The form of a good answer.** "Most people believe in x, but the truth is the opposite of x." Source: same.
5. **0 to 1, not 1 to n.** The book separates horizontal progress, copying things that work (1 to n), from vertical progress, doing new things (0 to 1). Source: same.
6. **Context.** The publisher describes the book as starting from the contrarian premise that we live in an age of technological stagnation, and says that tomorrow's leading companies will escape competition because their businesses will be unique. Source: Penguin Random House, Zero to One.

## When to use

- Writing or reviewing a startup thesis, a strategy memo, a pitch or a product bet.
- A plan reads like every competitor's plan.
- Before committing a quarter or a budget to a bet.
- Not for checking whether a market can be dominated once you're in it (use thiel-style-monopoly-check), and not for writing a positioning line (use positioning-statement).

## What you need

- The thesis or plan in a few sentences.
- What the user thinks most people in the field believe, and why they think so.
- The evidence behind the user's belief: data, customer conversations, something they've built or seen.
- What the plan asks for: time, money, people.

## Steps

1. **Write the claim in the book's form.** "Most people believe [x], but the truth is [opposite of x]." If it won't fit, the thesis is probably a variation, not a contrarian belief (principle 4).
2. **Check the "most people" half.** How do we know most people believe x? Cite what shows it (competitors' pitches, analyst notes, customer defaults) or mark [check: ...].
3. **Test against the two bad answers.** Is the claim already widely agreed? Is it one side of a familiar debate? If either, say so and ask for a sharper claim (principle 3).
4. **Test "important".** If it's true, what changes for customers, costs or the market? A true but small claim is noted as such.
5. **Test "true".** List the evidence for the claim, the strongest evidence against it, and the cheapest test that would show it's wrong. Mark weak evidence [check: ...].
6. **0 to 1 or 1 to n.** Does the plan do something new, or take something that works and copy it into a new place? Say which; both can be valid, but they are different bets (principle 5).
7. **Name the next step.** Our addition, not from the sources: one concrete step that acts on the claim or tests it, with what, for whom, by when, and with what resources.

## Output format

```markdown
# Contrarian check: [thesis in a line]
These are principles Peter Thiel has described publicly. Not affiliated with or endorsed by Peter Thiel or their companies.

## The claim
Most people believe [x], but the truth is [opposite of x].

## How we know most people believe x
- [Evidence] / [check: ...]

## Bad-answer test
| Test | Result |
|---|---|
| Already widely agreed? | |
| Just one side of a familiar debate? | |

## Important?
[What changes if it's true]

## True?
| For | Against | Cheapest test that could prove it wrong |
|---|---|---|

## 0 to 1 or 1 to n
[Which, and why]

## Next step
**Build:** [ ] · **For:** [ ] · **By:** [date] · **With:** [resources]

## Verdict
[Contrarian and supported / contrarian but unproven / not contrarian] - [one line]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We're building scheduling software for dental clinics. Our thesis: clinics need better scheduling. Most competitors add AI features. We think small clinics don't want more features; their real problem is that patients don't confirm appointments by phone, and they'd pay for confirmations by messaging app, with no scheduling at all. We've interviewed 30 clinic managers; 22 said no-shows were their top cost."

**Output (excerpt):**

```markdown
These are principles Peter Thiel has described publicly. Not affiliated with or endorsed by Peter Thiel or their companies.

## The claim
Most people believe small dental clinics need better scheduling software, but the truth is they need no-show prevention without scheduling software.

## Bad-answer test
| Test | Result |
|---|---|
| Already widely agreed? | The first draft ("clinics need better scheduling") is: every competitor says it. The rewritten claim is not. |
| Just one side of a familiar debate? | No |

## True?
| For | Against | Cheapest test that could prove it wrong |
|---|---|---|
| 22 of 30 managers named no-shows as top cost | Interviews were with managers who answered our outreach [check: selection] | Offer confirmations alone to 10 clinics at a price; count who pays |

## 0 to 1 or 1 to n
Closer to 1 to n: message confirmations likely exist elsewhere [check: existing services]; the new part is selling them alone to this segment.

## Next step
**Build:** confirmation-only service · **For:** small clinics · **By:** [date] · **With:** [check: people and time]

## Verdict
Contrarian but unproven - the paid test decides.
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] The claim is written as "Most people believe x, but the truth is the opposite of x."
- [ ] The "most people" half has evidence or a [check].
- [ ] Both bad-answer tests are answered.
- [ ] There is evidence against the claim and a test that could prove it wrong.
- [ ] The next step is concrete: what, for whom, a date and resources.
- [ ] No quote is attributed to Peter Thiel beyond the principles above.

## Common mistakes

- Calling a widely shared complaint ("the industry is broken") a contrarian truth.
- Treating "unpopular" as proof of "true".
- Finding a sharp claim and then naming no step that would test it.
- Inventing what "most people" believe without evidence.
