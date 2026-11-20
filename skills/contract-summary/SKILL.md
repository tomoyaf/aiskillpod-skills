---
name: contract-summary
description: Summarizes a commercial contract (MSA, SaaS agreement, order form, vendor or customer contract) into a one-page brief with parties, term, auto-renewal and notice dates, fees and payment terms, termination, liability cap, indemnities, IP, data, and unusual clauses, plus a key dates list. Use when someone asks to summarize a contract, "what am I signing?", "when does this renew?", or needs a contract brief for a manager or lawyer.
---

# Contract summary

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A good contract summary lets a busy reader know in one page what they pay, what they owe, how they get out, and which date they must not miss. Every line points at a section number so anyone can check it against the source.

## When to use

- Before signing a vendor, customer, or partner contract, to brief the signer.
- When a contract is already signed and someone asks "when does it renew?" or "can we cancel?".
- When handing a contract to counsel with the questions already listed.
- Not for redlining or negotiating wording. This brief describes; it doesn't draft.

## What you need

- The full contract, including order forms, schedules, and any terms linked by URL. If a linked document is missing, list it under "Not provided" and don't guess its contents.
- Which party the user is. If unknown, ask once.
- Today's date, to turn "90 days before renewal" into a calendar date. If the start date isn't in the text, write "[check: start date]".

## Steps

1. **Map the documents.** List every document that forms the contract and the order of precedence if stated. A clause in an order form may override the master agreement.
2. **Pull the commercial terms.** Parties (legal names), start date, initial term, renewal (automatic or not, renewal length), fees, price increases on renewal, payment terms, late fees, taxes. Copy numbers exactly; never round or convert currency.
3. **Pull the exit terms.** Termination for convenience (who, with what notice), for breach (cure period), for insolvency, and what happens after: refunds, fees still owed, data return.
4. **Pull the risk terms.** Liability cap (amount or formula, and what is carved out of it), exclusion of indirect or consequential damages (harm that follows from a breach rather than the breach itself, such as lost profits), indemnities (a promise by one party to pay the other for a future loss; say who covers whom for what), warranties, insurance. Explain each term in plain words in the brief; the reader may not know them.
5. **Pull IP and data.** Who owns what is created, licenses granted, feedback clauses, confidentiality, personal data, and whether a separate data processing agreement is referenced.
6. **Flag what is unusual.** Anything a reader would not expect in this kind of contract: exclusivity, minimum commitments, most-favored pricing, non-solicit, audit rights, unilateral change rights ("we may update these terms"), publicity rights. Quote each one.
7. **Build the key dates list.** Turn every deadline into a date: renewal date, last day to give notice of non-renewal, price change dates, payment due dates. If a date depends on a fact not in the text, write "[check: ...]".
8. **Write the brief.** One page. Questions for counsel go last as "[ask counsel: ...]"; never state what a law requires.

## Output format

```markdown
# Contract summary — [contract name], [counterparty]

_Not legal advice. A summary to check against the contract and with counsel._

**Parties:** [legal name] ([role]) and [legal name] ([role])  
**Documents:** [list, with precedence if stated]  
**User is:** [party]

## Key dates
| Date | What happens | Source |
|---|---|---|
| [date] | [event] | §[n] |

## Money
- Fees: [exact amounts and basis] (§[n])
- Payment terms: [net days, method, late fees] (§[n])
- Renewal pricing: [rule or "not stated"] (§[n])

## Term and exit
- Term: [length, start] · Renewal: [auto / manual, length] (§[n])
- Termination: [for convenience / breach / cure period] (§[n])
- After termination: [refunds, data, fees owed] (§[n])

## Risk
- Liability cap: [amount or formula; carve-outs] (§[n])
- Indemnities: [who covers whom for what] (§[n])
- Warranties and insurance: [summary] (§[n])

## IP and data
- [ownership, licenses, confidentiality, personal data, DPA] (§[n])

## Unusual clauses
- "[quote]" (§[n]) — [why it stands out]

## Questions for counsel
- [ask counsel: ...]

## Not provided
- [linked or missing documents]
```

## Example

**Input (excerpt):** User is Omar at Fernhill Studio, the customer. Contract with Tallyline Inc., signed 1 February 2026.

> 4.1 Initial term 12 months from the Effective Date. Renews automatically for successive 12-month terms unless either party gives 60 days' written notice.  
> 5.1 Fees: USD 18,000 per year, invoiced annually in advance, net 30.  
> 5.3 Tallyline may increase fees by up to 7% on each renewal.  
> 9.2 Each party's liability is capped at fees paid in the 12 months before the claim.  
> 12.4 Tallyline may list Customer as a customer in marketing materials.

**Output:**

```markdown
# Contract summary — Subscription agreement, Tallyline Inc.

_Not legal advice. A summary to check against the contract and with counsel._

**Parties:** Fernhill Studio (customer) and Tallyline Inc. (vendor) [check: legal names in the signature block]  
**Documents:** excerpt only  
**User is:** Fernhill Studio

## Key dates
| Date | What happens | Source |
|---|---|---|
| 2 December 2026 | Last day to send non-renewal notice (60 days before) | §4.1 |
| 1 February 2027 | Auto-renews for 12 months; fee may rise up to 7% | §4.1, §5.3 |
| 3 March 2027 | Renewal invoice due if issued on 1 February (net 30) | §5.1 |

## Money
- Fees: USD 18,000 per year, invoiced annually in advance (§5.1)
- Payment terms: net 30 (§5.1)
- Renewal pricing: up to 7% increase each renewal (§5.3)

## Term and exit
- Term: 12 months from 1 February 2026 · Renewal: automatic, 12 months (§4.1)
- Termination: only non-renewal found in excerpt [check: termination for breach]

## Risk
- Liability cap: fees paid in the prior 12 months, for both parties (§9.2); carve-outs [check: not in excerpt]

## Unusual clauses
- "Tallyline may list Customer as a customer in marketing materials" (§12.4) — publicity without asking first.

## Questions for counsel
- [ask counsel: does the cap apply to data breaches or confidentiality claims?]
- [ask counsel: can we require approval before Tallyline uses our name?]

## Not provided
- Full agreement beyond §4, §5, §9, §12
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] Every number is copied exactly and has a section reference.
- [ ] The non-renewal notice deadline is a calendar date, or "[check: ...]" explains what is missing.
- [ ] Unusual clauses are quoted, not paraphrased.
- [ ] Linked or missing documents are listed under "Not provided".
- [ ] No sentence states what a law requires.

## Common mistakes

- Missing the notice window. The renewal date matters less than the last day to say no.
- Reading only the master agreement when the order form changes the price or term.
- Calling a liability cap "mutual" without checking the carve-outs.
