---
name: ad-copy-variants
description: Writes ad copy variants for Google Search, Meta (Facebook and Instagram), and LinkedIn within each platform's character limits, with each variant testing one angle, plus a test matrix showing what each variant isolates. Use when someone asks for ad copy, ad variants, headlines for Google Ads, a Facebook or LinkedIn ad, A/B test copy, or "more versions of this ad".
---

# Ad copy variants

Variants are only useful if each one tests a single idea, so a winner tells you something. Write one angle per variant, keep everything else the same, and stay inside the limits so nothing gets cut off.

## When to use

- Launching a new campaign and you need 3 to 6 variants per platform to test.
- An ad is fatiguing and you need fresh angles with a clear hypothesis each.
- Not for organic social posts or landing page copy: different lengths, different job.

## What you need

- Product, audience, and the single action the ad drives (sign up, book a demo, buy).
- The landing page or offer the ad points to. If missing, ask once; ads that promise what the page doesn't deliver waste spend.
- Platforms. If not given, default to Google Search and Meta.
- Proof you can use: numbers, customer names, awards. Never invent one; mark gaps "[check: proof]".
- Optional: current best-performing ad, so variants test against it.

## Steps

1. **Pick 3 to 5 angles (our default).** Choose from: pain (what goes wrong without it), outcome (the result in numbers), proof (customers, ratings), objection (price, effort, switching), speed (time to first result), identity (who it's for). One angle per variant; label it.
2. **Fix the constants.** Same offer, same CTA, same landing page across variants. If the user wants to test the offer too, make that a separate row in the matrix, never mixed with an angle change.
3. **Write to the limits.** Count characters, including spaces:
   - Google Search (responsive search ads): 3 to 15 headlines of up to 30 characters, 2 to 4 descriptions of up to 90, and 2 display-URL paths of up to 15. Japanese, Chinese, and Korean characters count as 2. Headlines and descriptions can show in any order, so each must make sense alone. Put a keyword in headlines. Our default: write at least 8 headlines and all 4 descriptions.
   - Meta (Feed image ads): Meta's Ads Guide recommends primary text of 50 to 150 characters and a headline of 27 or fewer. Longer text is cut off, so the opening line must work alone. The guide gives no description length; our default is 25.
   - LinkedIn (single image ads): intro text 150 characters and headline 70 characters to avoid truncation.
   Platforms change these numbers; if a count looks off, check the platform's current spec page.
4. **Put the specific word first.** Lead with a number, the audience's job title, or the pain in their words. Cut "Discover", "Introducing", "The best way to".
5. **Check policy traps.** Meta bars ads that assert or imply the viewer's personal attributes such as health, religion, or vulnerable financial status ("Are you bankrupt?"); describe the service instead. Google's editorial policy bars capitalization, punctuation, or repetition that isn't used for its normal purpose ("FREE!!!"). Flag any "#1", "best", or number that needs proof.
6. **Build the test matrix.** One row per variant: angle, what it isolates, hypothesis, metric to judge (CTR for headlines, conversion rate for offers). Our default minimum before calling a winner: 1,000 impressions and 30 clicks per variant, or say "[check: volume]" if the budget can't reach it.

## Output format

```markdown
# Ad variants — [product], [audience]
**Constant across variants:** [offer], [CTA], [landing page]

## Google Search
**Headlines (30 max)**
| # | Headline | Chars | Angle |
|---|---|---|---|
| 1 | [text] | [n] | [angle] |

**Descriptions (90 max)**
| # | Description | Chars |
|---|---|---|

## Meta
### Variant [A] — [angle]
- Primary text (50–150): [opening line complete on its own]
- Headline (27 max): [text] ([n])
- Description (25 max, our default): [text] ([n])

## LinkedIn
### Variant [A] — [angle]
- Intro (first 150 chars complete): [text]
- Headline (70 max): [text] ([n])

## Test matrix
| Variant | Platform | Angle | Isolates | Hypothesis | Judge by | Minimum before deciding |
|---|---|---|---|---|---|---|

## Claims to verify
- [claim] — [check: source]
```

## Example

**Input:** "Ads for Tallyho, an expense app for 10–50 person agencies. Free trial, sign up. Proof: receipts auto-matched in under 10 seconds; 4.7 on G2 [from the user]. Meta and Google."

**Output:**

```markdown
# Ad variants — Tallyho, agency finance leads
**Constant across variants:** free trial, "Start free trial", tallyho.example/agencies

## Google Search
**Headlines (30 max)**
| # | Headline | Chars | Angle |
|---|---|---|---|
| 1 | Expense App for Agencies | 24 | keyword |
| 2 | Receipts Matched in 10 Seconds | 30 | speed |
| 3 | Rated 4.7 on G2 | 15 | proof |
| 4 | Stop Chasing Receipts | 21 | pain |
| 5 | Agency Expense Tracking | 23 | keyword |
| 6 | Close the Month Without Gaps | 28 | outcome |
| 7 | Built for 10–50 Person Teams | 28 | identity |
| 8 | Agency Expenses, Sorted | 23 | keyword |

**Descriptions (90 max)**
| # | Description | Chars |
|---|---|---|
| 1 | Snap a receipt and Tallyho matches it to the card charge in under 10 seconds. | 77 |
| 2 | Made for agencies of 10 to 50 people. Start a free trial, no card needed. [check: no card] | 73 |

## Meta
### Variant A — pain
- Primary text: Still chasing designers for last month's receipts? Tallyho matches each receipt to its card charge in under 10 seconds.
- Headline (27 max): Stop chasing receipts (21)
- Description (25 max): Free trial for agencies (23)

### Variant B — proof
- Primary text: Tallyho is rated 4.7 on G2. Receipts match to card charges in under 10 seconds.
- Headline (27 max): Tallyho: rated 4.7 on G2 (24)
- Description (25 max): Free trial for agencies (23)

## Test matrix
| Variant | Platform | Angle | Isolates | Hypothesis | Judge by | Minimum before deciding |
|---|---|---|---|---|---|---|
| A | Meta | pain | opening line | Naming the chase beats naming the product | CTR | 1,000 impressions, 30 clicks |
| B | Meta | proof | opening line | A rating lifts clicks among cautious buyers | CTR | 1,000 impressions, 30 clicks |

## Claims to verify
- "no card needed" — [check: trial terms]
- "Rated 4.7 on G2" — [check: current rating and the date it was taken]
```

## Checks before you send

- [ ] Every line is within its platform's character limit, with the count shown.
- [ ] Each variant changes one angle; offer, CTA, and page stay constant.
- [ ] Meta and LinkedIn opening lines make sense if the text is cut off at the fold.
- [ ] No number, rating, or customer name that isn't in the input or marked "[check: ...]".
- [ ] The test matrix states a hypothesis and a metric for every variant.

## Common mistakes

- Changing the headline, image, and offer at once, then not knowing why B won.
- Google headlines that only work in sequence ("Save time." / "And money."). Google shuffles them.
- Calling a winner after 200 impressions.
