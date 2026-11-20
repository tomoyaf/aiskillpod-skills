---
name: ontology-draft
description: Drafts a domain ontology for one business area - the competency questions it must answer, core classes with plain definitions, properties and relationships with cardinality, example instances, and naming rules - following the Ontology Development 101 method, in tables a non-engineer can review. Use when a team asks to define the core concepts of a business, design a data model in plain words, create an ontology, a taxonomy, a schema for a knowledge graph, or "what are the things we track and how do they relate".
---

# Ontology draft

An ontology is an agreed list of the things a business talks about (classes), what we record about them (properties), and how they relate, with definitions precise enough that two people would file the same thing the same way. Noy and McGuinness's Ontology Development 101 starts by setting the domain and scope with competency questions, the questions the ontology must answer; we do too, because an ontology that can't answer its questions is missing something, and one that answers questions nobody asks is too big.

## When to use

- Before building a knowledge graph, a CRM structure, a data warehouse, or a RAG system for one domain.
- When teams use the same word for different things ("customer", "account", "user").
- When a spreadsheet has grown columns nobody can define.
- Not for extracting facts from existing documents: use knowledge-graph-extraction once the classes exist.

## What you need

- The domain and its boundary ("B2B subscriptions from quote to renewal", not "the business").
- Who will use the ontology and for what.
- Example documents, spreadsheets, or system fields. If none, work from the domain description and mark classes "[proposal]".
- Existing standards the team already uses (an industry schema, schema.org, a CRM's objects). Reuse their names where they fit.

## Steps

1. **Write 5 to 10 competency questions.** Real questions the ontology must answer: "Which accounts renew in the next 90 days and who owns them?" These scope the work and test it at the end.
2. **List the terms.** Every noun and verb from the questions and source material, without structure yet.
3. **Pick the classes and define each in one sentence.** A class is a kind of thing with instances. Definition form: "A [class] is a [parent class] that [distinguishing feature]." Merge synonyms into one class and record the synonyms. If something moves in and out of a state ("active customer"), make it a property value, not a class.
4. **Build the hierarchy.** Every subclass must be "a kind of" its parent. Avoid a class with only one subclass, and avoid more than about a dozen direct subclasses. Mark classes that can't share instances as disjoint.
5. **Add properties and relationships.** Attach each to the most general class that has it. For each: name, value type (text, number, date, another class), and cardinality (exactly 1, 0 or 1, 1 or more, 0 or more). Add the inverse for key relationships (owns / owned_by).
6. **Create 2 to 3 example instances per core class.** Realistic but fictional. If an example doesn't fit, the class or property is wrong.
7. **Test against the competency questions.** For each question, show which classes and properties answer it. A question that can't be answered means something is missing; a class no question uses is a candidate to cut.

Our default naming rules: classes in singular UpperCamelCase (SalesOpportunity), properties in lower_snake_case starting with a verb or "has" (has_owner, renews_on), no abbreviations, and no words like "class" or "type" in names.

## Output format

```markdown
# Ontology draft — [domain]
**Scope:** [boundary] · **Users:** [who, for what] · **Status:** draft

## Competency questions
1. [Question]

## Classes
| Class | Parent | Definition | Synonyms (not used) |
|---|---|---|---|

## Properties and relationships
| Property | Of class | Value type | Cardinality | Inverse | Definition |
|---|---|---|---|---|---|

## Example instances
| Instance | Class | Property values |
|---|---|---|

## Question coverage
| Question | Answered by |
|---|---|

## Naming rules
- [Rules]

## Open decisions
- [Decision needed, options]
```

## Example

**Input:** "Domain: our SaaS subscriptions. We sell to companies; each company can have several workspaces; each workspace has a plan and seats. People call companies 'accounts' or 'customers'. We need to know who renews when, who owns each renewal, and which workspaces are over their seat limit."

**Output:**

```markdown
# Ontology draft — SaaS subscriptions
**Scope:** companies, workspaces, subscriptions, renewals · **Users:** CS and finance, for renewal tracking · **Status:** draft

## Competency questions
1. Which subscriptions renew in the next 90 days, and who owns each renewal?
2. Which workspaces use more seats than their plan allows?
3. How many workspaces does each company have?

## Classes
| Class | Parent | Definition | Synonyms (not used) |
|---|---|---|---|
| Company | — | A legal entity that buys or may buy our product | account, customer, organization |
| Workspace | — | A separate area of our product that a company's users log in to | instance, tenant |
| Subscription | — | A paid agreement for one workspace on one plan for a period | contract, license |
| Plan | — | A named package with a price and a seat limit | tier |
| Person | — | A human we record | contact, user |

## Properties and relationships
| Property | Of class | Value type | Cardinality | Inverse | Definition |
|---|---|---|---|---|---|
| has_workspace | Company | Workspace | 1 or more | belongs_to | Workspaces the company pays for |
| has_subscription | Workspace | Subscription | exactly 1 (current) | covers | The current paid agreement |
| on_plan | Subscription | Plan | exactly 1 | — | The plan bought |
| renews_on | Subscription | date | exactly 1 | — | Date the current period ends |
| has_renewal_owner | Subscription | Person | 0 or 1 | owns_renewal | Our person responsible for the renewal |
| allows_seats | Plan | number | exactly 1 | — | Maximum seats on the plan |
| uses_seats | Workspace | number | exactly 1 | — | Seats in use today |

## Example instances
| Instance | Class | Property values |
|---|---|---|
| Northpeak Ltd | Company | has_workspace: Northpeak-EU, Northpeak-US |
| Northpeak-EU | Workspace | uses_seats: 48; has_subscription: SUB-1042 |
| SUB-1042 | Subscription | on_plan: Team; renews_on: 2026-03-31; has_renewal_owner: Lena Ortiz |
| Team | Plan | allows_seats: 40 |

## Question coverage
| Question | Answered by |
|---|---|
| 1 | Subscription.renews_on, has_renewal_owner |
| 2 | Workspace.uses_seats vs Plan.allows_seats via Subscription.on_plan |
| 3 | Company.has_workspace (count) |

## Naming rules
- Classes: singular UpperCamelCase. Properties: lower_snake_case, verb or "has" first. No abbreviations.

## Open decisions
- Is a trial a Subscription with price 0, or its own class? Affects question 1.
```

## Checks before you send

- [ ] Every competency question maps to named classes and properties.
- [ ] Every class has a one-sentence definition naming its parent and what distinguishes it.
- [ ] Synonyms are merged into one class and listed, not modelled as separate classes.
- [ ] Every property has a value type and a cardinality.
- [ ] Each "is a kind of" link is true for every instance of the subclass.

## Common mistakes

- Making states into classes ("ChurnedCustomer"). Use a status property; things move in and out of states.
- Modelling everything the business has ever mentioned. Stop at what the competency questions need.
- Leaving definitions as the class name reworded ("A Customer is a customer"). Say what makes it different.
