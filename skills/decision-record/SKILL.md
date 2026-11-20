---
name: decision-record
description: Records a decision that has been made as a short decision-log entry - the decision in one sentence, context, options considered, why this one, who decided, the date, status, and what would make the team revisit it. Based on architecture decision record (ADR) and decision-log practice, written for any business decision. Use when a team has just decided something, someone asks to log or write up a decision, or people keep asking "why did we do this?".
---

# Decision record

A decision record lets someone six months from now understand what was decided, why, and when to reopen it, without asking the people who were there. It records a decision already made; it doesn't argue for one. Keep it short: Michael Nygard's 2011 post that introduced the architecture decision record (ADR) format says the whole document should be 1 or 2 pages, and our default is half a page.

## When to use

- A team just decided something that is costly to reverse or that people will question later: a tool, a vendor, a price, a policy, a hire plan, a process.
- Someone says "let's write that down" or asks for a decision log entry.
- A thread keeps asking "why did we pick X?" and the answer lives only in someone's head.
- Not for making the decision. To lay out options and get a recommendation approved, use a decision memo first, then record the result here.

## What you need

- What was decided, and by whom. If the decider is unclear, ask once; never guess. Write "[decider not confirmed]" if still unknown.
- The date it was decided. If missing, use the date of the source message and mark "[from message date]".
- The options that were on the table and why the others lost. If only one option was discussed, say so; don't invent alternatives.
- Optional: the thread, minutes, or doc where it was discussed, and the log's last entry number.

## Steps

1. **State the decision in one sentence, active voice.** Nygard writes the decision section "in full sentences, with active voice", typically starting "We will". Example: "We will use Dealbook as our CRM from 1 March."
2. **Write the context in 2 to 4 sentences.** The facts and pressures that forced a choice: deadline, cost, a customer, a constraint. Nygard says this section "is value-neutral. It is simply describing facts." Opinions go in the reasons.
3. **List the options considered.** One line each with its main trade-off. Atlassian's DACI play keeps a table of options with pros, cons, and cost. Include "do nothing" if it was a real option. Only list options that were actually discussed.
4. **Give the reasons.** 2 to 4 bullets that link back to the context: why this option beat the others. Then list consequences, good and bad. Nygard: "All consequences should be listed here, not just the 'positive' ones."
5. **Name who decided and who was consulted.** One decider (Atlassian's DACI play calls this the Approver, "the one person (yes: one!) who makes the decision") and the people consulted. The UK government's ADR framework also records stakeholders consulted.
6. **Set a revisit trigger.** A specific condition that would reopen it: a date, a number, or an event ("if we pass 20 sales reps", "if the price rises above our budget", "review on 1 March next year"). Our default: every record has one; "never" is allowed only when the decision is truly permanent, and then say why.
7. **Set the status and number.** Proposed, accepted, or superseded. Number entries in order and never reuse a number, as Nygard's format does. If this replaces an older decision, mark the old one "Superseded by #[n]" and keep it; Nygard keeps reversed decisions "around, but mark it as superseded".

## Output format

```markdown
## #[number] — [short noun phrase title]

**Status:** [proposed / accepted / superseded by #n] · **Date:** [date] · **Decided by:** [one name]  
**Consulted:** [names] · **Source:** [link to thread, minutes, or doc]

**Decision:** We will [one sentence].

**Context:** [2–4 sentences of facts.]

**Options considered:**
- **[Option A, chosen]:** [main trade-off]
- **[Option B]:** [main trade-off]
- **[Do nothing]:** [main trade-off, if it was considered]

**Why:**
- [reason linked to the context]

**Consequences:**
- [good and bad effects, what changes for whom]

**Revisit if:** [specific date, number, or event]
```

## Example

**Input:** Slack thread summary: "OK final call from Rosa (COO) on 3 Feb: we go with Dealbook, not FunnelHQ. Nadia and Felix were in on it. FunnelHQ's sales tier was about 3x the cost for our 6 reps, and we don't use marketing automation yet. Dealbook has the email sync we need. Downside is we'll have to migrate again if marketing wants FunnelHQ later. Spreadsheet is breaking, we lost 2 follow-ups last month. Last log entry was #11."

**Output:**

```markdown
## #12 — CRM for the sales team

**Status:** accepted · **Date:** 3 February · **Decided by:** Rosa (COO)  
**Consulted:** Nadia, Felix · **Source:** Slack thread, 3 February

**Decision:** We will move the sales team from the shared spreadsheet to Dealbook.

**Context:** The team of 6 reps tracks deals in a spreadsheet that is breaking. 2 follow-ups were lost last month. We need email sync with the CRM. We don't use marketing automation today.

**Options considered:**
- **Dealbook, chosen:** has the email sync we need; no marketing automation.
- **FunnelHQ sales tier:** marketing automation included, about 3 times Dealbook's cost for 6 reps.

**Why:**
- It replaces the breaking spreadsheet and has the email sync we need.
- FunnelHQ's sales tier costs about 3 times as much for 6 reps, and we don't use marketing automation yet.

**Consequences:**
- Reps move their open deals into Dealbook and stop using the spreadsheet.
- If marketing later needs FunnelHQ, we migrate CRM data a second time.

**Revisit if:** marketing wants FunnelHQ or starts using marketing automation.
```

## Checks before you send

- [ ] The decision is one active-voice sentence someone could act on.
- [ ] Exactly one decider is named, or "[decider not confirmed]".
- [ ] Every option listed was really discussed; nothing was added to look thorough.
- [ ] Consequences include at least one cost or downside.
- [ ] The revisit trigger is a specific date, number, or event.
- [ ] Facts, names, numbers, and dates all come from the source.

## Common mistakes

- Recording a discussion as a decision. If nobody with authority said yes, the status is "proposed".
- Editing an old entry when the decision changes. Write a new entry and mark the old one superseded; the history is the point.
- A context section that argues. Keep the case for the choice in "Why".
