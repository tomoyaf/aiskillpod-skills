---
name: call-summary-crm-notes
description: Turns a sales call transcript or rough notes into CRM-ready notes with plain-text fields - pain, impact, budget, authority, timeline, next step, stage suggestion, and risks - that paste straight into HubSpot, Salesforce, or Pipedrive. Use when someone shares a call transcript, Gong or Zoom notes, or bullet notes and asks to log the call, update the CRM, or write deal notes.
---

# Call summary to CRM notes

CRM notes are for the next person who opens the deal, including you in 3 weeks. Each field holds what the buyer said, short enough to scan, and "not discussed" when it wasn't. A blank field is honest; a guessed one poisons the forecast.

## When to use

- After any discovery, demo, or negotiation call with a transcript or notes.
- When a manager asks you to "update the deal" before a pipeline review.
- When handing a deal to another rep or to customer success.
- Not for an email to the buyer: use follow-up-email for that.

## What you need

- The transcript or notes. If speakers aren't labeled, ask once who the buyer was.
- The deal's current stage in the CRM, if known. If missing, suggest a stage and say it's a suggestion.
- Optional: the team's stage definitions. If not given, use the default stages in step 6.

## Steps

1. **Pull the buyer's statements only.** Fields hold what the buyer said or confirmed, not what the rep pitched. Quote short phrases in quotation marks when the wording matters ("we can't hire another analyst").
2. **Fill pain and impact separately.** Pain is the problem ("reports take 3 days"). Impact is what it costs them: money, hours, risk, a missed goal. If the buyer gave no number, write "no number given" rather than estimating.
3. **Fill budget, authority, timeline strictly.** These are the BANT fields (budget, authority, need, timing) as Salesforce defines them; pain covers need. Budget: amount, range, or where money comes from; "not discussed" if absent. Authority: name and title of who signs and who else weighs in. Timeline: a date or event they named ("before Q2 planning"). Never infer a date from "soon".
4. **Write the next step.** One line: who, what, date. If the call ended without a dated next step, write "none agreed" and put it first in Risks.
5. **List risks.** Max 4, most serious first: no next step, unknown signer, a competitor named, budget not confirmed, a champion who's leaving, a timeline tied to something outside their control.
6. **Suggest a stage.** HubSpot gives each deal stage a closing probability and uses it to weight the deal's amount, so a stage set too high inflates the weighted pipeline. Our default stages, if the team gives none: Discovery (pain not yet confirmed), Qualified (pain and impact confirmed, signer known), Solution (demo or proposal under review), Negotiation (price or terms being discussed), Commit (verbal yes with a date). Suggest the stage the evidence supports, not the one the rep hopes for. If it differs from the current stage, say why in one line.
7. **Format for pasting.** Our default: plain text, one field per line, no tables, no markdown, no emoji. HubSpot and Pipedrive note editors format text with a toolbar, not markdown, so pasted markdown symbols can show up as literal characters; plain text also fits single-line custom fields and mobile apps. Keep the whole note under 200 words.

## Output format

```markdown
Call: [date] - [company] - [call type]
Attendees: [buyer names and titles]; [our names]

Pain: [what's broken, in their words]
Impact: [cost in money, hours, or risk, or "no number given"]
Budget: [amount or source, or "not discussed"]
Authority: [signer name and title; others involved]
Timeline: [date or event they named, or "not discussed"]
Next step: [who does what by when, or "none agreed"]
Stage suggestion: [stage] (current: [stage or unknown]) - [one-line reason]
Risks: [1] [2] [3]
Competitors mentioned: [names or "none"]
Notes: [anything else the next rep must know, 1-2 lines]
```

## Example

**Input (excerpt):** call of Tuesday 4 November 2025; "Rep" is Sam, the account executive (AE).

> Priyanka (VP Finance, Oakridge Logistics): Month-end close takes us 9 days. The CFO wants it at 5 by the audit in March.
> Rep: What's driving the 9 days?
> Priyanka: Mostly matching carrier invoices. Two people do it by hand.
> Rep: Who else would be involved in choosing a tool?
> Priyanka: Our controller, Ben, runs the process. The CFO signs anything over 20k.
> Priyanka: We looked at Ledgerline last year but it was too heavy.
> Rep: I'll send a pilot plan Friday?
> Priyanka: Sure, and I'll get Ben on the next call.

**Output:**

```markdown
Call: 4 Nov - Oakridge Logistics - Discovery
Attendees: Priyanka (VP Finance); Sam (AE)

Pain: Month-end close takes 9 days, mostly hand-matching carrier invoices (2 people).
Impact: CFO wants close at 5 days before the March audit. No cost number given.
Budget: Not discussed. CFO signs anything over 20k.
Authority: CFO signs (name not given). Ben, Controller, runs the process. Priyanka, VP Finance, is the contact.
Timeline: Close at 5 days by the March audit.
Next step: Sam sends pilot plan by Fri 7 Nov; Priyanka brings Ben to the next call (date not set).
Stage suggestion: Discovery (current: unknown) - pain is clear but the signer hasn't been met and budget is unknown.
Risks: [1] Next call has no date. [2] CFO not met, name unknown. [3] Budget not discussed. [4] Looked at Ledgerline before; found it "too heavy".
Competitors mentioned: Ledgerline (evaluated last year, rejected)
Notes: Position the pilot as light to run; "too heavy" was the reason Ledgerline lost.
```

## Checks before you send

- [ ] Every field is filled, with "not discussed" or "none agreed" where the call didn't cover it.
- [ ] No budget, date, or name appears that the buyer didn't say.
- [ ] Pain and impact are different statements.
- [ ] The stage suggestion matches the stage definitions and gives a reason.
- [ ] Plain text only: no tables, bold, or emoji; under 200 words.

## Common mistakes

- Writing "Budget: likely ok" because the company is big. Write "not discussed".
- Logging the rep's pitch as the buyer's pain.
- Moving the stage up because the call felt good. Stage follows evidence: signer, pain, date.
