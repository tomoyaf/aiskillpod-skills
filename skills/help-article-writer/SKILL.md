---
name: help-article-writer
description: Writes a help-center or knowledge-base article for one customer task, titled by the task, with the answer first, numbered steps that use the exact UI labels, screenshot placeholders, a troubleshooting section, and related articles. Use when someone asks for a help article, a support doc, a how-to guide, a knowledge-base page, or to turn a ticket answer, release note, or rough notes into an article customers can follow alone.
---

# Help article writer

A help article lets a customer finish one task without contacting support. They arrive from search, scan for their task, and follow steps with the product open beside the article. Title it by the task, put the answer first, and make every step one action with the label exactly as it appears on screen.

## When to use

- A question keeps coming up in tickets and the answer lives only in agents' replies.
- A feature shipped and customers need to know how to use it.
- An existing article is long, out of date, or written in internal words.
- Not for an FAQ list across many questions: use faq-from-tickets. Not for release notes: use release-notes.

## What you need

- The task the article covers, and who does it (any user, admins only, a specific plan).
- The real steps: the screens, buttons, and menu names as the product shows them. If you only have a description, write the steps and mark each unsure label "[check label]".
- Known problems: errors customers hit, from tickets or the product team.
- Optional: existing articles to link as related.

## Steps

1. **Title it by the task.** Start with a verb in the form customers search: "Export your contacts to CSV", "Add a teammate to your workspace". Not "Export feature" or "Understanding exports". One task per article; if the notes cover 2 tasks, write 2 articles.
2. **Answer in the first 2 sentences.** Say what the task does and the shortest path: "You can export contacts from **Contacts > Export**. The file arrives by email within a few minutes." Then who can do it and what they need first (role, plan, permission).
3. **Write numbered steps, one action each.** Start each step with the verb. Put UI labels in bold, exactly as shown, including capitals. Write menu paths as **Settings** > **Team**, with the arrows not bold. Give the location before the action: "In the top-right corner, click **Settings**." Keep it to 3 to 10 steps; if longer, split into sections with their own headings.
4. **Say what success looks like.** After the last step, one line on what the customer should see when it worked: a message, a file, a new item in a list.
5. **Mark screenshots where they help.** Add a placeholder after a step where the target is hard to find or the screen is busy, not after every step. Write what the screenshot shows, so it can be taken later and serves as alt text.
6. **Add troubleshooting from real problems.** Each item is the symptom in the customer's words as a heading, then the cause and fix in 1 to 3 sentences. Use only problems from tickets or the product team; don't invent errors.
7. **Link 2 to 4 related articles.** The next task they'll likely do, and the prerequisite. Use the articles' real titles if given; otherwise write "[related: topic]".

## Output format

```markdown
# [Verb-first task title]

[What this does and the shortest path, 1–2 sentences.]

**Who can do this:** [role / plan] · **Before you start:** [prerequisite, or remove]

## [Task, or first part of the task]
1. [Location], click **[Label]**.
2. [...]

![Screenshot: what it shows]

When it works, [what the customer sees].

## Troubleshooting
### [Symptom in customer words]
[Cause and fix, 1–3 sentences.]

## Related articles
- [Article title]
```

## Example

**Input:**

> Notes from product: admins can invite teammates from Settings → Team → "Invite people" button, type emails (comma separated), choose role Member or Viewer, then Send invites. Invite expires in 7 days. Tickets: people say invite email never arrived (usually spam folder, or wrong email); "Invite people" is greyed out for non-admins.

**Output:**

```markdown
# Invite a teammate to your workspace

You can invite teammates from **Settings** > **Team** > **Invite people**. They get an email with a link to join; the link works for 7 days.

**Who can do this:** workspace admins

## Send an invite
1. In the left menu, click **Settings**.
2. Click **Team**.
3. Click **Invite people**.
4. Type one or more email addresses, separated by commas.
5. Choose a role: **Member** or **Viewer**.
6. Click **Send invites**.

![Screenshot: the Invite people window with two emails typed and the role menu open]

When it works, each person appears in the Team list as "Invited" until they join.

## Troubleshooting
### The invite email never arrived
Ask them to check their spam or junk folder. If it isn't there, check the address in the Team list, then send the invite again.

### Invite people is greyed out
Only admins can invite. Ask a workspace admin to invite them, or to make you an admin.

## Related articles
- [related: change a teammate's role]
- [related: remove a teammate]
```

## Checks before you send

- [ ] The title starts with a verb and names one task.
- [ ] The first 2 sentences answer the question without the steps.
- [ ] Every step has one action, and every UI label is bold and matches the product or is marked "[check label]".
- [ ] The article says who can do it and what success looks like.
- [ ] Every troubleshooting item comes from tickets or the product team.
- [ ] No internal words (ticket, SKU, feature flag, backend) appear.

## Common mistakes

- Opening with background ("Teams are an important part of..."). The reader came for the steps.
- Writing "Navigate to the settings page and configure your team". Name each click.
- A screenshot after every step. It makes the page long and goes out of date with every UI change.
