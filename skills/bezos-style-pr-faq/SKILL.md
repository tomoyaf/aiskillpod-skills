---
name: bezos-style-pr-faq
description: Drafts or reviews an internal working-backwards PR/FAQ for a product, feature or service before anything is built - a one-page press release written from the customer's side, an FAQ that answers the hard customer and internal questions, a so-what test, and a list of what would stop it - following the working-backwards approach Jeff Bezos described in the Amazon shareholder letters and the PR/FAQ format Amazon describes. Use when someone has a product idea, feature proposal or new service and asks for a PR/FAQ, a working backwards doc, a future press release, or wants to know whether the idea is worth building before the team starts.
---

# Bezos-style working-backwards PR/FAQ

These are principles Jeff Bezos has described publicly in the Amazon shareholder letters (the 2008 letter on working backwards from customer needs, the 2016 letter on resisting proxies), together with the PR/FAQ format as Amazon describes it in its 2024 shareholder letter (written by Andy Jassy) and in an excerpt from Working Backwards by Colin Bryar and Bill Carr published on Amazon's website. Not affiliated with or endorsed by Jeff Bezos or their companies. The skill turns an idea into an internal press release and FAQ written before the build, or reviews a draft one, and says plainly where the idea fails the so-what test.

## Ground rules

- Do not attribute quotes or opinions to Jeff Bezos beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Jeff Bezos; review the user's material against the principles below.
- This is an internal thinking document, not a news release for journalists. For a release that will go out to the press, use press-release-draft.
- Never invent customer evidence, prices, dates or numbers. Anything the user hasn't given is written as [check: ...].
- Keep the attribution straight: the 2008 and 2016 letters are Bezos's; the PR/FAQ page limits and review practice come from Bryar and Carr's excerpt; the "before we start coding" practice and the list of hard FAQ questions come from the 2024 letter.
- If the idea doesn't pass the so-what test, say so. A PR/FAQ that ends with a recommendation not to build yet is a good result.

## The principles

1. **Work backwards from customer needs, not forward from your skills.** Bezos contrasts working backwards from a customer need with a skills-forward approach that asks what else the company can do with what it is already good at. Used alone, skills-forward never pushes the company to build new skills; working backwards often does. Source: 2008 letter to shareholders (Kindle example).
2. **Write the press release and FAQ before building.** Amazon writes a press release and an FAQ before it starts coding a service or feature. The release checks that the proposal would be remarkable to customers; the FAQ forces the hard questions. Source: Amazon 2024 letter to shareholders, "Working backwards documents".
3. **The release must survive "so what?".** Executives reviewing a PR often ask "so what?". If the release doesn't describe something meaningfully better (faster, easier, cheaper) than what customers already have, or a step change in their experience, it isn't worth building. Source: Bryar and Carr excerpt on Amazon's website.
4. **The FAQ covers the customer and the cost.** The FAQ gives the details of the customer experience and a clear-eyed assessment of how expensive and hard the product will be to build. The 2024 letter lists the kinds of questions: which customers will use it, what they'll like most, what they'll be most disappointed with, why the launch line is drawn where it is, why it beats current alternatives, how to think about pricing, and why the architecture is what it is. Sources: Bryar and Carr excerpt; 2024 letter.
5. **Short on purpose.** The press release is a few paragraphs and always under one page; the FAQ is five pages or less. The limit is a forcing function for distilled thinking, not a report of all the work done. Source: Bryar and Carr excerpt.
6. **Review by reading, revise many times, and expect most not to ship.** In the review, everyone reads the document silently first; the most senior people tend to speak last. Drafts go through many rounds. Most PR/FAQs never become products, which the authors call a feature: it saves build resources for the best ideas. Source: Bryar and Carr excerpt.
7. **Don't let surveys stand in for the customer.** Bezos warns that market research and surveys can become proxies for customers. The owner of the product must understand the customer, have a vision and love the offering; research then helps find blind spots. Source: 2016 letter to shareholders, "Resist Proxies".

## When to use

- A product idea, feature, new service or internal tool is about to get people or budget.
- A team is excited about something it can build and nobody has written down who it is for.
- You want to compare several ideas on the same page before choosing one.
- Reviewing a PR/FAQ someone else wrote.
- Not for a press release to journalists (use press-release-draft), not for a decision between options that already exist (use decision-memo), and not for a full requirements document (use prd-from-notes once the PR/FAQ is approved).

## What you need

- The idea in a few sentences, and who it is for.
- What those customers do today instead, and what bothers them about it.
- Any evidence you have: interviews, support tickets, usage data, lost deals.
- Known constraints: budget, team, deadline, dependencies, regulation.
- A rough price or business model, if there is one.

## Steps

