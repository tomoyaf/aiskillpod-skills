---
name: strategy-approach-picker
description: Picks the right strategy framework for a situation - asks what decision is being made, the time horizon, how predictable and shapeable the market is, and what the main unknown is (industry attractiveness, your own resources, a bottleneck, a new market, a competitor's moves, why customers buy), then recommends one or two of the library's strategy skills with why, what to bring, and in what order, or says plainly that none fits. Use when someone asks which strategy framework to use, where to start with strategy, five forces or SWOT or VRIO, a list of business strategy frameworks, 経営戦略 フレームワーク, or "we need a strategy but don't know how to approach it".
---

# Choose a strategy approach

Most strategy frameworks answer one kind of question well and others badly. Five forces explains an industry's profits, not why a customer switched; a SWOT lists factors but doesn't choose among them. Picking the method is the first strategic choice. "Your Strategy Needs a Strategy" (Reeves, Love, and Tillmanns, Harvard Business Review, 2012) argues that the right approach depends on the environment: how predictable it is and how far you can shape it. BCG's "Why Strategy Needs a Strategy" (Reeves, Deimler, and Love, 2012) and its strategy palette add a third dimension, how harsh it is. Michael Porter's "What Is Strategy?" (HBR, 1996) adds a test for the output: strategy means choosing a distinct position and what not to do, not just running the same activities better. This skill asks a few questions, then routes to one or two of the 20 other strategy skills in this library, in order, with what to bring to each.

## When to use

- Someone says "we need a strategy" and the team doesn't agree on where to start.
- A team is about to run a familiar framework (often SWOT) out of habit and wants to check it fits.
- A founder or manager has a specific strategic question and wants the method that answers it.
- Not for running a framework: once the route is chosen, use that skill. Not for operational decisions with known options (use decision-memo) or goal setting (use okr-draft).

## What you need

- The decision to be made, and who makes it by when.
- The time horizon: this quarter, this year, several years.
- What the user knows about the market: is it stable and predictable, changing fast, or in crisis? Can one company change the rules?
- The main unknown: the thing that, if known, would make the decision easy.
- If the user can't answer a question, don't guess. Route on what is known and say which answer would change the route.

## Steps

1. **Ask for the decision.** "What will you decide differently after this work?" If the answer is "nothing specific", ask what triggered the request (a board meeting, a loss, a stall) and turn that into a decision. A framework without a decision produces a document nobody uses.

2. **Ask the horizon.** This quarter points toward constraint, funnel, and experiment skills; one to three years toward positioning, resources, and growth options; beyond that toward scenarios and maps.

3. **Read the environment.** Ask three questions, from BCG's palette: Can you predict demand and competition a year out? Can your company, alone or with partners, change how the market works? Is the business under threat right now (cash, a crisis, a collapse in demand)? A predictable, hard-to-shape market suits analysis-then-plan methods; an unpredictable one suits experiments; a harsh one puts survival first. If the user isn't sure, route to strategy-style-selector first.

4. **Find the main unknown.** Ask: "If you knew one thing for certain, which would make the decision easy?" Map the answer to the routing table at the end of these steps. If two unknowns are tied, pick the one the other depends on.

5. **Pick one or two skills and set the order.** Recommend at most two. For each, say why it fits this situation, what to bring (data, people, time), and what it will produce. When there are two, put first the one whose output feeds the second.

6. **Say what the route won't answer.** Name the question the chosen skills leave open, so nobody expects the framework to settle it.

7. **Say when none fits.** If the question is operational, financial, or about goals rather than strategy, say so and name the skill that fits better. If the user has no decision and no trigger, say a framework will not help yet and suggest writing the decision first.

### Routing table

| Main unknown or situation | Skill | Brings out |
|---|---|---|
| Is this industry or market worth being in; why are margins low? | five-forces-analysis | The forces that set the industry's profit |
| Compete on cost or on difference, broadly or in a niche? | generic-strategy-choice | One generic position and what to stop |
| Where in our own activities do cost and value come from? | value-chain-analysis | The activities to fix, cut, or build on |
| Which of our resources give an advantage others can't copy? | vrio-analysis | Resources graded by value, rarity, imitability, organization |
| Which kind of strategy process fits a market this predictable and shapeable? | strategy-style-selector | A style (classical, adaptive, visionary, shaping, renewal) for the environment |
| Everyone competes on the same factors; how to stand apart? | errc-strategy-canvas | Factors to eliminate, reduce, raise, create |
| We have goals but no real strategy; what is the core challenge? | strategy-kernel | Diagnosis, guiding policy, coherent actions |
| How do our choices fit together from aim to systems? | strategy-choice-cascade | Aspiration, where to play, how to win, capabilities, systems |
| Will our advantage last as we grow? | durable-advantage-check | Which sources of lasting advantage you have or lack |
| Output is held back by one step or resource | toc-five-focusing-steps | The constraint and how to exploit and lift it |
| Sales roles, hand-offs, and stage metrics are unclear | funnel-stage-design | Roles per stage and the metric each owns |
| Demand for a new product is uncertain | build-measure-learn | The riskiest assumption and the smallest test |
| Early adopters bought, mainstream buyers don't | beachhead-plan | One segment to win first and how |
| Why do customers buy, switch, or leave? | jtbd-switch-interview | The job, the forces behind switching |
| Which parts of our product or stack will commoditize; what to build, buy, or outsource? | wardley-map | A map of components by evolution, and moves |
| How do we stand against one named competitor? | know-enemy-and-yourself | A two-sided comparison and where to engage |
| The team is reacting to urgent events; is it a real change? | five-rings-situational-review | Signal vs noise, act, watch, or let go |
| Where to grow next: new products, new markets, or both? | ansoff-growth-options | Growth options ranked by risk |
| Big outside forces could go several ways over years | scenario-planning | Plausible futures and moves that hold across them |
| A quick shared picture of strengths, weaknesses, opportunities, threats, turned into actions | swot-tows-analysis | Factors and paired strategies |

Common pairs, in order: five-forces-analysis then generic-strategy-choice; jtbd-switch-interview then beachhead-plan; vrio-analysis then durable-advantage-check; win or loss evidence from win-loss-analysis then know-enemy-and-yourself; scenario-planning then strategy-kernel.

## Output format

```markdown
# Strategy approach: [situation in a few words]

**Decision:** [what will be decided, by whom, by when]
**Horizon:** [quarter / year / several years]
**Environment:** predictable [yes / no / unsure] · shapeable [yes / no / unsure] · under threat [yes / no]
**Main unknown:** [one sentence]

## Recommended route
1. **[skill]** — why: [one or two sentences tied to the answers above]. Bring: [data, people, time]. You'll get: [output].
2. **[skill]** (optional) — why: [...]. Bring: [...]. You'll get: [...].

## What this route won't answer
- [question left open]

## Considered and not chosen
- [skill] — [why not, one line]

## Would change the route
- If [answer], use [skill] instead.
```

## Example

**Input:** "I run Mado Clinic, appointment software for dental clinics in Japan. 180 paying clinics, growth has been flat for two quarters. Board meeting in 6 weeks and they want a strategy for next year: some say expand to veterinary clinics, some say add payments for existing clinics. Market is fairly stable; two big rivals, pricing hasn't moved in years. We're not in trouble: 20 months of runway. Honestly I don't know why the clinics that chose us chose us over the big two."

**Output:**

```markdown
# Strategy approach: flat growth, where to grow next

**Decision:** whether next year's growth bet is veterinary clinics, payments for current clinics, or neither — CEO proposes, board decides in 6 weeks
**Horizon:** one year
**Environment:** predictable yes (stable market, stable pricing) · shapeable no [check: no sign given] · under threat no (20 months runway)
**Main unknown:** why clinics chose Mado over the two large rivals

## Recommended route
1. **jtbd-switch-interview** — why: both growth options assume we know what clinics hire us for; we don't. If the reason is "simple to set up", vets may value it too; if it's "fits dental workflows", payments for current clinics is the safer bet. Bring: 8 to 12 clinics that switched to us in the last 30 to 90 days (older switches recall less, so mark them), and one person to interview. You'll get: the job and the forces behind switching. Time: [check: interview schedule].
2. **ansoff-growth-options** — why: the board's question is new market vs new product for the current market, which is what this matrix lays out. Bring: the interview findings, current revenue per clinic, and what each option needs to build. You'll get: the options ranked by risk, with the first steps.

## What this route won't answer
- Whether the dental market itself can support higher prices: that's five-forces-analysis, worth running if both growth options fail.

## Considered and not chosen
- swot-tows-analysis — would list factors but not settle the vets-vs-payments choice.
- strategy-style-selector — the environment is already clear: predictable and stable.

## Would change the route
- If the interviews show clinics chose Mado mainly on price, run generic-strategy-choice before ansoff-growth-options.
```

## Checks before you send

- [ ] The decision, horizon, environment, and main unknown are stated from the user's answers, or marked unsure.
- [ ] At most two skills are recommended, in order, each with why, what to bring, and what it produces.
- [ ] Every skill named exists in the routing table, or is an existing skill named for a case outside strategy.
- [ ] The output says what the route won't answer.
- [ ] If nothing fits, it says so and points to a better skill instead of forcing a framework.
- [ ] No market facts were invented to justify the route.

## Common mistakes

- Defaulting to SWOT because everyone knows it. It's a quick shared picture, not a way to choose.
- Recommending four frameworks "to be thorough". Each takes real time; two in the right order beat four in parallel.
- Running an analysis-then-plan method in a market that changes every quarter. Match the method to the environment first.
- Routing on the topic instead of the unknown. "Competitors" as a topic could mean five forces, a head-to-head comparison, or a switch interview; the unknown decides.
