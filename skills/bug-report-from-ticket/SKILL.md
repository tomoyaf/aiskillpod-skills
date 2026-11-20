---
name: bug-report-from-ticket
description: Turns a customer complaint, support ticket, or chat into an engineering-ready bug report with steps to reproduce, expected vs actual behavior, environment, impact, evidence, and a list of what is still missing to ask the customer. Use when a ticket reports something broken and needs to go to engineering, when someone asks to "write up this bug", "file a bug", "make a Jira or Linear issue from this ticket", or when engineers keep bouncing tickets back for more detail.
---

# Bug report from ticket

An engineer should be able to reproduce the bug from the report alone, without reading the ticket thread. Separate what the customer saw from what you guess caused it, and list what's missing instead of filling gaps with assumptions.

## When to use

- A ticket describes something broken and needs to go to engineering.
- Engineering bounced a ticket back with "can't reproduce" or "need more info".
- Several tickets describe the same failure and need one report.
- Not for feature requests or how-to questions: route those with ticket-triage.

## What you need

- The ticket or chat thread, with any screenshots, error text, or links described.
- The customer's environment if known: plan, browser or app version, device, OS, account or workspace ID.
- Your own reproduction attempt, if you tried. If you didn't, say "not yet reproduced".
- If a fact is missing, don't guess it. Put it under "Ask the customer".

## Steps

1. **Write a title that names the failure and where.** Pattern: "[Action] [fails how] [where/when]": "Export to CSV drops rows over 1,000 in Reports". Not "Export broken" and not the customer's words "URGENT bug!!".
2. **Write steps to reproduce as numbered, single actions.** Start from a known state ("Logged in as an Admin on the Team plan"). One click or input per step. Use exact UI labels in bold. If the customer's steps are vague, write what you can and mark the uncertain step "[unconfirmed]".
3. **State expected vs actual.** Expected: what the product should do, per docs or past behavior. Actual: what happened, in observable terms (message text, what appeared, what didn't). Quote error messages exactly.
4. **Record the environment and frequency.** Browser, app version, OS, plan, account ID, time it happened with time zone. Frequency: every time, sometimes (x of y tries), once.
5. **Size the impact.** Number of customers or tickets reporting it, whether there's a workaround, and whether money, data, or security is involved. Suggest a severity (S1 to S4) and say why in one line.
6. **Attach the evidence.** List screenshots, recordings, logs, and ticket IDs. Keep customer personal data out of the report; reference the ticket ID instead.
7. **List what to ask the customer.** Each missing fact as a question the support rep can paste: "Which browser and version were you using?" Max 4 questions, most important first.

## Output format

```markdown
# [Title: action, failure, where]

**Severity (suggested):** [S1–S4] — [reason]
**Reported by:** [ticket IDs] · **Customers affected:** [number known]
**Reproduced by us:** [yes / no / not yet tried]

## Steps to reproduce
1. [Start state]
2. [Single action, **UI label**]
3. [...]

## Expected
[What should happen]

## Actual
[What happened; exact error text in quotes]

## Environment
- Browser/app: [...] · OS/device: [...] · Plan: [...] · Account: [ID]
- When: [date, time, time zone] · Frequency: [every time / x of y / once]

## Impact
[Who is blocked, workaround or none, money/data/security involved?]

## Evidence
- [Screenshot / log / ticket link]

## Ask the customer
1. [Question]

## Notes (not confirmed)
- [Hypotheses about cause, clearly marked as guesses]
```

## Example

**Input:**

> Ticket #2291 from Ola at Fernhill Studio: "When I upload a logo in Brand settings it just spins forever. Tried twice. Chrome. It's a PNG, about 6 MB. Need this for a client pitch tomorrow." Support note: tried a 1 MB PNG on our test account, it worked.

**Output:**

```markdown
# Logo upload never finishes for a 6 MB PNG in Brand settings

**Severity (suggested):** S2 — one customer blocked on a deadline, workaround likely (smaller file)
**Reported by:** #2291 · **Customers affected:** 1
**Reproduced by us:** no — a 1 MB PNG uploaded fine; 6 MB not yet tried

## Steps to reproduce
1. Log in to a workspace as an Admin.
2. Open **Settings > Brand**.
3. Click **Upload logo** and pick a PNG of about 6 MB.
4. Wait.

## Expected
The logo uploads and shows a preview, or an error says the file is too large.

## Actual
The upload spinner keeps spinning and never finishes. No error shown. Happened on 2 of 2 tries.

## Environment
- Browser/app: Chrome, version [unknown] · OS/device: [unknown] · Plan: [unknown] · Account: see #2291
- When: [date and time unknown] · Frequency: 2 of 2 tries

## Impact
One customer blocked before a client pitch tomorrow. Possible workaround: compress the logo under 1 MB. No money, data, or security involved.

## Evidence
- Ticket #2291

## Ask the customer
1. Could you send a screenshot of the screen while it spins?
2. Which Chrome version are you on? (Menu > Help > About Google Chrome)
3. Does a smaller copy of the logo, under 1 MB, upload?

## Notes (not confirmed)
- May be a missing file-size limit or error message on large uploads.
```

## Checks before you send

- [ ] Someone who never saw the ticket can follow the steps without asking.
- [ ] Expected and actual are separate, and actual is what was observed, not a guess.
- [ ] Error messages are quoted exactly; unknown environment fields say "[unknown]".
- [ ] Guesses about the cause are only under "Notes (not confirmed)".
- [ ] No customer email, phone, or payment detail is in the report.
- [ ] "Ask the customer" has 4 questions or fewer, ready to paste.

## Common mistakes

- Writing "it doesn't work" as the actual result. Say what the screen showed.
- Filling in a browser or version because it's likely. Unknown is more useful than wrong.
- Mixing 2 failures in one report. If the steps differ, file 2.
