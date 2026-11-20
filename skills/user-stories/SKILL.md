---
name: user-stories
description: Turns a feature idea or PRD section into user stories in the As a / I want / so that form, each with acceptance criteria written as Given/When/Then scenarios, edge cases, and out-of-scope notes, then checks every story against INVEST. Use when someone asks for user stories, tickets, acceptance criteria, a backlog breakdown, or "split this feature into stories" for Jira, Linear, or a sprint.
---

# User stories with acceptance criteria

A good story names who gains what and why, and its acceptance criteria say exactly how the team will know it's done. The "so that" clause is not decoration: if you can't write one, the story may not be worth building. Each story should be small enough to finish in one sprint and testable without asking the author.

## When to use

- After a PRD or feature brief is agreed and the work needs to go into a backlog.
- When a ticket exists but nobody can say when it's done.
- When a big feature has to be split before estimating.
- Not for deciding whether to build the feature: use prd-from-notes or feature-prioritization first.

## What you need

- The feature description, PRD section, or notes.
- The user types involved (customer, admin, guest). If missing, ask once; then use "user" and mark "[assumption: role]".
- Known rules and limits (permissions, plan limits, formats). Anything not given becomes an open question, not an invented rule.

## Steps

1. **List the roles and their goals.** For each role, write what they are trying to get done with this feature. One role per story; a story for "users and admins" is 2 stories.
2. **Write each story as As a / I want / so that.** Dan North describes this template as forcing the author to state the value. The "so that" names an outcome the user cares about, not a restated feature. If the honest "so that" is "because we said so", flag the story for descoping.
3. **Split by user-visible slices.** Split along workflow steps, business rule variants, data types, or happy path first and exceptions later. Never split by technical layer ("backend story", "frontend story"): each story must deliver something a user can try.
4. **Write acceptance criteria as Given/When/Then.** Given = the starting state. When = the one action. Then = the observable outcome. Join extra conditions with "And". Write 2 to 5 scenarios per story (our default): the happy path, at least 1 failure path, and any rule boundary.
5. **List edge cases.** Check each story against: empty data, very long input, duplicates, no permission, lost connection, the same action twice, and what happens to existing data. Each edge case either becomes a scenario or goes to out of scope.
6. **Write out-of-scope notes.** State what this story deliberately doesn't do, so reviewers don't expect it.
7. **Run the INVEST check.** Bill Wake's INVEST: Independent, Negotiable, Valuable, Estimable, Small, Testable. Mark each letter pass or fail. If Small fails, split again. If Testable fails, the acceptance criteria are too vague. If Independent fails, note the dependency.

## Output format

```markdown
# User stories: [feature]

## Story [n]: [short title]
**As a** [role], **I want** [capability], **so that** [outcome].

**Acceptance criteria**
- **Scenario: [name]**
  Given [starting state]
  When [action]
  Then [observable outcome]

**Edge cases**
- [case] → [covered by scenario x / out of scope]

**Out of scope**
- [what this story doesn't do]

**INVEST:** I [pass/fail] · N [pass/fail] · V [pass/fail] · E [pass/fail] · S [pass/fail] · T [pass/fail] — [note on any fail]

## Open questions
- [rule or limit not stated in the input]
```

## Example

**Input:** "Owners should be able to invite their accountant as a read-only user. Read-only users can't change anything. Owners can remove them."

**Output:**

```markdown
# User stories: Read-only seat for accountants

## Story 1: Invite a read-only user
**As an** account owner, **I want** to invite someone by email as read-only, **so that** my accountant can review my numbers without me exporting files.

**Acceptance criteria**
- **Scenario: Owner sends an invite**
  Given I am an account owner on the Team page
  When I enter an email address, choose "Read-only", and select Send invite
  Then the person receives an invite email
  And they appear in the team list as "Read-only, invited"
- **Scenario: Email already on the team**
  Given the email belongs to an existing team member
  When I send a read-only invite to it
  Then I see "This person is already on your team" and no invite is sent

**Edge cases**
- Invalid email format → shows an inline error, covered by the form's existing validation [assumption]
- Invite never accepted → out of scope (expiry is an open question)

**Out of scope**
- Changing an existing member's role to read-only.

**INVEST:** I pass · N pass · V pass · E pass · S pass · T pass

## Story 2: Read-only users can view but not change
**As an** accountant with read-only access, **I want** to see every page the owner sees, **so that** I can review the books without risk of changing them.

**Acceptance criteria**
- **Scenario: Viewing invoices**
  Given I am signed in as a read-only user
  When I open the Invoices page
  Then I see all invoices
  And no Create, Edit, or Delete buttons are shown
- **Scenario: Blocked change**
  Given I am signed in as a read-only user
  When I try to change an invoice through a saved link to its edit page
  Then I see "You have view-only access" and nothing is saved

**Edge cases**
- Export to CSV → open question: is exporting a "change"?

**Out of scope**
- Comments or notes from read-only users.

**INVEST:** I pass · N pass · V pass · E pass · S fail · T pass — touches every page; split by page group (invoices, clients, settings) if the estimate exceeds one sprint.

## Story 3: Remove a read-only user
**As an** account owner, **I want** to remove a read-only user, **so that** a former accountant loses access.

**Acceptance criteria**
- **Scenario: Owner removes access**
  Given a read-only user is on my team
  When I select Remove and confirm
  Then they are signed out within [check: how fast?] and can't sign in to this account
- **Scenario: Removed user tries to sign in**
  Given a read-only user has been removed
  When they try to sign in to this account
  Then sign-in is refused and they see none of the account's data

**Out of scope**
- Removal notifications to the removed person.

**INVEST:** I fail (needs Story 1) · N pass · V pass · E pass · S pass · T pass — depends on Story 1.

## Open questions
- Do invites expire? After how long?
- Can read-only users export data?
- How many read-only users per account?
```

## Checks before you send

- [ ] Every story has one role and a "so that" that names a user outcome.
- [ ] Every story has at least 1 failure-path scenario.
- [ ] Every Then is observable on screen or in data, not "works correctly".
- [ ] No rule, limit, or number appears that isn't in the input; missing ones are open questions.
- [ ] Each story has an INVEST line, and every fail has a note.
- [ ] No story is split by technical layer.

## Common mistakes

- "As a user, I want a button" stories. Name the outcome, not the control.
- Acceptance criteria that restate the story. Each scenario must be something a tester could fail.
- Hiding 3 features in one story's scenarios. If scenarios need different roles or screens, split.
