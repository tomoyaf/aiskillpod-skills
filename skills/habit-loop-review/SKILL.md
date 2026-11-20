---
name: habit-loop-review
description: Reviews whether a product earns repeat use with the Hooked Model from Nir Eyal's Hooked - trigger (external and internal), action, variable reward and investment - finds the weakest phase with usage evidence, proposes one change per phase, and runs an ethics check on whether the habit serves the user. Use when someone asks about the Hooked model, habit-forming products, retention or engagement, why users don't come back, triggers and rewards, or designing a product people use every day.
---

# Habit loop review

Nir Eyal's Hooked (2014) describes a four-phase loop he calls the Hooked Model, first published on his blog. A **trigger** prompts use; at first it is external (a notification, an email, a colleague's message), and over time an internal one (a feeling or routine, such as boredom or uncertainty) takes over. An **action** is the simplest step taken in hope of a reward. A **variable reward** satisfies the need while leaving some of it open, so the next visit matters. An **investment** is something the user puts in (data, content, settings, reputation) that makes the product better next time and loads the next trigger. This skill finds which phase is weakest for a product and proposes changes, with an ethics check, because Eyal also writes about the line between helping a habit and manipulating one.

## When to use

- Users sign up and try the product, then don't come back.
- The team wants a product used weekly or daily, and needs to know what to change first.
- Before adding notifications, streaks or rewards, to check they'd help the loop.
- Not for analyzing interview notes: use user-interview-synthesis. Not for the activation steps of the first session: use customer-onboarding-plan.

## What you need

- What the product does, who uses it, and how often they should use it to get value.
- Usage data: return rate by week, which actions repeat users take, where others stop.
- Current triggers: notifications, emails, integrations.
- What users put into the product over time.
- If usage numbers are missing, mark claims "[check: data]". Never invent retention figures.

## Steps

1. **Set the habit target.** Name the habit: who, which action, how often ("a team lead reviews this week's tickets every Monday"). Check that the frequency fits the value; a product used yearly isn't a habit product, and the review should say so.
2. **Name the internal trigger.** Write the feeling or moment that comes just before the user needs the product, in the user's words if the input has them. If no clear internal trigger exists, that is the main finding.
3. **Review the external triggers.** List each one, when it fires and what it asks. Check that each leads to one action and arrives near the internal trigger's moment.
4. **Review the action.** Count the steps from trigger to reward. Find the step where people stop, from the data. Propose the cut that makes the action easier.
5. **Review the reward.** Say what the user gets and whether it varies in a way that matters to them (Eyal names rewards of the tribe, the hunt and the self). Flag a fixed or empty reward.
6. **Review the investment.** List what the user puts in that improves the product for them next time, and whether it sets up the next trigger. Flag a loop where nothing is stored.
7. **Pick the weakest phase.** Using the data, name the phase where most users drop out and propose one change for it, with a metric. Add at most one change for each other phase.
8. **Run the ethics check.** Eyal's question is whether the product improves the user's life and whether the maker would use it. State whether the habit serves the user, and remove any change that relies on hiding costs or exploiting compulsion.

## Output format

```markdown
# Habit loop review: [product]

**Habit target:** [who, action, how often]

## The loop today
| Phase | What happens now | Evidence | Strength (weak / ok / strong) |
|---|---|---|---|
| Internal trigger | | | |
| External trigger | | | |
| Action | | | |
| Variable reward | | | |
| Investment | | | |

## Weakest phase
**[phase]** — [why, with data]
**Change:** [one change] · **Metric:** [what moves if it works]

## Other changes (one per phase at most)
- [phase]: [change]

## Ethics check
**Does the habit serve the user?** [yes / partly / no, and why]
**Removed or rejected:** [changes that would manipulate]
```

## Example

**Input:** "Our app helps restaurant managers in Bogotá order produce from local suppliers. Managers should order 3 times a week. Data: 61% of new managers place a first order; only 18% order in week 4. Repeat managers almost all use 'reorder last basket'. The only trigger is a weekly promo email. Ordering takes 9 taps. Prices change daily and managers say they open the app 'to see if tomatoes went down'. Nothing is saved except the last basket."

**Output:**

```markdown
# Habit loop review: produce ordering app

**Habit target:** a restaurant manager places an order 3 times a week.

## The loop today
| Phase | What happens now | Evidence | Strength |
|---|---|---|---|
| Internal trigger | Not knowing today's prices before ordering | managers open the app "to see if tomatoes went down" | ok |
| External trigger | Weekly promo email | the only trigger; doesn't match a 3-a-week rhythm | weak |
| Action | 9 taps to order; "reorder last basket" is shorter | repeat managers almost all reorder | ok |
| Variable reward | Daily prices: today's tomatoes may be cheaper | managers check for price drops | strong |
| Investment | Only the last basket is saved | nothing else is stored | weak |

## Weakest phase
**External trigger** — 61% order once but 18% order in week 4, and the only prompt is weekly and promotional.
**Change:** a message on each manager's usual order days with today's prices for their last basket, linking straight to reorder. · **Metric:** week-4 ordering rate.

## Other changes (one per phase at most)
- Investment: let managers save more than one basket ("weekday", "weekend") and price alerts for chosen items.
- Action: put "reorder last basket" on the first screen [check: tap count after the change].

## Ethics check
**Does the habit serve the user?** Yes: it saves the manager time and money on orders they must place anyway.
**Removed or rejected:** countdown "deals" that pressure managers to order more than they need.
```

## Checks before you send

- [ ] The habit target names who, which action and how often, and the frequency fits the value.
- [ ] Each phase cites evidence from the input, or is marked "[check: data]".
- [ ] One weakest phase is chosen from the data, with one change and a metric.
- [ ] No more than one extra change per phase.
- [ ] The ethics check is answered, and any manipulative idea is removed.

## Common mistakes

- Adding notifications when the internal trigger is missing. More prompts without a real need train users to ignore them.
- Rewards that never vary. A fixed reward stops pulling people back.
- Forgetting investment. Without stored value, each visit starts from zero.
- Building a habit the user wouldn't choose. Eyal's own later book, Indistractable (2019), is about resisting unwanted habits.
