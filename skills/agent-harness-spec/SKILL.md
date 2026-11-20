---
name: agent-harness-spec
description: Writes a one-page harness spec for an AI agent before a team lets it run a multi-step job - the goal and the test for done, the tools it may use and their limits, the files it reads and the progress notes it keeps between sessions, how it works in small steps, when it stops, which actions wait for a person, and what gets logged. Use when someone plans an AI agent, an automation that runs on its own, a long task in Claude Code, Codex or a similar agent, or asks why their agent drifts, loops, forgets earlier work or declares a job done too early.
---

# Agent harness spec

A harness is everything around the model that turns it into an agent: the instructions it starts with, the tools it can call, the files and notes it reads, the loop that runs it, and the rules for stopping and asking a person. Anthropic's engineering team describes its Claude Agent SDK as a general-purpose agent harness, and its write-up on long-running agents found two common failures: the agent tries to do everything at once and runs out of context halfway, or a later session sees some progress and declares the job done. Their fixes were in the harness, not the model: a first session that sets up a feature list and a progress file, then sessions that each finish one item, record it, and leave things in a clean state. This skill writes those decisions down before the agent runs, in words a non-engineer owner can check.

## When to use

- Planning an AI agent or an automation that takes several steps without a person between them.
- Handing a long task to Claude Code, Codex, Cursor or another coding or research agent.
- An agent keeps drifting, looping, forgetting what it did, or calling a job done that isn't.
- Not for the assistant's wording and tone (use context-engineering-brief) or for testing results at scale (use eval-set-builder).

## What you need

- The job in one or two sentences, and who asked for it.
- The tools or systems the agent would touch (email, CRM, files, code, web).
- What "done" looks like, as checkable items if possible.
- What must never happen (sending to customers, deleting data, spending money).
- Who will watch it and how much of their time it may take.

## Steps

1. **Write the goal and the done test.** One sentence of goal, then a numbered list of items that are each pass or fail ("Each of the 40 product pages has a price and a photo"). The agent may change an item's status, never its wording or the list's length.
2. **List the tools and their limits.** For each tool: what the agent uses it for, read or write, and a limit (which folder, which mailbox, how many per run). Remove any tool the goal doesn't need. Two tools that do the same thing confuse the agent; keep one.
3. **Set the memory files.** Name the files the agent reads at the start of every session and writes at the end: the done list, a progress note (what was finished, what is next, what went wrong), and where its work is saved. A new session starts from these, not from memory.
4. **Make it work in small steps.** One item per step: read the progress note, pick the next open item, do it, check it, record it. No step starts a second item before the first is recorded.
5. **Write the stop rules.** Stop when every item passes; when the same item fails 3 times; when a limit from step 2 would be crossed; when time or cost passes a cap you set. On stopping, the agent writes why in the progress note.
6. **Mark the human gates.** List the actions that wait for a named person's approval: anything sent outside the team, deleted, paid, published or merged. Say how the agent asks (a message, a comment, a draft left for review).
7. **Decide what gets logged.** Each step leaves a line: time, item, tool calls, result. The owner can read the log in five minutes and see what happened.
8. **Run a short pilot.** Start with 3 to 5 items, read every step's log, fix the spec, then let it run on the rest.

## Output format

```markdown
# Harness spec: [agent name]

**Goal:** [one sentence] · **Owner:** [name] · **Asked by:** [name]

## Done when
1. [Pass/fail item]

## Tools
| Tool | Used for | Read/Write | Limit |
|---|---|---|---|

## Memory files
- Done list: [file] — the agent updates status only
- Progress note: [file] — finished, next, problems
- Work saved to: [place]

## Each step
Read the progress note → pick the next open item → do it → check it → record it.

## Stop when
- [Condition] → [what the agent writes]

## Waits for a person
- [Action] → [who approves, how the agent asks]

## Log
[Where, and what each line holds]

## Pilot
[First items, who reads the log, when]
```

## Example

**Input:** "We want an agent to update the 40 product pages on our Shopify store from the new supplier price sheet, and email the supplier if a product is missing from the sheet. I'm the ops lead; I can check it for 15 minutes a day."

**Output:**

```markdown
# Harness spec: price sheet updater

**Goal:** Every product page shows the supplier's new price from the November sheet. · **Owner:** Ops lead · **Asked by:** Ops lead

## Done when
1. Each of the 40 products has the sheet's price on its page (one line per product in done-list.md).
2. Each product missing from the sheet is listed in missing.md with its SKU.

## Tools
| Tool | Used for | Read/Write | Limit |
|---|---|---|---|
| Spreadsheet | Read the November price sheet | Read | That one file |
| Shopify | Update a product's price | Write | Price field only; no other fields |
| Email | Draft a note to the supplier | Write | Drafts only; never sends |

## Memory files
- Done list: done-list.md — the agent changes "open" to "done" or "failed", nothing else
- Progress note: progress.md — finished, next, problems
- Work saved to: Shopify; drafts in the ops mailbox

## Each step
Read progress.md → take the next open product → update its price → reload the page and compare with the sheet → record it.

## Stop when
- All 40 lines are done or failed → summary at the top of progress.md.
- A product fails 3 times → mark failed with the error, move on.
- A new price is more than 30% off the old one → stop and ask.

## Waits for a person
- The supplier email → the agent leaves a draft; the ops lead sends it.
- Any price change over 30% → the agent asks in progress.md and waits.

## Log
log.md: time, SKU, old price, new price, result.

## Pilot
First 5 products; the ops lead reads log.md and the 5 pages, then lets it run on the rest.
```

## Checks before you send

- [ ] The done test is a list of pass/fail items the agent can't rewrite.
- [ ] Every tool has a purpose, read or write, and a limit; unneeded tools are gone.
- [ ] The agent reads and writes a progress note every session.
- [ ] Stop rules cover success, repeated failure, crossed limits and a time or cost cap.
- [ ] Sending, deleting, paying and publishing wait for a named person.
- [ ] A pilot of a few items comes before the full run.

## Common mistakes

- A vague goal ("clean up the store") with no list of done items, so the agent decides when it's finished.
- Giving the agent every tool "just in case". More tools mean more wrong choices.
- No progress note, so each new session starts over or repeats work.
- Letting the agent edit its own done list or tests to make them pass.
