---
name: product-teardown
description: Writes a competitor product teardown from public pages, a free trial, screenshots described in text, or the user's trial notes, covering onboarding steps, pricing and packaging, the core loop, strengths, gaps, and what to copy and what not to, with every claim marked verified or unverified. Use when someone asks for a competitor teardown, competitive analysis of a product, "how does X onboard users", "how does X price", or what to learn from a rival's product.
---

# Product teardown

A teardown is useful when it tells your team what to do differently on Monday. Describe what the product actually does, step by step, from evidence; separate what you saw from what you guess; and end with a short list of what to copy, what to avoid, and where to stand out. The goal is to beat the competitor, not to clone it.

## When to use

- Before designing onboarding, pricing, or a feature a competitor already has.
- When sales or leadership asks "how do they do it?" about a rival.
- After someone completes a trial of a competitor and has notes.
- Not for a sales battlecard with objection handling: use competitor-battlecard. Not for choosing a vendor to buy: use vendor-comparison.

## What you need

- The competitor's name and the evidence: public page text, pricing page text, help docs, trial notes, or described screenshots, each with the date seen.
- What your team wants to learn (onboarding, pricing, a feature). If missing, ask once; otherwise cover all sections.
- Optional: your own product's equivalent, to compare.

## Steps

1. **Tag every claim's source.** Each fact gets "verified" (seen in the trial notes or quoted page text, with date) or "unverified" (from memory, a review site, or inference). Pricing and plan limits change often; never state a price you didn't see in the input, write "[check: current price]".
2. **Map onboarding step by step.** From the first page to the first moment of value: each screen, what it asks, how many fields, whether a credit card is required, and the time taken if noted. Count the steps. Mark where a new user could get stuck.
3. **Lay out pricing and packaging.** Plans, what limits separate them (seats, usage, features), the free plan or trial, and the upgrade trigger: the moment the product asks for money. Only from the input.
4. **Describe the core loop.** What action does a user repeat, what do they get back, and what brings them back (emails, notifications, shared work)? One short paragraph.
5. **List strengths and gaps.** Use NN/g's 10 usability heuristics as a lens where it helps: system status, plain language, error recovery, help. Strengths are things a user would miss if gone. Gaps are where users get stuck, pay before seeing value, or need help.
6. **Decide what to copy, what not to, and where to stand out.** NN/g's advice on competitive evaluations: look for strengths, trends, unique solutions, and gaps, and turn the findings into recommendations for your own product. Copy only what fits your users; say why for each. "Don't copy" covers things that work for them because of their scale, brand, or segment.
7. **List what to verify next.** Each unverified claim that matters for a decision becomes a check: sign up for the trial, read the pricing page, ask a customer who switched.

## Output format

```markdown
# Teardown: [competitor] — [focus]

**Evidence:** [sources and dates seen] · **Prepared:** [date]

## Summary
- [3 bullets: the most important things the team should know]

## Onboarding
| # | Screen / step | What it asks | Notes | Source |
|---|---|---|---|---|
| 1 | [step] | [fields or choices] | [friction or strength] | verified [date] / unverified |

**Steps to first value:** [n] · **Card required:** [yes / no / unverified]

## Pricing and packaging
| Plan | Price | Key limits | Source |
|---|---|---|---|
| [plan] | [as seen or check] | [limits] | verified [date] / unverified |

**Upgrade trigger:** [when the product asks for money]

## Core loop
[One paragraph.]

## Strengths
- [strength] — [evidence]

## Gaps
- [gap] — [evidence]

## For us
- **Copy:** [what] — [why it fits our users]
- **Don't copy:** [what] — [why it doesn't fit]
- **Stand out:** [where we can be clearly better]

## To verify
- [unverified claim] — [how to check]
```

## Example

**Input (trial notes, 2 May):** "Signed up for Ledgerly. Step 1: email + password. Step 2: 'What do you do?' dropdown, 12 options. Step 3: connect bank — can skip. Step 4: template picker for first invoice, prefilled with sample client. Sent a test invoice in about 4 minutes. No card asked. Pricing page: Free (5 invoices/month), Pro, Team — I didn't note Pro price. Every sent invoice has 'Sent with Ledgerly' footer. Reminder email to me next day: 'Your invoice was viewed.' I heard they're raising prices."

**Output:**

```markdown
# Teardown: Ledgerly — onboarding and pricing

**Evidence:** trial notes, 2 May · **Prepared:** [date]

## Summary
- A new user sends a first invoice in about 4 minutes with no card; the sample client removes the blank-page problem.
- The free plan's limit is invoices per month, so the upgrade trigger arrives with real usage.
- Every free invoice carries their brand to the user's clients.

## Onboarding
| # | Screen / step | What it asks | Notes | Source |
|---|---|---|---|---|
| 1 | Sign-up | Email, password | Standard | verified 2 May |
| 2 | Role | Dropdown, 12 options | Long list; purpose unclear to a new user | verified 2 May |
| 3 | Connect bank | Bank connection | Skippable, good | verified 2 May |
| 4 | First invoice | Template, prefilled sample client | Strong: user sees a finished invoice at once | verified 2 May |

**Steps to first value:** 4 · **Card required:** no

## Pricing and packaging
| Plan | Price | Key limits | Source |
|---|---|---|---|
| Free | Free | 5 invoices per month | verified 2 May |
| Pro | [check: current price] | [check: limits] | not noted |
| Team | [check: current price] | [check: limits] | not noted |

**Upgrade trigger:** the 6th invoice in a month [assumption, from the free limit].

## Core loop
The user sends an invoice, the client views it, and Ledgerly emails the user that it was viewed, which brings them back to check payment. The "Sent with Ledgerly" footer shows the product to every client.

## Strengths
- Prefilled first invoice — first value in about 4 minutes.
- "Invoice viewed" email — a reason to return the next day.

## Gaps
- 12-option role dropdown before any value.
- Price increase rumor — unverified.

## For us
- **Copy:** a prefilled sample invoice — our users also start from a blank screen [check: our data].
- **Don't copy:** a branded footer on paid plans — our users are agencies who send work under their own brand [check].
- **Stand out:** ask nothing before the first invoice; move the role question after it.

## To verify
- Pro and Team prices and limits — read the pricing page and record the date.
- Price increase — check their changelog or announcements; drop it if not found.
- Whether the footer shows on paid plans — trial a paid plan or read the help docs.
```

## Checks before you send

- [ ] Every row in onboarding and pricing has a source tag: verified with a date, or unverified.
- [ ] No price, limit, or number appears that isn't in the input.
- [ ] Rumors and inferences are marked unverified or "[assumption]".
- [ ] "For us" has at least 1 copy, 1 don't copy, and 1 stand out, each with a reason.
- [ ] Every unverified claim that affects a recommendation is in "To verify".

## Common mistakes

- Writing a feature list. A teardown follows the user's path; the order of steps is the finding.
- Copying a competitor's pricing because it's visible. Their limits fit their costs and segment, not yours.
- Stating remembered prices as fact. Pricing pages change; date what you saw.
