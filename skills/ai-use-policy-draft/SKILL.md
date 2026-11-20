---
name: ai-use-policy-draft
description: Drafts a short, plain-language company AI use policy - approved tools, data that must never be pasted into AI tools, when a person must review AI output, when to disclose AI use, who owns the policy and approves new tools - and flags every point that needs legal review. Use when a founder, ops lead, or manager asks for an AI policy, AI acceptable use policy, ChatGPT policy, generative AI guidelines for staff, or rules for using AI at work.
---

# AI use policy draft

> Not legal advice. This is a first-pass draft to prepare for a lawyer's review; it doesn't replace one.

A policy people follow fits on 2 pages and answers 4 questions: which tools, what data never goes in, when a human checks the output, and who to ask. The UK's National Cyber Security Centre advises against putting sensitive information into public AI tools, because the provider can see queries and may use them to develop its service. So the core of the policy is a short, concrete list of data classes, with examples, and an approved-tools list that says which tools have business terms.

## When to use

- A company or team has people using ChatGPT, Claude, Gemini, or Copilot without rules.
- Before rolling out an AI tool company-wide.
- A customer or investor asks "do you have an AI policy?".
- Not for a full AI governance or risk management program, and not for customer-facing AI product terms: those need legal and security specialists.

## What you need

- The AI tools in use or planned, and whether each is on a business plan or personal accounts.
- What data the company handles: customer data, health or financial data, source code, contracts, employee data.
- Any regulations or customer contracts that restrict data use. Never guess these; if unknown, mark "[check: legal]".
- Who will own the policy (a person) and who approves new tools.

## Steps

1. **State the purpose in 2 sentences.** Encourage use, protect data and customers. Say it applies to all staff and contractors, on any device, for work tasks.
2. **List approved tools.** Tool, plan, approved uses, and whether data entered is used for training under the company's account settings [check: vendor terms for each]. Everything not listed is not approved for company data. Say how to request a new tool.
3. **Define data classes with examples.** Our default 3 classes. Never enter: passwords and keys, customer or employee personal data, health or financial account data, unreleased financials, contracts and legal matters, anything a customer contract restricts. Approved tools only: internal documents, non-public plans, source code [check: legal and security]. Any tool: public information and your own writing with nothing confidential. Give 2 to 3 examples per class from this company's work.
4. **Set review rules.** A person checks AI output before it is sent outside the company, published, used in a decision about a person (hiring, performance, pay), or used for legal, financial, medical, or security matters. The person who uses it is responsible for it. Facts, numbers, quotes, and citations are verified against a source.
5. **Set disclosure rules.** When to tell customers or readers that AI was used: our default is chatbots and automated replies say so, and content that's materially AI-generated is disclosed where a customer contract, platform rule, or law requires it [check: legal for your markets]. Don't present AI output as a named person's personal work where that would mislead.
6. **Name owners and the update cycle.** A policy owner (a person), who approves tools, where to report a mistake or a data leak and how fast, and a review date. Our default: every 6 months, because tools and terms change.
7. **Flag legal review.** List every point that depends on law, contracts, or vendor terms with "[check: legal]": data protection, sector rules, customer contract clauses, IP ownership of outputs, employee monitoring, and disclosure requirements.

## Output format

```markdown
# [Company] AI use policy
*Draft for legal review. Not legal advice. Version [n], [date]. Owner: [name].*

## Why this policy
[2 sentences]

## Approved tools
| Tool | Plan | Approved for | Data used for training? |
|---|---|---|---|
| [tool] | [business / enterprise] | [uses] | [no / check: vendor terms] |
Anything not listed: not approved for company data. Request a tool: [how].

## What you can put in
| Never | Approved tools only | Any tool |
|---|---|---|
| [examples] | [examples] | [examples] |

## Check before you use it
- [Review rules]

## Telling people AI was used
- [Disclosure rules]

## If something goes wrong
Report to [person/channel] within [time]: [what to report].

## Owners
- Policy owner: [name] · Tool approvals: [name] · Next review: [date]

## Points for legal review
- [ ] [Point] [check: legal]
```

## Example

**Input:** "Policy for Lumen Health Analytics, 40 people. We process anonymized and some identifiable patient data for clinics. Team uses ChatGPT (some personal accounts), we're buying Claude Team. Engineers use GitHub Copilot Business. Owner: Hugo (COO)."

**Output:**

```markdown
# Lumen Health Analytics AI use policy
*Draft for legal review. Not legal advice. Version 0.1, 4 Nov. Owner: Hugo.*

## Why this policy
We want everyone to use AI to work faster. We also handle patient data for clinics, so these rules decide which tools and which data are allowed.

## Approved tools
| Tool | Plan | Approved for | Data used for training? |
|---|---|---|---|
| Claude | Team | Writing, analysis of internal documents | [check: vendor terms and admin settings] |
| GitHub Copilot | Business | Code in company repositories | [check: vendor terms] |
| ChatGPT | personal accounts | Public information only, until a business plan is approved | [check] |
Anything not listed: not approved for company data. Request a tool: #it-requests, Hugo approves.

## What you can put in
| Never | Approved tools only | Any tool |
|---|---|---|
| Patient data, even if you think it's anonymized; clinic contracts; passwords and API keys; employee HR records | Internal docs, roadmaps, non-patient code | Public research, your own draft wording |

## Check before you use it
- A person checks any AI output before it goes to a clinic, is published, or informs a decision about an employee.
- Every number, citation, and clinical statement is verified against its source.
- Nothing AI-generated is used for clinical advice.

## Telling people AI was used
- Any automated reply to clinics says it is automated.
- Other disclosure follows clinic contracts [check: legal].

## If something goes wrong
Report to Hugo or #security within 1 hour: what was entered, which tool, when.

## Owners
- Policy owner: Hugo · Tool approvals: Hugo with the security lead · Next review: May

## Points for legal review
- [ ] Health data rules for each market served [check: legal]
- [ ] Clinic contract clauses on subprocessors and AI [check: legal]
- [ ] Whether "anonymized" data meets the legal standard [check: legal]
- [ ] Vendor data-use terms for each approved tool [check: legal and security]
```

## Checks before you send

- [ ] The legal disclaimer appears at the top of the skill output and the policy draft.
- [ ] Every "never" data class has concrete examples from this company.
- [ ] Every approved tool names a plan; personal accounts are not approved for company data unless explicitly decided.
- [ ] Review rules cover external use, decisions about people, and legal, financial, medical, or security matters.
- [ ] Nothing about law, regulation, or vendor terms is stated as fact; each is marked "[check: ...]".
- [ ] The policy names a person as owner and a review date.

## Common mistakes

- Banning AI outright. People use it anyway on personal accounts, where you can't see or control the data.
- Writing "don't enter sensitive data" with no examples. People don't know what counts.
- Copying another company's policy without checking which laws and contracts apply to you.
