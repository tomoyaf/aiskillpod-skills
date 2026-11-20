---
name: proposal-check
description: Reviews a sales proposal or quote document before it goes to the buyer and returns a scored review with must-fix and nice-to-have edits. Checks that it restates the buyer's problem in their words, scope, price clarity, next step and decision date, risk reversal, and the client's name. Use when someone shares a proposal, quote, SOW draft, or pitch doc and asks "can you check this before I send it?" or "review my proposal".
---

# Proposal check before you send

A proposal wins when the buyer sees their own problem in the first paragraph, knows exactly what they get and pay, and knows what happens next. Review it as the buyer's most skeptical stakeholder would read it, and fix what costs the deal first.

## When to use

- Before a proposal, quote, statement of work, or pricing doc goes to a prospect.
- When a deal stalled after a proposal and you want to know why.
- When a rep asks "is this good enough to send?".
- Not for contract terms or legal review: use a lawyer, or contract-summary for a first read.

## What you need

- The proposal text (pasted, or the doc's content).
- The buyer's own words about their problem: call notes, an email, or a discovery summary. If missing, ask once; if still missing, score criterion 1 as "can't verify" and say so.
- The client's exact company name and the contact's name and title. If missing, take them from the doc and flag them for the rep to confirm.
- Optional: the deal size and the competitor in play.

## Steps

1. **Read the first screen as the buyer.** If the first 150 words (our default threshold) talk about your company, not their problem, that's a must-fix. HubSpot's proposal guide puts company background at the end: buyers care about their problem first. The opening restates their problem in their words and the cost of leaving it.
2. **Compare the problem statement to the buyer's words.** Quote 1–2 phrases from the notes. If the proposal uses your jargon ("operational efficiency") where they said something concrete ("we lose 2 days a month on invoices"), rewrite it in theirs.
3. **Check scope.** Every deliverable is a noun with a quantity or a boundary ("3 workshops", "up to 40 users"). Flag anything open-ended ("ongoing support", "as needed"). List what's out of scope; if there's no out-of-scope line, add one.
4. **Check price clarity.** One total the buyer can repeat to their boss. Each line has unit, quantity, and amount; recurring vs one-time is labeled; tax, currency, and payment terms are stated. If the math doesn't add up, it's a must-fix. Prices sit in a table, not in prose (our default); Proposify's 2026 data found proposals with interactive pricing tables, where buyers adjust quantities or options, won 2x more often. If there are more than 3 options, our default is to cut to 2–3 with one marked "recommended".
5. **Check the next step and decision date.** There must be one named action ("sign by", "book the kickoff call"), a date, and who does it. A validity date on the price is expected. Missing either is a must-fix. If the buyer can't sign inside the doc or with an e-signature link, add one as a nice-to-have: in Proposify's 2026 data, e-signed proposals closed 60% faster.
6. **Check risk reversal.** Look for something that lowers the buyer's risk: pilot, phased start, cancellation terms, guarantee, references, or a named success measure. If none, suggest the one that fits the deal size; never invent a guarantee the seller didn't offer.
7. **Check names and typos.** Search every mention of the client's company and contact name. A misspelled client name, another client's name left from a template, or the wrong title is a must-fix. Note other typos as nice-to-have unless they're in the price or the name. If the proposal runs past 13 pages, flag it: Proposify's 2026 report found winning proposals average 11 pages and losing ones 13.
8. **Score and sort.** Our default rubric: score each of the 7 criteria 0–2 (0 missing, 1 weak, 2 good), total out of 14. Must-fix: anything that would confuse, mislead, or embarrass. Nice-to-have: everything else. Max 5 nice-to-haves.

## Output format

```markdown
# Proposal check: [client] — [proposal title]

**Score:** [n]/14 — [Send / Send after must-fixes / Rewrite first]

| Criterion | Score (0–2) | Note |
|---|---|---|
| Their problem, in their words | [0–2] | [one line] |
| Cost of the problem | [0–2] | [one line] |
| Scope and out-of-scope | [0–2] | [one line] |
| Price clarity | [0–2] | [one line] |
| Next step and decision date | [0–2] | [one line] |
| Risk reversal | [0–2] | [one line] |
| Names and typos | [0–2] | [one line] |

## Must-fix
1. [Where] — [what's wrong] → [replacement text]

## Nice-to-have
- [Where] — [edit]

## Rewritten opening (optional)
[2–4 sentences in the buyer's words]
```

Verdict rule (our default): 12–14 send; 8–11 send after must-fixes; under 8 rewrite first.

## Example

**Input:** Proposal "Shipping reporting automation", sent Wednesday 4 November 2026, from Brightline Analytics to "Harbor Freight Co." (spelled that way 4 times; the call notes say the client is "Harbour Freight Co."). Opening: "Brightline is a leading data partner founded in 2015..." Notes: buyer said "our ops team rebuilds the same shipping report by hand every Monday, about 6 hours". The benefit is put as "saves time", with no figure. Pricing: setup 4,000 EUR, 900 EUR/month, "support as needed". The Monday report first comes up on page 2; a 30-day cancellation clause sits on page 4. Ends with "Let us know your thoughts."

**Output:**

```markdown
# Proposal check: Harbour Freight Co. — Shipping reporting automation

**Score:** 4/14 — Rewrite first

| Criterion | Score (0–2) | Note |
|---|---|---|
| Their problem, in their words | 0 | Opens with Brightline's history; the Monday report isn't mentioned until page 2. |
| Cost of the problem | 1 | "Saves time" — the buyer gave a number (6 hours a week). |
| Scope and out-of-scope | 1 | "Support as needed" is open-ended; no out-of-scope line. |
| Price clarity | 1 | Setup and monthly are separate; no total for year one, no payment terms. |
| Next step and decision date | 0 | Ends "Let us know your thoughts." No date, no action. |
| Risk reversal | 1 | Mentions a 30-day cancellation on page 4; not near the price. |
| Names and typos | 0 | Client name spelled "Harbor" 4 times; the notes say "Harbour". |

## Must-fix
1. Every mention of "Harbor Freight Co." → "Harbour Freight Co." (confirm with the rep).
2. Opening → replace with the rewritten opening below.
3. Pricing → add "Year one total: 14,800 EUR (4,000 setup + 12 × 900). Payment terms: [confirm with Brightline]."
4. Closing → "Next step: sign by Friday 20 November so the first automated report runs Monday 7 December." [assumption: confirm the dates with the buyer]

## Nice-to-have
- Scope: change "support as needed" to "email support, reply within 1 business day" [confirm with Brightline].
- Move the 30-day cancellation line next to the price.
- Add "Out of scope: reports other than the weekly shipping report."

## Rewritten opening (optional)
Every Monday your ops team rebuilds the shipping report by hand, about 6 hours a week. This proposal replaces that with a report that builds itself every Monday, so those hours go back to the team from the first week.
```

## Checks before you send

- [ ] Every criterion has a score and a one-line reason.
- [ ] Every must-fix has replacement text, not just a complaint.
- [ ] The client's name was checked against the source, not just the doc itself.
- [ ] Any total you wrote is computed from the doc's own numbers; nothing invented.
- [ ] No guarantee, discount, or term was added that the seller didn't offer.
- [ ] Nice-to-haves are 5 or fewer.

## Common mistakes

- Praising the design while the price is unclear. Price and next step come before layout.
- Writing "make it more customer-focused". Write the sentence that does it.
- Inventing a decision date. Suggest one and mark it "[assumption: confirm with the buyer]".
