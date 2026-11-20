---
name: jtbd-switch-interview
description: Plans and synthesizes jobs-to-be-done switch interviews - an interview guide that walks a recent switcher back through their timeline (first thought, passive looking, active looking, deciding, first use), a timeline and four-forces summary per interview (push of the situation, pull of the new solution, anxiety of the new solution, habit of the present), and a job statement across interviews with the decisions it implies. Use when someone asks for jobs to be done interview questions, a switch interview script, a JTBD timeline, a forces of progress diagram, why customers switched to or away from a product, or what job customers hire the product for.
---

# Jobs-to-be-done switch interview

Jobs to be done says people don't buy products; they hire them to make progress in a particular circumstance, and that progress has functional, social, and emotional sides. Clayton Christensen and co-authors set out the idea most fully in "Know Your Customers' Jobs to Be Done" (Harvard Business Review, September 2016) and the book Competing Against Luck (2016). The switch interview is the field method that Bob Moesta and Chris Spiek of The Re-Wired Group teach: talk to someone who recently switched, replay the decision in order from the first thought to first use, and let the four forces of progress (push, pull, anxiety, habit) come out of the story. In Demand-Side Sales 101, Moesta treats selling as the buyer's timeline rather than a funnel. This skill turns that into a guide, a summary per interview, and a job statement the team can act on.

## When to use

- Before interviewing customers who recently bought, switched to a competitor, or cancelled.
- After 4 or more switch interviews, to find the job behind the switches.
- When a team argues about "why people buy" from opinions or survey answers.
- When win-loss notes say "price" or "features" and you suspect the real reason sits earlier.
- Not for general discovery interviews about a problem space (use interview-guide), and not for theming a large pile of mixed research notes (use user-interview-synthesis).

## What you need

- The switch to study: from what to what ("from spreadsheets to our tool", "from us to Competitor X", "from nothing to a first hire of a bookkeeper").
- Who to interview: people who made that switch in the last 30 to 90 days, plus anyone who nearly switched and stopped. If the user can't recruit recent switchers, say the memories will be weaker and mark the readout "[check: recall older than 90 days]".
- For synthesis: notes or transcripts per interview, with dates and quotes. If notes are summaries without quotes, say so and lower confidence.
- The decision the research should inform (positioning, onboarding, pricing, roadmap). If missing, ask once.

Never fill a timeline step or a force the person didn't describe. Write "[not covered]" and add the question to the next interview.

## Steps

