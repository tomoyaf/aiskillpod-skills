---
name: seo-brief
description: Writes a content brief for one search query - search intent, the answer to put in the first paragraph, H2 outline based on what currently ranks, questions to answer, entities to cover, internal links, and a word range - and marks any data it can't verify. Use when someone asks for an SEO brief, content brief, article outline, "what should we write for this keyword", or a brief to hand a writer or freelancer.
---

# SEO content brief

A brief wins when the writer can produce a page that answers the query better than what ranks, without doing the research again. One query per brief, one intent per page (our default). The answer goes first, and the page must add something the ranking pages don't: Google's helpful content guidance asks whether a page offers "original information, reporting, research, or analysis" and flags pages that mainly summarize others.

## When to use

- Before a writer, freelancer, or AI drafts an article meant to rank for a query.
- When refreshing a page that ranks on page 2 for its main query.
- When a team has a keyword list and needs to know what each page should say.
- Not for keyword research across a whole site, or for technical SEO fixes: this is one page, one query.

## What you need

- The target query, in the searcher's words. If given several, pick the one with the clearest intent and list the others as secondary.
- What the company sells and who the reader is, so the page can point to the product honestly.
- What ranks now: the top 5 to 10 results' titles and headings, from a search you can run or the user pastes. If you can't see search results, say so, build the outline from intent, and mark it "[not checked against live results]".
- Optional: search volume and difficulty from a tool, and the site's existing pages for internal links.

## Steps

1. **Name the intent.** Informational (learn), commercial (compare), transactional (buy or sign up), or navigational (a brand). Check it against what ranks: if the top results are lists of tools, a how-to guide won't rank. If intent is mixed, pick the dominant one and say what share of results follow it.
2. **Write the answer first.** 2 to 3 sentences that answer the query directly, to open the page. A searcher who reads only this should have their answer. If the query has a number (cost, time, steps), the answer states it, with a source or a "[verify]" mark.
3. **Build the H2 outline from what ranks, then beat it.** List the subtopics that appear in 3 or more of the top results: those are expected (our default threshold). Add 1 to 2 subtopics none of them covers well, ideally first-hand: your own data, a worked example, a template. Google's guidance asks for "first-hand expertise". 5 to 8 H2s, each written as the question or claim it answers.
4. **Collect the questions.** 5 to 8 questions searchers ask around this query (from "People also ask", forums, sales calls, support tickets). Each maps to an H2 or a short FAQ entry.
5. **List entities and terms.** The people, tools, standards, and concepts a complete answer names. A page about "SOC 2 audit cost" that never says "auditor", "Type I", "Type II" looks thin.
6. **Write the title and meta description.** Google sets no length limit on either; it cuts them to fit the device width, and it often writes the snippet from page text instead of the meta description. So front-load the query words. Our default for English: title under 60 characters, meta under 155, so they rarely get cut. Chinese, Japanese and Korean characters are wider, and the cut follows display width, not character count: for CJK text, results typically show roughly 30–35 characters of a title and 60–120 of a description (approximate figures from Japanese SEO publishers: Devo's SEO Lab gives about 30–35 title characters on desktop, GMO TECH about 120 description characters on desktop and about 60 on phones). So keep CJK titles to about 30–35 characters and descriptions to about 120, with the key words in the first 60. The title describes this page only, a few descriptive words, no repeated keywords (Google's title link guidance).
7. **Pick internal links.** 3 to 5 links out to related pages on the site, with anchor text, and 1 to 2 pages that should link in to this one. Only list pages that exist; mark guesses "[confirm URL]".
8. **Set length and proof.** Google says it has no preferred word count. Give a word range only as a planning guide (our default: what it takes to cover the outline, checked against the length of the top results) and tell the writer never to pad to hit it. List the data, examples, or screenshots the page needs. Anything you couldn't verify gets "[verify: what and where]"; tell the writer never to publish a number with that mark still on it.

## Output format

```markdown
# Brief: [query]

**Intent:** [type] — [what the searcher wants to walk away with]
**Reader:** [who] · **Page type:** [guide / comparison / list / template]
**Secondary queries:** [list]
**Word range:** [n–n] · **Checked against live results:** [yes, date / no]

## Answer first (open the page with this)
[2–3 sentences]

## Title and meta
- Title (our default for English: under 60 chars; CJK: about 30–35): [title]
- Meta description (our default for English: under 155 chars; CJK: about 120, key words in the first 60): [text]

## Outline
1. H2: [heading] — [what it must say, proof needed]

## Questions to answer
- [question] → [H2 number or FAQ]

## Entities to cover
[comma-separated list]

## Internal links
- Out: [anchor] → [URL]
- In: [page] should link here with "[anchor]"

## Proof and data
- [item] — [source, or "[verify: ...]"]

## Notes for the writer
- Don't publish any line still marked [verify].
- [where the product fits, in one honest line]
```

## Example

**Input:** Query "how to write a job description". Company: Hirewell, a hiring tool for startups. User pasted top 5 titles: 4 are guides with templates, 1 is a list of examples.

**Output:**

```markdown
# Brief: how to write a job description

**Intent:** Informational — a writer wants a structure and an example they can copy today.
**Reader:** Startup founders and first managers hiring without a recruiter · **Page type:** guide with template
**Secondary queries:** job description template, job description example
**Word range:** 1,600–2,400 (planning guide, not a target) [verify: length of top 5] · **Checked against live results:** titles only, pasted by user

## Answer first (open the page with this)
A job description has 6 parts: title, a 2-line summary of the role, what the person will do in the first 6 months, must-have skills, pay range, and how to apply. Write the outcomes before the requirements; candidates decide on what they'll do, not the list of skills.

## Title and meta
- Title (our default for English: under 60 chars): How to write a job description (with a free template)
- Meta description (our default for English: under 155 chars): The 6 parts every job description needs, a copy-ready template, and 3 examples from startup roles.

## Outline
1. H2: The 6 parts of a job description — one paragraph each
2. H2: Write outcomes, not duties — before/after example
3. H2: Should you include salary? — pay transparency laws [verify: which regions require it]
4. H2: Job description template — copyable block
5. H2: 3 examples: engineer, sales rep, ops lead — the gap none of the top 5 fills with startup roles
6. H2: Mistakes that shrink your applicant pool — gendered words, 15-item requirement lists

## Questions to answer
- How long should a job description be? → FAQ
- What's the difference between a job description and a job post? → FAQ
- Do I need to list a salary range? → H2 3

## Entities to cover
job title, role summary, responsibilities, requirements, salary range, pay transparency, applicant tracking system, inclusive language

## Internal links
- Out: "job post template" → /templates/job-post [confirm URL]
- In: /blog/first-hire should link here with "write the job description"

## Proof and data
- Effect of listing salary on applications — [verify: find a primary study]

## Notes for the writer
- Don't publish any line still marked [verify].
- Mention Hirewell once, in the template section, as where the template can be used.
```

## Checks before you send

- [ ] One query, one intent, stated in the first lines.
- [ ] The answer-first block answers the query in 3 sentences or fewer.
- [ ] Each H2 is phrased as the question or claim it answers.
- [ ] Every number or claim the AI couldn't verify carries a "[verify: ...]" mark.
- [ ] Internal links point only to known pages or carry "[confirm URL]".
- [ ] The brief says whether it was checked against live results.

## Common mistakes

- Copying the top result's outline. Match the expected subtopics, then add what none of them has.
- Stuffing 20 keywords. List entities a complete answer names; the writer uses them where they fit.
- Burying the answer under an intro about why the topic matters.
