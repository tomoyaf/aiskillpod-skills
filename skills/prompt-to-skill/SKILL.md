---
name: prompt-to-skill
description: Turns a prompt or chat that worked well into a reusable SKILL.md a team can share - a valid name, a description that says what it does and when to use it, inputs, numbered steps with decision rules, an output template, a worked example, and checks - following the Agent Skills format. Use when someone says "save this as a skill", "make this reusable", "turn my prompt into a skill", wants to share a prompt with their team, or asks how to write a SKILL.md for Claude, ChatGPT, or a coding agent.
---

# Prompt to skill

A good prompt lives in one person's chat history; a skill lets the whole team get the same result. The Agent Skills format is a folder with a SKILL.md: front matter with a `name` and a `description`, then instructions. The AI reads only the name and description until a task matches, so the description decides whether the skill is ever used, and the body only needs what the AI wouldn't do by default.

## When to use

- A prompt or conversation produced a result someone wants again.
- Several people on a team write their own version of the same prompt.
- Converting a long "prompt template" doc into something an AI can pick up on its own.
- Not for one-off questions, or tasks the AI already does well with a one-line request.

## What you need

- The prompt, or the conversation where it worked, including the corrections you gave along the way. The corrections are the valuable part.
- 1 to 2 examples of output you were happy with.
- Who will use the skill and in which tools. If unknown, write for any AI and avoid tool-specific features.

## Steps

1. **Find the reusable part.** Separate what's fixed (the procedure, format, rules, corrections you gave) from what changes each time (the inputs). The changing parts become "What you need".
2. **Name it.** Lowercase letters, numbers, and hyphens, 64 characters or fewer, matching the folder name; no "claude" or "anthropic". Prefer what it does: `weekly-client-report`, `processing-invoices`. Avoid vague names (`helper`, `utils`).
3. **Write the description.** Third person, under 1,024 characters, no XML tags. Say what it does, then "Use when..." with the words a user would actually type ("recap", "follow-up", "minutes"). This is what the AI matches against; vague descriptions ("Helps with documents") never trigger.
4. **Write the steps.** Numbered, each with a short name and a concrete rule. Keep only instructions that change the output: the corrections you made in the chat, thresholds, "if X, do Y" decisions. Cut explanations the AI already knows.
5. **Add the output template and one example.** A fenced template with [placeholders], then one realistic input and its full output. One concrete example teaches format better than paragraphs of description.
6. **Add checks.** 4 to 7 verifiable checks the AI runs before answering ("Every action item has an owner"), not wishes ("is high quality").
7. **Test it on fresh inputs.** Run it in a new chat on 3 different real inputs, including one awkward case. Fix what it got wrong in the skill, then run again. Keep the body under 500 lines; ours aim for well under 200.

## Output format

````markdown
---
name: [lowercase-hyphenated-name]
description: [What it does, third person]. Use when [situations and the words users type].
---

# [Title]

[1–3 sentences: what good output achieves and the principle behind it.]

## When to use
- [Situation]
- Not for [nearby task it shouldn't handle].

## What you need
- [Input] — if missing, [ask once / proceed and mark "[assumption]"].

## Steps
1. **[Step name].** [Concrete instruction with a decision rule.]

## Output format
```markdown
[Template with [placeholders]]
```

## Example
**Input:** [realistic input]
**Output:** [full output]

## Checks before you send
- [ ] [Verifiable check]
````

## Example

**Input:** "I keep pasting this into ChatGPT: 'Here are my notes from a customer call. Write a follow-up email: thank them, recap what we agreed, list next steps with dates, under 150 words, no buzzwords, end with one clear question.' I usually have to remind it to use the customer's own words and not invent dates."

**Output:**

````markdown
---
name: call-follow-up-email
description: Writes a short follow-up email after a customer call from rough notes - thanks, a recap of what was agreed, next steps with owners and dates, and one closing question, under 150 words. Use when someone shares call notes and asks for a follow-up email, a recap email, or "send them a summary".
---

# Call follow-up email

A follow-up confirms what was agreed while the call is fresh, so nothing drifts. Keep it short, in the customer's own words, and end with one question that moves things forward.

## When to use
- After a sales or customer call, from notes or a transcript.
- Not for a cold email to someone you haven't spoken to.

## What you need
- The call notes. If dates for next steps are missing, write "date to confirm" instead of inventing one.
- The customer's name and company.

## Steps
1. **Recap only what was agreed.** Use the customer's own words for their goals and terms.
2. **List next steps.** Each with an owner and a date from the notes, or "date to confirm".
3. **End with one question.** The single answer you need to move forward.
4. **Cut to 150 words.** No buzzwords; one idea per sentence.

## Output format
```markdown
Subject: [Company] — next steps from [day]'s call

Hi [name],

Thanks for [specific thing]. To recap, we agreed [1–2 lines].

Next steps:
- [Owner]: [step] by [date or "date to confirm"]

[One question]?

[Signature]
```

## Example
**Input:** "Call with Ines at Portwell. They want to cut onboarding time. Agreed to a 2-week pilot. I send the pilot plan Friday. Need to know who their admin is."
**Output:**
Subject: Portwell — next steps from today's call
Hi Ines, thanks for walking me through your onboarding process. To recap, we agreed on a 2-week pilot focused on cutting onboarding time.
Next steps:
- Me: send the pilot plan by Friday
- Portwell: name an admin for the pilot, date to confirm
Who should I set up as your admin?

## Checks before you send
- [ ] Under 150 words.
- [ ] Every date comes from the notes or says "date to confirm".
- [ ] Ends with exactly one question.
- [ ] Uses the customer's terms, not ours.
````

## Checks before you send

- [ ] The name is lowercase with hyphens, 64 characters or fewer, and has no "claude" or "anthropic".
- [ ] The description is third person, says what it does, includes "Use when", and is under 1,024 characters with no XML tags.
- [ ] Every correction from the original chat appears as a step or a check.
- [ ] The skill has an output template and one full worked example.
- [ ] It was tested on 3 fresh inputs, and the fixes went into the skill.

## Common mistakes

- Copying the prompt in as-is. Turn reminders you had to give ("don't invent dates") into steps; that's what the skill adds.
- Explaining things the AI knows ("an email is a message..."). Every line costs context; keep the ones that change the output.
- A description that says what but not when. The AI can't pick a skill it can't match to the request.
