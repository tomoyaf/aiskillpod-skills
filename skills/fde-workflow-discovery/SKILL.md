---
name: fde-workflow-discovery
description: Writes forward deployed engineer (FDE) style discovery notes for one customer or team workflow - shadowing and interview questions, the current steps as a swimlane table with actor, tool, time and pain, data in and out, exceptions, where AI fits and where it doesn't, a success metric, and a small pilot proposal. Use when someone is about to sit with a customer or internal team to find where AI can help, or asks for workflow discovery, process mapping, a current-state map, a shadowing guide, or an AI pilot proposal.
---

# FDE workflow discovery

Forward deployed engineers sit with a customer's team and make the product work inside their real systems and workflows. The discovery that comes first is the part anyone can do: watch the work as it happens, write down every step with its time and pain, and only then decide where AI fits. People describing their work from memory leave out the workarounds and exceptions that decide whether an AI pilot succeeds; watching them work catches those.

## When to use

- Before proposing an AI tool or agent for a customer's or your own team's process.
- When a team says "we want to use AI for X" and nobody has mapped X.
- After a pilot stalls, to find the steps that were missed.
- Not for scoring many tasks at once to pick a target (use automation-opportunity-scan first).

## What you need

- The workflow in one sentence, with a start and end trigger ("from invoice email received to invoice paid").
- Access to 2 to 3 people who do the work, ideally while they do it.
- Example inputs and outputs (forms, emails, files), with personal data removed.
- If you can't observe, run the questions as an interview and mark the map "[from interview, not observed]".

## Steps

1. **Bound the workflow.** Name the start trigger, end state, the people involved, and the volume (how many per week). One workflow per discovery; split if it branches into two jobs.
2. **Shadow first, ask during.** Watch real work for 30 to 60 minutes. Ask in the moment: "What are you looking for there?", "What happens if that field is blank?", "Where did you learn to do it this way?", "What do you do when this goes wrong?". Note workarounds: copy-paste, side spreadsheets, sticky notes, messages to a colleague.
3. **Map the current steps as a swimlane table.** One row per step: actor, step, tool, minutes per item, and pain (wait, rework, error, boredom). Order by time. Mark decision points ("if amount > $8,000 → manager").
4. **List data in and out.** For each step, what information goes in (from where, what format) and what comes out. Mark data that is personal, confidential, or regulated.
5. **Collect the exceptions.** What happens 1 time in 10 or 1 in 100: missing fields, unusual formats, disputes, urgent cases. Count them if you can. Exceptions usually take the most time and break naive automation.
6. **Mark where AI fits.** For each step: AI drafts or extracts and a person checks; AI does it alone; or stays human. Our default rule: AI alone only where the output is easy to check and a mistake is cheap to undo; anything touching money, legal terms, or a decision about a person keeps a human approval.
7. **Set one success metric and a pilot.** One metric with a baseline from the map (minutes per item, error rate, turnaround time). The pilot: one step or a few, 2 to 4 weeks, a small volume, a named owner on the customer side, what "go / stop" looks like.

## Output format

```markdown
# Workflow discovery — [workflow], [team / customer]
**Trigger → end:** [start] → [end] · **Volume:** [n per week] · **Observed:** [who, date] or [from interview]

## Swimlane: current state
| # | Actor | Step | Tool | Min/item | Pain |
|---|---|---|---|---|---|
| 1 | [role] | [step] | [tool] | [n] | [wait / rework / error / none] |

## Data in and out
| Step | In (source, format) | Out | Sensitive? |
|---|---|---|---|

## Exceptions
| Exception | How often | What happens now |
|---|---|---|

## Where AI fits
| Step | AI role | Human check | Why |
|---|---|---|---|
| [#] | drafts / extracts / does alone / none | [who checks] | [reason] |

## Success metric
[Metric]: baseline [n] → target [n]

## Pilot proposal
- Scope: steps [#] for [volume], [weeks]
- Owner (customer side): [name]
- Go if: [threshold] · Stop if: [threshold]

## Questions still open
- [question]
```

## Example

**Input:** "Shadowed Ravi (AP clerk at Corvel Foods) for an hour. Invoices arrive by email as PDFs (~120/week). Opening the email and saving the PDF takes him ~30 sec. He types supplier, amount, PO number into the ERP (about 4 min each); he calls it tedious and says typos slip in. The invoices carry supplier bank details. If no PO number, he emails the buyer (~2 min to write) and waits (~1 in 8 invoices, wait 1–2 days). Over $8k needs manager Leena's approval in the ERP. Some suppliers send scanned images, harder to read."

**Output:**

```markdown
# Workflow discovery — supplier invoice entry, Corvel Foods AP
**Trigger → end:** invoice email received → invoice approved in ERP · **Volume:** ~120 per week · **Observed:** Ravi, 1 hour

## Swimlane: current state
| # | Actor | Step | Tool | Min/item | Pain |
|---|---|---|---|---|---|
| 1 | AP clerk | Open email, download PDF | Email | 0.5 | none |
| 2 | AP clerk | Type supplier, amount, PO number into ERP | ERP | 4 | boredom, typos |
| 3 | AP clerk | If no PO: email buyer, wait | Email | 2 + 1–2 days wait | wait |
| 4 | Manager (Leena) | If > $8,000: approve | ERP | [check] | wait |

## Data in and out
| Step | In (source, format) | Out | Sensitive? |
|---|---|---|---|
| 2 | PDF or scanned image | ERP invoice record | supplier bank details: yes |
| 3 | Invoice without PO | Email to buyer | no |

## Exceptions
| Exception | How often | What happens now |
|---|---|---|
| Missing PO number | ~1 in 8 | Email buyer, wait 1–2 days |
| Scanned image instead of PDF | [check: count] | Harder to read |

## Where AI fits
| Step | AI role | Human check | Why |
|---|---|---|---|
| 2 | extracts fields into a review screen | Ravi confirms each | easy to check against the PDF; payment data needs a human |
| 3 | drafts the email to the buyer | Ravi sends | low risk, saves typing |
| 4 | none | Leena | approval of spend stays human |

## Success metric
Minutes per invoice for step 2: baseline 4 → target under 1.5

## Pilot proposal
- Scope: step 2 for 2 suppliers that send clean PDFs, 3 weeks
- Owner (customer side): Ravi, with Leena informed
- Go if: under 1.5 min/invoice and no more errors than today · Stop if: errors rise

## Questions still open
- How are typos caught today, and how many reach payment?
- Does the ERP accept imports, or must fields be typed?
```

## Checks before you send

- [ ] The workflow has one start trigger, one end state, and a weekly volume.
- [ ] Every swimlane row has an actor, a tool, and minutes, or "[check]".
- [ ] Exceptions are listed with how often they happen.
- [ ] Every step touching money, legal terms, or decisions about a person keeps a human check.
- [ ] The success metric has a baseline taken from the map.
- [ ] The pilot names a customer-side owner and go/stop thresholds.

## Common mistakes

- Mapping the official process from a document instead of the work as done. The workarounds are the real process.
- Proposing to automate the whole workflow. Pilot the one step with the clearest time cost and the easiest check.
- Ignoring the exceptions because they're rare. They decide whether people trust the pilot.
