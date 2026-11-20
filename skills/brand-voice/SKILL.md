---
name: brand-voice
description: Extracts a brand voice guide from 3 to 5 sample texts (traits with do and don't pairs, a word list, sentence habits) and rewrites a draft in that voice. Use when someone asks for a brand voice, tone of voice guide, style guide, "make this sound like us", "rewrite in our voice", or wants copy from several writers to sound like one company.
---

# Brand voice guide and rewrite

A voice guide is useful only if two different writers who follow it produce copy a reader can't tell apart. So every trait comes with a do and a don't taken from real sentences, and the guide is proven by rewriting one draft in it. Voice is the personality that stays the same; tone is how it shifts with the reader's situation (Mailchimp's style guide: "the same voice all the time, but your tone changes").

## When to use

- A team has a few pieces of copy it likes and wants new copy to match them.
- Writers, freelancers, or AI drafts sound like different companies.
- Someone shares a draft and asks to "make it sound like us".
- Not for inventing a brand from nothing with no samples: ask for 3 texts the team likes, even from other companies.

## What you need

- 3 to 5 sample texts the team says sound right: web pages, emails, posts, support replies. Fewer than 3: ask once for more; if none come, proceed and mark the guide "[assumption: based on 2 samples]".
- Optional: 1 text that sounds wrong to them. A negative sample sharpens every "don't".
- Optional: a draft to rewrite. If none, write the guide only.
- Who the reader is (buyer role, how technical). If missing, infer it from the samples and say so.

## Steps

1. **Read for patterns, not adjectives.** Measure what the samples actually do: average sentence length, how often they use "you" vs "we", contractions, questions, numbers, jargon, exclamation marks, how sentences open. Write the numbers down; "short sentences" means nothing until you say "12 words on average".
2. **Place the samples on the 4 tone dimensions.** Nielsen Norman Group's dimensions: formal vs casual, serious vs funny, respectful vs irreverent, matter-of-fact vs enthusiastic. Say where the samples sit on each; NN/g warns against the extreme end of every dimension.
3. **Name 3 to 4 traits.** Each trait is a "this, not that" pair, the form Mailchimp's guide uses ("smart but not snobbish"): "Direct, not blunt", "Expert, not academic". Our default is 4 at most, because nobody remembers more. If two traits produce the same edits, merge them.
4. **Prove each trait with a do and a don't.** The "do" is a sentence quoted from the samples. The "don't" is the same idea written the wrong way. If you can't quote a sample for a trait, drop the trait.
5. **Build the word list.** Words they use (product terms, verbs they repeat), words they avoid (jargon, hype, words the samples never use where competitors do). 8 to 15 entries per side. Include how they name the product and the customer.
6. **Write the mechanics and the tone shifts.** Headline case, numerals vs words, Oxford comma, emoji, exclamation marks, contractions, greeting and sign-off. Only list what the samples settle; mark the rest "not decided". Add 1 line on how tone shifts for bad news (an outage, a price rise): same traits, less humor, more plain.
7. **Rewrite the draft.** Keep every fact and claim; change only wording, order, and length. Then list the 3 to 5 biggest changes with the trait each one serves, so the writer learns the guide instead of just getting new copy.
8. **Flag what voice can't fix.** If the draft lacks proof, a clear offer, or a reader, say so in one line. Don't hide a weak message under a good tone.

## Output format

```markdown
# [Brand] voice guide

**Reader:** [who we write for, in one line]
**Based on:** [list of samples]

## Traits
| We are | Not | Do (from samples) | Don't |
|---|---|---|---|
| [trait] | [overdone version] | "[quoted sentence]" | "[same idea, wrong]" |

## Sentence habits
- Average sentence: [n] words. Longest allowed: [n].
- [you/we ratio, contractions, questions, numbers]

## Words
| Use | Avoid |
|---|---|
| [word] | [word] — [why] |

## Tone dimensions
Formal–casual: [where] · Serious–funny: [where] · Respectful–irreverent: [where] · Matter-of-fact–enthusiastic: [where]

## Mechanics
- [headline case, numerals, punctuation, emoji, sign-off; "not decided" where samples don't settle it]
- Bad news: [how tone shifts]

## Rewrite
**Before:** [draft]
**After:** [rewrite]

**What changed**
1. [change] — [trait]

**Voice can't fix:** [missing proof/offer, or "nothing"]
```

## Example

**Input:** 3 samples from Fernway, a payroll app for restaurants: the home page, an onboarding email, and 1 support reply. Lines from them: "Payday shouldn't eat your Sunday." "Run payroll in 4 minutes from your phone." "Tips split by hours worked, automatically." Counted across the full samples: sentences average 9 words, the longest has 18, and "you" appears 3 times as often as "we". All 3 use contractions, sentence-case headlines, and numerals for numbers, with no emoji and no questions in headlines. Draft to rewrite: "Fernway is a comprehensive, innovative payroll solution that empowers restaurant owners to streamline their operations."

**Output:**

```markdown
# Fernway voice guide

**Reader:** Restaurant owners and managers, not finance people [assumption: inferred from the samples; confirm with the team].
**Based on:** home page, onboarding email, 1 support reply

## Traits
| We are | Not | Do (from samples) | Don't |
|---|---|---|---|
| Plain | Dumbed down | "Run payroll in 4 minutes from your phone." | "Process compensation disbursements efficiently." |
| On their side | Chummy | "Payday shouldn't eat your Sunday." | "Hey friend! We've got your back!!" |
| Specific | Number-stuffed | "Tips split by hours worked, automatically." | "Advanced tip allocation capabilities." |

## Sentence habits
- Across the full samples, not just the lines quoted above: average sentence 9 words; longest allowed 18.
- "You" appears 3 times as often as "we". Contractions always. No questions in headlines.

## Words
| Use | Avoid |
|---|---|
| payday, run payroll | solution, operations — say nothing |
| tips, split | empower, streamline — hype verbs |
| hours worked, automatically | comprehensive, innovative — claims with no proof |
| from your phone, you (never "restaurant owners") | compensation, capabilities — finance and software jargon |

## Tone dimensions
Fairly casual · Mostly serious, light humor in headlines · Respectful · Matter-of-fact

## Mechanics
- Sentence case headlines. Numerals for all numbers. No emoji. Oxford comma: not decided.
- Bad news: drop the humor, keep the short sentences.

## Rewrite
**Before:** Fernway is a comprehensive, innovative payroll solution that empowers restaurant owners to streamline their operations.
**After:** Fernway runs payroll for your restaurant, start to finish.

**What changed**
1. "Payroll solution" became what it does: "runs payroll" — Plain
2. "Restaurant owners" became "your restaurant" — On their side
3. "Comprehensive" became "start to finish"; "innovative" and "streamline their operations" were cut, as they claim nothing a reader can check — Specific

**Voice can't fix:** proof. The draft gives no number. The samples' "Run payroll in 4 minutes from your phone." would fit if it holds for this page [check: the 4-minute claim applies here].
```

## Checks before you send

- [ ] Every "do" is a sentence quoted from a sample, not written by you.
- [ ] 3 or 4 traits, each a "this, not that" pair.
- [ ] Sentence habits include at least 2 measured numbers, and all 4 tone dimensions are placed.
- [ ] The rewrite keeps every fact in the draft and adds none.
- [ ] Each listed change names the trait it serves.

## Common mistakes

- Traits like "friendly, professional, innovative". Every company claims them; they change no sentence.
- Rewriting into your own house style instead of the samples'. Recheck sentence length against the measured average.
- Adding claims during the rewrite to make it punchier. Voice changes wording, never facts.
