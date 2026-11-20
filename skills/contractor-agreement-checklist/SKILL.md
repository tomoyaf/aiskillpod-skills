---
name: contractor-agreement-checklist
description: Checks an independent contractor or freelancer agreement before signing, covering scope and deliverables, IP assignment, confidentiality, payment, termination, and misclassification risk flags, and returns a checklist with quotes and questions for a lawyer. Use when hiring a freelancer or consultant, reviewing a contractor contract, a statement of work, or asking "is this contractor agreement OK?".
---

# Contractor agreement checklist

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A contractor agreement goes wrong in 2 ways: the company doesn't end up owning the work it paid for, or the relationship looks like employment. This checklist finds both before signing, with the contract's own words as evidence.

## When to use

- A startup is hiring a freelancer, agency, or consultant and has a draft agreement or statement of work.
- A contractor sends their own terms and the company wants to know what to push back on.
- An existing contractor's role has grown and someone asks whether the paperwork still fits.
- Not for employment contracts or deciding someone's legal status. Status questions go to counsel.

## What you need

- The agreement and any statement of work. If there is no written agreement, say so and list what the checklist would need.
- Which side the user is on: the company or the contractor. If unknown, ask once.
- How the work actually happens: hours, who sets them, tools provided, how long it has run, whether the person works for others. If missing, ask once; the misclassification flags depend on it.
- Countries or states of both parties. If missing, mark "[check: location]"; rules differ by place.

## Steps

1. **Check scope and deliverables.** Green if the work is defined by outcomes and deliverables with acceptance criteria. Yellow if it is "services as requested". Red if it reads like a job description with duties and reporting lines.
2. **Check IP.** Look for a present assignment of work product ("hereby assigns") and what it covers. Flag if it only says "will assign", if pre-existing materials of the contractor are not carved out and licensed, or if moral rights or open-source use are silent. If the company is the user and there is no assignment at all, mark red. Add "[ask counsel: is this wording effective to transfer ownership where the contractor is based?]".
3. **Check confidentiality.** Covered, for how long, and what happens to materials at the end. A missing confidentiality clause is yellow.
4. **Check payment.** Rate or fixed fee, invoicing, payment terms in days, expenses, late payment, who pays taxes. Copy numbers exactly. If payment is tied to acceptance, check that acceptance has a deadline.
5. **Check termination.** Notice for either side, payment for work done, return of materials, and which clauses survive. An agreement with no exit for the company is red.
6. **Scan for misclassification signals.** The contract's label doesn't settle status: the US Department of Labor's Fact Sheet 13 says a worker may be an employee regardless of the title given or an independent contractor agreement signed, and the IRS says to look at the entire relationship. Compare the contract and the facts against the factors those agencies list: who controls how, when, and where the work is done; who supplies tools and pays expenses; whether the worker can profit or lose through their own decisions; whether the relationship is open-ended or exclusive; whether the work is central to the business; and employee-style benefits. In the UK, HMRC's CEST tool asks similar questions about who decides the work and how it is paid. List each signal present with its source. Never conclude a status; write "[ask counsel: given these signals, what is the classification risk in this location?]".
7. **Check the rest.** Liability and indemnity, insurance, subcontracting, non-solicit, governing law. Quote anything one-sided. If the company is in the US and the agreement covers trade secrets or confidential information, check for the whistleblower immunity notice of 18 U.S.C. § 1833(b), which the statute says applies to contractors and consultants too; if absent, add "[ask counsel: should we add the § 1833(b) notice?]".
8. **Write the checklist.** Rate each area, then list the top 3 fixes and the questions for counsel.

## Output format

```markdown
# Contractor agreement checklist — [contractor] and [company]

_Not legal advice. Prepared for review by counsel._

**User is:** [company / contractor]  
**Locations:** [company] / [contractor] or [check: location]

| Area | Rating | What it says (quote, section) | Note |
|---|---|---|---|
| Scope and deliverables | [green/yellow/red] | "[quote]" (§[n]) | [one line] |
| IP assignment | | | |
| Pre-existing materials | | | |
| Confidentiality | | | |
| Payment | | | |
| Termination | | | |
| Liability and indemnity | | | |
| Governing law | | | |

## Misclassification signals
| Signal | Present? | Source |
|---|---|---|
| [signal] | [yes / no / unknown] | [contract § or "user said"] |

## Top 3 fixes
1. [fix, and the clause]

## Questions for counsel
- [ask counsel: ...]
```

## Example

**Input:** Dana at Pinecrest Health (the company) is hiring Marco Ruiz as a contract designer. Facts: Marco works Monday to Friday 9 to 5 on Pinecrest's laptop and Slack, no end date, and Pinecrest is his only client. Agreement excerpt:

> 2. Contractor will perform design duties as directed by the Head of Product.  
> 6. Contractor agrees to assign to Pinecrest any work product upon request.  
> 7. Fee: EUR 5,200 per month, paid within 45 days of invoice.  
> 10. Pinecrest may terminate at any time.

**Output:**

```markdown
# Contractor agreement checklist — Marco Ruiz and Pinecrest Health

_Not legal advice. Prepared for review by counsel._

**User is:** company  
**Locations:** [check: location of both parties]

| Area | Rating | What it says (quote, section) | Note |
|---|---|---|---|
| Scope and deliverables | red | "design duties as directed by the Head of Product" (§2) | Reads like a job; no deliverables. |
| IP assignment | red | "agrees to assign ... upon request" (§6) | A promise to assign later, not an assignment. |
| Pre-existing materials | yellow | Not addressed | Marco's own templates may be in the work. |
| Confidentiality | yellow | Not in excerpt | [check: full agreement] |
| Payment | yellow | "EUR 5,200 per month, paid within 45 days" (§7) | Monthly retainer, not tied to deliverables. |
| Termination | yellow | "Pinecrest may terminate at any time" (§10) | One-sided; payment for work done is silent. |

## Misclassification signals
| Signal | Present? | Source |
|---|---|---|
| Company controls when and how work is done | yes | user said: 9 to 5, Monday to Friday; §2 |
| Company supplies tools | yes | user said: laptop, Slack |
| Open-ended relationship | yes | no end date |
| Works only for this company | yes | user said |
| No chance of profit or loss from own decisions | yes | fixed monthly fee, §7 |

## Top 3 fixes
1. Replace §2 with deliverables and acceptance criteria.
2. Change §6 to a present assignment with a license for pre-existing materials.
3. Add payment for work done to date on termination (§10).

## Questions for counsel
- [ask counsel: given the 5 signals present, what is the classification risk where Marco works?]
- [ask counsel: is the revised IP wording effective in Marco's location?]
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] The IP row says whether the wording is a present assignment or a promise to assign.
- [ ] Every misclassification signal has a source: a clause or a fact the user gave.
- [ ] The output never says the person "is" a contractor or an employee.
- [ ] Payment numbers are copied exactly.
- [ ] Missing locations are marked "[check: location]".

## Common mistakes

- Reviewing only the paper. Classification risk comes from how the work happens, so ask about the facts.
- Accepting "all work product belongs to the company" without checking for assignment wording.
- Trusting the title "independent contractor" on the first page. Agencies look at the whole relationship, not the label.
- Forgetting the contractor's pre-existing tools and templates, which then sit inside the deliverable unlicensed.
