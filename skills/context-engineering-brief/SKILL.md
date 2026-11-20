---
name: context-engineering-brief
description: Writes a context brief (system prompt or instructions) for an AI assistant or agent - role, goal, audience, what it can and can't do, sources of truth, tools, output format, a few examples, edge cases, and when to hand off to a human - kept short and ordered by importance. Use when someone sets up a custom GPT, a Claude project, a Gemini gem, a Copilot agent, or a support bot, or asks to write a system prompt, improve AI instructions, or fix an assistant that keeps doing the wrong thing.
---

# Context engineering brief

An assistant does what its context makes most likely. Anthropic's guidance on context engineering is to find "the smallest set of high-signal tokens that maximize the likelihood of your desired outcome": specific enough to guide, without hardcoding brittle if-then logic. It also advises a few diverse, canonical examples over a laundry list of edge cases. So the brief (our default) puts the most important instructions first, uses a few concrete examples instead of long rule lists, and names where the truth lives instead of pasting it all in.

## When to use

- Setting up a custom GPT, Claude project, Gemini gem, Copilot agent, or support bot.
- An assistant keeps making the same mistake, and the instructions have grown long.
- Handing an assistant to a team, so everyone knows what it's for and what it won't do.
- Not for preparing the documents it searches (use rag-source-prep) or testing it (use eval-set-builder).

## What you need

- What the assistant is for and who will use it.
- What it must never do (policy, data, tone, promises).
- Where the facts live: documents, a knowledge base, a tool.
- 2 to 3 examples of good answers, if they exist. If not, write them in step 6 and mark "[draft]".
- Known failures, if it's an existing assistant. These are the most valuable input.

## Steps

1. **Write the role and goal in 2 sentences.** Who it is for and what a successful conversation achieves: "You help our CS team answer billing questions from customers. A good answer is correct, cites the policy section, and is ready to paste."
2. **State the audience and tone.** Who reads the output, their expertise, and 2 to 3 tone rules with an example phrase. Skip generic rules the AI follows anyway ("be helpful").
3. **List can and can't.** Can: the tasks in scope. Can't: things outside scope, things it must refuse, and promises it must never make (refunds, legal advice, delivery dates). Each "can't" says what to do instead.
4. **Name the sources of truth.** Which document or tool is authoritative for which topic, and what to do when sources disagree or nothing answers the question ("Say you don't know and suggest [contact]"). Point to sources; don't paste whole documents into the instructions.
5. **Describe the tools, if any.** One line each: what it does and when to use it. If two tools overlap so that a person couldn't say which to use, merge or remove one.
6. **Fix the output format.** A template or a short example of the exact shape: length, headings, what to include. Add 2 to 3 diverse examples of input and ideal output. Examples teach more than rules.
7. **Cover edge cases and escalation.** The 3 to 5 situations most likely to go wrong (angry user, out-of-scope request, missing information, request for personal data), each with the expected behavior. Name when to hand to a human and how.
8. **Order by importance and cut.** Put the rules that matter most near the top, in plain headings. Delete any line you can't tie to a real or likely failure. Start minimal, then add a rule only when testing shows it's needed.

## Output format

```markdown
# [Assistant name] — instructions

## Role and goal
[2 sentences]

## Audience and tone
- Audience: [who, expertise]
- Tone: [rule] — e.g., "[example phrase]"

## You can
- [In-scope task]

## You can't (and what to do instead)
- [Never do X] → [do Y]

## Sources of truth
| Topic | Source | If missing or conflicting |
|---|---|---|

## Tools
- [tool]: [what it does] — use when [condition]

## Output format
[Template or description]

## Examples
**User:** [input]
**You:** [ideal output]

## Edge cases
- [Situation] → [behavior]

## Hand off to a human when
- [Condition] → [how: who, channel]
```

## Example

**Input:** "Custom GPT for our sales team at Fieldnote (field-service scheduling SaaS). Should draft replies to prospect questions about features and pricing. Pricing is in 'Pricing 2025' doc, features in 'Product FAQ'. It keeps promising custom integrations and quoting discounts. Discounts need sales manager (Ivy) approval."

**Output:**

```markdown
# Fieldnote sales reply assistant — instructions

## Role and goal
You draft replies for Fieldnote's sales reps to prospects' questions about features and pricing. A good draft is accurate to the Pricing 2025 and Product FAQ documents, ready for the rep to paste, and never commits the company to anything those documents don't state.

## Audience and tone
- Audience: operations managers at field-service companies; not technical.
- Tone: plain and direct, under 150 words — e.g., "Yes, crews can see their schedule offline."

## You can
- Answer feature and pricing questions from the two documents.
- Suggest a next step (demo, trial).

## You can't (and what to do instead)
- Quote or hint at discounts → write "[Rep: discounts need Ivy's approval]" in the draft.
- Promise custom integrations or roadmap items → say what exists today and offer to pass the request on.
- Answer security or legal questions → write "[Rep: route to security questionnaire process]".

## Sources of truth
| Topic | Source | If missing or conflicting |
|---|---|---|
| Prices, plans | Pricing 2025 | Say "let me confirm" and flag for the rep |
| Features | Product FAQ | Don't guess; flag for the rep |

## Output format
A reply of 150 words or fewer, then a line "Notes for rep:" listing anything to check.

## Examples [draft]
**User:** Do you integrate with QuickBooks, and can you build us a SAP connector?
**You:** [QuickBooks answer from the Product FAQ.] A custom SAP connector isn't something we can promise; I'll pass your request to our product team. Would a 20-minute demo help?
Notes for rep: Fill in the QuickBooks answer from the Product FAQ. SAP request — log it in the CRM.

**User:** What's the price for 25 technicians, and can you do 20% off if we sign this month?
**You:** For 25 technicians, the price depends on the plan; the plan table in our pricing sheet shows each option, and I'm happy to walk you through which fits. On the 20% question, I'll check with my manager and come back to you.
Notes for rep: [Rep: discounts need Ivy's approval]. Fill in the plan price from Pricing 2025 before sending.

## Edge cases
- Prospect asks for a discount → draft without a number; add "[Rep: discounts need Ivy's approval]".
- Question not covered by either document → "Let me check and come back to you today", plus a note for the rep.

## Hand off to a human when
- The prospect mentions a contract, legal terms, or a competitor's price-match → rep handles; tag Ivy in the CRM.
```

## Checks before you send

- [ ] The role and goal fit in 2 sentences at the top.
- [ ] Every "can't" says what to do instead.
- [ ] Each topic has one named source of truth and a rule for when it's missing.
- [ ] There are 2 or more concrete examples showing the exact output shape.
- [ ] Every rule traces to a known or likely failure; generic advice is cut.
- [ ] Escalation names a person or channel.

## Common mistakes

- Pasting entire documents into the instructions. Point to them as sources.
- Writing 40 if-then rules for edge cases. Give examples and a principle; add rules only for failures you've seen.
- Writing "never" with no alternative. The assistant then refuses or improvises; tell it what to do.
