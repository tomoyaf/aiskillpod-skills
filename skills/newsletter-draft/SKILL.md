---
name: newsletter-draft
description: Drafts a company or customer newsletter issue from a list of updates - picks one lead story, writes 3 to 5 short items, and ends with one call to action - plus subject line and preheader options. Use when someone shares product updates, news, or links and asks for a newsletter, a monthly update email, a customer update, "this month at [company]", or an issue draft.
---

# Newsletter issue draft

A newsletter gets opened next month only if this month's was worth reading. That means one story told properly, a few items a reader can scan in 10 seconds, and one thing to do. Everything else waits for the next issue.

## When to use

- A monthly or biweekly customer, user, or community newsletter is due.
- Someone has a pile of updates (features, posts, events, hires) and needs an issue.
- An internal company newsletter, with the same rules.
- Not for a single-purpose promo email or a launch: those have one message, not several items.

## What you need

- The list of updates, with links. If an item has no detail, ask once; if none comes, keep it to one line or drop it.
- Who reads it (customers, prospects, users, staff) and what they care about. If missing, assume customers and mark "[assumption]".
- The one action this issue wants (book a call, try a feature, register). If none is given, pick the action tied to the lead story and say so.
- Optional: a past issue, to match length and tone.

## Steps

1. **Choose the lead story.** Score each update on: does it change what the reader can do, does it have a number or a customer in it, is it new since the last issue. The top scorer leads. A feature customers asked for beats a company milestone; a hire or award never leads a customer newsletter.
2. **Write the lead: 80 to 150 words (our default).** Most important fact first (NN/g's inverted pyramid): what changed, what the reader can now do, one concrete example or number, one link. Open with the reader's situation, not "We're thrilled".
3. **Write 3 to 5 short items.** Each: a bold 3 to 7 word title, 1 to 2 sentences, one link. Order by usefulness to the reader. More than 5 items: cut the weakest and list them under "Not in this issue" for the user.
4. **Write one CTA.** One button or link, verb-first, tied to the lead story. Other links stay inside items; no second button.
5. **Write subject lines and a preheader.** 3 subject options; Mailchimp recommends no more than 9 words and 60 characters, and our default is under 50 so mobile inboxes show it whole. One names the lead story's benefit, one uses its number, one is plain ("[Company] in [month]: [lead]"). Preheader (preview text) under 90 characters with the key words first, as Litmus recommends; it adds what the subject leaves out and never repeats it.
6. **Cut to fit.** Our default: total body under 400 words. Every item must survive "would a reader miss this?". Check every name, number, and date against the input; never invent a metric or quote.
7. **Add the footer the law asks for.** A newsletter to customers or prospects that promotes your products is commercial email. In the US, CAN-SPAM covers it, business-to-business included (the FTC's compliance guide): a valid physical postal address and a clear way to unsubscribe, honored within 10 business days. Include a line that it's an ad by default; leave it out only when the user confirms that every recipient gave prior affirmative consent to receive it, as people who signed up for the newsletter have (15 U.S.C. § 7704(a)(5)(B)). If that isn't confirmed, keep the line. Sending more than 5,000 messages a day to Gmail accounts also brings Gmail's bulk-sender rules, including one-click unsubscribe. For recipients in other countries, add "[check: local email rules]". An internal newsletter to staff isn't commercial email. The footer doesn't count toward the word limit.

## Output format

```markdown
**Subject options**
1. [benefit]
2. [number]
3. [plain]

**Preheader:** [text]

---

# [Issue title]

[Lead story, 80–150 words, with link]

## Also new
**[Item title].** [1–2 sentences.] [link]

**[Item title].** [1–2 sentences.] [link]

[CTA button text] → [link]

[Sign-off, name]
[Postal address] · [Unsubscribe link] · [A line that it's an ad: keep it unless every reader's sign-up is confirmed]

---
**Not in this issue:** [dropped items, or "none"]
```

## Example

**Input:** Readers: customers of Pallet, warehouse inventory software, who signed up for the newsletter. Issue: February. Updates: (1) barcode scanning now works offline in the iOS and Android apps from version 4.2: scan as usual, and counts sync when the device reconnects; if two devices count the same bin while offline, both counts are kept and the bin is flagged for review; turn it on under Settings → Scanning → Offline mode; asked for by 40+ customers, most of them for cold rooms and loading docks where the Wi-Fi drops; (2) new help article on setting up rolling cycle counts without stopping picks; (3) we hired a VP of Sales; (4) 45-minute webinar on 12 March about stock levels and staffing before peak season; (5) CSV export is 3x faster: large inventory exports that took minutes now finish in seconds; (6) office moved. Action: try offline scanning. Sign-off: Dana, Pallet customer team.

**Output:**

```markdown
**Subject options**
1. Scan barcodes with no Wi-Fi
2. Offline scanning, asked for by 40+ of you
3. Pallet in February: offline scanning

**Preheader:** Plus CSV exports 3x faster, and a peak-season webinar on 12 March.

---

# Scanning now works without Wi-Fi

Cold rooms and loading docks where the Wi-Fi drops are no longer dead zones. Barcode scanning in the Pallet app now works offline: scan as usual, and counts sync the moment your device reconnects. If two devices count the same bin while offline, Pallet keeps both counts and flags the bin for review, so no count is overwritten. More than 40 of you asked for this, most of you for exactly those spots. It works in the iOS and Android apps from version 4.2; turn it on under Settings → Scanning → Offline mode. [link]

## Also new
**CSV export, 3x faster.** Large inventory exports that took minutes now finish in seconds. [link]

**Cycle counts, step by step.** A new help article on setting up rolling counts without stopping picks. [link]

**Peak-season prep webinar, 12 March.** 45 minutes on stock levels and staffing before peak season. [link]

Turn on offline scanning → [link]

Dana, Pallet customer team
You're getting this because you signed up for Pallet's customer newsletter. Pallet · [postal address] · Unsubscribe: [link]

---
**Not in this issue:** VP of Sales hire, office move (not useful to customers).
```

## Checks before you send

- [ ] One lead story, 80 to 150 words, about what the reader can now do.
- [ ] 3 to 5 short items, each with one link.
- [ ] Exactly one CTA button, verb-first, tied to the lead.
- [ ] Subject lines under 50 characters (9 words max); preheader under 90 and doesn't repeat the subject.
- [ ] Body under 400 words; every number and date matches the input.
- [ ] For US recipients: a postal address and a way to unsubscribe, and a line that it's an ad unless the user confirmed that every reader signed up.

## Common mistakes

- Leading with company news (funding, hires, awards) in a customer newsletter.
- Giving every item the same weight. Readers skim; the lead gets the space.
- Adding a second CTA "just in case". A second button competes with the one that matters.
