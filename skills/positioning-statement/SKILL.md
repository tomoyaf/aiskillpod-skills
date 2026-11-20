---
name: positioning-statement
description: Drafts product positioning using April Dunford's 5 components - competitive alternatives, unique attributes, value, best-fit target customer, and market category - and ends with a one-line positioning statement. Use when someone asks for positioning, a positioning statement, "how do we describe what we do", differentiation, a value proposition, or why customers pick us over the alternatives.
---

# Positioning statement

Positioning starts from what customers would do if you didn't exist, not from your feature list. Work through the 5 components in order, because each one depends on the one before; the one-line statement comes last, as a summary, never as the starting point.

## When to use

- Before writing a homepage, pitch deck, or sales deck, when nobody agrees on how to describe the product.
- When deals are lost to "we'll keep doing it in spreadsheets" or the wrong buyers keep signing up.
- Not for a tagline or slogan: positioning is the input a tagline is written from.

## What you need

- What the product does and its main features.
- Your 3 to 10 happiest customers: who they are, why they bought, what they used before. This matters most; if missing, ask once, then proceed and mark every customer claim "[assumption]".
- Lost deals and what those buyers chose instead, if known.
- Optional: current homepage copy, so the draft can be compared against it.

## Steps

1. **List the competitive alternatives.** Ask Dunford's question: what would a customer do if the product didn't exist? Often the answer is "do nothing", meaning they keep a spreadsheet, a manual process, or an intern. List those next to named competitors, in customers' words. Skip competitors you never meet in deals.
2. **Find the unique attributes.** What you have that the alternatives don't: features, capabilities, expertise. Our default: keep only attributes a customer could verify, and drop any the main alternative also has.
3. **Turn each attribute into value.** For each attribute, ask "so what for customers?" until the answer is something the customer measures: hours, money, risk, revenue. Our default: group the values into 1 to 3 themes. Value with no attribute behind it gets cut.
4. **Name the best-fit customer.** The characteristics that make a customer care a lot about that value: company size, role, situation, trigger event. Write it so a sales rep could disqualify a lead in 1 call. "SMBs" is too wide; "clinics with 3+ dentists and a front-desk team" works.
5. **Choose the market category.** The frame that makes your value obvious to that customer. Two options: an existing category customers already understand, usually narrowed to a niche ("embeddable database for mobile devices"), or a new category, which takes a lot of effort to make meaningful to buyers. Dunford recommends starting from an existing category.
6. **Write the one-line statement.** Our default template: "For [target customer] who [situation], [product] is a [category] that [key value]. Unlike [main alternative], we [unique attribute]." Under 45 words.
7. **Stress-test it (our default).** Would a happy customer recognize themselves? Could a competitor say the same sentence truthfully? If yes, return to step 2. Note the weakest component and what evidence would firm it up.

## Output format

```markdown
# Positioning — [product]

## 1. Competitive alternatives
- [Alternative in customers' words] — [why they use it today]

## 2. Unique attributes
| Attribute | Missing from | Verifiable how |
|---|---|---|

## 3. Value
| Value theme | From attributes | Measured as |
|---|---|---|

## 4. Best-fit target customer
- **Who:** [traits]
- **Trigger:** [event that makes them look]
- **Not a fit:** [traits that disqualify]

## 5. Market category
**[Category]** — [why this frame; options rejected and why]

## One-line positioning statement
For [target customer] who [situation], [product] is a [category] that [key value]. Unlike [main alternative], we [unique attribute].

## Stress test
- Weakest component: [which] — [what evidence would help]
- Could a competitor say this? [yes/no and why]
```

## Example

**Input:** "Pennant: inventory software. Syncs stock across Shopify, Etsy and a physical shop in real time, handles bundles. Happy customers: 6 small homeware brands, 2–10 staff, selling on 2–3 channels, all came from spreadsheets after overselling at Christmas. One lost deal went to a big ERP."

**Output:**

```markdown
# Positioning — Pennant

## 1. Competitive alternatives
- Spreadsheets updated by hand — cheap and familiar until a busy season
- A full ERP — chosen by brands planning to grow fast; one lost deal [from input]
- Each channel's built-in stock count — free, but no sync between channels

## 2. Unique attributes
| Attribute | Missing from | Verifiable how |
|---|---|---|
| Real-time stock sync across Shopify, Etsy and in-store | Spreadsheets, channel tools | Sell 1 in-store, see the count drop online |
| Bundle stock that draws down component items | Spreadsheets, channel tools | Sell a gift set, see each item drop |
| Set up in an afternoon [assumption] | ERP | [check: typical setup time] |

## 3. Value
| Value theme | From attributes | Measured as |
|---|---|---|
| No overselling in peak season | Real-time sync, bundles | Cancelled orders, refunds |
| Hours back each week | Real-time sync | Hours spent reconciling sheets |

## 4. Best-fit target customer
- **Who:** product brands with 2 to 10 staff selling physical goods on 2 or 3 channels, including at least 1 marketplace
- **Trigger:** an oversold peak season, or adding a second sales channel
- **Not a fit:** brands needing purchasing, accounting and warehouse management in one system

## 5. Market category
**Multichannel inventory software for small product brands** — a subsegment of inventory management. "ERP" invites a feature comparison Pennant loses; a new category would need teaching.

## One-line positioning statement
For small product brands selling on 2 or 3 channels who oversell when stock lives in spreadsheets, Pennant is multichannel inventory software that keeps every channel's count right in real time. Unlike spreadsheets, we update stock the moment anything sells, bundles included.

## Stress test
- Weakest component: unique attributes — other sync tools may match real-time sync [check: 2–3 named competitors]. Bundles may be the true differentiator.
- Could a competitor say this? Possibly, for sync alone; the bundle claim narrows it.
```

## Checks before you send

- [ ] The 5 components appear in order, and the statement comes last.
- [ ] At least one alternative is a non-product (spreadsheet, hiring, doing nothing) or it says why none applies.
- [ ] Every value traces back to a unique attribute in the table.
- [ ] The target customer includes at least one "not a fit" trait.
- [ ] The one-line statement is under 45 words and names the main alternative.
- [ ] Customer claims not in the input are marked "[assumption]" or "[check: ...]".

## Common mistakes

- Starting with the statement and back-filling the components to fit it.
- Listing "easy to use" or "great support" as unique attributes. Every alternative claims them.
- Picking a new category because it sounds bigger, then spending a year explaining it.
