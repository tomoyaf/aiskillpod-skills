---
name: roadmap-update
description: Writes a product roadmap update for stakeholders (leadership, sales, CS, investors, or customers) in a Now, Next, Later format, tied to outcomes, with what moved since the last update and why, what the team is not doing, firm commitments kept separate, and clear asks. Use when someone asks for a roadmap update, a product update for the team, a quarterly roadmap review, or "what's coming and what changed" from a backlog, planning notes, or the last roadmap.
---

# Roadmap update

Stakeholders read a roadmap update to learn three things: what changed, why, and what it means for them. Lead with what moved. Tie each item to the problem or outcome it serves, keep dates only for true commitments, and say plainly what the team won't do, so nobody plans around it.

## When to use

- Monthly or quarterly roadmap reviews for leadership, sales, CS, or the board.
- After priorities change and people need to know what slipped and why.
- For a customer-facing "what's coming" note (with a stricter filter, see step 6).
- Not for shipped work: use release-notes. Not for deciding priorities: use feature-prioritization first.

## What you need

- The current roadmap or list of initiatives with status.
- The last update, so you can show what moved. If missing, ask once; otherwise say "first update, no changes shown".
- The reasons for any changes. If a reason isn't given, write "[check: reason]" rather than inventing one.
- The audience. Default to internal leadership.

## Steps

1. **Sort into Now, Next, Later.** Janna Bastow's Now-Next-Later format: Now = being worked on and well defined; Next = follows once Now finishes, less detailed; Later = bigger problems not yet broken into solutions. Columns don't need to be the same size.
2. **Write each item as a problem or outcome.** "Cut time to first invoice from 2 days to 1 hour", not "Invoice wizard". Link it to the business objective it serves. This follows Marty Cagan's point that roadmaps should state the problem and outcome, not just a feature list.
3. **Show what moved and why.** Compare with the last update. For each item that moved columns, was added, or dropped, give one reason: new evidence, a customer commitment, capacity, a dependency. Put this section first.
4. **Keep commitments separate.** Items with a promised date (a contract, a legal deadline, a launch event) go in their own list with the date and owner. Cagan calls these high-integrity commitments; everything else carries no date.
5. **Say what we're not doing.** List 2 to 5 requests the team decided against or parked, with the reason. Sales and CS need this most.
6. **Adjust for the audience.** Leadership: outcomes, risks, decisions needed. Sales and CS: what to tell customers and what not to promise. Customers: Now and Next only, no internal names, no dates except committed ones, and "plans can change" stated once.
7. **End with asks.** Name the decision, resource, or input you need, from whom, by when. If there are no asks, write "No asks this time".

## Output format

```markdown
# Roadmap update — [period]

**For:** [audience] · **Since last update:** [date]

## What changed
- **[Item]** moved [from → to] — [reason]
- **Added:** [item] — [reason]
- **Dropped:** [item] — [reason]

## Now
- **[Outcome]** — [objective it serves] · [status: on track / at risk] · [owner]

## Next
- **[Outcome]** — [objective it serves]

## Later
- **[Problem to solve]**

## Commitments with dates
| Commitment | Date | Owner | Status |
|---|---|---|---|

## What we're not doing
- [Request] — [reason]

## Asks
- [Ask] — [from whom] by [date]
```

## Example

**Input:** "May update for leadership. We make invoicing software for small-business owners. Last month Now was: auto reminders for late invoices, CSV export. Next: read-only seats so owners can share their books with their accountant, mobile app. CSV export shipped. Auto reminders slipped because interviews showed owners chase late payers by text, not email; we're re-scoping them to texts. SSO is promised to Northwind by June 30. We're dropping the mobile app for now; only 2% of sessions are mobile. Need a decision on whether CS can promise read-only seats to customers."

**Output:**

```markdown
# Roadmap update — May

**For:** leadership · **Since last update:** [date]

## What changed
- **CSV export** shipped (moved out of Now).
- **Payment reminders** stays in Now, re-scoped to text messages — interviews showed users chase by text, not email.
- **Added:** SSO for Northwind — promised to Northwind by June 30.
- **Dropped:** mobile app — 2% of sessions are mobile.

## Now
- **Get late invoices paid without manual chasing** (payment reminders by text) — retention objective [check: name] · at risk (re-scoped) · [owner]
- **SSO for Northwind** — customer commitment · [check: status] · [owner]

## Next
- **Let owners share books with their accountant** (read-only seats) — expansion objective [check: name]

## Later
- **Using the product on a phone** — revisit if mobile sessions grow.

## Commitments with dates
| Commitment | Date | Owner | Status |
|---|---|---|---|
| SSO for Northwind | June 30 | [owner] | [check: status] |

## What we're not doing
- Mobile app — 2% of sessions are mobile; parked for now.
- Email-only reminders — users told us they chase by text.

## Asks
- Can CS tell customers read-only seats are coming? It's in Next, not committed. — decision from [leadership] by [date]
```

## Checks before you send

- [ ] "What changed" comes first and every move has a reason from the input or "[check: reason]".
- [ ] Every Now and Next item is written as an outcome or problem, not just a feature name.
- [ ] Only commitments carry dates.
- [ ] "What we're not doing" has at least 2 items, or says why it's empty.
- [ ] Every ask names who decides and by when.
- [ ] A customer version has no internal names, owners, or uncommitted dates.

## Common mistakes

- Putting dates on Next and Later items to look certain. Those dates get forwarded as promises.
- Hiding a slip inside the Now list. Put it in "What changed" with the reason.
- Listing 20 items. Keep Now to what the team is actually doing this period.
