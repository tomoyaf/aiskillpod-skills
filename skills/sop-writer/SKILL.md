---
name: sop-writer
description: Turns a person's spoken or written explanation, or a screen-recording transcript, into a standard operating procedure with purpose, trigger, roles, numbered steps using the exact button and field names, decision points, quality checks, an owner, and a review date. Use when someone asks to write an SOP, document a process, make a how-to or checklist for the team, or "write down how we do this" so someone new can do it alone.
---

# SOP writer

A good SOP lets someone with limited experience of the task do it successfully without supervision (the bar set in the US EPA's guidance on writing SOPs). Write each step as one action in the active voice and present tense, with the exact words the person will see on screen, and put every judgment call in the open as an if/then.

## When to use

- A person who knows a process explains it out loud, in a Loom, or in a messy doc, and the team needs it written down.
- Handing a recurring task to a new hire, contractor, or another team.
- A process keeps going wrong because everyone does it slightly differently.
- Not for a one-off project plan (use project-kickoff-brief) or a policy that states rules without steps.

## What you need

- The explanation or transcript. Screen-recording transcripts with "click here" need the screen named; ask once what was on screen, then mark unclear spots "[confirm: which button]".
- The tools used (app names, which account or workspace).
- Who does the task and who it's for. If missing, write "[role to confirm]".
- How often it happens and what starts it.

## Steps

1. **Name the outcome and the trigger.** Purpose is one sentence on what is true when the task is done ("The customer has an invoice in their inbox and it is logged in Xero"). Trigger is the event that starts it ("A deal is marked Won in HubSpot"), not "when needed".
2. **List roles, not names.** "Ops coordinator does steps 1-8; finance lead approves step 6." Add the current person's name in brackets once, so the SOP survives a staffing change.
3. **Write one action per step.** Say where before what, then an imperative verb, with UI labels in bold exactly as they appear: "On the **Invoices** page, select **New invoice**", "In **Due date**, pick 30 days from today." Short actions in the same place on screen may share a step; otherwise split them. Our default: if a section passes 12 steps, split it under headings.
4. **Pull out every decision.** Phrases like "usually", "depends", "if it's a big one" are decisions. Write each as "If [condition], go to step X; otherwise continue." Turn vague limits into numbers, and if the explainer gave none, mark "[confirm threshold]".
5. **Add the checks.** What the doer verifies before calling it done (the record exists, the total matches, the email was sent). Add the 1-3 mistakes the explainer said happen most.
6. **Fill the admin fields.** Owner (a role that keeps it current), last updated, and a review date. EPA guidance suggests a periodic review every 1-2 years and an update whenever the process changes; our default is 12 months, or 6 if the tool changes often. Note that a person other than the writer should test the draft before it is final.
7. **Flag gaps instead of guessing.** Anything the source didn't say goes in "Open questions for the owner"; never invent a field name or a setting.

## Output format

```markdown
# SOP: [task name]

**Purpose:** [what is true when this is done]
**Trigger:** [event that starts it] · **Frequency:** [how often]
**Roles:** [role] does the steps; [role] approves [what]. ([current person])
**Tools:** [apps and accounts]
**Time:** about [minutes]

## Steps
1. [Verb] **[exact UI label]** ...
2. ...
   - If [condition], go to step [n]. Otherwise continue.

## Done when
- [ ] [Verifiable check]

## Common mistakes
- [Mistake] — [how to avoid it]

## Open questions for the owner
- [Gap from the source]

**Owner:** [role] · **Last updated:** [date] · **Review by:** [date] · **Tested by:** [someone other than the writer]
```

## Example

**Input (Loom transcript excerpt):** "So when someone books a demo, it lands in Calendly, I go into HubSpot, find the contact, if they're over 50 people I put Marco as owner otherwise it's me, set the lifecycle stage to SQL, and then I send the prep email from the template, the 'demo prep' one. I get about 10 a week and it takes me 4 minutes." Context from the requester: Aiko is the SDR, HubSpot is the sales workspace, the sales ops lead owns the process. Labels visible in the recording: Contacts, Search, Company size, Contact owner, Lifecycle stage, Sales Qualified Lead, Email, Templates, Send.

**Output:**

```markdown
# SOP: Route a new demo booking

**Purpose:** Every booked demo has the right owner in HubSpot and the prospect has the prep email.
**Trigger:** A demo is booked in Calendly · **Frequency:** about 10 a week
**Roles:** SDR does all steps. ([Aiko])
**Tools:** Calendly, HubSpot (sales workspace)
**Time:** about 4 minutes

## Steps
1. Open the new booking in Calendly and copy the prospect's email address. [confirm: how the contact is found]
2. In HubSpot, go to **Contacts** and paste the address in **Search**.
3. Open the contact and check **Company size**.
   - If it is over 50 employees, set **Contact owner** to Marco. Otherwise set it to yourself.
4. Set **Lifecycle stage** to **Sales Qualified Lead**.
5. Click **Email**, then **Templates**, and pick **demo prep**.
6. Click **Send**.

## Done when
- [ ] The contact owner matches the size rule.
- [ ] Lifecycle stage shows Sales Qualified Lead.
- [ ] The prep email appears in the contact's activity.

## Open questions for the owner
- What if the contact doesn't exist in HubSpot yet? [confirm]
- Is "over 50 people" based on HubSpot's Company size field or what the prospect wrote? [confirm]

**Owner:** Sales ops lead · **Last updated:** 4 November · **Review by:** 4 November next year (12-month default) · **Tested by:** [confirm: another SDR]
```

## Checks before you send

- [ ] Every step is one action that starts with a verb.
- [ ] Every UI label is in bold and comes from the source, or is marked "[confirm]".
- [ ] Every "usually" or "depends" in the source became an if/then with a number or "[confirm threshold]".
- [ ] The trigger is an event, not "as needed".
- [ ] Owner is a role, a review date is set, and someone other than the writer is named to test the draft.

## Common mistakes

- Writing "update the CRM". Say which record, which field, which value.
- Leaving the expert's shortcuts in ("do the usual"). A new person doesn't know the usual.
- Guessing a button name to make the SOP look finished. A wrong label costs more than "[confirm]".
