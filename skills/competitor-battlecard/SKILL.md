---
name: competitor-battlecard
description: Builds a one-page sales battlecard against one competitor from public information and your win-loss notes - when we win, when we lose, the competitor's strengths, landmine questions to plant, claims not to make, and an honest side-by-side comparison - with every unverified claim marked. Use when a rep or marketer asks for a battlecard, competitive card, "how do we beat X", competitor comparison for sales, or talk tracks against a named rival.
---

# Competitor battlecard

A battlecard is what a rep glances at 5 minutes before a call. It has to be brief (our default: one page), name where the rival is stronger, and give the rep questions to ask rather than claims to make. One piece of bad intel is enough to lose sellers' trust in the card.

## When to use

- A named competitor shows up in 2 or more open deals.
- Before a sales kickoff or onboarding a new rep.
- When an existing card is older than 6 months (our default) or the rival changed pricing or launched something.
- Not for market-wide positioning: use positioning-statement. Not for a public comparison page: claims there need marketing-claims-check.

## What you need

- The competitor's name and URL.
- Public info: their site, pricing page, docs, changelog, review sites, job posts. If you can't browse, ask the user to paste it.
- Your win-loss notes against them. If none, say the "when we win/lose" sections are hypotheses and mark them "[unverified]".
- Your own product's strengths and gaps, honestly. If not given, ask once.

## Steps

1. **Mark every claim's source.** Each fact about the rival gets a tag: [site], [pricing page], [review], [win-loss], or [unverified]. Anything a rep heard secondhand is [unverified]. Add the date the info was checked.
2. **Write "when we win" from deals, not features.** 3 bullets max, each a buyer situation: "Teams under 50 people who need to be live this week". Use win-loss notes first; feature claims only if there are no notes.
3. **Write "when we lose" just as plainly.** 3 bullets max. If the rival is truly better for a segment, say so and tell the rep to qualify out early.
4. **Name their strengths.** Their top 3 advantages, each with how the rep should respond. Skipping this leaves the rep unprepared when the buyer raises it.
5. **Write 2 to 3 landmine questions.** Crayon defines landmines as 2 to 3 high-impact questions that highlight a competitor's gaps; the rep plants one early so the buyer discovers a gap that matters to them: "How will you handle approvals when a manager is out?" A question, not an attack, and (our default) it never names the rival. Each ties to a real, sourced gap.
6. **List what not to say.** Claims that are false, outdated, or easy for the rival to rebut. "Don't say they have no mobile app; they launched one in March [changelog]."
7. **Build the honest comparison.** Every "Better" row must be provable; unprovable lines go to the unverified list. 5 to 8 rows the buyer cares about. Use "Better", "Same", "Worse" from your side, with one-line proof. At least one row should say "Worse" if that's true; a card with none loses trust.
8. **Add the 3 objections they'll raise and keep it short.** Each objection about you gets a response in acknowledge-clarify-respond form (our default), under 40 words. Cut anything a rep can't use on a call; if it runs past one page, drop the comparison to 5 rows first.

## Output format

```markdown
# Battlecard: [us] vs [competitor]
Checked: [date] · Sources: [list]

**In one line:** [Who they are and who they're best for.]

## When we win
- [buyer situation] [source]

## When we lose
- [buyer situation] [source] — [qualify out, or how to compete]

## Their strengths and how to respond
- [strength] [source] — [response]

## Landmine questions to plant
- "[question]" — exposes [gap] [source]

## Don't say
- [claim to avoid] — [why] [source]

## Honest comparison
| What the buyer cares about | Us vs them | Proof |
|---|---|---|
| [criterion] | [Better / Same / Worse] | [one line] [source] |

## What they'll say about us
- **"[objection]"** — [response, under 40 words]

## Unverified claims to check
- [claim] — [how to verify]
```

## Example

**Input:** Us: Tallyo (expense approvals for small teams), no user minimum. Rival: Ledgerline. Their site: "Enterprise-grade policy engine", pricing starts at 12 per user, minimum 25 users. Their changelog: mobile app launched March (we have one too). Our win-loss: won 3 of 4 deals under 30 people ("live same day"); lost 2 deals over 150 people on multi-entity support. A rep heard Ledgerline is slow to support.

**Output:**

```markdown
# Battlecard: Tallyo vs Ledgerline
Checked: 4 November · Sources: Ledgerline site, pricing page, changelog; our win-loss notes

**In one line:** Ledgerline is a policy-heavy expense tool built for multi-entity finance teams.

## When we win
- Teams under 30 people who want approvals running the same day [win-loss, 3 of 4]
- Buyers put off by a 25-user minimum [pricing page]

## When we lose
- Companies over 150 people with several legal entities [win-loss, 2 deals] — qualify out unless they'll run one entity first

## Their strengths and how to respond
- Complex policy rules [site] — agree; ask whether they need them in year one.
- Multi-entity support [win-loss] — qualify early; don't compete on it.

## Landmine questions to plant
- "How many people will use it in year one?" — exposes the 25-user minimum [pricing page]
- "Who will set up the approval rules, and how long can that take?" — tests setup effort vs our same-day start [win-loss]

## Don't say
- "They don't have a mobile app." They launched one in March [changelog].
- "Their support is slow." Heard secondhand only [unverified].

## Honest comparison
| What the buyer cares about | Us vs them | Proof |
|---|---|---|
| Time to first approval | Better | Live same day in 3 won deals [win-loss] |
| Small-team pricing | Better | No user minimum; theirs is 25 [pricing page] |
| Mobile app | Same | Both have one [changelog] |
| Multiple legal entities | Worse | Lost 2 deals on it [win-loss] |
| Complex policy rules | Worse | Their main pitch [site] |

## What they'll say about us
- **"Tallyo won't scale with you."** — Fair to ask. How many entities will you run in 2 years? If it's one, we're built for that; if several, let's talk about it now.

## Unverified claims to check
- Ledgerline support response time — ask 2 of their former customers or check recent reviews.
```

## Checks before you send

- [ ] Every fact about the competitor has a source tag and the card has a checked date.
- [ ] Secondhand or unsourced claims are under "Unverified", never in the comparison.
- [ ] The comparison has at least one honest "Worse" row, or says why there is none.
- [ ] There are 2 to 3 landmine questions, each a question tied to a sourced gap.
- [ ] Their strengths section names at least one real advantage with a response.

## Common mistakes

- Copying the rival's feature list. Reps need buyer situations and questions, not a spec sheet.
- Telling reps to attack the competitor. Buyers trust the rep who is fair about a rival.
- Letting the card age. A landmine about a feature they shipped last month costs the deal.