1. **Pin the switch and the sample.** Write the switch as "from X to Y" and the recruiting rule: switched in the last 30 to 90 days, the person who made the decision, and a mix that includes near-switchers. The jobstobedone.org guidance is that patterns for one job often show within 5 to 8 interviews; plan at least that many before calling a pattern.
2. **Write the interview guide on the timeline.** Open with the documentary framing: "We're reconstructing what happened, like a film; small details matter and there are no wrong answers." Pin down when and where they bought as a memory anchor, then start at the first thought and move forward in order: first thought, passive looking, the event that started active looking, active looking, deciding, buying, first use, ongoing use. Ask for events, places, people, and dates, not opinions. Plan 45 to 90 minutes. If the user asks only for synthesis, leave the guide out of the output.
3. **Add probes for each force without naming the forces.** Push: "What was happening that made the old way stop working?" Pull: "What did you picture life looking like after?" Anxiety: "What almost stopped you?" Habit: "What did you like about the old way?" Add probes for the trade-off ("What did you give up to get this?") and for language ("What did you call it then?").
4. **After each interview, rebuild the timeline.** One row per stage with the date or rough time, what happened, and the triggering event that moved the person to the next stage. Keep their words in quotes. Mark missing stages "[not covered]".
5. **Sort what you heard into the four forces.** Push of the situation and pull of the new solution move the person toward the switch. Anxiety of the new solution and habit of the present hold them back. Each item is one concrete line with a quote or a fact from the notes. Note which side won and what tipped it.
6. **Write the job for each interview.** One sentence in our format: "When [circumstance], I want to [progress], so I can [outcome]; without [the anxiety that nearly stopped me]." Add the functional, social, and emotional sides if the notes show them.
7. **Compare across interviews.** Line up the per-interview jobs and forces. Group interviews whose circumstance and progress match; a different circumstance usually means a different job, even for the same product. Count how many interviews support each element, and keep the outliers visible.
8. **Write the cross-interview job statement and decisions.** One job statement per group with its supporting count, the forces that matter most, and 3 to 5 decisions: what to say (pull, in the customers' words), what to remove (anxiety), what event to watch for (the trigger), and what to stop building. Each decision names an owner or "[owner: to confirm]".

## Output format

```markdown
# Switch interviews: from [X] to [Y]
**Decision this informs:** [decision] · **Interviews:** [n] ([n] switched, [n] nearly switched) · **Dates:** [range]

## Interview guide
**Recruit:** [rule] · **Length:** [minutes]
**Opening:** [documentary framing script]
| Stage | Questions | Probes |
|---|---|---|
| First thought | [question] | [probe] |
| Passive looking | | |
| Event that started active looking | | |
| Active looking | | |
| Deciding | | |
| Buying and first use | | |
| Ongoing use | | |

## Interview [n]: [role, context] ([date])
### Timeline
| Stage | When | What happened | Their words |
|---|---|---|---|
### Four forces
| Toward the switch | Against the switch |
|---|---|
| **Push:** [item] | **Anxiety:** [item] |
| **Pull:** [item] | **Habit:** [item] |
**What tipped it:** [event or fact]
**Job:** When [circumstance], I want to [progress], so I can [outcome]; without [anxiety].

## Across interviews
| Element | Interviews supporting | Note |
|---|---|---|
**Job statement:** When [circumstance], I want to [progress], so I can [outcome]; without [anxiety]. ([n] of [n] interviews)
**Outliers:** [interview, what differs]

## Decisions
1. [Decision] — evidence: [interviews] — owner: [name]
## Gaps for the next interviews
- [question not covered]
```

## Example

**Input:** "Synthesize 4 switch interviews. Switch: small bookkeeping firms moving client document requests from email and shared spreadsheets to our portal, DocuNest. Decision: what our homepage should lead with. Notes:
A (owner, 6-person firm, signed 21 Sep): first thought in March when a client sent bank statements to the wrong staff member and a deadline was missed. Browsed tools in April after seeing a peer post on a forum, did nothing. Active looking started after the June tax deadline, 'I spent the whole week chasing PDFs.' Compared DocuNest and one rival; chose DocuNest because clients don't need a login and 'everything lands in one place, not in whoever's inbox.' Worry: 'my older clients won't use another app.' Liked that the spreadsheet was free and everyone knew it.
B (office manager, 9-person firm, signed 2 Oct): first thought before the June deadline, when staff spent days chasing clients for documents and a new hire couldn't tell which were outstanding. Active looking after the owner asked for a weekly status of missing documents. Wanted 'one list of what's missing per client.' Anxiety: moving 200 client folders. Habit: staff used email folders they'd built over years.
C (owner, 3-staff firm, nearly switched, stopped 12 Oct): first thought after the June deadline, same chasing problem. Trial looked good. Stopped because setup meant re-entering every client and the busy season started.
D (owner, 4-person firm, signed 1 Sep): wanted to look more professional to new clients; a client had commented that emailing tax documents felt unsafe. Chose DocuNest for the branded upload page."

**Output:**

```markdown
# Switch interviews: from email and spreadsheets to DocuNest
**Decision this informs:** what the homepage leads with · **Interviews:** 4 (3 switched, 1 nearly switched) · **Dates:** 1 Sep to 12 Oct

## Interview A: owner, 6-person firm (signed 21 Sep)
### Timeline
| Stage | When | What happened | Their words |
|---|---|---|---|
| First thought | March | Client's statements went to the wrong staff member; a deadline was missed | [not covered] |
| Passive looking | April | Saw a peer's forum post about tools; did nothing | [not covered] |
| Event that started active looking | After the June tax deadline | A week lost to chasing documents | "I spent the whole week chasing PDFs." |
| Active looking | [check: dates] | Compared DocuNest and one rival | [not covered] |
| Deciding | By 21 Sep | Chose DocuNest: clients upload without a login, and documents arrive in one place | "Everything lands in one place, not in whoever's inbox." |
| Buying and first use | [not covered] | [not covered] | |
| Ongoing use | [not covered] | [not covered] | |
### Four forces
| Toward the switch | Against the switch |
|---|---|
| **Push:** missed deadline; a week chasing PDFs | **Anxiety:** "my older clients won't use another app" |
| **Pull:** "everything lands in one place"; clients can upload without a login | **Habit:** the spreadsheet was free and everyone knew it |
**What tipped it:** the June deadline week.
**Job:** When a filing deadline is close and documents are scattered across inboxes, I want every client's documents in one place, so I can file on time; without making clients learn a new app.

## Interview B: office manager, 9-person firm (signed 2 Oct)
**Push:** days chasing clients before the June deadline; a new hire couldn't see what was outstanding. **Pull:** "one list of what's missing per client." **Anxiety:** moving 200 client folders. **Habit:** years of email folders. **Tipped by:** the owner asking for a weekly missing-documents status.
**Job:** When the team grows and no one can see what's outstanding, I want one list of missing documents per client, so I can report status without asking around; without a painful migration.

## Interview C: owner, 3-staff firm (nearly switched, stopped 12 Oct)
**Push:** the same June chasing problem. **Pull:** the trial looked good [check: which parts]. **Anxiety:** re-entering every client. **Habit:** [not covered]. **What won:** anxiety, as the busy season started.
**Job:** When a deadline has just gone by in chasing documents, I want to stop chasing clients for them, so I can file on time; without re-entering every client.

## Interview D: owner, 4-person firm (signed 1 Sep)
**Push:** a client said emailing tax documents felt unsafe. **Pull:** a branded upload page. **Anxiety:** [not covered]. **Habit:** [not covered]. **Job:** When new clients judge us on first contact, I want a professional, safe way to collect documents, so I can win their trust. (Different circumstance: likely a second job.)

## Across interviews
| Element | Interviews supporting | Note |
|---|---|---|
| Push: chasing documents before a deadline | A, B, C (3 of 4) | Peaks after the June deadline |
| Pull: one place / one list of what's missing | A, B (2 of 4) | |
| Anxiety: client adoption or migration effort | A, B, C (3 of 4) | Stopped C |
| Habit: free, familiar spreadsheet or email folders | A, B (2 of 4) | |
**Job statement:** When a filing deadline is close and client documents are scattered, I want one list of what each client still owes and one place for it to arrive, so I can file on time; without making clients learn an app or re-entering every client. (3 of 4 interviews; provisional, since 4 interviews is below the 5 to 8 a pattern needs)
**Outliers:** D hires DocuNest to look professional and safe to new clients.

## Decisions
1. Lead the homepage with deadline-week chasing and "one list of what each client still owes", not features — evidence: A, B, C — owner: [owner: to confirm]
2. Put "clients upload without a login" and client-list import next to the main call to action to answer the two anxieties — evidence: A, B, C — owner: [owner: to confirm]
3. Time outreach for the weeks after a tax deadline, when A started looking actively and C first thought of switching — evidence: A, C — owner: [owner: to confirm]
4. Test a second page for the "professional and safe" job before acting on one interview — evidence: D — owner: [owner: to confirm]

## Gaps for the next interviews
- Sample: 4 interviews is below the 5 to 8 a pattern needs; confirm this job in 1 to 4 more.
- Recall: the notes don't give interview dates [check: recall older than 90 days].
- First use and ongoing use: not covered in any interview.
- Passive looking for B, C, D.
- Anxiety and habit for D, and habit for C.
- More near-switchers like C, to size the migration anxiety.
```

## Checks before you send

- [ ] Every interviewee switched (or nearly switched) in the last 30 to 90 days, or the readout says otherwise.
- [ ] Each timeline is in order, and every stage holds an event from the notes or "[not covered]".
- [ ] Each force item traces to a quote or a fact in the notes; none are inferred from the product's features.
- [ ] Anxiety and habit are filled in, not only push and pull.
- [ ] The job statement names a circumstance, not a demographic, and gives its supporting count.
- [ ] Outliers are kept, not averaged away.
- [ ] Decisions have evidence and an owner, and gaps become next questions.

## Common mistakes

- Asking "why did you buy?" and writing down the rationalized answer. Replay the events and the reason shows up in the story.
- Interviewing only happy customers. Near-switchers show the anxiety and habit that stop most buyers.
- Writing the job as a product feature ("I want an upload portal"). The job is the progress, in the customer's circumstance.
- Merging different circumstances into one job. Two triggers usually mean two jobs and two messages.
- Stopping at a nice diagram. The output is what to say, what to remove, and when to show up.
