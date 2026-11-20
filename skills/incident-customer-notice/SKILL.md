---
name: incident-customer-notice
description: Writes customer-facing incident and outage notices for each stage (investigating, identified, monitoring, resolved) and the follow-up postmortem summary, saying what happened, who was affected, what was done, and what changes, with a plain apology and no hedging. Use when there is an outage, a status page update, a service disruption, a data or billing incident, or when someone asks for an incident email, a status update, or a post-incident summary for customers.
---

# Incident customer notice

During an incident, customers need to know 3 things fast: is it us, does it affect them, and when will they hear more. After it, they need to know what happened, that someone owns it, and what changes so it doesn't happen again. Post early, say only what is confirmed, and give a time for the next update every time.

## When to use

- Something is down, slow, or wrong for customers and you need a status page post or email.
- The incident moved to a new stage and needs an update.
- It's resolved and customers need a summary of what happened and what changes.
- Not for a security breach involving personal data: that has legal notice rules; draft with your lawyer or privacy lead. Not for a single customer's ticket: use reply-in-our-tone.

## What you need

- What customers see (errors, slowness, wrong data), which product areas, which customers or regions, and the start time with time zone.
- The current stage and what the team has confirmed. Unconfirmed causes stay out of customer notices.
- For the resolved notice and summary: end time, cause in plain words, the fix, what changes, any customer action needed (re-run a job, check invoices).
- If a fact is missing, write "[check: ...]". Never estimate a fix time the team didn't give.

## Steps

1. **Name the stage.** Use one of: Investigating (symptoms seen, cause unknown), Identified (cause found, fix in progress), Monitoring (fix in place, watching), Resolved. Post the first Investigating update within 15 minutes of knowing customers are affected. Then the postmortem summary as a separate message.
2. **Lead with impact in customer terms.** "Some customers can't log in" or "Invoices sent today may show the wrong tax". Name the feature as customers know it. Say who is affected if known; if not, "some customers".
3. **Say what you're doing, only what's confirmed.** Investigating: "We're looking into it." Identified: name the cause in plain words, once confirmed. Monitoring: "A fix is in place and we're watching." No guesses at cause, no blame on a vendor in early updates.
4. **Give the next update time.** Every update ends with "Next update by [time, time zone]". Our default: every 30 minutes while customers are blocked, and never more than 1 hour between updates while anyone is affected. Post at that time even if nothing changed, and say so.
5. **Write the resolved notice.** Start time, end time, duration, what was affected, what fixed it, and any action customers must take. Apologize once, plainly: "We're sorry. This stopped you from [task] for [duration]." No "any inconvenience", no "may have experienced".
6. **Write the postmortem summary within the time you promise.** What happened (timeline in 3 to 6 lines), why (root cause in plain words), what we did, what changes (concrete actions with owners or dates if given), and how to get help. Our default: send it within 5 business days.
7. **Keep it short and the same across channels.** Status page, email, and in-app banner say the same facts. Status updates are 2 to 4 sentences.

## Output format

```markdown
**[Stage] — [Feature / service]: [impact in a few words]**
[Date, time, time zone]

[What customers see and who is affected.] [What we're doing.] [Customer action, if any.]
Next update by [time, time zone].
```

Resolved and summary:

```markdown
**Resolved — [Feature]: [impact]**
From [start] to [end] ([duration]), [what was affected and for whom]. [What fixed it.] [Action customers need, or "You don't need to do anything."] We're sorry: [what it stopped them from doing].

# What happened on [date]: [feature] [impact]
**Summary:** [2–3 sentences]
**Timeline ([time zone])**
- [time] — [event]
**Why it happened:** [root cause, plain words]
**What we're changing:** [actions, with dates if given]
**If you need help:** [contact]
```

## Example

**Input:**

> 09:12 UTC: payments page returns errors for EU customers. 09:40: identified as an expired certificate on payment provider connection. 09:55: certificate renewed, payments working. 10:30: confirmed stable, resolved. About 380 failed checkout attempts; customers can retry. Changes: automatic certificate renewal and an alert 30 days before expiry, owner: platform team, by end of month.

**Output (excerpt):**

```markdown
**Investigating — Checkout: payments failing for some EU customers**
4 June, 09:20 UTC

Some customers in the EU see an error when paying at checkout. We're looking into it now.
Next update by 09:50 UTC.

**Identified — Checkout: payments failing for some EU customers**
4 June, 09:45 UTC

We found the cause: an expired security certificate on our connection to our payment provider. We're renewing it now.
Next update by 10:15 UTC.

**Resolved — Checkout: payments failing for some EU customers**
From 09:12 to 09:55 UTC (43 minutes), EU customers could not complete payment at checkout. We renewed the expired certificate and payments are working. If your payment failed, please try again; you were not charged for failed attempts [check: confirm no charges]. We're sorry: this stopped you from paying for 43 minutes.
```

## Checks before you send

- [ ] The first line names the stage, the feature, and the impact.
- [ ] Every update gives a next update time with a time zone.
- [ ] No cause is stated before the team confirmed it.
- [ ] The resolved notice has start, end, duration, and any customer action.
- [ ] The apology is one plain sentence, without "any inconvenience" or "may have".
- [ ] Times, counts, and changes all come from the input or are marked "[check: ...]".

## Common mistakes

- Waiting to post until the cause is known. Post "Investigating" first.
- Missing a promised update time. Post "No change yet" rather than nothing.
- Blaming a vendor. Customers chose you; own it, name the vendor only in the summary if it helps.
