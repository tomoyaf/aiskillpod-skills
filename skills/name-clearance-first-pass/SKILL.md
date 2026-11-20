---
name: name-clearance-first-pass
description: Runs a first-pass screen of a product, brand, or company name before you commit to it, with search steps across trademark databases (USPTO, EUIPO TMview, J-PlatPat, WIPO Global Brand Database), domains, app stores, and social handles, a similarity check on sound, look, meaning, and related goods, a risk rating, and questions for a trademark attorney. Use when someone asks "can we use this name?", "is this name taken?", wants a trademark search, or is naming a product or startup.
---

# Name clearance first pass

> Not legal advice. This is a first-pass checklist to prepare for a lawyer's review; it doesn't replace one.

A first pass saves money by killing obviously risky names before anyone pays for a full search or a logo. It never says a name is "clear": it says what was searched, what was found, and which hits a trademark attorney should look at.

## When to use

- Choosing between 2 to 5 candidate names for a product, feature, or company.
- Before buying a domain, designing a logo, or filing a trademark application.
- When someone finds a similar name online and asks "is this a problem?".
- Not for a clearance opinion or a filing decision. Only a trademark attorney gives those.

## What you need

- The candidate names, spelled exactly.
- What the name will be used for: the goods or services, in plain words ("project management software for agencies").
- Where you sell now and plan to sell within 2 years (countries). If unknown, ask once; otherwise search the US, EU, and the user's home country and mark "[assumption]".
- Search results, if the user ran searches. If you can't search the web yourself, give the search steps and a blank results table for the user to fill; never invent hits.

## Steps

1. **Pin down the goods and services.** Write them in plain words, then find the likely Nice classes with a classification tool such as the EUIPO's TMclass. Mark the classes "[check: classes with counsel]"; classes guide the search but don't limit what counts as related.
2. **Search the trademark registers.** For each market: USPTO trademark search for registered and pending US marks; TMview (EUIPO), which covers all EU national offices, the EUIPO, and many offices outside the EU; J-PlatPat (Japan Patent Office) for Japan, by keyword and by goods/services; the WIPO Global Brand Database for international registrations under the Madrid System and participating national offices. Search exact spelling, plurals, spaces and hyphens, and sound-alike spellings.
3. **Search for unregistered use.** The USPTO advises checking common-law use (unregistered names used in commerce) and the internet, because earlier unregistered use can affect rights. Search the web, domain registries for the main extensions, the Apple App Store and Google Play, the main social platforms for handles, and company registers in the home country.
4. **Compare each hit on 2 questions.** Are the names similar in sound, appearance, or meaning and overall impression (the USPTO's likelihood-of-confusion factors)? And are the goods or services related: the same, competing, sold to the same buyers, or sold or advertised together? A hit matters only when both are yes.
5. **Rate each name.** Our default: red if an identical or near-identical live mark covers related goods in a target market; yellow if a similar mark covers related goods, or an identical one covers unrelated goods, or an unregistered user in your space predates you; green if no hit meets either test. Green still means "nothing found in a first pass", not "clear".
6. **Note the practical blockers.** Domain taken or for sale, app store name taken, handle taken, a descriptive name (it says what the product does) that may be weak. These don't decide legal risk but change cost.
7. **Write the questions for counsel.** One per yellow or red hit, plus whether to order a full search. The EUIPO notes that earlier marks can coexist by agreement or be challenged, so list those options as questions, not advice.

## Output format

```markdown
# Name clearance first pass — [names], [date]

_Not legal advice. A first-pass screen for a trademark attorney's review, not a clearance opinion._

**Use:** [goods and services in plain words]  
**Likely classes:** [n, n] [check: classes with counsel]  
**Markets searched:** [countries]

## Searches run
| Source | Query | Date | Hits worth a look |
|---|---|---|---|
| [USPTO / TMview / J-PlatPat / WIPO GBD / web / domains / app stores / social] | [exact query] | [date] | [n or "none"] |

## Hits
| Name | Hit | Where | Goods/services | Similar? | Related? | Note |
|---|---|---|---|---|---|---|
| [candidate] | [mark or user] | [register, number, status] | [their goods] | [yes/no: sound, look, meaning] | [yes/no] | [one line] |

## Ratings
| Name | Rating | Why | Practical blockers |
|---|---|---|---|
| [candidate] | [green/yellow/red] | [one line] | [domain, app store, handles] |

## Questions for a trademark attorney
- [ask counsel: ...]

## Not searched
- [markets or sources not covered]
```

## Example

**Input:** Kofi at a 6-person startup is naming a meeting-notes app sold in the US and EU. Candidates: "Notewise", "Quillo". Kofi's search results: USPTO shows a live registration "NOTEWISE" for "note-taking software" (class 9). TMview shows "QUILLO" registered in Spain for "stationery, pens" (class 16). quillo.com is for sale; @quillo on X is taken by an inactive account. No app named Quillo in either store.

**Output:**

```markdown
# Name clearance first pass — Notewise, Quillo, 4 November

_Not legal advice. A first-pass screen for a trademark attorney's review, not a clearance opinion._

**Use:** a mobile and web app that records meetings and writes notes  
**Likely classes:** 9, 42 [check: classes with counsel]  
**Markets searched:** US, EU

## Searches run
| Source | Query | Date | Hits worth a look |
|---|---|---|---|
| USPTO | Notewise, Note Wise, Quillo, Quilo | [check: date Kofi searched] | 1 |
| TMview | same queries | [check: date] | 1 |
| Domains, app stores, X | both names | [check: date] | 2 |

## Hits
| Name | Hit | Where | Goods/services | Similar? | Related? | Note |
|---|---|---|---|---|---|---|
| Notewise | NOTEWISE | USPTO, live registration [check: number] | note-taking software | yes: identical | yes: same goods | Direct conflict in the US. |
| Quillo | QUILLO | Spain, via TMview [check: number, status] | stationery, pens | yes: identical | unclear: writing tools vs software | Ask counsel. |

## Ratings
| Name | Rating | Why | Practical blockers |
|---|---|---|---|
| Notewise | red | Identical live US mark for the same goods | — |
| Quillo | yellow | Identical Spanish mark for stationery; relatedness to software unclear | quillo.com for sale; @quillo on X taken (inactive) |

## Questions for a trademark attorney
- [ask counsel: could stationery in class 16 be considered related to note-taking software in the EU?]
- [ask counsel: should we order a full search for Quillo in the US and EU before we buy the domain?]

## Not searched
- J-PlatPat and WIPO Global Brand Database (no plans outside the US and EU) [assumption]
- Company registers
```

## Checks before you send

- [ ] The disclaimer line is at the top, and no name is called "clear" or "available".
- [ ] Every hit came from a search the user or you actually ran; none is invented.
- [ ] Each hit is judged on both similarity and relatedness of goods.
- [ ] Searches run, with exact queries, and sources not searched are both listed.
- [ ] Every yellow and red name has a question for counsel.
- [ ] Classes are marked for counsel to confirm.

## Common mistakes

- Searching only the exact spelling. Sound-alikes and spaces ("Note Wise") count.
- Treating a free domain as proof the name is free to use.
- Ignoring a mark in an unrelated class without asking whether buyers could still see a link.
