---
name: faq-from-tickets
description: Turns a batch of support tickets, chats, or emails into an FAQ. Clusters them by the underlying question, counts how often each comes up, writes each question in the customer's own words with a short answer, and flags answers that need product or policy confirmation. Use when someone shares an export of tickets or chat logs and asks for an FAQ, "top questions", "what do customers keep asking", or help-center gaps.
---

# FAQ from tickets

An FAQ built from tickets answers the questions customers actually ask, in the words they use, ordered by how often they ask. Count first, write second: the frequency tells you which 10 answers save the most replies.

## When to use

- You have an export of tickets, chat transcripts, or support emails (20 or more is ideal).
- The help center feels out of date and you want to know what's missing.
- A new product area launched and you want its FAQ from the first month of questions.
- Not for a single ticket that needs a reply: use reply-in-our-tone.

## What you need

- The tickets: text, ideally with a date and the agent's reply. Remove names, emails and card numbers before pasting; if you see them, don't repeat them.
- The answers, if known: past agent replies, help articles, or policy notes. If a ticket has no answer anywhere, draft one and flag it "[confirm: ...]".
- Optional: the current FAQ, so you can mark which questions are new.

## Steps

1. **Read every ticket and write its question in one line.** Use the customer's words, not the product team's: "Why was I charged twice?" not "Duplicate billing event". If a ticket asks 2 things, write 2 questions.
2. **Cluster by the underlying question.** "Can I get my money back?" and "How do refunds work?" are one cluster. "Refund for an annual plan" and "refund after cancelling" are separate if the answer differs. Rule: same answer, same cluster.
3. **Count and rank.** Count tickets per cluster. Sort by count, highest first. Clusters with 1 ticket go under "Seen once" unless the answer is about money, data loss or security.
4. **Pick the question wording.** For each cluster, pick the most common phrasing from the tickets as the FAQ question. Keep it a question a customer would type into search.
5. **Write the answer in 1 to 4 sentences.** Answer first, then the one condition or step that matters. Name buttons exactly as the product shows them, in bold. Take the answer from agent replies or docs given; never invent a policy, a price or a timeline.
6. **Flag what needs confirmation.** Mark an answer "[confirm: product]" or "[confirm: policy]" when agents answered it differently from each other, when it depends on a rule you haven't seen, or when it promises money or time. Say what to confirm.
7. **Note the fix behind the FAQ.** If a cluster has 5 or more tickets and comes from a confusing screen or a bug, add one line under "Fix the cause" so the FAQ isn't the only answer.

## Output format

```markdown
# FAQ draft from [N] tickets ([date range])

## Top questions
### 1. [Question in customer words] — [count] tickets
[Answer, 1–4 sentences.]
[confirm: what to check, with whom — or remove]

### 2. [...]

## Seen once
- [Question] — [one-line answer or "no answer found"]

## Fix the cause
- [Cluster] ([count] tickets): [the screen, bug, or email that creates the question]

## Notes
- New vs current FAQ: [questions not in the current FAQ, or "no current FAQ given"]
- Tickets skipped: [count and why, e.g. spam, not a question]
```

## Example

**Input (5 of 41 tickets, excerpt):**

> 1. "how do i add my accountant so she can see invoices" — Agent: Settings > Team > Invite, pick Viewer.
> 2. "Can my bookkeeper log in without paying for a seat?" — Agent: Viewers are free.
> 3. "I cancelled but got charged again??" — Agent: renewal ran before cancel; refunded.
> 4. "charged after cancelling" — Agent: cancels take effect at end of period, no refund.
> 5. "where do I download invoices" — Agent: Billing > Invoices > Download PDF.

**Output (excerpt):**

```markdown
# FAQ draft from 41 tickets (1–30 September)

## Top questions
### 1. How do I add my accountant so they can see invoices? — 9 tickets
Go to **Settings > Team > Invite** and choose **Viewer**. Viewers can see invoices, and they don't use a paid seat.

### 2. Why was I charged after I cancelled? — 7 tickets
[confirm: policy — agents gave 2 answers: one refunded, one said cancels take effect at the end of the billing period. Confirm the rule with the billing owner before publishing.]

### 3. Where do I download my invoices? — 6 tickets
Go to **Billing > Invoices** and click **Download PDF** next to the invoice.

## Fix the cause
- Charged after cancelling (7 tickets): the cancel screen doesn't say when the plan ends.

## Notes
- New vs current FAQ: no current FAQ given.
- Tickets skipped: 3 (spam, 2 thank-you replies).
```

## Checks before you send

- [ ] Every cluster has a ticket count, and the list is sorted by count.
- [ ] Each question uses wording that appears in the tickets.
- [ ] Every answer comes from an agent reply or doc given, or carries a "[confirm: ...]" flag.
- [ ] Clusters where agents disagreed are flagged, not silently resolved.
- [ ] No customer name, email, or account detail appears in the FAQ.

## Common mistakes

- Clustering by product area ("Billing") instead of by question. "Billing" is a section, not an FAQ entry.
- Picking the clearest agent answer when two agents contradicted each other. Flag it; the policy owner decides.
- Writing long answers. If an answer needs more than 4 sentences, it's a help article: note it for help-article-writer.
