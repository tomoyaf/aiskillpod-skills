---
name: altman-style-startup-review
description: Reviews a startup or new product against the advice Sam Altman wrote in his Startup Playbook for Y Combinator founders - a clear idea someone desperately needs, a product a small number of users love, focus and intensity, never losing momentum, and the CEO's jobs - and against the focus and long-term thinking in his essay How To Be Successful (2019), then names the one thing to stop and the growth metric to watch weekly. Use when a founder asks whether their startup is on track, what to focus on, whether users really love the product, why growth stalled, or how Sam Altman or Y Combinator would look at their company.
---

# Altman-style startup review

These are principles Sam Altman has described publicly in his Startup Playbook, written for Y Combinator founders, and his essay How To Be Successful (January 2019). Not affiliated with or endorsed by Sam Altman or their companies. The skill reviews the user's startup against the cited advice and returns findings and next steps; it reports what the sources say, and it does not speak for him.

## Ground rules

- Do not attribute quotes or opinions to Sam Altman beyond the cited sources.
- Never imitate him or write in his voice; review the user's material against the principles below.
- Use the user's numbers. Never invent user counts, growth rates or revenue; mark gaps "[check: ...]".
- The playbook is written for startups that aim to grow fast. For a business that doesn't, say which principles fit and which don't.

## When to use

- A founder wants an outside check on whether the startup is on track.
- Growth has stalled and the team is busy on many things.
- Before deciding to add a second product or market.
- Not for a fundraising deck review or a financial model: use model-assumptions-review. Not for planning the first users by hand: use paul-graham-style-unscalable-plan.

## The principles

1. **A clear idea someone desperately needs.** The playbook asks what the company builds and why, in a clear and short answer, and who desperately needs it; best if the founder is the target user. Source: Startup Playbook, Part I.
2. **Users who love it.** It is better to make something a small number of users love than something many users like; a sign of love is users telling friends without being asked. Source: Startup Playbook, introduction and Part I.
3. **Test the idea by launching or selling.** Launch and watch (better for consumer ideas) or try to sell before building, such as a letter of intent (better for enterprise ideas). Source: Startup Playbook, Part I.
4. **Focus and intensity.** Say no a lot; don't start the next thing until the first is dominated; do the few things very fast and decisively. Source: Startup Playbook, Part IV, Focus & Intensity.
5. **Never lose momentum.** Growth that isn't bought at a loss fixes most problems; the company does what the CEO measures, so pick the metric and review it often. Source: Startup Playbook, Part IV, Growth.
6. **The CEO's jobs.** Set vision and strategy, evangelize, hire and manage, raise money, and set the quality bar. Source: Startup Playbook, Part IV, Jobs of the CEO.
7. **Long-term thinking and focus.** In How To Be Successful, Altman lists focus and taking a long-term view among his 13 points, and suggests letting small opportunities go to pursue step changes. Source: How To Be Successful, points 1 and 6.

## What you need

- What the startup builds, for whom, and why now.
- Users and revenue, and how fast each has grown in recent weeks or months.
- Evidence of love: referrals, retention, what users say unprompted.
- What the team is working on now, with rough time shares.
- If any of this is missing, ask once, then mark it "[check]".

## Steps

1. **State the idea in one sentence** and name who desperately needs it. Flag a long or vague answer.
2. **Test for love.** From the input, list signs users love the product (unprompted referrals, retention, usage) and signs they only like it. Grade: love, like, or unknown.
3. **Check how the idea was tested.** Consumer: was it launched? Enterprise: did anyone commit to buy? Name the next test if neither.
4. **Map the work.** List the projects in flight with their time share. Mark each as serving the first thing or a next thing.
5. **Check momentum.** Name the one growth metric, its recent trend and how often it's reviewed. If there's no metric, propose one.
6. **Check the CEO's jobs.** For each of the five jobs, note whether someone is doing it and whether it's getting time.
7. **Recommend.** One thing to stop, one thing to do more intensely, the metric to review every week, and the next test if love is unknown.

## Output format

```markdown
# Startup review (Altman-style): [company]

These are principles Sam Altman has described publicly in his Startup Playbook and How To Be Successful (2019). Not affiliated with or endorsed by Sam Altman or their companies.

## The idea in one sentence
[sentence] · **Who desperately needs it:** [who] · **Clear?** [yes/no]

## Love or like
**Grade:** love / like / unknown — [evidence]

## How the idea was tested
[launch / sale / neither] — [next test]

## Work in flight
| Project | Time share | First thing or next thing |
|---|---|---|

## Momentum
**Metric:** [metric] · **Trend:** [numbers] · **Reviewed:** [how often]

## The CEO's jobs
| Job | Who | Getting time? |
|---|---|---|

## Recommendations
- **Stop:** [one thing]
- **Do more intensely:** [one thing]
- **Review weekly:** [metric]
- **Next test:** [if love is unknown]
```

## Example

**Input:** "We're 3 founders building a scheduling app for dog walkers in Lima. 140 walkers use it; 60 signed up in the last 4 weeks, 31 of them invited by another walker. Weekly active walkers went 70, 82, 95, 104 over the last 4 weeks. We're also building a pet-owner app and talking to a vet chain about a partnership. Time: walker app 40%, owner app 35%, vet partnership 25%. We look at sign-ups once a month. Nobody owns fundraising."

**Output:**

```markdown
# Startup review (Altman-style): dog walker scheduling app

These are principles Sam Altman has described publicly in his Startup Playbook and How To Be Successful (2019). Not affiliated with or endorsed by Sam Altman or their companies.

## The idea in one sentence
Scheduling for dog walkers in Lima. · **Who desperately needs it:** independent walkers juggling many clients [check: what they used before] · **Clear?** yes

## Love or like
**Grade:** love, early — 31 of the last 60 sign-ups were invited by another walker, unprompted [check: whether the app asks them to invite].

## How the idea was tested
Launched to walkers, and they use it weekly. Next test: whether walkers will pay [check: revenue].

## Work in flight
| Project | Time share | First thing or next thing |
|---|---|---|
| Walker app | 40% | first thing |
| Pet-owner app | 35% | next thing |
| Vet chain partnership | 25% | next thing |

## Momentum
**Metric:** weekly active walkers · **Trend:** 70, 82, 95, 104 over 4 weeks · **Reviewed:** sign-ups monthly; no weekly review

## The CEO's jobs
| Job | Who | Getting time? |
|---|---|---|
| Vision and strategy | [check] | [check] |
| Evangelize | [check] | [check] |
| Hire and manage | [check] | [check] |
| Raise money | nobody | no |
| Quality bar | [check] | [check] |

## Recommendations
- **Stop:** the pet-owner app and the vet partnership until walkers in Lima are won.
- **Do more intensely:** the walker app, with the 60% of time freed.
- **Review weekly:** weekly active walkers.
- **Next test:** ask walkers to pay [check: price] and see how many do.
```

## Checks before you send

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Each finding cites the user's input; nothing about users, growth or revenue is invented.
- [ ] The love grade cites evidence, or says unknown.
- [ ] One thing to stop and one metric to review weekly are named.
- [ ] Nothing is presented as Sam Altman's opinion of this company.

## Common mistakes

- Treating fast sign-ups as love. Referrals and retention say more.
- Adding a second product to fix slow growth in the first.
- Reviewing the growth metric monthly. Momentum needs a short loop.
- Using the review to speak for Altman. It applies his published advice; it doesn't predict what he'd say.
