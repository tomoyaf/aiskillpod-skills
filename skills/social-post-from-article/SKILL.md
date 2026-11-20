---
name: social-post-from-article
description: Turns one article or blog post into a LinkedIn post, an X thread, and a short post, each opening with a hook built from the article's most specific point (a number, a result, a surprising claim), with no hashtag spam. Use when someone shares an article, blog post, or report and asks to repurpose it, "turn this into posts", write a LinkedIn post, a thread, or social copy to promote it.
---

# Social posts from an article

A repurposed post works when someone who never clicks still learns the article's best point. So the hook is the most specific thing in the article, the post delivers it in full, and the link is a bonus, not the payoff.

## When to use

- A blog post, guide, report, or case study just went live and needs promotion.
- An old article still performs on search and deserves another round on social.
- A founder or employee wants to post about the company's article in their own name.
- Not for announcing a launch or news with no article behind it: write launch copy instead.

## What you need

- The article text or URL. Without the full text, ask for it; a title alone produces generic posts.
- Who posts it: the company account or a named person. A person's post speaks in "I"; a company's in "we".
- Optional: the audience, and any line the author wants kept. If missing, take the audience from the article.

## Steps

1. **Find the 3 most specific points.** Rank every claim in the article by specificity: a number with a unit, a named result, a counterintuitive finding, a mistake with its cost. "Onboarding matters" is not a point; "Customers who finish setup on day 1 churn half as often" is.
2. **Write the hook from the top point.** First line under 12 words, states the point or the tension in it. No "Here's why...", no questions you then answer, no "I'm excited to share". If the article has no specific point, say so and use the clearest how-to step instead.
3. **LinkedIn post: 120 to 220 words (our default; LinkedIn allows up to 3,000 characters).** Hook, a blank line, then the point delivered in full with 1 example from the article, then 2 to 4 short lines of supporting points, then the link with one line of what else is in the article. Line breaks every 1 to 2 sentences. Link in the post unless the user says first comment.
4. **X thread: 4 to 7 posts.** Post 1 is the hook and stands alone. Each next post carries one point and makes sense if read alone. Last post: the link and one line on what the article adds. X's limit is 280 characters a post for standard accounts; any link counts as 23 characters, and emoji count as 2 (X developer docs). Our default: stay under 270 to leave room for edits; number posts only if the thread has 5 or more.
5. **Short post: under 200 characters.** One point, one link. Usable on X, Threads, Bluesky, or as a Slack share.
6. **Tags and mentions.** Our default: 0 to 2 hashtags, only ones people actually follow for the topic; none on X. Mention a person or company only if the article names them and they'd want it.
7. **Check every claim against the article.** Each number and quote must appear in the article word for word. Don't round, don't upgrade "may" to "will".

## Output format

```markdown
# Posts for: [article title]

**Top point used as hook:** [the point]
**Poster:** [company / name]

## LinkedIn
[post]

## X thread
1/ [post]
2/ [post]

## Short post
[post]

## Other hooks to test
- [hook from point 2]
- [hook from point 3]
```

## Example

**Input:** Article "What we learned from 400 support tickets" by Mira Okafor, head of support at Brightlane (invoicing app). Mira read all 400 tickets one by one. Key finding: 38% of tickets came from one settings page, invoice settings. The feature wasn't the problem, the words were: "Apply" saved for one invoice, "Save" saved for all of them, and most people guessed wrong. Renaming the 2 buttons to "Save for this invoice" and "Save for all invoices" cut tickets from that page by 60% the next month; nothing else on the page changed. The article also says most "bugs" were wording and the angriest tickets came after a silent failure, not an error message, and it ends with the tagging sheet the team used. Poster: Mira.

**Output:**

```markdown
# Posts for: What we learned from 400 support tickets

**Top point used as hook:** Renaming 2 buttons cut tickets from one page by 60% the next month.
**Poster:** Mira Okafor

## LinkedIn
We renamed 2 buttons and tickets from one page fell 60%.

I read all 400 of our support tickets, one by one.

38% came from a single page: invoice settings.

People weren't confused by the feature. They were confused by the words. "Apply" saved for one invoice. "Save" saved for all of them. Most people guessed wrong.

We changed the buttons to "Save for this invoice" and "Save for all invoices". Tickets from that page dropped 60% the next month. Nothing else on the page changed.

What else the 400 tickets showed:
- Most "bugs" were wording.
- The angriest tickets came after a silent failure, not an error message.

The full breakdown is in the article. It ends with the tagging sheet our team used: [link]

## X thread
1/ We renamed 2 buttons and tickets from one page fell 60%.

2/ I read 400 support tickets. 38% came from one page: invoice settings.

3/ "Apply" saved for one invoice. "Save" saved for all. Most people guessed wrong.

4/ New labels: "Save for this invoice" and "Save for all invoices". Tickets from that page fell 60% the next month.

5/ The rest of what 400 tickets showed, plus the tagging sheet: [link]

## Short post
38% of our support tickets came from one page. 2 renamed buttons cut them by 60%. [link]

## Other hooks to test
- I read 400 support tickets. Most "bugs" were wording.
- Our angriest tickets came after silent failures, not error messages.
```

## Checks before you send

- [ ] The hook is the article's most specific point, under 12 words.
- [ ] Every number and quote appears in the article exactly.
- [ ] Each X post makes sense read alone and is under 270 characters, counting each link as 23.
- [ ] The LinkedIn post is 120 to 220 words and teaches the point without the click.
- [ ] 2 hashtags or fewer in total; none on X.

## Common mistakes

- Summarizing the article ("In our new post, we explore..."). Deliver the point instead.
- Making all 3 formats the same text cut to length. Each format gets its own shape.
- Holding back the answer to force a click. Readers notice and stop reading your posts.
