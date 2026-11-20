---
name: wartime-peacetime-check
description: Tells a leader whether the company is in peacetime or wartime in Ben Horowitz's sense from The Hard Thing About Hard Things and his 2011 post Peacetime CEO/Wartime CEO - a large lead in a growing market versus an existential threat - and checks whether the leader's management style, priorities and communication match, including the hard calls the book covers (layoffs, firing an executive, telling the truth to the team). Use when someone asks about wartime versus peacetime CEO, The Hard Thing About Hard Things, Ben Horowitz, a company in crisis, a hard call a founder is avoiding, or whether the management style fits the situation.
---

# Wartime or peacetime check

Ben Horowitz co-founded Loudcloud, which became Opsware and was sold to Hewlett-Packard in 2007. His book The Hard Thing About Hard Things (2014) grew from his blog and covers the hard parts of running a company: layoffs, demoting or firing executives, telling the team bad news, and the leader's own state of mind. In his 2011 post Peacetime CEO/Wartime CEO, he defines peacetime as a time when a company has a large advantage over rivals in its core market and the market is growing, so it can widen the market and its strengths. Wartime is when the company faces an imminent threat to its existence, from rivals, a market or economic shift, or supply problems. He writes that he was a peacetime CEO for about nine months, then a wartime CEO for seven years, and that the two need very different styles. This skill places a company in one state, then checks whether the leader is acting for that state and which hard call is waiting.

## When to use

- Results have turned and the leader isn't sure whether to change how the company is run.
- A founder is putting off a hard decision: a layoff, an executive who isn't working, a pivot.
- Before a board meeting or all-hands where the situation must be explained honestly.
- Not for a formal decision write-up: use decision-memo. Not for the conversation with one person: use difficult-conversation-prep.

## What you need

- The core market: share or lead against rivals, growth, and the trend.
- The threats: rivals, market change, cash runway, key customers, supply.
- How the leader runs things now: meetings, decision speed, priorities, how widely decisions are discussed.
- Any decision being delayed, and for how long.
- If runway or market data is missing, mark it "[check]". Never invent a rival's numbers.

## Steps

1. **Test for peacetime.** Does the company have a large lead in its core market, and is the market growing? Cite the evidence for each.
2. **Test for wartime.** List each threat to the company's survival and how soon it could arrive. A short runway, a rival taking the core market, or a market shift that removes demand each count.
3. **Call the state.** Peacetime, wartime, or moving from one to the other. Say why in two sentences.
4. **Compare the style to the state.** Horowitz's post contrasts the two: in peacetime, a leader widens the opportunity, builds the culture and lets teams find their way, with broad consensus; in wartime, the leader focuses on the one threat, follows a clear plan and decides fast, even against consensus. List where the current practices fit and where they don't.
5. **Name the waiting hard call.** From the input, name the decision that is being delayed and what the delay costs per week or month. The book's view is that delay usually makes these calls worse.
6. **Plan the truth-telling.** Draft what the leader tells the team about the state and the hard call: what happened, what it means, what will change. Horowitz argues for telling people the truth, including bad news.
7. **Set the next 30 days.** Three actions with owners, and the signal that would show the state has changed.

## Output format

```markdown
# Wartime or peacetime check: [company]

**Date:** [date] · **Leader:** [name]

## Peacetime test
**Large lead in the core market?** [yes/no, evidence] · **Market growing?** [yes/no, evidence]

## Wartime test
| Threat | How soon | Evidence |
|---|---|---|

## The state
**[Peacetime / wartime / moving to wartime / moving to peacetime]** — [two sentences]

## Style against state
| Practice now | Fits the state? | Change |
|---|---|---|

## The hard call waiting
**Decision:** [what] · **Delayed for:** [time] · **Cost of delay:** [per week or month]

## What to tell the team
[Short draft: what happened, what it means, what changes]

## Next 30 days
1. [action, owner, date]
**Signal the state has changed:** [signal]
```

## Example

**Input:** "We run a 40-person delivery-route software company in Spain. Until last year we led our niche with about half the regional couriers as customers [our estimate]. In the last 6 months a funded rival has signed 9 of our 60 customers at half our price. Runway is 11 months. We still hold quarterly offsites to brainstorm new products, and every roadmap decision needs agreement from all 6 department heads. Our VP of Sales has missed target for 3 quarters; I've postponed the conversation twice."

**Output:**

```markdown
# Wartime or peacetime check: delivery-route software

**Date:** [date] · **Leader:** [check: name]

## Peacetime test
**Large lead in the core market?** It was: about half the regional couriers [your estimate]; now falling. · **Market growing?** [check]

## Wartime test
| Threat | How soon | Evidence |
|---|---|---|
| Funded rival at half price taking customers | Now | 9 of 60 customers lost in 6 months |
| Runway | 11 months | your figure |

## The state
**Moving to wartime.** A rival is taking the core market at half the price, and runway is under a year. The company's survival depends on keeping its core customers.

## Style against state
| Practice now | Fits the state? | Change |
|---|---|---|
| Quarterly offsites for new products | No | Pause; focus on retaining and winning couriers |
| Roadmap decisions need all 6 heads to agree | No | The CEO decides the roadmap for the next two quarters after hearing the heads |

## The hard call waiting
**Decision:** the VP of Sales, 3 quarters below target · **Delayed for:** two postponements [check: weeks] · **Cost of delay:** each quarter without a working sales lead while customers leave [check: pipeline effect]

## What to tell the team
"A funded rival has signed 9 of our customers at half our price in 6 months. We have 11 months of cash. For the next two quarters we're focused on one thing: keeping and winning couriers. New product ideas wait. I'll make roadmap calls faster, after hearing from each team."

## Next 30 days
1. Hold the conversation with the VP of Sales this week [check: date]; prepare it with difficult-conversation-prep.
2. Call each of the 51 remaining customers to learn their risk of leaving [check: owner].
3. Decide a price and contract response to the rival [check: owner, date].
**Signal the state has changed:** no customer lost for a quarter, and runway above [check: months].
```

## Checks before you send

- [ ] Both tests cite evidence from the input, or are marked "[check]".
- [ ] One state is called, in two sentences.
- [ ] The style table names current practices from the input, not generic advice.
- [ ] The hard call is named with how long it has waited and what the delay costs.
- [ ] Nothing judges a named person beyond the facts given; people decisions are framed as the leader's call.

## Common mistakes

- Declaring wartime to justify a style the leader prefers. The test is the threat, not the mood.
- Staying in wartime after the threat passes. Horowitz describes the styles as fitting different times.
- Hiding bad news to protect morale. People usually find out, and trust falls further.
- Treating the hard call as a matter of finding the perfect answer. The book's point is that there often isn't one, and delay is a choice too.
