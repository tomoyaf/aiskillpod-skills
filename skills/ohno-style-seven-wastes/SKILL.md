---
name: ohno-style-seven-wastes
description: Walks one process step by step and sorts what it finds into Taiichi Ohno's seven wastes as the Lean Enterprise Institute defines them - overproduction, waiting, conveyance, processing, inventory, motion, correction - plus value-creating and incidental work, then ranks the wastes and proposes kaizen steps, starting with overproduction, which feeds the other six. Works for offices and services as well as factories. Use when a process feels slow or expensive, before automating a process, when lead time must come down, or when someone asks for a waste walk, a lean review, muda, or "where does the time go".
---

# Ohno-style seven wastes review

These are principles Taiichi Ohno described publicly in his work on the Toyota Production System, as the Lean Enterprise Institute's lexicon summarises them, and as Toyota describes the system. Not affiliated with or endorsed by Taiichi Ohno or their companies. The skill goes through a process one step at a time, labels each step as value-creating work, incidental work or one of the seven wastes, and proposes what to remove first.

## Ground rules

- Do not attribute quotes or opinions to Taiichi Ohno beyond the cited sources.
- Do not role-play, imitate, or write in the voice of Taiichi Ohno; review the user's material against the principles below.
- Waste is in the process, not in the people. Never label a person as waste.
- Use the user's own timings and counts; mark anything estimated "[estimate]" and anything missing "[check: ...]".
- Translating the wastes to office work is our adaptation; say so in the output.

## The principles

1. **The seven wastes.** Ohno's categorisation of the seven major wastes found in mass production: overproduction (producing ahead of what the next process or customer needs), waiting, conveyance (moving things unnecessarily), processing (unnecessary or incorrect processing), inventory (more than the minimum stock a pull system needs), motion (unnecessary or straining movement, such as looking for tools or documents) and correction (inspection, rework, scrap). Source: Lean Enterprise Institute lexicon, "7 Wastes".
2. **Overproduction is the worst.** It contributes to the other six. Source: same entry.
3. **See work before waste.** Work splits into value-creating work, incidental work (needed now but not valuable to the customer) and waste (creates no value and can be removed). Source: same entry.
4. **Eliminate waste, shorten lead time.** Toyota describes its production system as aiming to eliminate waste thoroughly and shorten lead times, and credits Ohno with helping establish it. Source: Toyota, "Toyota Production System".

## When to use

- A process that takes too long or costs too much: order to delivery, quote to contract, hire to first day, ticket to resolution.
- Before automating something, so you don't automate waste.
- A team that is busy all day but output doesn't rise.
- Not for finding the root cause of one incident (use ohno-style-five-whys) or for scanning a whole company for automation (use automation-opportunity-scan).

## What you need

- The process, from its trigger to its end, as the work is really done (not as the manual says).
- For each step: who does it, how long it takes, how long work waits before it, and how many items are in it.
- How much the customer or next step actually needs, and when.
- Any defect, rework or return counts.

## Steps

1. **Draw the process.** One row per step, from trigger to end, with time spent working and time waiting before it. Add the total lead time and the total working time.
2. **Label every step (principle 3).** Value-creating (the customer would pay for it), incidental (needed now, not valuable in itself), or waste. Be strict: approvals, re-keying and searching are rarely value-creating.
3. **Name the waste type (principle 1).** For each waste step, pick one of the seven. Office translations we use: overproduction = reports or work done before anyone asked; waiting = queues for approval or information; conveyance = handing files between tools or people; processing = extra fields, extra formatting, gold-plating; inventory = backlogs and work in progress; motion = searching, switching windows, walking; correction = rework, fixes, re-sends.
4. **Look for overproduction first (principle 2).** What gets made before it is needed? It usually causes inventory, waiting and correction downstream.
5. **Measure the size.** For each waste: time per item, items per week, and the share of lead time. Rank by size.
6. **Propose kaizen steps (principle 4).** For the top three wastes, one change each that removes it (not one that makes it faster). State the expected change in lead time, from the user's numbers.
7. **Pick a first test.** One change, one week, one measure of lead time before and after.

## Output format

```markdown
# Seven wastes review: [process]
These are principles Taiichi Ohno described publicly. Not affiliated with or endorsed by Taiichi Ohno or their companies. The office translations of the wastes are our adaptation.

## Summary
Lead time [x], working time [y] ([z]% of lead time). Biggest waste: [type, step]. First test: [change].

## The process
| # | Step | Who | Work time | Wait before | Label | Waste type |
|---|---|---|---|---|---|---|

## Wastes ranked
| Rank | Waste type | Where | Time per item | Items per week | Share of lead time |
|---|---|---|---|---|---|

## Kaizen steps
| Waste | Change that removes it | Expected effect | Owner |
|---|---|---|---|

## First test
[One change, one week, the measure]

## Principles used
[Numbered, with sources]
```

## Example

**Input:** "Our quote process at a printing company: sales takes the request by email (10 min), types it into the estimating sheet (15 min), waits for the estimator (usually 1 day), estimator prices it (20 min), sales re-types it into a quote template (15 min), manager approves (waits half a day, 2 min), sales sends it. About 1 in 5 quotes goes back for corrections. We also price every option for every job in case they ask. 60 quotes a week."

**Output (excerpt):**

```markdown
These are principles Taiichi Ohno described publicly. Not affiliated with or endorsed by Taiichi Ohno or their companies. The office translations of the wastes are our adaptation.

## Summary
Lead time about 1.5 working days; working time about 62 minutes. Biggest waste: waiting for the estimator. Overproduction: pricing every option in case it is asked for. First test: price only the options the customer requested, for one week.

## The process
| # | Step | Who | Work time | Wait before | Label | Waste type |
|---|---|---|---|---|---|---|
| 1 | Take the request by email | Sales | 10 min | - | Value-creating | - |
| 2 | Type it into the estimating sheet | Sales | 15 min | - | Waste | Conveyance (re-keying between tools) |
| 3 | Estimator prices the job | Estimator | 20 min | 1 day | Value-creating | Waiting (the day before it) |
| 4 | Price every option, asked or not | Estimator | [check: minutes] | - | Waste | Overproduction |
| 5 | Re-type into the quote template | Sales | 15 min | - | Waste | Conveyance |
| 6 | Manager approves | Manager | 2 min | half a day | Incidental | Waiting |
| 7 | Corrections on 1 in 5 quotes | Sales, estimator | [check] | - | Waste | Correction |
```

## Checks

- [ ] The attribution and not-affiliated lines are in the output.
- [ ] Every step is labelled value-creating, incidental, or a named waste.
- [ ] Overproduction was looked for first.
- [ ] Sizes come from the input or are marked [estimate] or [check].
- [ ] Each proposed change removes a waste rather than speeding it up.
- [ ] One first test with a before-and-after measure.

## Common mistakes

- Speeding up a wasteful step (a faster re-keying macro) instead of removing it.
- Calling every approval waste; some are incidental work that is still needed.
- Ignoring waiting because nobody is "doing" anything during it; in most office processes it is most of the lead time.
