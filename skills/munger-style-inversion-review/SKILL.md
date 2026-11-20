---
name: munger-style-inversion-review
description: Reviews a plan, goal or decision by inversion - work out what would guarantee failure, then make sure the plan avoids it - and checks it against several models from different fields, following ideas Charlie Munger described in his talks (many hard problems are best solved when they are addressed backward; a latticework of models) and that the Berkshire Hathaway letters report (find out where you could die and never go there; wonderful businesses at fair prices). Use when a team is about to commit to a plan, wants a pre-mortem, asks "what could kill this", needs to stress-test a goal, or keeps seeing one problem through only one lens.
---

# Munger-style inversion review

These are principles Charlie Munger described publicly in his talks, as published in Poor Charlie's Almanack, and as Warren Buffett reports them in the Berkshire Hathaway shareholder letters. Not affiliated with or endorsed by Charlie Munger or their companies. The skill turns the question around: instead of asking how the plan succeeds, it lists how it would fail for certain, checks the plan avoids each one, and looks at the plan through models from more than one field.

## Ground rules

- Do not attribute quotes or opinions to Charlie Munger beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Charlie Munger; review the user's material against the principles below.
- Failure modes must be specific to this plan, with the mechanism ("a single customer is 40% of revenue, so one cancellation stops payroll"), not generic ("market risk").
- Never invent facts or numbers about the plan; mark gaps "[check: ...]".
- The model list is ours, not Munger's; say so in the output.

## The principles

1. **Invert.** Many hard problems are best solved when they are addressed backward: invert, always invert. Source: Charlie Munger, quoted on the Stripe Press page for Poor Charlie's Almanack.
2. **Find where you could die, and don't go there.** Buffett's 1996 letter says Berkshire tries to "reverse engineer" its future with Charlie's dictum about knowing where he is going to die so he never goes there, and steers clear of any possible consequence it can't tolerate, however remote. Source: 1996 letter.
3. **A latticework of models.** You need models in your head, and you arrange your experience, both vicarious and direct, on that latticework of models. Source: Charlie Munger, quoted on the Stripe Press page for Poor Charlie's Almanack.
4. **Wonderful businesses at fair prices.** Buffett's 2023 letter recounts Munger's 1965 advice: add wonderful businesses purchased at fair prices and give up buying fair businesses at wonderful prices. Source: 2023 letter.

## When to use

- Before committing to a plan, a launch, a hire, a large contract or a purchase.
- A goal everyone agrees on too quickly.
- A team that sees a problem only through one discipline (only finance, only engineering).
- Not for a post-incident root cause (use ohno-style-five-whys) or a full decision memo (use decision-memo).

## What you need

- The plan or goal, and what success looks like with a date.
- The key facts: money, people, customers, dependencies, timelines.
- What the team already worries about.
- Which consequences the business could not survive (cash running out, losing a licence, a safety incident).

## Steps

1. **State the goal and success.** One line: what, by when, measured how.
2. **Invert it (principle 1).** Write the opposite: "How would we make sure this fails?" List 8 to 12 concrete ways, each with its mechanism. Include slow failures (a cost that grows quietly) as well as sudden ones.
3. **Mark the ones you can't survive (principle 2).** For each failure, ask: if it happened, could the business recover? Mark the unrecoverable ones. These must be avoided outright, however unlikely; they are not traded off against upside.
4. **Check the plan against each failure.** Does the plan already avoid it, partly avoid it, or walk into it? Quote the part of the plan that decides.
5. **Look through other models (principle 3).** Re-read the plan with 3 to 5 models from different fields, chosen for this case. Our default list: incentives (who gains from each choice), opportunity cost, compounding, margin of safety, second-order effects, base rates, and supply and demand. For each, one sentence on what it reveals that the others don't.
6. **Check quality against price (principle 4), when buying something.** Is this a wonderful thing at a fair price, or a fair thing at a price that looks like a bargain? Say which, with evidence.
7. **Rewrite the plan.** List changes that remove the unrecoverable failures first, then the most likely others. Name an owner for each.

## Output format

```markdown
# Inversion review: [plan]
These are principles Charlie Munger described publicly. Not affiliated with or endorsed by Charlie Munger or their companies. The list of models is ours.

## Goal
[What, by when, measured how]

## How we'd make sure it fails
| # | Failure | Mechanism | Recoverable? | Plan today: avoids / partly / walks into |
|---|---|---|---|---|

## Places we must never go
[The unrecoverable failures, and the rule that keeps us away from each]

## Other models
| Model | What it shows about this plan |
|---|---|

## Quality and price (if buying)
[Wonderful at fair, or fair at "wonderful"; evidence]

## Changes to the plan
| Change | Removes failure # | Owner |
|---|---|---|

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We're a 12-person bakery-café chain with 3 shops. Plan: open 4 more shops in 12 months, funded by a 90M yen bank loan. One supplier provides all our flour at a discount. Our head baker trains everyone. Same-store sales grew 8% last year."

**Output (excerpt):**

```markdown
These are principles Charlie Munger described publicly. Not affiliated with or endorsed by Charlie Munger or their companies. The list of models is ours.

## How we'd make sure it fails
| # | Failure | Mechanism | Recoverable? | Plan today |
|---|---|---|---|---|
| 1 | Open all 4 before any is profitable | Loan repayments start while 4 shops lose money | No, if cash runs out [check: loan terms and cash] | Walks into it |
| 2 | Lose the flour supplier | One supplier; the discount hides the dependency | Yes, at higher cost | Walks into it |
| 3 | The head baker can't train 4 new teams | One trainer for 7 shops | Partly: quality drops | Walks into it |

## Places we must never go
Running out of cash before new shops break even. Rule: open one shop at a time; the next opens only when the last one covers its own costs [check: months to break even from the first 3 shops].

## Other models
| Model | What it shows about this plan |
|---|---|
| Base rates | How long new shops of the first 3 took to break even is better evidence than the 8% growth |
| Second-order effects | Four openings at once pull the head baker out of the current shops |
| Incentives | [check: whether the bank's covenants reward speed or safety] |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output, and the model list is marked as ours.
- [ ] Every failure has a mechanism specific to this plan.
- [ ] Unrecoverable failures are separated and get a rule, not a trade-off.
- [ ] Each failure is matched to the part of the plan that avoids or walks into it.
- [ ] At least three models from different fields are used.
- [ ] Every fact comes from the input or is marked [check].

## Common mistakes

- Listing generic risks instead of how this plan fails.
- Weighing an unrecoverable failure against upside; the 1996 letter's point is to steer clear of what you can't tolerate.
- Using one favourite model for everything.
