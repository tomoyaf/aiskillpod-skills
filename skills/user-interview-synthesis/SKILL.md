---
name: user-interview-synthesis
description: Synthesizes several user interview transcripts or notes into atomic observations, affinity themes with counts across participants, supporting quotes, jobs-to-be-done, insights separated from assumptions, and recommendations with a confidence level. Use when someone shares customer interview notes, research call transcripts, or discovery calls and asks what users said, for themes, patterns, insights, or a research readout.
---

# User interview synthesis

A synthesis is useful when a reader can see how many people said a thing, in their own words, and how sure the team should be. Count participants, not mentions. Keep what users did apart from what they said they would do, and never let one loud interview become a theme.

## When to use

- After 3 or more user interviews, discovery calls, or usability sessions.
- When the team asks "what did we learn?" or needs a readout before a decision.
- Not for one interview: use call-summary-crm-notes or meeting-minutes. Not for support tickets or survey comments at volume: use feedback-themes.

## What you need

- Transcripts or notes, one per participant, with a participant label (P1, P2 or a pseudonym).
- The research question the interviews were meant to answer. If missing, ask once; if still missing, infer it and mark "[assumption: research question]".
- Optional: each participant's segment (role, company size, plan), so you can split themes by segment.

## Steps

1. **Extract atomic observations.** One observation = one fact about one participant: something they did, felt, said, or used. Tag each with the participant and whether it is behavior ("did"), opinion ("said"), or a request ("wants"). Past behavior is the strongest signal; requests are the weakest.
2. **Group into themes.** Use affinity diagramming as NN/g describes it: group by content first, name the group afterward, don't force a fixed number of clusters, and let an observation sit in 2 clusters when it fits both. Cluster observations that describe the same underlying need or pain. Name each theme as a statement from the user's side ("Owners check cash daily from their phone"), not a topic ("Mobile").
3. **Count participants per theme.** Write "5 of 8 participants". Our rule: a theme needs at least 2 participants; single-participant observations go under "Worth watching". If a theme comes from one segment only, say so.
4. **Pick quotes.** 1 to 2 verbatim quotes per theme, attributed to the participant label. Quote exact words; if the notes are paraphrased, label them "(paraphrase)".
5. **Write jobs-to-be-done.** A job is the progress a person is trying to make in a particular situation (Christensen Institute); include functional, social, and emotional sides when the data shows them. For the top themes: "When [situation], I want to [motivation], so I can [outcome]." Base each on observed behavior, not on feature requests.
6. **Separate insights from assumptions.** An insight is supported by behavior from 2 or more participants. Anything the team believed before the interviews that the data didn't test stays an assumption. List contradicting evidence openly.
7. **Recommend with confidence.** Each recommendation links to themes, names an owner if the user gave one, and gets a confidence level on our default scale: High (behavior from half or more of participants), Medium (several participants, mostly said not did), or Low (few participants or one segment). Add what research would raise the confidence.

## Output format

```markdown
# Interview synthesis: [research question]

**Participants:** [n] ([segments]) · **Dates:** [range] · **Interviewer(s):** [names]

## Top findings
1. [Theme statement] — [x of n]
2. [Theme statement] — [x of n]
3. [Theme statement] — [x of n]

## Themes
### [Theme statement] — [x of n participants]
- **Evidence:** [observations, tagged did/said/wants, with participant labels]
- **Quotes:** "[quote]" — [P#]
- **Segments:** [all, or which]

## Jobs to be done
- When [situation], I want to [motivation], so I can [outcome]. ([themes])

## Insights vs. assumptions
| Statement | Status | Evidence |
|---|---|---|
| [statement] | Insight / Assumption / Contradicted | [participants and type] |

## Recommendations
| Recommendation | Based on | Confidence | To raise confidence |
|---|---|---|---|
| [action] | [themes] | High / Medium / Low | [next research] |

## Worth watching
- [single-participant observation] — [P#]
```

## Example

**Input (summarized notes, 4 interviews on invoice follow-up):**

> P1 (agency owner): chases late invoices every Friday from a spreadsheet. "I hate being the bad guy."
> P2 (freelancer): sends reminders by text from her phone, not email. Wants auto reminders.
> P3 (agency owner): has a bookkeeper chase invoices. Didn't know who was late until month end.
> P4 (freelancer): copy-pastes the same reminder email; "I soften it every time so it doesn't sound rude."

**Output:**

```markdown
# Interview synthesis: How do small service businesses follow up on late invoices?

**Participants:** 4 (2 agency owners, 2 freelancers) · **Dates:** [dates] · **Interviewer(s):** [names]

## Top findings
1. Following up feels socially awkward — 2 of 4
2. Follow-up is manual and repeated — 3 of 4

## Themes
### Following up feels socially awkward — 2 of 4
- **Evidence:** P1 did: chases weekly, said dislikes being "the bad guy". P4 did: rewrites the tone each time.
- **Quotes:** "I hate being the bad guy." — P1; "I soften it every time so it doesn't sound rude." — P4
- **Segments:** both

### Follow-up is manual and repeated — 3 of 4
- **Evidence:** P1 did: spreadsheet every Friday. P2 did: texts from phone. P4 did: copy-pastes one email.
- **Quotes:** "I soften it every time" — P4
- **Segments:** both

## Jobs to be done
- When a client is late, I want the reminder sent in a polite tone without me writing it, so I can get paid without straining the relationship. (themes 1, 2)

## Insights vs. assumptions
| Statement | Status | Evidence |
|---|---|---|
| Follow-up is repeated manual work | Insight | P1, P2, P4 (did) |
| Users want automatic reminders | Assumption | P2 only (wants) |
| Email is the right channel | Contradicted | P2 uses text messages |

## Recommendations
| Recommendation | Based on | Confidence | To raise confidence |
|---|---|---|---|
| Test pre-written polite reminder templates | Themes 1, 2 | High | 4 more interviews; watch whether users edit the template |
| Explore text reminders before building more email features | Theme 2 (P2 texts) | Low | Ask 5 freelancers which channel they used last time |

## Worth watching
- No live view of who is late until month end — P3
```

## Checks before you send

- [ ] Every theme shows "x of n participants" and has at least 2 participants.
- [ ] Every quote is verbatim and attributed, or labeled "(paraphrase)".
- [ ] Each observation is tagged did, said, or wants.
- [ ] Every recommendation names its themes and a confidence level.
- [ ] Nothing appears that isn't in a transcript or note; no invented participants or numbers.
- [ ] Contradicting evidence is shown, not dropped.

## Common mistakes

- Counting mentions instead of people. One participant saying "export" 9 times is 1 of n.
- Treating feature requests as needs. Ask what the person was trying to do when they asked.
- Writing themes as topics ("Pricing"). A theme says something that could be wrong.
