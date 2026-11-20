---
name: five-rings-situational-review
description: Runs a wide-view situational review modeled on Miyamoto Musashi's teaching on the gaze in The Book of Five Rings (五輪書) - separates what is moving on the surface (alerts, daily metric swings, one loud message, a rival's announcement) from the underlying situation and the other side's intent, sets each surface event against a longer timeline, and sorts it into act now, watch with a trigger, or let go. Use when a team is reacting to an urgent number or event and someone asks to step back, see the big picture, check whether a drop or spike is real, avoid overreacting, 観の目, Book of Five Rings lessons for business, or a calm read of the situation before a decision.
---

# Wide-view situational review

Miyamoto Musashi (1584–1645) began writing the text later called The Book of Five Rings (五輪書) in 1643 and entrusted it to his student Terao Magonojō shortly before he died; no copy in his own hand survives. It has five scrolls named Earth, Water, Fire, Wind, and Void (地・水・火・風・空). In the Water scroll, on where to put your eyes, Musashi says the gaze should be large and wide, and that there are two ways of seeing: 観 (kan) and 見 (ken). His line is 「観の目強く、見の目弱く」. In our rendering: make the eye that takes in the whole strong and the eye that fixes on things weak; see the far as if it were near and the near as if it were far. He adds that you should know the opponent's sword without staring at it, and that this gaze is the same in a duel and in a battle. In the Wind scroll he says the gaze in strategy is set, broadly, on the other person's mind, and in a large battle on the state of the enemy's forces. Musashi was writing about a fighter's eyes; using it for a business review is our analogy, not his claim. The skill keeps his order: take in the whole first, read the other side, and only then act on the detail.

## When to use

- A metric dropped or spiked, an alert fired, or one customer's angry message has the whole team reacting.
- A competitor announced something and the team wants to answer this week.
- Before a weekly or monthly decision meeting, to separate real changes from noise.
- When a team has been firefighting for weeks and nobody can say whether the business is better or worse.
- Not for a head-to-head comparison with one competitor (use know-enemy-and-yourself). Not for building futures over years (use scenario-planning). Not for writing up the metrics themselves (use monthly-kpi-summary).

## What you need

- The decision that is pending, or the urgent event that started the review. If neither is clear, ask once.
- The surface events: what happened, when, and how big (numbers with dates).
- A longer view of the same numbers: at least 8 to 12 periods of history, or last year's same period. If missing, ask for it; without it, write "[check: history needed]" and don't call anything a trend.
- Who else is involved: customers, a competitor, a partner, your own team. What they have done, not what people think they will do.
- Never invent a baseline or a reason. Mark guesses as "[inference]" and missing facts as "[check: ...]".

## Steps

1. **Name the pull.** Write the event that is pulling everyone's attention and the decision people want to make about it, in one sentence each. Note how long ago it happened. Many urgent items are less than a day old.

2. **List what you see (見), without explaining it.** Every surface event with its date, size, and source: "Sign-ups 31 yesterday, usual weekday range unknown [check]". No causes yet. Separating seeing from explaining is the point of the exercise; a cause written too early steers the rest of the review.

3. **Take in the whole (観).** Put each event on the longer timeline. Compare it with the normal range of the last 8 to 12 periods and with the same period last year. Ask how often something this size has happened before and what followed. Mark each event "inside the usual range", "outside it", or "no history".

4. **See the far as if near.** List the slow changes that don't show up in a single day: a trend over months, a shift in the customer mix, a rival's direction over the past year, a regulation coming into force. For each, write what it means for the decision in front of you this week. Teams usually have this information and leave it out of urgent meetings.

5. **See the near as if far.** For each urgent event, ask: will this matter in 90 days, and to whom? Would we act on it if it had happened a month ago and we were reading about it now? An event that fails both questions is a candidate for "let go".

6. **Read the other side.** For each party the situation depends on (a customer, a competitor, a partner, your own team), write what they actually did, what that suggests they intend [inference], and what state they're in (resources, timing, pressure). Musashi puts the gaze on the opponent's mind, not on the sword: watch the decision behind the move, not the move alone.

7. **Sort and decide.** Put each event in one row: signal (it changes the underlying situation), noise (inside the usual range, no change in intent), or unknown (needs a test). Then decide: act now (signal, and waiting costs more than acting), watch with a trigger (a named number or event that would move it to "act"), or let go. One owner per "act now".

8. **Set the standing gaze.** Musashi warns that this way of seeing can't be picked up in the moment when things are hectic, so it has to become the normal way of looking. Write the 3 to 5 numbers or signals the team will review on a fixed rhythm, each with its usual range, so the next spike is read against the whole and not alone.

## Output format

```markdown
# Wide-view review: [situation]
**Pending decision:** [one sentence] · **Started by:** [event, date] · **Reviewed:** [date]

## What we see (surface)
| Event | When | Size | Source |
|---|---|---|---|

## The whole (against history)
| Event | Usual range / last year | Inside, outside, or no history |
|---|---|---|

## Far things brought near
- [slow change] — means for this decision: [one line]

## Near things pushed far
- [urgent event] — matters in 90 days? [yes / no / unknown] — to whom: [who]

## The other side
| Party | What they did | What it suggests [inference] | Their state |
|---|---|---|---|

## Sort and decide
| Event | Signal / noise / unknown | Decision | Trigger or owner |
|---|---|---|---|

## Standing gaze
| Signal to review | Rhythm | Usual range |
|---|---|---|

## Next actions
- [action] — [owner] — [date]
```

