---
name: dpa-checklist
description: Checks a data processing agreement (DPA, data processing addendum) clause by clause for controller and processor roles, subprocessors, security measures, breach notice, international transfers, deletion, and audit rights, with GDPR-style terms flagged for counsel. Use when a customer or vendor sends a DPA, a security or privacy review asks for one, or someone asks "can we sign this DPA?".
---

# DPA checklist

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A DPA says who decides what happens to personal data, who handles it, and what each side owes when something goes wrong. A good first pass shows which promises the user can actually keep with their current setup, because a signed promise they can't keep is the real risk.

## When to use

- An enterprise customer sends their DPA with a contract.
- The user's company must sign a vendor's DPA (analytics, email, CRM, hosting).
- A privacy or security review asks whether a DPA is in place and what it says.
- Not for deciding which privacy laws apply to the company. That is a question for counsel.

## What you need

- The DPA and the main agreement it attaches to. If the main agreement is missing, note that liability and termination may sit there.
- Which side the user is on: the party whose data it is (often called controller) or the party handling it for them (often called processor). If unclear, ask once.
- The user's facts: where data is hosted, which subprocessors they use, how fast they can detect and report an incident, how they delete data. If missing, mark each promise "[check: can we do this?]".

## Steps

1. **Confirm roles and scope.** Use the list in GDPR Article 28(3) as the checklist frame: subject matter and duration, nature and purpose, types of personal data, categories of people, and then 8 processor duties (documented instructions, staff confidentiality, security, sub-processor conditions, help with data subject requests, help with security and breach duties, delete or return at the end, information and audits). Find who is named controller and processor. If the roles don't match how the service works (for example, the vendor also uses the data for its own product), mark red and ask counsel.
2. **Check processing on instructions.** The processor should act only on documented instructions. Note any right the processor keeps to use data for its own purposes (analytics, product improvement, model training): always flag it.
3. **Check subprocessors.** Is authorization specific or general? Under general authorization, the European Commission's Q&A on its standard clauses says the processor names each sub-processor (categories are not enough), notifies changes in writing, and the parties set the notice period; the controller can object. Check that the DPA says how many days' notice and what happens after an objection. If the user is the processor, compare the list to the user's real vendors; a missing vendor is red.
4. **Check security measures.** Is there a schedule of technical and organizational measures? Compare each promise to the user's facts. A promise with no matching fact gets "[check: ...]".
5. **Check breach notification.** Note the deadline exactly as written. The Commission's standard clauses use "without undue delay" and leave a fixed number of hours to the parties, so a hard hour count is a negotiated term. Note what the notice must contain. If the user is the processor and can't meet the deadline today, mark red.
6. **Check transfers.** Where data goes and which mechanism the DPA names. The Commission's 2021 standard contractual clauses for transfers cover controllers or processors in the EU sending data to ones outside it, and its Q&A says a transfer impact assessment comes before relying on them; check whether one exists. Do not judge whether the mechanism is sufficient: "[ask counsel: is this transfer mechanism adequate for these countries?]".
7. **Check deletion, return, and audits.** Deletion or return at the end, within how long, and certification. Audit rights: how often, notice, who pays, whether a third-party report can replace an on-site audit. Unlimited on-site audits at the processor's cost are red for a processor.
8. **Check liability and the rest.** Whether the DPA has its own liability terms or follows the main agreement's cap, indemnities, assistance with data subject requests, and order of precedence. Then write the table, the gaps, and the questions.

## Output format

```markdown
# DPA checklist — [counterparty], [date]

_Not legal advice. Prepared for review by counsel._

**User's role:** [controller / processor / unclear]  
**Data and purpose:** [categories, people, purpose, as written]

| Area | Rating | What it says (quote, section) | Can we do it? |
|---|---|---|---|
| Roles and scope | [green/yellow/red] | "[quote]" (§[n]) | [yes / no / check] |
| Instructions and own use | | | |
| Subprocessors | | | |
| Security measures | | | |
| Breach notice | | | |
| Transfers | | | |
| Deletion and return | | | |
| Audits | | | |
| Liability | | | |
| Data subject requests | | | |

## Promises we can't confirm yet
- [promise] — [check: who can confirm]

## Questions for counsel
- [ask counsel: ...]
```

## Example

**Input:** Ravi at Lumen Forms (processor, a form builder) received a DPA from customer Halden Bank. Facts: hosted in Frankfurt, subprocessors are a cloud host, an email provider, and an error tracker; incidents are reviewed next business day. DPA excerpt:

> 3.2 Processor shall notify Controller of any Personal Data Breach within 24 hours of becoming aware.  
> 5.1 Processor shall not engage subprocessors other than those listed in Annex 3 (Annex 3: cloud hosting provider, email provider).  
> 8.1 Controller may audit Processor's premises at any time on 2 business days' notice, at Processor's cost.  
> 9.1 On termination Processor shall delete all Personal Data within 30 days.

**Output:**

```markdown
# DPA checklist — Halden Bank, 4 November

_Not legal advice. Prepared for review by counsel._

**User's role:** processor  
**Data and purpose:** [check: not in excerpt]

| Area | Rating | What it says (quote, section) | Can we do it? |
|---|---|---|---|
| Breach notice | red | "within 24 hours of becoming aware" (§3.2) | no: incidents are reviewed next business day |
| Subprocessors | red | Annex 3 lists cloud hosting and email | no: the error tracker is missing |
| Audits | red | "at any time on 2 business days' notice, at Processor's cost" (§8.1) | check: cost and frequency are unlimited |
| Deletion and return | green | "delete all Personal Data within 30 days" (§9.1) | check: backups included? |
| Transfers | — | Not in excerpt | [check: full DPA] |

## Promises we can't confirm yet
- 24-hour breach notice — [check: can engineering commit to weekend on-call?]
- Deletion within 30 days including backups — [check: backup retention period]

## Questions for counsel
- [ask counsel: can we propose a third-party audit report instead of on-site audits, once a year?]
- [ask counsel: should we add the error tracker to Annex 3 or propose a notice-and-object process?]
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] Every promise the user's side makes has a "Can we do it?" answer or a "[check: ...]".
- [ ] The breach deadline is quoted exactly as written.
- [ ] The subprocessor list was compared to the user's real vendors when the user is the processor.
- [ ] No sentence says a transfer mechanism or clause is legally sufficient.
- [ ] Any right to use data for the other side's own purposes is flagged.

## Common mistakes

- Treating the DPA as boilerplate. Its deadlines and audit terms create real operational work.
- Forgetting that the main agreement's liability cap may or may not cover the DPA.
- Listing the vendors you plan to use instead of the ones you use today.
