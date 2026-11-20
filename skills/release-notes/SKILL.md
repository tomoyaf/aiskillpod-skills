---
name: release-notes
description: Writes customer-facing release notes from a list of merged changes, pull requests, or tickets, grouped into New, Improved, and Fixed, with each line leading with the benefit to the user and no internal jargon or ticket IDs. Also writes an internal changelog variant for the team. Use when someone pastes merged PRs, a Jira or Linear export, or a sprint list and asks for release notes, a changelog, "what's new", or a product update.
---

# Release notes

Customers read release notes to answer one question: what can I do now that I couldn't before? Lead every line with that answer in their words. Leave out what they can't see, and never make them decode a ticket title.

## When to use

- After a release, from a list of merged PRs, tickets, or commit messages.
- For a "What's new" page, an in-app changelog, or a monthly product update email.
- When the team also needs an internal changelog with ticket IDs for support and sales.
- Not for a launch announcement of one big feature: use launch-announcement.

## What you need

- The list of changes: PR titles, ticket titles and descriptions, or commit messages.
- The release name or date. If missing, ask once, then write "[release date]".
- Who the customers are, so you pick their words. If unknown, write for a non-technical user.
- Optional: links to help articles for new features.

## Steps

1. **Drop what customers can't see.** Refactors, dependency bumps, test changes, CI, internal tools, and logging go only into the internal variant. If a change has no visible effect, it isn't a release note.
2. **Sort into New, Improved, Fixed.** New = something users couldn't do before. Improved = something they could do, now faster, clearer, or broader. Fixed = something that was broken and now works. If a ticket is unclear, put it in the internal list with "[check: what changed for users?]" rather than guessing.
3. **Rewrite each line benefit-first.** Start with what the user can now do, then how. "Export invoices to CSV from the Invoices page", not "Added CSV export endpoint". Use the product's screen and button names, not code names.
4. **Write fixes so users recognize the bug.** Describe the symptom they saw: "Dates no longer shift by one day for users in Asia time zones." Don't blame or over-apologize. Skip fixes for bugs that never reached customers.
5. **Order by impact.** The most-used or most-requested change goes first in each group. Merge several tickets that are one change for the user into one line.
6. **Cut length.** One line per change, 20 words or fewer (our default; a sentence or two is the usual guidance). Add a 1-sentence intro only if one change dominates the release. Link a help article when a new feature needs setup.
7. **Write the internal variant.** Use the Keep a Changelog types: Added, Changed, Deprecated, Removed, Fixed, Security, latest release first with its date. Add ticket IDs, an "Internal" group for invisible work, and anything support should know (changed behavior, known issues, migration steps).

## Output format

```markdown
## [Release name or date]

[Optional: 1 sentence on the biggest change.]

### New
- [What users can now do, and where.] [Link if setup is needed]

### Improved
- [What got better, in the user's terms.]

### Fixed
- [Symptom the user saw, now fixed.]

---

## Internal changelog — [release name or date]

### Added
- [Plain description] ([ticket ID], [owner])

### Changed
- [Plain description] ([ticket ID])

### Deprecated / Removed
- [Plain description, or remove this section] ([ticket ID])

### Fixed
- [Plain description] ([ticket ID])

### Security
- [Plain description, or remove this section] ([ticket ID])

### Internal
- [Refactors, dependency updates, tooling] ([ticket ID])

### Support should know
- [Changed behavior, known issues, or "nothing"]
```

## Example

**Input:**

> LIN-412 Add CSV export to invoices list
> LIN-418 Fix timezone offset bug in due date picker (UTC+8 and later)
> LIN-420 Bump stripe-node to 14.2
> LIN-421 Invoice list pagination now 50 instead of 20
> LIN-425 Refactor PDF renderer
> LIN-426 Reminder emails: add customer's company name to subject

**Output:**

```markdown
## March 12 release

### New
- Export your invoices to a CSV file from the Invoices page, ready for your spreadsheet or accountant.

### Improved
- The Invoices page now shows 50 invoices at a time, so you scroll less.
- Reminder emails now include your customer's company name in the subject line, so they stand out in the inbox.

### Fixed
- Due dates no longer move back a day for users in Asia and Australia time zones.

---

## Internal changelog — March 12

### Added
- CSV export on the invoices list (LIN-412)

### Changed
- Invoice list page size 20 to 50 (LIN-421)
- Customer company name in reminder subject (LIN-426)

### Fixed
- Due date picker offset for UTC+8 and later (LIN-418)

### Internal
- stripe-node 14.2 (LIN-420)
- PDF renderer refactor (LIN-425)

### Support should know
- Customers who filter reminder emails by subject may need to update their filter (LIN-426).
```

## Checks before you send

- [ ] The customer section has no ticket IDs, code names, or words like "endpoint", "refactor", or "bump".
- [ ] Every line starts with what the user can do or what they'll notice.
- [ ] Each change appears in exactly one group.
- [ ] No change is described beyond what the ticket says; unclear ones carry "[check: ...]" in the internal list.
- [ ] Every line is 20 words or fewer.

## Common mistakes

- Copying ticket titles with light edits. "Fix timezone offset bug" means nothing to a customer; describe the symptom.
- Listing invisible work to make a release look bigger. It buries the changes people care about.
- Promising what's next in release notes. Keep them to what shipped.
