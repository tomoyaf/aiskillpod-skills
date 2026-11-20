---
name: terms-update-notice
description: Drafts the customer notice for a Terms of Service or Privacy Policy update, by email and in-app banner, saying what changed in plain words, the effective date, what users need to do, and where to read the full text, with a summary of changes table and links. Flags changes that may need consent rather than notice. Use when someone says "we updated our terms", "privacy policy change email", "notify users of new terms", or asks how to announce a policy change.
---

# Terms update notice

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A good update notice lets a customer learn in 30 seconds what changed for them, from when, and whether they must act. It never hides a change that matters inside a list of small ones, because a quiet change to how data is used is exactly what regulators object to.

## When to use

- Your Terms of Service, Privacy Policy, Acceptable Use Policy, or DPA changes and customers must hear about it.
- You need the email, the in-app banner, and the "what changed" summary at the top of the policy page.
- Not for writing the new terms or deciding if a change is allowed. Counsel decides that; this skill announces it.

## What you need

- The old and new text, or a list of changes with section numbers. If only the new text is given, ask once for the old one; without it you can't say what changed and must write "[check: what changed]".
- The effective date and the date the notice goes out. If missing, write "[check: effective date]"; never pick one.
- What users must do, if anything (accept, opt in, opt out, nothing). If not stated, write "[check: required action]".
- Links to the full new text and, ideally, a redline or archived old version.
- Who receives it: all users, paying customers, admins only, a region.

## Steps

1. **List each change and sort it.** For every change, write one plain sentence of what it means for the user. Then sort: affects users' rights, money, or data (material, by our default) or wording only (minor). If unsure, treat it as material.
2. **Flag changes that may need more than notice.** The FTC warned in February 2024 that adopting more permissive data practices, such as sharing data with third parties or using it for AI training, through a quiet, retroactive change to terms or a privacy policy may be unfair or deceptive. In its Gateway Learning case, the order barred applying material privacy policy changes to data already collected without consumers' consent. So if a change uses existing data in a new way, mark it "[ask counsel: is notice enough, or do we need consent for data already collected?]" and don't draft it as notice-only until counsel answers.
3. **Lead with the 1 to 3 changes that matter.** The subject line and first sentence name the most important change, not "We've updated our terms". Minor wording fixes go in one closing line.
4. **State the dates and the action.** Effective date in full ("1 December 2026"). What happens if the user does nothing, as stated in the input; if the input doesn't say, write "[check: what happens if the user does nothing]". If an action is required, give one button or link for it.
5. **Point to the full text.** Link the new version and the old version or a redline. Say where questions go (an address or help page, never a no-reply mailbox).
6. **Draft 3 pieces.** An email (under 200 words, our default), an in-app banner (under 25 words), and a "Summary of changes" table for the top of the policy page. Same facts, same dates in all 3.
7. **Strip spin.** Don't write "to serve you better" or "we value your privacy" around a change that takes something from the user. Say what it is.

## Output format

```markdown
_Not legal advice. Draft for review by counsel before sending._

## Email
**Subject:** [Most important change] — effective [date]

[1 sentence: what changes and from when.]

What's changing:
- [Change 1 in plain words] ([section])
- [Change 2]

What you need to do: [action, or "nothing"; what happens if you do nothing]

Read the new [Terms/Privacy Policy]: [link] · Compare with the previous version: [link]
Questions: [contact]

## In-app banner
[Under 25 words: change, date, link]

## Summary of changes (top of policy page)
| Section | What changed | Effective |
|---|---|---|
| [n] | [plain words] | [date] |

## Flags for counsel
- [ask counsel: ...]
```

## Example

**Input:** Ada at Mapleform (survey tool). Privacy Policy changes, effective 1 December 2026, notice sent 1 November 2026: (1) adds a new subprocessor for email delivery, §6; (2) survey responses may now be used to train Mapleform's answer-suggestion model, §4; (3) fixes typos in §9. Action: the company plans "notice only". Links: mapleform.example/privacy, mapleform.example/privacy/2025.

**Output:**

```markdown
_Not legal advice. Draft for review by counsel before sending._

## Email
**Subject:** How we may use survey responses is changing — effective 1 December 2026

From 1 December 2026, Mapleform may use survey responses to train our answer-suggestion feature.

What's changing:
- Survey responses may be used to train our answer-suggestion model (§4). [check: does this apply to responses collected before 1 December?]
- We're adding a new email delivery provider to our subprocessor list (§6).
- We fixed typos in §9; nothing about your rights changes there.

What you need to do: [check: required action — see flags for counsel]

Read the new Privacy Policy: mapleform.example/privacy · Compare with the previous version: mapleform.example/privacy/2025
Questions: [check: contact address]

## In-app banner
From 1 December, survey responses may train our suggestion feature. See what's changing.

## Summary of changes (top of policy page)
| Section | What changed | Effective |
|---|---|---|
| §4 | Survey responses may be used to train the answer-suggestion model | 1 December 2026 |
| §6 | New email delivery subprocessor | 1 December 2026 |
| §9 | Typo fixes only | 1 December 2026 |

## Flags for counsel
- [ask counsel: §4 uses existing data in a new way. Is notice enough, or do we need consent, at least for responses collected before 1 December?]
- [ask counsel: is 30 days' notice appropriate for the regions we serve?]
```

## Checks before you send

- [ ] The disclaimer line is at the top of the output.
- [ ] The subject line names the most important change, not "We've updated our terms".
- [ ] Every change appears in plain words with its section number.
- [ ] Any new use of existing data is flagged for counsel, not sent as notice-only.
- [ ] Effective date and required action match in the email, banner, and table, or carry "[check: ...]".
- [ ] Links go to the new text and to the old version or a redline.

## Common mistakes

- Burying the change that matters between typo fixes.
- Writing "by continuing to use the service you agree" without checking with counsel that it's enough for this change.
- Sending from a no-reply address, so customers with questions have nowhere to go.
