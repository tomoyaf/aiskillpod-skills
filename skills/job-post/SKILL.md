---
name: job-post
description: Writes a job post (job ad, job listing, job description for a careers page or LinkedIn) from a role intake or scorecard - an honest title, the work in the first 6 months, at most 5 must-haves kept apart from nice-to-haves, a pay-range line where pay-transparency rules may apply, an inclusive-language check, and clear steps to apply. Use when you need to post a role, rewrite a job ad that gets few or wrong applicants, or turn intake notes into a listing.
---

# Job post from a role intake

A job post is a sales page for the work, read by people who already have a job. Say what they will actually do in the first 6 months, what they must already be able to do, and what it pays. Everything else is shorter than you think.

> Not legal advice. Pay-transparency and anti-discrimination rules differ by country, state and city. Lines marked "[check: local law / HR]" need HR or counsel before you post.

## When to use

- You have a role intake, a scorecard, or a hiring manager's notes and need a post for your careers page, LinkedIn, or a job board.
- An existing post gets few applicants, or many who can't do the job.
- You hire in places with pay-transparency rules and need the pay line right.
- Not for an internal job description used for grading or contracts; that needs HR's own format.

## What you need

- The role intake or scorecard: outcomes, must-haves, level, location. If missing, ask for the 3 things the hire must get done in 6 months; without them, run role-intake first.
- The pay range and where the role can be filled (cities, countries, remote). If no range is given, write "[pay range needed]" and don't post.
- How to apply and what happens next (steps, rough timing). If missing, use our default: apply form, then a 30-minute call, then the interview loop.
- Optional: the company's own one-paragraph description and benefits list.

## Steps

1. **Pick an honest title.** Use the title people search for and that matches the level: "Customer Support Lead", not "Customer Happiness Ninja". Our default: no rockstar, ninja, guru, or invented levels. If the internal title differs, use the searchable one and mention the internal one once.
2. **Write the opening in 2 to 3 sentences.** What the team does, why the role exists now, and who the hire reports to. No company history.
3. **Describe the first 6 months.** 3 to 5 bullets, each an outcome with a rough time: "By month 3, you run the weekly support report on your own." Take them from the intake's outcomes; don't invent new ones.
4. **Split must-haves from nice-to-haves.** At most 5 must-haves, each something you'd reject a candidate for lacking. Move everything else to nice-to-haves, or delete it. Acas lists "recent graduate" and "highly experienced" as wording that can discriminate on age, and says you must be able to prove a good reason for any requirement in the advert. Our default: write the skill or experience itself, not a number of years. Our default: drop degree requirements unless the job needs one.
5. **Add the pay line.** State a real range and what it covers (base, commission, equity). Then check where the role can be filled:
   - New York State: the NY DOL page says the law applies to New York State businesses with 4 or more employees, who must list a compensation range, provide a job description, and say if the role is commission-based. New York City has its own law too. Whether a remote role outside New York is covered: [check: local law / HR].
   - California: the Labor Commissioner's FAQ says employers with 15 or more employees (at least 1 in California) must put the pay scale, a good-faith estimate of the salary or hourly range, in the posting itself, for any role that may be filled in California, in person or remotely. A link to the range doesn't count.
   - EU: Directive (EU) 2023/970 gives applicants a right to pay information before employment and bans asking about salary history; member states had to transpose it by 7 June 2026 (European Commission). How each country applies it: [check: local law / HR].
   - Anywhere else, or if unsure: add "[check: local law / HR]" next to the pay line. This list is a starting point, not the full set of rules.
6. **Run the inclusive-language check.** Remove anything that states or implies a preference for a protected group: the EEOC says an ad may not show a preference for or discourage applicants by protected traits, and gives "recent college graduates" as an example that may discourage people over 40. Replace gendered nouns ("salesman", "handyman") with neutral ones. Research by Gaucher, Friesen and Kay (2011) found women rated ads with more masculine wording ("competitive", "dominant") less appealing than the same ads with more feminine wording; balance them with plain descriptions of the work. Ask for no photo, date of birth, or marital status.
7. **Write how to apply.** One link, what to send (CV, or 3 short questions), the steps with rough timing, and a line saying how to ask for adjustments in the process. Our default: no cover letter unless you will read it.
8. **Cut to 300 to 600 words** (our default). Read it as the candidate: delete every line that doesn't help them decide to apply.

## Output format

