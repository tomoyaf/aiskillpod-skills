---
name: inamori-style-right-as-a-person-check
description: Checks a business decision or plan against the judgment criterion Kazuo Inamori described as the root of the Kyocera Philosophy - what is right as a human being (be honest, don't deceive, don't lie) - and against his Twelve Management Principles, such as a clear purpose for the business, concrete goals, maximum sales with minimum expenses, and pricing as management. Use when a founder or manager faces a hard call (a price, a cut corner, a customer promise, a supplier dispute), wants a plan checked for purpose and concrete goals, or asks whether a decision would hold up if everyone could see how it was made.
---

# Inamori-style "right as a person" decision check

These are principles Kazuo Inamori described publicly in a 2010 lecture and on the Kazuo Inamori website that Kyocera runs. Not affiliated with or endorsed by Kazuo Inamori or their companies. The skill puts one decision or plan through his stated judgment criterion and the Twelve Management Principles, and reports where it passes, where it fails and what would change it.

## Ground rules

- Do not attribute quotes or opinions to Kazuo Inamori beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Kazuo Inamori; review the user's material against the principles below.
- Judge the decision, not the person who brings it. Name the facts each judgment rests on.
- This is a thinking aid, not legal or compliance advice. Where a law or contract decides the question, say "[check: legal]" and stop there.
- Never invent numbers or facts about the case; mark gaps "[check: ...]".

## The principles

1. **What is right as a human being.** Inamori said the root of the Kyocera Philosophy is the question "what is right as a human being", and holding to that answer; in practice, the plain morals taught to children: be honest, don't deceive people, don't lie. He called this a primitive judgment criterion. Source: lecture "なぜ経営に哲学が必要なのか" (Why management needs a philosophy), 20 January 2010, Inamori archive.
2. **A company needs a shared standard of thinking.** In the same lecture he said a company aiming high needs a way of thinking that serves as its standard. Source: same lecture.
3. **The Twelve Management Principles.** Among them: make the purpose and meaning of the business clear (1), set concrete goals (2), maximise sales and minimise expenses (5), pricing is management (6), and deal sincerely, with consideration for others (11). Source: "経営12カ条", Kazuo Inamori website.
4. **Accounting decided from what is right.** His accounting principles (稲盛会計学) are presented as judging accounting matters by what is right in principle, not by custom; the seven principles include one-to-one correspondence, double-checking, and transparent ("glass-walled") management. Source: "稲盛会計学", Kazuo Inamori website.

## When to use

- A decision where profit and fairness pull in different directions: a price rise on a captive customer, delaying a refund, hiding a defect, a supplier squeeze.
- A plan or budget that needs a check for purpose and concrete goals before it's approved.
- A team that argues about "the rules" and needs one standard to judge by.
- Not for choosing between options on cost and time alone; use decision-memo for that, and decision-record to write down what was decided.

## What you need

- The decision or plan, in a few sentences.
- Who is affected: customers, employees, suppliers, the community.
- The options being considered, including the one the user prefers.
- The facts: numbers, promises made, what each party knows.

## Steps

1. **State the decision plainly.** One sentence: who will do what, to whom, and what they will gain or lose. Remove euphemisms ("optimise the refund window" becomes "make refunds slower").
2. **Apply the right-as-a-person test (principle 1).** For each option ask: is it honest? Does it deceive anyone, by statement or by silence? Does anyone have to be told less than the truth for it to work? Mark pass, fail or unclear, and quote the fact that decides it.
3. **Test it in daylight (principles 1 and 4).** Would the option survive if every affected party saw exactly how and why it was made? Transparent ("glass-walled") management is one of the stated accounting principles; apply the same test to the decision.
4. **Check the plan against the Twelve Principles (principle 3).** Is the purpose of the business, or of this project, stated? Are the goals concrete (a number and a date)? Does the plan raise sales and cut expenses, or only one? Has someone accountable set the price on purpose? Is there sincerity and consideration toward the other side?
5. **Find the right option, not the comfortable one.** If the preferred option fails step 2 or 3, look for one that passes and still meets the business goal, and say what it costs.
6. **Write the standard down (principle 2).** Turn the judgment into one sentence the team can reuse next time ("We tell customers about a known defect before they buy").
7. **Report.** Verdict per option, the deciding facts, the option that passes, and the reusable standard.

## Output format

```markdown
# Decision check: [decision in one line]
These are principles Kazuo Inamori described publicly. Not affiliated with or endorsed by Kazuo Inamori or their companies.

## The decision, plainly
[One sentence]

## Options
| Option | Honest? | Deceives anyone? | Survives daylight? | Verdict |
|---|---|---|---|---|

## Plan against the Twelve Principles
| Principle | Present in the plan? | Gap |
|---|---|---|
| Purpose and meaning of the business clear | | |
| Concrete goals | | |
| Maximum sales, minimum expenses | | |
| Pricing set on purpose | | |
| Sincerity and consideration | | |

## Recommendation
[The option that passes, what it costs, and why]

## Our standard from now on
[One sentence the team can reuse]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We make a B2B scheduling app. A bug double-billed about 40 customers last quarter. Finance found it last week. Option A: refund quietly when customers notice. Option B: email all 40 now, refund automatically, and apologise. Option B costs about 1.2M yen in refunds this month. I lean to A because Q4 is tight."

**Output (excerpt):**

```markdown
These are principles Kazuo Inamori described publicly. Not affiliated with or endorsed by Kazuo Inamori or their companies.

# Decision check: how to handle 40 double-billed customers

## The decision, plainly
Keep money customers didn't owe unless they notice it themselves (A), or tell all 40 and return it now (B).

## Options
| Option | Honest? | Deceives anyone? | Survives daylight? | Verdict |
|---|---|---|---|---|
| A: refund when noticed | No: keeps money known to be wrong | Yes, by silence | No | Fails |
| B: tell and refund now | Yes | No | Yes | Passes |

## Recommendation
Option B. It costs about 1.2M yen this month, from the input; the Q4 gap should be met by raising sales and cutting expenses (principle 3), not by keeping overcharges. [check: legal - consumer and contract terms on billing errors].

## Our standard from now on
When we find we charged a customer wrongly, we tell them and correct it before they ask.
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Each option has a verdict with the fact that decides it.
- [ ] No fact or number appears that isn't in the input or marked [check].
- [ ] Legal questions are flagged, not answered.
- [ ] The output ends with one reusable standard.
- [ ] Every principle used is listed with its source.

## Common mistakes

- Using the test to moralise about people instead of judging the option.
- Calling an option honest because nothing false was said; silence that misleads also fails.
- Stopping at "fails" without finding an option that passes and still meets the goal.
