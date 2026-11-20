---
name: security-questionnaire-answers
description: Drafts answers to a customer security questionnaire (vendor security assessment, CAIQ, infosec review, due diligence spreadsheet) only from the user's own policies and facts, marks every unknown for an owner, and never claims a certification or control that isn't evidenced. Use when a prospect sends a security questionnaire, asks "can you fill in our vendor assessment?", or procurement needs security answers before a deal closes.
---

# Security questionnaire answers

> Not legal advice. This is a first-pass draft to prepare for a lawyer's review; it doesn't replace one.

A security questionnaire answer is a written promise to a customer, often attached to the contract. The best answer is short, true, and backed by a document the user can send. A "no" with a plan beats a "yes" nobody can prove.

## When to use

- A prospect's procurement or security team sends a questionnaire or spreadsheet.
- A renewal comes with an updated vendor assessment.
- You are building a reusable answer bank from past questionnaires.
- Not for writing the security policies themselves, or for claiming compliance with a standard. Those need the policy owner and, for compliance, an auditor.

## What you need

- The questions, in their original numbering.
- The user's evidence: security policies, past answered questionnaires, audit reports, architecture notes, vendor list, and facts they state. If there is no evidence at all, ask for it once before drafting; don't draft from general knowledge.
- Who owns open items (an engineer, the founder). If unknown, write "[owner: to confirm]".
- Optional: the deal context, to know which questions block signing.

## Steps

1. **Index the evidence.** List each source with a short name (for example "Access policy v2, March 2026"). Every answer cites one of these names or a statement the user made in this conversation.
2. **Recognize the format.** Standard questionnaires such as the Cloud Security Alliance's CAIQ ask Yes/No questions mapped to a controls framework. Keep their answer options and numbering; add detail in the comment field, not by changing the answer.
3. **Sort the questions.** Mark each one: answerable from evidence, partly answerable, or unknown. Unknowns go to the open items list with an owner; never fill them from what companies usually do.
4. **Draft yes/no answers strictly.** Answer "Yes" only if the evidence shows the control exists today. "Partly" when it exists for some systems or some of the time; say which. "No" when it doesn't, followed by a compensating control or plan only if the user gave one. "Not applicable" only with a reason.
5. **Never overclaim certifications.** Name a certification, audit report, or attestation (SOC 2, ISO 27001, PCI DSS, penetration test) only if the user provided the report or stated it with its date and scope. A SOC 2 report is issued by a CPA firm under AICPA standards, so "SOC 2 compliant" without a report is an overclaim. A cloud host's certification is not the user's: AWS's shared responsibility model, for example, splits security "of" the cloud (the provider) from security "in" the cloud (the customer's data, apps, and settings). If relevant, write "Hosted on [provider], which reports holding [certification]" and never imply the user holds it.
6. **Keep each answer short.** 1 to 3 sentences: the answer, how it works, the evidence name. No marketing words ("bank-grade", "military-grade", "fully secure").
7. **Flag contractual promises.** Where a question asks for a commitment (breach notice within X hours, data location, right to audit), mark it "[commitment: confirm with counsel]", because the answer may become part of the contract.
8. **Write the answer sheet and the open items.** Keep the questionnaire's numbering so answers paste back in.

## Output format

```markdown
# Security questionnaire — [customer], [date]

_Not legal advice. Answers drafted from the evidence listed; review before sending._

## Evidence used
- [E1] [document name, version, date]
- [E2] [statement by user, date]

## Answers
| # | Question | Answer | Detail | Evidence |
|---|---|---|---|---|
| [n] | [question, short] | [Yes / Partly / No / N/A / Unknown] | [1 to 3 sentences] | [E1] |

## Open items
| # | What we need | Owner | Blocks the deal? |
|---|---|---|---|
| [n] | [missing fact or document] | [name or "owner: to confirm"] | [yes / no / unknown] |

## Commitments to confirm with counsel
- #[n]: [commitment] — [commitment: confirm with counsel]
```

## Example

**Input:** Mei at Brightloop (a scheduling app) gets 5 questions from Ostara Insurance. Evidence: "Access policy v3 (June 2026): SSO with MFA for all staff on admin tools; access reviewed quarterly." User says: "We're on AWS in Ireland. No SOC 2 yet, we started with an auditor in September. We have backups daily."

> 1. Do you hold a SOC 2 Type II report?  
> 2. Is MFA enforced for all administrative access?  
> 3. Where is customer data stored?  
> 4. Do you encrypt data at rest?  
> 5. Will you notify us of a breach within 24 hours?

**Output:**

```markdown
# Security questionnaire — Ostara Insurance, 4 November

_Not legal advice. Answers drafted from the evidence listed; review before sending._

## Evidence used
- [E1] Access policy v3, June 2026
- [E2] Mei's statements, 4 November 2026

## Answers
| # | Question | Answer | Detail | Evidence |
|---|---|---|---|---|
| 1 | SOC 2 Type II report | No | Brightloop does not hold a SOC 2 report. An audit engagement started in September 2026. | [E2] |
| 2 | MFA on admin access | Yes | All staff reach admin tools through SSO with MFA. Access is reviewed quarterly. | [E1] |
| 3 | Data location | Yes | Customer data is stored on AWS in Ireland. | [E2] |
| 4 | Encryption at rest | Unknown | Not covered by the evidence. | — |
| 5 | Breach notice in 24 hours | Unknown | No incident policy provided. [commitment: confirm with counsel] | — |

## Open items
| # | What we need | Owner | Blocks the deal? |
|---|---|---|---|
| 4 | Confirm encryption at rest for databases and backups | [owner: to confirm] | unknown |
| 5 | Incident response policy and the notice time we can meet | Mei | unknown |
| 1 | Expected date of the SOC 2 report, if we want to share one | Mei | unknown |

## Commitments to confirm with counsel
- #5: breach notice within 24 hours — [commitment: confirm with counsel]
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] Every "Yes" cites evidence that shows the control exists today.
- [ ] No certification, audit, or pen test is named unless the user provided it with a date.
- [ ] A provider's certification is never presented as the user's own.
- [ ] Every "Unknown" appears in open items with an owner or "[owner: to confirm]".
- [ ] Commitments are flagged for counsel.

## Common mistakes

- Answering "Yes" because the control is planned. Planned is "No" plus the plan.
- Copying last year's answers without checking they're still true.
- Writing long security essays. Reviewers score short, specific answers higher.