```markdown
# [Honest title] — [location or "Remote, [countries/time zones]"]

[2–3 sentences: what the team does, why this role exists now, who you report to.]

## What you'll do in your first 6 months
- [By month 1–2: outcome]
- [By month 3: outcome]
- [By month 6: outcome]

## You must have
- [Must-have 1, written as a skill or experience]
- [Up to 5 in total]

## Nice to have
- [Nice-to-have, or remove this section]

## Pay and benefits
- [Range, currency, per year/hour; what it includes] [check: local law / HR]
- [Key benefits, one line each]

## How to apply
- [Link] — send [what]. [Steps and rough timing.]
- Need an adjustment to apply or interview? Tell us at [contact].

---
**Language check (remove before posting):** [words changed, and why]  
**Pay check (remove before posting):** [where the role can be filled, rule noted, or "[check: local law / HR]"]
```

## Example

**Input:** Intake from Marta (Head of Ops, Fernbrook, a 40-person invoicing software company in Brooklyn, NY). Company paragraph: Fernbrook makes invoicing software for small accounting firms and freelancers, with about 2,000 customers; two engineers and Marta answer about 350 tickets a week between other work, most about invoice templates, payment reminders and bank sync, and the engineers go back to product work once the lead owns the queue. Role: first Customer Support Lead, remote within the US, base salary, no commission. Outcomes: own the queue by month 2, run a weekly report on the top reasons customers write in for the product team by month 3, cut first-reply time from 20 hours to 6 by month 4, write the help center's top 30 articles by month 6. Must-haves: 3+ years in B2B SaaS support, Zendesk (the lead sets up our views and macros from scratch), clear writing, "young and hungry", degree. Nice to have: has written help-center articles; enough SQL to look up an account's data. Range $78,000–$92,000. Benefits: health, dental and vision insurance; 401(k) with a 4% match; 25 days of paid time off; $1,500 home-office budget; core hours 10 am–3 pm Eastern, no weekend shifts. Process: a 30-minute call with Marta, a 2-hour exercise answering sample tickets, paid $150, then meeting 3 teammates; about 3 weeks from application to offer. Apply at fernbrook.example/jobs with a CV, no cover letter; questions and adjustments to jobs@fernbrook.example.

**Output:**

```markdown
# Customer Support Lead — Remote (US)

Fernbrook, a 40-person company in Brooklyn, makes invoicing software for small accounting firms and freelancers, and about 2,000 customers use it. Today two engineers and Marta answer about 350 tickets a week between their other work, most of them about invoice templates, payment reminders and bank sync, so we're hiring our first support lead to own customer support. You report to Marta, Head of Ops.

## What you'll do in your first 6 months
- By month 2: own the support queue, so the engineers can go back to product work.
- By month 3: run a weekly report for the product team on the top reasons customers write in.
- By month 4: bring first-reply time from about 20 hours to 6.
- By month 6: write the help center's top 30 articles.

## You must have
- Hands-on support experience for a B2B software product.
- Daily use of a ticketing tool such as Zendesk; you'll set up our views and macros from scratch.
- Clear written English; you'll write most of our help center.

## Nice to have
- You've written help-center articles before.
- Enough SQL to look up an account's data on your own.

## Pay and benefits
- $78,000–$92,000 base per year, not commission-based. [check: local law / HR]
- Health, dental and vision insurance.
- 401(k) with a 4% match.
- 25 days of paid time off.
- $1,500 to set up your home office.
- Work from anywhere in the US. Core hours are 10 am–3 pm Eastern, with no weekend shifts.

## How to apply
- Apply at fernbrook.example/jobs — send your CV. No cover letter needed.
- What happens next: a 30-minute call with Marta, a 2-hour exercise answering sample tickets (we pay $150 for it), then meeting 3 teammates. About 3 weeks from application to offer.
- Questions about the role, or need an adjustment to apply or interview? Tell us at jobs@fernbrook.example.

---
**Language check (remove before posting):** removed "young and hungry" (implies an age preference); "3+ years" became the experience itself; removed the degree (not needed to do the job).  
**Pay check (remove before posting):** remote US, so it may be filled in California: range in the post itself. Fernbrook is a New York business with 4 or more employees: range, description and commission status included. Other states, and New York City's own rules: [check: local law / HR].
```

## Checks before you send

- [ ] The title is one a candidate would search for, at the right level.
- [ ] There are 5 must-haves or fewer, and each is a real reason to reject.
- [ ] The first-6-months bullets come from the intake, not from imagination.
- [ ] The pay line has a real range, or the post is held with "[pay range needed]"; any unchecked location says "[check: local law / HR]".
- [ ] No word states or implies a preference by age, sex, race, religion, disability, national origin, or family status.
- [ ] The apply section names the link, what to send, the steps, and how to ask for adjustments.

## Common mistakes

- A wish list of 12 requirements. Each extra must-have shrinks the pool; keep the ones you'd reject for.
- "Competitive salary" instead of a range. Where a range is required, it doesn't meet the rule; everywhere else it tells the candidate nothing.
- Describing the company for 3 paragraphs before the job. Candidates scan for the work and the pay.
