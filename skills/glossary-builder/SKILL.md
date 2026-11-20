---
name: glossary-builder
description: Builds a team glossary from documents - each term with a plain-words definition, the preferred spelling, synonyms and old names to avoid, an example sentence, and an owner - so people and AI tools write about the business the same way. Use when a team asks for a glossary, a list of terms, a style word list, consistent terminology, "what do we call X", or wants to give an AI assistant the company's vocabulary.
---

# Glossary builder

When one team says "account", another says "customer", and the product says "workspace", every document and every AI answer drifts. A glossary picks one term per concept, defines it in words a new hire understands, and lists the words not to use. Style guides like GOV.UK's A to Z and Google's developer word list work this way: one entry per term, a short rule, "use X, not Y".

## When to use

- New hires, customers, or AI assistants keep using inconsistent words for the same thing.
- Before writing help articles, a sales deck, or AI instructions, so they share vocabulary.
- Merging teams or products that named things differently.
- Not for designing how concepts relate to each other (use ontology-draft) or a full writing style guide (use brand-voice).

## What you need

- Source documents: help articles, product UI text, sales decks, contracts, Slack threads, tickets.
- Who the glossary is for: internal staff, customers, or both.
- Any existing term decisions (product names, legal names). If none, propose and mark "[proposal]".

## Steps

1. **Collect candidate terms.** Product and feature names, business concepts, acronyms, metrics, and any word used in more than one way. Count how often each variant appears and where.
2. **Group variants by concept.** "Account", "customer", "client org" may be one concept or three. Decide by asking: do they always refer to the same thing? If not, they are separate entries with sharper definitions.
3. **Pick the preferred term.** Prefer the word customers see in the product, then the most common variant, then the plainest. Record the others as "don't use" with the reason (old name, ambiguous, internal jargon).
4. **Write the definition in plain words.** One or two sentences, for someone who has never seen the product. Say what it is and what makes it different from the nearest similar term. No definition that repeats the term ("A workspace is a workspace for...").
5. **Add usage notes.** Capitalization and spelling (one word, hyphenated, title case), plural, whether the acronym needs spelling out on first use, and one example sentence.
6. **Assign an owner per term.** The person or team who decides changes (product for feature names, legal for contract terms, finance for metrics).
7. **Format for people and AI.** A table sorted A to Z, plus a short "Use / Don't use" list that can be pasted into AI instructions as-is.

## Output format

```markdown
# [Team / company] glossary
*Version [n], [date]. Audience: [internal / customers / both]. Changes: ask the term's owner.*

| Term | Definition (plain words) | Don't use | Usage notes | Example | Owner |
|---|---|---|---|---|---|
| [term] | [1–2 sentences] | [variants, why] | [spelling, case, acronym] | [sentence] | [person/team] |

## For AI instructions (paste as-is)
- Use "[term]", not "[variant]" or "[variant]".

## Open decisions
- [Two teams disagree on X] — options: [a / b] — decider: [name]
```

## Example

**Input:** "Docs for Shiftly (staff scheduling app). UI says 'Workspace'. Sales deck says 'account' and 'org'. Support tickets say 'company'. Help center uses 'shift swap' and 'trade request' for the same feature. Finance reports 'MRR' and 'monthly revenue'. Some docs say 'log-in', others 'login'."

**Output:**

```markdown
# Shiftly glossary
*Version 1, 4 Nov. Audience: both. Changes: ask the term's owner.*

| Term | Definition (plain words) | Don't use | Usage notes | Example | Owner |
|---|---|---|---|---|---|
| log in / login | "Log in" is the action; "login" is the noun or adjective | log-in | Verb: two words. Noun: one word | "Log in with your work email." | Product |
| MRR | Monthly recurring revenue: the subscription revenue we expect every month, excluding one-off fees | monthly revenue (ambiguous: may include one-off fees) | Spell out on first use in customer-facing text | "MRR grew to [number] in March." | Finance |
| shift swap | A request from one employee to give their shift to a coworker, which a manager approves | trade request (old name) | Lowercase; plural "shift swaps" | "Send a shift swap from the Schedule tab." | Product |
| Workspace | The space in Shiftly where one employer manages its schedules and staff; a company can have more than one | account, org, company (ambiguous with the legal customer) | Capitalized as in the UI | "Invite managers to your Workspace." | Product |

## For AI instructions (paste as-is)
- Use "Workspace", not "account", "org", or "company", for the place in Shiftly where schedules live.
- Use "shift swap", not "trade request".
- Use "log in" (verb) and "login" (noun), never "log-in".
- Use "MRR" only for recurring revenue; spell out on first use.

## Open decisions
- Do we need a separate term for the paying legal entity (e.g., "customer") vs the Workspace? — options: add "customer" as its own entry / leave it — decider: Head of Product
```

## Checks before you send

- [ ] Each concept has exactly one preferred term.
- [ ] Every definition is understandable without knowing the product and doesn't repeat the term.
- [ ] Every "don't use" variant says why.
- [ ] Each term has an owner who decides changes.
- [ ] The AI instructions list matches the table exactly.

## Common mistakes

- Defining a term with jargon from the same glossary. Define it in words a new hire knows.
- Keeping two "acceptable" synonyms. Pick one; the point is consistency.
- Leaving it in a doc nobody opens. Paste the short list into your AI assistant's instructions and the help center style guide.
