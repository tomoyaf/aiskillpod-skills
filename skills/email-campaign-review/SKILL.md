---
name: email-campaign-review
description: Reviews a marketing email before it's sent - subject line and preheader, a single CTA, how it scans on a phone, links, personalization fallbacks, and the compliance footer with unsubscribe - and returns a send or fix-first verdict with line edits. Use when someone shares a marketing email, newsletter, or promo draft and asks to review, proofread, QA, or "check before I hit send".
---

# Email campaign review

The review answers one question: can this go out now? Broken merge tags, a missing unsubscribe, and 3 competing buttons are fix-first; wording preferences are not. Say the verdict first, then only the edits that change results.

## When to use

- Before sending a promotional email, newsletter, or announcement to a list.
- When an email's open or click rate dropped and you want a second look at the next one.
- Not for one-to-one sales emails or transactional receipts: different rules for both.

## What you need

- The email: subject, preheader, body, button labels, and every link URL. HTML or a screenshot both work; with a screenshot, say links couldn't be checked.
- The audience segment and the email's one goal (click to X, buy Y, register for Z). If the goal is missing, ask once; without it you can't judge the CTA.
- Merge fields used (first name, company) and their fallbacks. If unknown, flag every merge tag as "fallback: to confirm".
- Sender name and the region of the list (affects footer rules).

## Steps

1. **Check the inbox view.** The subject must not mislead about what's inside (CAN-SPAM). Our defaults: subject under 50 characters, no ALL CAPS words, no more than 1 emoji. Preheader under 90 characters, adds to the subject instead of repeating it, and isn't the default "View in browser" text. Sender name is a person or the brand people recognize.
2. **Find the one CTA.** Count distinct actions. Our default: one primary action, repeated at most twice (button above the fold and once near the end). Two or more different actions is a fix-first unless it's a newsletter. Button label is verb-first and names the result ("Book your seat", not "Click here").
3. **Scan as a phone reader.** Our default: assume a 375 px wide screen. The point and the button should be visible within the first screen (about 4 short lines plus a button). Paragraphs of 3 lines or fewer. Text is live text, not an image. Images have alt text.
4. **Check every link.** Each URL goes where its label says, has UTM tags if the team uses them, and none points to a staging or preview domain. Flag duplicate links with different UTMs.
5. **Test personalization.** For each merge tag, read the sentence with the fallback in place ("Hi there,") and with an empty value ("Hi ,"). An empty-value bug is fix-first.
6. **Check compliance.** US (CAN-SPAM, per the FTC): accurate From and Reply-To, the email clearly identified as an ad, a valid physical postal address, and a clear way to opt out, honoured within 10 business days. Every sender to Gmail keeps the spam rate in Postmaster Tools below 0.3% (Gmail's target is below 0.1%). Gmail and Yahoo, for bulk senders (Gmail: more than 5,000 messages a day to Gmail accounts), also require one-click unsubscribe in the headers (RFC 8058) plus a visible unsubscribe link in the body, SPF, DKIM, and a DMARC policy (p=none is enough). Yahoo asks that unsubscribes are honoured within 2 days. Authentication and spam rate live outside the email; if the user can't confirm them, list them as "[check: sending setup]". Our default: a line saying why the reader gets this email. EU, UK, and other lists have their own consent rules; mark "[check: legal]" rather than stating law you haven't confirmed.
7. **Give the verdict.** Fix first if any of these: broken or empty merge tag, missing unsubscribe or address, a wrong or staging link, no clear CTA, or a factual claim (price, date) that contradicts the input. Otherwise send, with optional edits.

## Output format

```markdown
**Verdict:** [Send / Fix first] — [one-line reason]

## Fix first
| # | Where | Problem | Edit |
|---|---|---|---|
| 1 | [subject / line / link] | [problem] | [exact replacement] |

## Worth changing
| # | Where | Suggestion | Why |
|---|---|---|---|

## Checklist
- Subject ([n] chars): [ok / issue]
- Preheader ([n] chars): [ok / issue]
- CTA: [count] distinct actions — [ok / issue]
- Mobile first screen: [ok / issue]
- Links: [n] checked — [ok / issue]
- Merge tags: [list with fallbacks]
- Footer: unsubscribe [yes/no], one-click [yes/no / not needed], address [yes/no], reason [yes/no]
```

## Example

**Input:** Subject "🎉🎉 HUGE NEWS: Our Spring Webinar Series is here and you're invited!", preheader "View this email in your browser". Body: "Hi *|FNAME|*, ... The series has 3 sessions ... Register for the webinar ... Also check out our new pricing page ... Follow us on LinkedIn". Button "Click here", below 2 paragraphs, links to app-staging.fernwood.example/webinar. Footer has unsubscribe, no address. Goal: webinar registrations.

**Output:**

```markdown
**Verdict:** Fix first — the button goes to a staging site and the footer has no postal address.

## Fix first
| # | Where | Problem | Edit |
|---|---|---|---|
| 1 | Button link | Points to app-staging.fernwood.example | Use the live registration URL [check: correct URL] |
| 2 | Footer | No physical postal address (CAN-SPAM requires one for US recipients) | Add the company's postal address |
| 3 | "Hi *\|FNAME\|*," | No fallback set; empty names show "Hi ," | Set the fallback to "there" |
| 4 | Body | 3 actions: register, pricing page, LinkedIn | Keep register; move pricing and LinkedIn to the footer or cut them |

## Worth changing
| # | Where | Suggestion | Why |
|---|---|---|---|
| 1 | Subject (67 chars) | "Spring webinars: 3 sessions, pick yours" | Fits on a phone; drops caps and doubled emoji |
| 2 | Preheader | "3 sessions this spring. Pick the one that fits your week." | The default text wastes the second line |
| 3 | Button | "Save my seat" | Names the result |

## Checklist
- Subject (67 chars): over 50, caps, 2 emoji
- Preheader (31 chars): default browser text
- CTA: 3 distinct actions — cut to 1
- Mobile first screen: button sits below 2 paragraphs — move it up
- Links: 4 checked — 1 staging
- Merge tags: FNAME, no fallback
- Footer: unsubscribe yes, one-click [check: sending volume], address no, reason no
```

## Checks before you send

- [ ] The verdict is the first line, and fix-first items are only those listed in step 7.
- [ ] Every edit is an exact replacement, not "make it punchier".
- [ ] Subject and preheader lengths are counted and shown.
- [ ] Every link and merge tag in the input is listed as checked.
- [ ] Legal points say "[check: legal]" unless the rule is certain.

## Common mistakes

- Burying a broken link under 12 style comments.
- Rewriting the whole email when 3 edits would do.
- Passing an image-only email because it looks good on desktop.