1. **Name the customer and the need (principle 1).** One sentence: who the customer is and what need they have, in their words where the user has them. If the idea starts from what the team is already good at rather than from a customer, say so and find the customer need first, or mark it [check: which customer asked for this].
2. **Write the headline and subheading.** The headline names the product and what changes for the customer. The subheading says who it is for and the main benefit in one sentence. No internal jargon.
3. **Write the release body (principles 2, 5).** Under one page: the problem as the customer feels it, the solution, how it works from the customer's side, one quote from a fictional company spokesperson and one from a fictional customer (both labelled as illustrative, never a real person), and how to start. Dates and prices the user hasn't given stay as [check: ...].
4. **Run the so-what test (principle 3).** Compare against what customers use today. Is it meaningfully faster, easier or cheaper, or a step change? Write the answer in one line. If the answer is no, stop here and say so before writing the FAQ.
5. **Write the customer FAQ (principle 4).** Questions a customer would ask: what it costs, how it differs from the alternative, what it doesn't do, what happens to their data, how to stop using it.
6. **Write the internal FAQ (principle 4).** The 2024 letter's questions, answered or marked [check]: which customers, what they'll like most, what will disappoint them, why the launch line is here, why better than alternatives, pricing, architecture choices. Add cost, team, timeline, dependencies and the riskiest assumption.
7. **List what would stop it (principle 6).** The open problems the FAQ surfaced, each with what would solve it (more time, a partner, a cheaper technology, a smaller first version) or a note that it can't be solved now.
8. **Check the evidence (principle 7).** For every claim about what customers want, note its evidence. Where the only evidence is a survey average, say what direct customer understanding is missing.
9. **Prepare the review.** Suggest a reading-first review: reviewers read silently, then comment, most senior last. Note the version number; expect more drafts.

## Output format

```markdown
# PR/FAQ: [product name] (draft [n], [date])
These are principles Jeff Bezos has described publicly. Not affiliated with or endorsed by Jeff Bezos or their companies. Internal document; not for publication.

## Press release
**[Headline]**
*[Subheading: who it is for and the main benefit]*

[City], [check: launch date] - [Paragraph 1: what launches and for whom]

[Paragraph 2: the problem, as the customer feels it]

[Paragraph 3: the solution and how it works from the customer's side]

"[Illustrative quote]," said [fictional spokesperson, role].

"[Illustrative quote]," said [fictional customer, who they are].

[How to start, price if known]

## So-what test
Customers today: [alternative] · Better because: [faster / easier / cheaper / step change, with the evidence] · Verdict: passes / doesn't pass yet

## Customer FAQ
**Q: [question]**
A: [answer]

## Internal FAQ
**Q: Which customers will use this first?**
A:
**Q: What will they like most? What will disappoint them most?**
A:
**Q: Why is the launch line drawn here?**
A:
**Q: Why is this better than current alternatives?**
A:
**Q: How should we think about pricing?**
A:
**Q: Why these architectural choices?**
A:
**Q: What will it cost, who builds it, and how long will it take?**
A:
**Q: What is the riskiest assumption?**
A:

## What would stop it
| Problem | What would solve it | Can we solve it now? |
|---|---|---|

## Evidence behind customer claims
| Claim | Evidence | Gap |
|---|---|---|

## Review plan
Read silently first; most senior comments last. Next draft after: [date].

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "We run a small bookkeeping firm for restaurants. We've built a script that reads supplier invoices from email. Idea: sell it as an app so restaurant owners see food costs per dish each week. Owners tell us they find out food costs only at month end, from us. 6 of our 40 clients said in a survey they'd 'probably' pay. No price yet."

**Output (excerpt):**

```markdown
These are principles Jeff Bezos has described publicly. Not affiliated with or endorsed by Jeff Bezos or their companies. Internal document; not for publication.

## Press release
**Plate Cost shows restaurant owners what each dish cost them this week**
*For independent restaurants that learn their food costs only at month end*

[City], [check: launch date] - Plate Cost reads supplier invoices as they arrive by email and shows, every Monday, what each dish on the menu cost to make last week.

Owners today see food costs once a month, from their bookkeeper, weeks after a supplier raised a price ...

"[Illustrative quote about seeing a price rise the same week]," said [fictional founder, Plate Cost].

## So-what test
Customers today: a month-end report from the bookkeeper · Better because: weekly instead of monthly, per dish instead of a total [check: do owners act on weekly numbers?] · Verdict: passes if owners change menus or orders on weekly data; not shown yet

## Internal FAQ
**Q: Which customers will use this first?**
A: Our existing restaurant clients, who already send us their invoices. [check: how many have recipes written down per dish]
**Q: What will disappoint them most?**
A: Dishes without written recipes get no per-dish cost until someone enters the recipe.
**Q: How should we think about pricing?**
A: [check: price] The survey (6 of 40 "probably") is a proxy; talk to those six about what they would stop doing if they had weekly costs.

## What would stop it
| Problem | What would solve it | Can we solve it now? |
|---|---|---|
| Most clients have no per-dish recipes | Start with each restaurant's best-selling dishes, entered with the owner | Yes, but it is manual |
| The script was built for our own staff, not owners | A simpler weekly email before an app | Yes |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output, and it is marked internal.
- [ ] The customer and their need are named before the product.
- [ ] The press release fits on one page and uses no internal jargon.
- [ ] Quotes in the release are labelled illustrative and come from fictional people only.
- [ ] The so-what test has a verdict, and a "doesn't pass" verdict is stated plainly.
- [ ] The internal FAQ answers the 2024 letter's questions or marks them [check].
- [ ] No invented prices, dates or customer numbers.
- [ ] Customer claims show their evidence; survey-only claims are flagged.

## Common mistakes

- Writing the release about the technology (how invoices get parsed) instead of what changes for the customer.
- Treating the PR/FAQ as a launch announcement and skipping the internal FAQ, where the hard questions are.
- Long documents with appendices that avoid deciding what matters.
- Taking a survey percentage as proof that customers want it.
- Treating a PR/FAQ that doesn't get approved as wasted work.
