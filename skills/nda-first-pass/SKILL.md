---
name: nda-first-pass
description: Reviews a non-disclosure agreement (NDA, confidentiality agreement) clause by clause and returns a green/yellow/red table with quotes from the text and questions for a lawyer. Flags one-way terms, broad definitions, missing exclusions, residuals clauses, and non-solicit or non-compete terms hidden in an NDA. Use when someone sends you an NDA to sign, asks "is this NDA OK?", or wants a first pass before counsel reviews it.
---

# NDA first pass

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A good first pass lets the reader see in one minute which clauses are normal, which need a question, and which would stop them signing. Quote the contract's own words for every flag; a flag without a quote is an opinion.

## When to use

- A prospect, partner, investor, or vendor sends an NDA and asks you to sign.
- You want to know what to ask your lawyer before you pay for a full review.
- You are comparing their NDA with your own template.
- Not for deciding whether to sign. That call belongs to the signer and their counsel.

## What you need

- The full NDA text. If only part is pasted, review what you have and list the missing sections as "[not provided]".
- Which side the user is on: disclosing, receiving, or both. If unknown, ask once; otherwise assume "receiving" and mark "[assumption]".
- Why the NDA exists (a sales demo, a partnership talk, a hire). It changes what "too broad" means.
- Optional: the user's own NDA template or a list of terms they always refuse.

## Steps

1. **Classify it.** Mutual (both sides protect each other's information) or one-way. If it is one-way and the user also shares information, mark it red: their information has no protection.
2. **Read the definition of confidential information.** Green if it covers information marked or identified as confidential. Yellow if it covers "all information" with no marking. Red if it also covers information the user already has or develops on their own.
3. **Check the exclusions.** Our default checklist has 4: already public, already known to the receiver, received from a third party without a duty, and developed independently. Each one missing is yellow; 2 or more missing is red. Also check the stated purpose: the UK IPO's NDA guidance advises stating the permitted purpose as precisely as possible, so a missing or vague purpose is yellow.
4. **Check term and survival.** Note how long the agreement lasts and how long the duty survives after it ends. The UK IPO's guidance says confidentiality is commonly limited to 3 or 5 years, with some information (know-how, customer lists, personal data) kept confidential indefinitely. If the duty never ends for ordinary business information, mark yellow and flag "[ask counsel: is an indefinite term appropriate for this information?]".
5. **Check what the receiver may do.** Permitted disclosure (employees, advisers, affiliates with a need to know), disclosure required by law or court order with notice, return or destruction at the end (and whether backups and one archival copy are allowed), and a statement that no license or IP right is granted.
6. **Hunt for clauses that don't belong.** Residuals (the receiver may use what stays in its people's memory): red for a discloser, flag either way. Non-solicitation of employees, non-compete, exclusivity, standstill, or an obligation to buy: red, because these are commercial terms, not confidentiality.
7. **Check the remedies and boilerplate.** Injunctive relief (note if it waives any bond or is one-sided), indemnity or liquidated damages (red by our default: unusual in an NDA), governing law and courts, assignment, and who signs. If the parties are in different countries and no law or courts are named, mark yellow. State the governing law as written; never say what that law requires. If the NDA is between a US company and its own employee, contractor, or consultant, check for a notice of immunity for confidential disclosures to government officials or attorneys (18 U.S.C. § 1833(b)). If absent, flag "[ask counsel: does this agreement need the § 1833(b) notice?]". Skip this for NDAs between companies.
8. **Write the table and the questions.** One row per clause area. Each yellow or red row gets one question for counsel. End with the 3 changes that matter most.

## Output format

```markdown
# NDA first pass — [counterparty], [date]

_Not legal advice. Prepared for review by counsel._

**Type:** [mutual / one-way, who discloses]  
**User's side:** [disclosing / receiving / both]  
**Purpose stated:** [quote or "not stated"]

| Area | Rating | What it says (quote, section) | Why it matters |
|---|---|---|---|
| Definition | [green/yellow/red] | "[quote]" (§[n]) | [one line] |
| Exclusions | | | |
| Term and survival | | | |
| Permitted disclosure | | | |
| Required by law | | | |
| Return or destroy | | | |
| No license | | | |
| Residuals | | | |
| Non-solicit / non-compete / other | | | |
| Remedies | | | |
| Governing law and courts | | | |
| Whistleblower notice (employees, contractors) | | | |

## Top 3 changes to ask for
1. [Change, and the clause it fixes]

## Questions for counsel
- [ask counsel: ...]

## Not found in the text
- [Areas with no clause, or "none"]
```

## Example

**Input (excerpt):** User is Lena at Quarry Labs, about to demo to Northbeam Retail. Northbeam sent its NDA.

> 1. "Confidential Information" means all information disclosed by Northbeam to Recipient, in any form.  
> 3. Exclusions: information that is or becomes public through no fault of Recipient.  
> 5. Obligations survive indefinitely.  
> 8. For 24 months, Recipient shall not solicit any Northbeam employee.  
> 11. Governed by the laws of the State of New York.

**Output:**

```markdown
# NDA first pass — Northbeam Retail, 4 November

_Not legal advice. Prepared for review by counsel._

**Type:** one-way, Northbeam discloses  
**User's side:** both (Quarry Labs will show its product in the demo) [assumption]  
**Purpose stated:** not stated — yellow: use of the information isn't limited to the demo

| Area | Rating | What it says (quote, section) | Why it matters |
|---|---|---|---|
| Type | red | "disclosed by Northbeam to Recipient" (§1) | Quarry Labs' demo material gets no protection. |
| Definition | yellow | "all information ... in any form" (§1) | No marking needed, so almost anything said counts. |
| Exclusions | red | Only "public through no fault of Recipient" (§3) | Prior knowledge, third-party and independent development are missing. |
| Term and survival | yellow | "survive indefinitely" (§5) | No end date for ordinary business information. |
| Non-solicit | red | "shall not solicit any Northbeam employee" for 24 months (§8) | A hiring restriction inside an NDA. |
| Governing law | green | "laws of the State of New York" (§11) | Noted as written. |
| Permitted disclosure, return or destroy, no license, remedies | — | Not in the excerpt | [not provided] |

## Top 3 changes to ask for
1. Make it mutual so the demo is covered (§1).
2. Add the 3 missing exclusions (§3).
3. Remove the non-solicit (§8).

## Questions for counsel
- [ask counsel: is an indefinite survival term acceptable for non-trade-secret information under New York law?]
- [ask counsel: does the non-solicit restrict ordinary hiring through public job posts?]

## Not found in the text
- Permitted disclosure, return or destroy, no license, remedies (excerpt only)
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] Every yellow and red row quotes the contract and names the section.
- [ ] No sentence states what a law requires; those are "[ask counsel: ...]".
- [ ] Residuals and any non-solicit, non-compete, or exclusivity terms are called out, even if absent ("none found").
- [ ] Areas missing from the text are listed, not rated green.
- [ ] The top 3 changes point at specific clauses.

## Common mistakes

- Rating a missing clause green because nothing bad is written. Missing is its own finding.
- Rewriting the NDA. The output is questions and asks; counsel drafts the wording.
- Ignoring which side the user is on. A residuals clause helps a receiver and hurts a discloser.
