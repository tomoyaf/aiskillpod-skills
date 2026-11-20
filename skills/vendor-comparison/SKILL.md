---
name: vendor-comparison
description: Compares 2 to 5 vendors, tools, or agencies against weighted criteria the user agrees to first, then gives a scoring table, total cost of ownership, risks, and a recommendation, marking every claim that comes only from the vendor as unverified. Use when someone asks to compare vendors, pick a tool, evaluate suppliers or agencies, build a comparison matrix, or decide "which one should we buy".
---

# Vendor comparison

A useful comparison makes the choice obvious and shows why, using criteria agreed before anyone looked at prices. UK government buyers work the same way: the evaluation model is set and tested before bids come in, a mandatory threshold can be pass/fail, and cost means whole-life cost, not the initial price. Score from evidence and say plainly which claims are the vendor's own word.

## When to use

- Choosing between 2-5 software tools, agencies, suppliers, or contractors.
- A team is split and needs a shared, visible basis for the decision.
- Renewing a contract and checking whether to switch.
- Not for a single vendor's invoice (use invoice-check) or a deep security review (use security-questionnaire-answers).

## What you need

- The vendors and whatever you have on each: quotes, pricing pages, demo notes, references, trial results.
- The need: what problem, how many users or volume, budget, and the must-haves.
- Who decides. If budget or volume is missing, ask once; otherwise compute cost at "[assumption: N users]".

## Steps

1. **Agree the criteria and weights before scoring.** Propose 4-7 distinct criteria with weights adding to 100, and avoid giving 2 criteria the same weight (for example: fit to must-haves 30, total cost 25, ease of use 18, support 12, security and data 9, vendor stability 6). Show them and stop for the user to confirm or change. If the user says "just go", state that you used your proposed weights.
2. **Apply must-haves as pass/fail first.** A vendor that fails a must-have is out, whatever its score. Say which must-have and the evidence.
3. **Score 1-5 per criterion with evidence.** Weighted total = sum of (score × weight) ÷ 5, so 100 is the maximum. 5 = clearly best on this need, 3 = adequate, 1 = poor. Each score cites its source: trial, reference call, contract, or "vendor claim". A score that rests only on a vendor claim gets "(unverified)".
4. **Compute whole-life cost over the contract term** (our default: 2 years): acquisition (licence or fees, setup, migration), running (add-ons needed to meet must-haves, admin and training time), and exit (data export, notice period). Use the same user count for all. Price not in the inputs is "[check: price]", never an estimate presented as fact.
5. **List risks per vendor.** Lock-in, price rises at renewal, small company or new product, missing features promised "on the roadmap", data location. 1-3 per vendor.
6. **Recommend.** If 2 or more people will decide, suggest each scores alone first and then agrees a consensus score, as government evaluators do. Name one vendor and the 2 reasons that decided it. If the top 2 are within 5 points of 100, say it's close and name the tie-breaker (usually cost or a reference call). Add what to verify before signing.

## Output format

```markdown
**Vendor comparison — [need], [date]**

**Recommendation: [Vendor]** — [2 deciding reasons]. Verify before signing: [items].

**Criteria (agreed):** [criterion weight, ...]

**Must-haves**
| Must-have | [Vendor A] | [Vendor B] |
|---|---|---|
| [must-have] | [pass/fail + evidence] | ... |

**Scores (1-5, weighted total out of 100)**
| Criterion (weight) | [Vendor A] | [Vendor B] |
|---|---|---|
| [criterion (w)] | [score] — [evidence or "vendor claim (unverified)"] | ... |
| **Weighted total** | [n] | [n] |

**Total cost over [term]**
| Cost | [Vendor A] | [Vendor B] |
|---|---|---|
| Fees | ... | ... |
| Setup and migration | ... | ... |
| Add-ons needed | ... | ... |
| **Total** | ... | ... |

**Risks**
- [Vendor]: [risk]

**Unverified claims to check:** [list]
```

## Example

**Input:** Choose a help desk for 8 support agents, 2 years, budget around 10,000 a year. Must-have: Slack integration. Helpwise: 39/agent/month, Slack yes (tested in trial), setup free, quote has no renewal price cap. Tixly: 29/agent/month, Slack "coming Q3" per sales rep, setup 1,500. Desko: 45/agent/month, Slack yes per docs, "replies within 1 hour" per sales deck, 4.8 on reviews, references not called, setup price not given. User confirmed weights: must-haves fit 35, cost 30, ease 20, support 15.

**Output:**

```markdown
**Vendor comparison — help desk for 8 agents, 4 November**

**Recommendation: Helpwise** — Slack integration proven in our trial, and 2-year fees are 1,152 below Desko before Desko's setup cost. Verify before signing: renewal price cap, data export format.

**Criteria (agreed):** must-have fit 35, cost 30, ease of use 20, support 15

**Must-haves**
| Must-have | Helpwise | Tixly | Desko |
|---|---|---|---|
| Slack integration | pass — tested in trial | fail — "coming Q3", vendor claim | pass — docs (unverified) |

Tixly is out: the must-have is a roadmap promise.

**Scores (1-5, weighted total out of 100)**
| Criterion (weight) | Helpwise | Desko |
|---|---|---|
| Must-have fit (35) | 5 — trial | 4 — docs (unverified) |
| Cost (30) | 4 — quote | 3 — pricing page |
| Ease of use (20) | 4 — trial | 4 — review sites (unverified) |
| Support (15) | 3 — [check: no reference yet] | 4 — vendor claim (unverified) |
| **Weighted total** | 84 | 74 |

**Total cost over 2 years**
| Cost | Helpwise | Desko |
|---|---|---|
| Fees (8 agents × 24 months) | 7,488 | 8,640 |
| Setup | 0 | [check: price] |
| **Total** | 7,488 | 8,640 + setup |

**Risks**
- Helpwise: renewal price not capped in the quote.
- Desko: Slack and support scores rest on vendor material only.

**Unverified claims to check:** Desko Slack integration, Desko support response times.
```

## Checks before you send

- [ ] The weights were shown before scoring, no 2 share a value, and the output says whether the user confirmed them.
- [ ] Any vendor failing a must-have is out, with the evidence.
- [ ] Every score names its source; vendor-only claims say "(unverified)".
- [ ] Costs use the same term and volume for every vendor, and no price is invented.
- [ ] The recommendation names one vendor and 2 reasons.

## Common mistakes

- Picking weights after seeing scores, which bends the result toward the favourite.
- Comparing monthly list price instead of the full cost over the term.
- Scoring a roadmap feature as if it exists.