## Example

**Input:** "Panic this morning. We run Hikari Forms, a form builder for clinics. Sign-ups yesterday: 31; the day before 52. Weekly sign-ups for the last 12 weeks: 290, 305, 270, 310, 295, 288, 320, 300, 280, 315, 298, 302. Yesterday was a public holiday. Also, a big clinic chain (our second-largest customer, 7% of revenue) emailed the CEO angry about a slow export; support says the fix ships Thursday. And our rival FormDesk announced a free plan yesterday. The CEO wants to launch our own free plan this week. Paid conversions from trial: 21% each of the last 3 months. Last month 3 of our 40 churned accounts named price."

**Output:**

```markdown
# Wide-view review: holiday sign-up dip, angry customer, FormDesk free plan
**Pending decision:** launch a free plan this week? · **Started by:** sign-up drop and FormDesk announcement, yesterday · **Reviewed:** [date]

## What we see (surface)
| Event | When | Size | Source |
|---|---|---|---|
| Daily sign-ups fell | Yesterday | 31 vs 52 the day before | [product data] |
| Angry email from clinic chain | Yesterday | Customer is 7% of revenue | [CEO inbox] |
| FormDesk free plan | Yesterday | Announcement only | [their site] |

## The whole (against history)
| Event | Usual range / last year | Inside, outside, or no history |
|---|---|---|
| Daily sign-ups | Weekly 270–320 for 12 weeks; daily range not given | No history for holidays [check: last holiday's sign-ups] |
| Customer complaint | — | No history given |
| Trial-to-paid | 21% for 3 months | Inside the usual range |

## Far things brought near
- Weekly sign-ups have been flat for 12 weeks (270–320) — means for this decision: the question is growth, not yesterday's dip.
- 3 of 40 churned accounts named price last month — means for this decision: price matters to some, but most churn has other reasons [check: the other 37].

## Near things pushed far
- Holiday dip — matters in 90 days? no, unless it continues on working days — to whom: nobody yet.
- Angry clinic chain — matters in 90 days? yes, 7% of revenue — to whom: revenue and references.
- FormDesk free plan — matters in 90 days? unknown — to whom: prospects comparing tools.

## The other side
| Party | What they did | What it suggests [inference] | Their state |
|---|---|---|---|
| Clinic chain | Escalated to the CEO | Wants a named owner and a date, not a discount | [check: renewal date] |
| FormDesk | Announced a free plan | Going after volume at the low end | [check: limits of the free plan] |
| Our team | CEO wants a free plan this week | Reacting to FormDesk, not to our own data | Firefighting |

## Sort and decide
| Event | Signal / noise / unknown | Decision | Trigger or owner |
|---|---|---|---|
| Holiday sign-up dip | Noise, likely | Let go | Revisit if weekly sign-ups fall below 270 |
| Clinic chain complaint | Signal | Act now: CEO calls them today with Thursday's fix date | CEO |
| FormDesk free plan | Unknown | Watch: read their free-plan limits; track lost trials that name FormDesk | Act if trial-to-paid falls below [check: threshold to agree] |
| Our free plan this week | — | Not this week; decide after 4 weeks of data | [owner] |

## Standing gaze
| Signal to review | Rhythm | Usual range |
|---|---|---|
| Weekly sign-ups | Weekly | 270–320 |
| Trial-to-paid | Monthly | 21% |
| Top-10 customer health | Weekly | [check: define] |
| Lost trials naming a rival | Weekly | [check: no baseline yet] |

## Next actions
- Call the clinic chain with the fix date — CEO — today
- Pull sign-ups for the last two holidays — [owner] — tomorrow
- Read FormDesk's free-plan terms — [owner] — this week
```

## Checks before you send

- [ ] Surface events are listed with dates and sizes before any cause is given.
- [ ] Each event is compared with a longer history, or marked "no history" with a check.
- [ ] At least one slow change is written down and tied to the decision.
- [ ] Inferences about anyone's intent are marked "[inference]".
- [ ] Every event ends as signal, noise, or unknown, with act, watch (with a trigger), or let go.
- [ ] Each "act now" has one owner and a date.
- [ ] The standing gaze lists signals with their usual ranges.
- [ ] Any line from the Book of Five Rings is our rendering, and the review doesn't claim Musashi wrote about business.

## Common mistakes

- Explaining before listing. The first cause someone names becomes the story, and the review only confirms it.
- Calling a trend from two data points. Without history, write "no history" and get it.
- Reading the rival's move and not its intent. A free plan aimed at a different segment may need no answer.
- Treating "step back" as "do nothing". The review should end with at least one action, often a small and fast one.
- Making Musashi say more than he wrote. He describes where a fighter's eyes go; the business reading is ours.
