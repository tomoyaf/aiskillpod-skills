---
name: ticket-triage
description: Triages a batch of incoming support tickets into a table with category, severity on an S1 to S4 rubric, the team or person to route to, and a first reply for each. Use when a support inbox or queue needs sorting, someone pastes new tickets and asks to "triage", "prioritize", "route", or "sort the queue", or when deciding what to answer first after a weekend or an outage.
---

# Ticket triage

Triage decides in a minute per ticket what it is, how bad it is, who owns it, and what the customer hears now. Severity follows a written rubric, not the customer's tone: an angry message about a typo is S4, a polite one about lost data is S1.

## When to use

- A queue built up (Monday morning, after a launch or an outage) and you need an order.
- New tickets need routing to support, billing, engineering, or sales.
- A teammate is new and needs a consistent severity call.
- Not for writing a full reply to one ticket: use reply-in-our-tone. Not for writing the engineering bug: use bug-report-from-ticket.

## What you need

- The tickets: text, ticket ID, customer or plan if known, time received.
- Your categories and routing (who handles what). If not given, use the defaults below and say so.
- Your severity rubric if you have one; otherwise use the one below.

## Severity rubric (our default; replace with yours)

| Level | Definition | First reply within |
|---|---|---|
| S1 | Many customers can't use the product, or data loss, security exposure, or money taken wrongly | 1 hour |
| S2 | One customer blocked on a core task with no workaround, or a paying customer's deadline at risk | 4 business hours |
| S3 | Something broken or confusing with a workaround; a how-to question | 1 business day |
| S4 | Feature request, cosmetic issue, general feedback | 2 business days |

Default categories and routing: Bug → engineering on-call; Billing → billing owner; How-to → support; Account access → support; Feature request → product; Sales question → sales. Security or data exposure always goes to the security owner as well, at S1.

## Steps

1. **Read each ticket for the facts, not the tone.** Note what is broken or asked, how many people it affects, whether there's a workaround, and whether money, data or security is involved.
2. **Assign one category.** If a ticket fits 2, pick the one whose owner must act first (a bug that caused a wrong charge is Billing first: the customer needs the money back, then engineering fixes the cause).
3. **Assign severity with the rubric.** Write the rubric line that decided it in 5 words or fewer. If 3 or more tickets report the same failure within an hour, raise all of them to S1 and flag a possible incident. If you're unsure between 2 levels, pick the higher one.
4. **Route to an owner.** A named person or a queue from the routing list. If the routing list doesn't cover it, write "[route: unclear]".
5. **Write the first reply.** 1 to 3 sentences: confirm what you understood, say what happens next and when (from the severity's reply time). Ask for the one missing fact that blocks progress, such as a screenshot or the account email. No fix promises.
6. **Sort the table.** S1 first, then S2, and within a level by oldest first. Put duplicates on one row with all IDs.

## Output format

```markdown
# Triage — [date, time] — [N] tickets

**Possible incident:** [what and which tickets, or "none"]

| ID | Summary | Category | Sev | Why | Route to | First reply |
|---|---|---|---|---|---|---|
| [ID] | [what's wrong, 1 line] | [category] | [S1–S4] | [rubric reason] | [owner] | [1–3 sentences] |

**Needs a human call:** [tickets where the severity or route was unclear, and why]
```

## Example

**Input:**

> #812 (Pro plan, 08:02): "Your export deletes my rows!!! 300 rows gone after I clicked Export."
> #813 (Free, 08:10): "would be great to have dark mode"
> #814 (Pro, 08:15): "Charged 2 times this month, please fix"
> #815 (Team, 08:20): "How do I add a teammate?"

**Output:**

```markdown
# Triage — 4 March, 08:30 — 4 tickets

**Possible incident:** none yet; watch for more export reports after #812

| ID | Summary | Category | Sev | Why | Route to | First reply |
|---|---|---|---|---|---|---|
| 812 | Rows deleted after Export | Bug | S1 | data loss | Engineering on-call | Thanks for telling us right away. Losing rows is serious and our engineers are looking now; I'll update you within the hour. Could you tell me which file you exported and roughly when? |
| 814 | Double charge this month | Billing | S1 | money taken wrongly | Billing owner | I'm sorry about the double charge. Our billing team is checking it now and I'll update you within the hour with what we found. |
| 815 | How to add a teammate | How-to | S3 | how-to question | Support | Go to **Settings > Team > Invite** and enter their email. Reply here if the invite doesn't arrive. |
| 813 | Dark mode request | Feature request | S4 | feature request | Product | Thanks for the idea. I've passed it to our product team. |

**Needs a human call:** none
```

## Checks before you send

- [ ] Every ticket has exactly one category, one severity, and one owner.
- [ ] Each severity names the rubric reason; none is based on tone alone.
- [ ] Anything with data loss, a security exposure, money taken wrongly, or many customers unable to use the product is S1.
- [ ] First replies promise a time from the rubric, never a fix date.
- [ ] The table is sorted S1 to S4, then oldest first.

## Common mistakes

- Marking every paying customer S2. Plan affects order within a level, not the level.
- Writing a full solution in the first reply for an S1. Acknowledge, set the update time, get the missing fact.
- Leaving 3 tickets about the same failure as 3 separate S2s. That's an incident.
