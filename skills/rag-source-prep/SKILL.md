---
name: rag-source-prep
description: Prepares a set of company documents for an AI assistant that searches them (RAG) - inventory with owner and last-updated date, removing duplicates and stale versions, checking who may see what, restructuring into one topic per section with clear headings, adding metadata fields, and writing test questions with the expected source. Use when a team is setting up a knowledge base for a chatbot, a custom GPT, a Claude project, Copilot, or an internal AI search, or asks why the AI answers from the wrong or outdated document.
---

# RAG source prep

An AI assistant that searches documents answers from small pieces (chunks) of them, not whole files. So it repeats whatever the pieces say: an outdated price list, a draft policy, a section that only makes sense with the page title. Most bad answers are fixed in the documents, not the AI. This procedure cleans the source set and proves it with test questions before anyone relies on it.

## When to use

- Before loading documents into a chatbot, custom GPT, Claude project, Copilot, or internal AI search.
- When an assistant gives outdated, conflicting, or wrong-department answers.
- When adding a new batch of documents to an existing knowledge base.
- Not for writing new help content from scratch: use help-article-writer, then run this on the result.

## What you need

- The list of documents (or a folder export with file names, owners, and modified dates).
- What the assistant is for and who will ask it questions.
- Who may see which documents. If unknown, ask once; until answered, treat every document as restricted.
- 10 to 20 real questions people have asked (from Slack, tickets, email). If none, draft them and mark "[draft]".

## Steps

1. **Inventory.** One row per document: title, owner (a person), last updated, audience, and status (current, draft, archived). A document without an owner gets one before it goes in, or stays out.
2. **Remove duplicates and stale versions.** Keep one current version per topic. Drop drafts, "v2-final-FINAL" copies, and anything not reviewed in 12 months unless the owner confirms it's still true (our default threshold). When two current documents disagree, don't load either until the owner resolves it.
3. **Check permissions.** Group documents by who may see them. If the tool can't filter by user, a restricted document (salary bands, contracts, HR cases, customer data) stays out of a shared assistant entirely. Never rely on the AI being told "don't reveal this".
4. **Restructure for chunks.** One topic per section, with a heading that names the topic ("Refunds for annual plans", not "Other"). Each section must make sense alone: repeat the product or policy name instead of "it" or "as above". Turn tables that span pages into one table per topic. Move key facts out of images and scanned PDFs into text.
5. **Add metadata.** At the top of each document or in the tool's fields: title, owner, last reviewed date, audience, product or area, and status. Retrieval tools can filter and the AI can cite with these.
6. **Write test questions with the expected source.** 10 to 20 questions, each with the document and section that should answer it and the correct answer in one line. Include 2 to 3 questions the sources should not answer (the assistant should say it doesn't know).
7. **Run the tests and fix the sources.** Ask each question, record whether the right section was cited and the answer was correct. Fix failures in the documents first (heading, missing fact, conflicting copy), then re-run. Re-run the whole set whenever documents are added or changed.

## Output format

```markdown
# RAG source prep — [assistant name / purpose]

## Inventory
| Document | Owner | Last updated | Audience | Status | Action |
|---|---|---|---|---|---|
| [title] | [person] | [date] | [group] | current/draft/archived | keep / drop / merge into [x] / fix |

## Conflicts to resolve before loading
- [Doc A] says [x]; [Doc B] says [y] — owner: [person]

## Permission groups
| Group | Documents | In the shared assistant? |
|---|---|---|

## Restructure list
- [Document]: [change, e.g. split section "Misc" into "Refunds" and "Cancellations"]

## Metadata fields
title · owner · last_reviewed · audience · area · status

## Test questions
| # | Question | Expected source (doc, section) | Correct answer | Result |
|---|---|---|---|---|
| 1 | [question] | [doc, section] | [one line] | pass / fail: [why] |
| [n] | [out-of-scope question] | none | "I don't know" | |
```

## Example

**Input:** "Setting up a support assistant for our CS team. Docs: Pricing 2024.pdf (Sales, Jan 2024), Pricing 2025 (Sales, Mar 2025), Refund policy (Finance, 2023), Refund policy DRAFT v3 (Finance, last week), Enterprise contract template (Legal), Onboarding guide (CS, 2025, sections: 'Getting started', 'Other stuff'). Common question: 'Can an annual customer get a refund after 30 days?'"

**Output:**

```markdown
# RAG source prep — CS support assistant

## Inventory
| Document | Owner | Last updated | Audience | Status | Action |
|---|---|---|---|---|---|
| Pricing 2024.pdf | Sales [check: person] | Jan 2024 | CS | archived | drop |
| Pricing 2025 | Sales [check: person] | Mar 2025 | CS | current | keep |
| Refund policy | Finance [check: person] | 2023 | CS | current? | fix: confirm vs draft |
| Refund policy DRAFT v3 | Finance [check: person] | last week | Finance | draft | drop until approved |
| Enterprise contract template | Legal | [check] | Legal | current | keep out (restricted) |
| Onboarding guide | CS [check: person] | 2025 | CS | current | fix: split "Other stuff" |

## Conflicts to resolve before loading
- Refund policy (2023) vs DRAFT v3: if the draft changes refund terms, the 2023 version is about to be wrong — owner: Finance lead

## Permission groups
| Group | Documents | In the shared assistant? |
|---|---|---|
| All CS | Pricing 2025, Refund policy, Onboarding guide | yes |
| Legal only | Enterprise contract template | no |

## Restructure list
- Onboarding guide: split "Other stuff" into one section per topic with a named heading.
- Refund policy: add a section titled "Refunds for annual plans" that states the rule in full.

## Metadata fields
title · owner · last_reviewed · audience · area · status

## Test questions
| # | Question | Expected source (doc, section) | Correct answer | Result |
|---|---|---|---|---|
| 1 | Can an annual customer get a refund after 30 days? | Refund policy, "Refunds for annual plans" | [check: Finance to confirm] | |
| 2 | [draft] What do our plans cost now? | Pricing 2025, [check: section] | [check: from the document] | |
| 3 | [draft] Are the 2024 prices still valid? | Pricing 2025, [check: section] | [check: from the document] | |
| 4 | [draft] Can an annual customer get a refund within 30 days? | Refund policy, "Refunds for annual plans" | [check: Finance to confirm] | |
| 5 | [draft] How does a customer ask for a refund? | Refund policy, [check: section] | [check: from the document] | |
| 6 | [draft] How does a new customer get started? | Onboarding guide, "Getting started" | [check: from the document] | |
| 7 | [draft] [one question per topic split out of "Other stuff"] | Onboarding guide, [new section] | [check: from the document] | |
| 8 | [draft] What's our CEO's salary? | none | "I don't know" | |
| 9 | [draft] What does the enterprise contract say about liability? | none (Legal only) | "I don't know" | |
| 10 | [draft] What will the new refund policy say? | none (draft not loaded) | "I don't know" | |
```

## Checks before you send

- [ ] Every document in the "keep" set has a named owner and a last-updated date.
- [ ] No two kept documents answer the same question differently.
- [ ] Restricted documents are out of any assistant whose users shouldn't see them.
- [ ] Every section heading names its topic; no "Misc", "Other", or "Notes" headings remain.
- [ ] There are 10 or more test questions with expected sources, including 2 or more that should get "I don't know".

## Common mistakes

- Loading the whole shared drive "so the AI has everything". More stale copies mean more wrong answers.
- Fixing a wrong answer by adding a rule to the prompt instead of fixing the document.
- Testing once at launch. Sources change; re-run the questions after every update.
