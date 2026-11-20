---
name: landing-copy-review
description: Reviews landing page copy section by section with concrete tests (standalone headline, so-what ladder, opposite test on adjectives, proof next to each claim, verb-first CTA, one job per section) and returns prioritized line edits. Use when someone shares a landing page, home page, or sales page draft or URL and asks for a copy review, feedback, "why isn't this converting", or headline and CTA edits.
---

# Landing page copy review

A good review gives the writer line edits they can paste today, ranked by how much each one costs in sign-ups. Opinions about tone come last. Every finding names the test it failed, so the writer can run the same test next time. The tests are our defaults; the reason behind them is measured: in Nielsen Norman Group's study, 79% of users scanned new pages and concise, scannable, objective copy scored 124% better on usability than promotional copy.

## When to use

- Before a landing page, home page, pricing page, or sales page goes live.
- When a page gets traffic but few sign-ups and the team suspects the words.
- When choosing between 2 headline or hero drafts.
- Not for design, speed, or SEO audits: say so in one line if you see an obvious problem there, and stay on copy.

## What you need

- The copy, in order, section by section (pasted text, a doc, or a URL you can read). If you can only see part of the page, review that part and say which sections are missing.
- Who the page is for and the one action it wants. If missing, infer both from the headline and CTA, and mark them "[assumption]".
- Optional: where visitors come from (ad, search, email). An ad visitor needs the ad's promise repeated in the headline.

## Steps

1. **Run the standalone headline test.** Most visitors scan, so the top of the page has to carry the main point on its own (NN/g's inverted pyramid: most important information first). Read only the headline and subhead. Can a stranger say what it is, who it's for, and why it beats what they do now? If they can't say what it is, that is the top finding, above everything else.
2. **Climb the so-what ladder on every benefit.** Ask "so what?" until the answer is something the reader feels (time, money, risk, status). Stop at the first rung a reader would care about; if the copy stops one rung lower ("AI-powered"), write the higher rung as the edit.
3. **Apply the opposite test to adjectives (our default).** If no competitor would claim the opposite ("fast", "easy", "powerful", "secure"), the word carries no information. Replace it with a number, a comparison, or a named example. If there is nothing concrete to say, cut the word.
4. **Check proof sits next to each claim.** A claim needs a number, a customer name, a quote, a screenshot, or a demo within the same section. Proof three sections later doesn't count. Flag claims with no proof anywhere as "add proof or soften".
5. **Check every CTA.** Starts with a verb, says what happens next ("Start free trial", "Get the checklist"), not "Submit" or "Learn more". NN/g found a bare "Learn more" leaves users unsure where it goes and loses meaning for screen-reader users. Our default: one primary CTA wording repeated across the page; a second, lower-commitment CTA is allowed once.
6. **One job per section (our default).** Name each section's job in 3 words (explain, prove, handle objection, ask). Two jobs in one section, or two sections with the same job: merge or cut. Check the biggest objection for this buyer (price, switching cost, trust) is answered somewhere above the last CTA.
7. **Rank and write the edits.** Must-fix: blocks understanding or the action (headline, CTA, missing proof on the main claim). Should-fix: weakens persuasion. Polish: wording. Max 10 edits; each one quotes the current line and gives the replacement. Never invent proof: write "[add: customer number]" where proof is needed.

## Output format

```markdown
# Copy review: [page name]

**Reader:** [who] · **Action:** [the one action] · **Traffic:** [source, if known]
**Verdict:** [1 sentence: ship, ship after must-fixes, or rewrite the hero]

## Must-fix
1. **[Section] — [test failed]**
   Now: "[current line]"
   Edit: "[replacement]"
   Why: [one line]

## Should-fix
[same shape]

## Polish
[same shape]

## Section jobs
| Section | Job | Keep / merge / cut |
|---|---|---|

## Not reviewed
- [sections not seen, design or SEO notes in one line each]
```

## Example

**Input:** Hero for Tallyroom, shift scheduling for clinics. Headline: "The smarter way to manage your team." Subhead: "Powerful, easy scheduling software." CTA: "Learn more". Section 3 has a quote from a clinic manager saying swaps take 2 minutes instead of a day. Sections 2 and 4 and the pricing block were not shared.

**Output:**

```markdown
# Copy review: Tallyroom home page hero

**Reader:** Clinic office managers [assumption] · **Action:** start a trial [assumption] · **Traffic:** not given
**Verdict:** Rewrite the hero; the rest can ship after the CTA fix.

## Must-fix
1. **Hero headline — standalone test**
   Now: "The smarter way to manage your team."
   Edit: "Shift scheduling for clinics, with shift swaps sorted in minutes."
   Why: The current line could be any HR, chat, or project tool.
2. **Hero CTA — verb-first, says what happens**
   Now: "Learn more"
   Edit: "Start free trial"
   Why: "Learn more" asks for a click without saying what it gets.

## Should-fix
1. **Hero subhead — opposite test, proof next to claim**
   Now: "Powerful, easy scheduling software."
   Edit: "Shift swaps take 2 minutes instead of a day, says [manager name, clinic]."
   Why: No one sells weak, hard software; the section 3 quote is the proof, move it up, and check its wording with the customer before launch.

## Polish
None in the hero.

## Section jobs
| Section | Job | Keep / merge / cut |
|---|---|---|
| Hero | Explain | Keep, rewrite |
| 3 Quote | Prove | Keep, reuse in hero |

## Not reviewed
- Sections 2, 4 and the pricing block were not shared.
```

## Checks before you send

- [ ] The headline test result is the first finding if the headline fails it.
- [ ] Every edit quotes the current line and gives a pasteable replacement.
- [ ] Every finding names the test it failed.
- [ ] No proof, number, or customer name was invented; gaps are "[add: ...]".
- [ ] 10 edits or fewer, sorted must-fix, should-fix, polish.

## Common mistakes

- Rewriting the whole page in your voice. The writer asked for edits; give the 10 that matter.
- Praising sections before the findings. Put the verdict first, then the edits.
- Calling a headline "unclear" without a replacement. Every finding ships with its fix.
