---
name: launch-announcement
description: Writes the copy set for a feature or product launch — a message house, then a blog intro, customer email, in-app message, and social posts that all say the same thing in the same words. Use when someone asks for launch copy, a feature announcement, a release email, an in-app banner, "announce this on LinkedIn", or a launch kit for a new product or feature.
---

# Launch announcement copy set

A launch lands when every channel repeats one message: who it's for, what they can now do, and why it matters. Build the message house first, then write each piece from it; no piece introduces a new claim.

## When to use

- Shipping a feature or product that customers or prospects should hear about.
- When the blog, email, and social copy were written by different people and say different things.
- Not for release notes that list every fix: use release notes. Not for a press release to journalists: use a press release.

## What you need

- What shipped, who it's for, and what they can do now that they couldn't before.
- The launch date, where it's available (all plans or some), and the price if any.
- Proof: a beta customer result, a number, a quote. If none, write the copy without proof and list "[proof: to collect]".
- Links: the blog post URL, the help article, the in-app location. If missing, use "[link: ...]".
- Optional: brand voice notes or a past announcement to match.

## Steps

1. **Build the message house.** Roof: one true, differentiating sentence (our default: under 20 words, the user as subject, "Clinic managers can now ..."). 3 to 4 pillars, each a distinct benefit. Under each pillar, its proof: a metric, a customer outcome, a quote. A pillar with no proof gets proof or gets cut. Then the facts: availability, price, limits. Every channel keeps the roof and pillars; only the format changes.
2. **Decide the tier.** Match effort to expected impact (Pragmatic Institute's launch tiers; the pieces per tier are our default). Tier 1 (rare and strategic: a new product or category): every piece, plus a press release. Tier 2 (an incremental improvement worth some attention): blog, email, in-app, social. Tier 3 (a maintenance release): general communication only, such as an in-app note and a changelog line. Say which tier and why; don't write a blog post for a tier-3 change.
3. **Write the blog intro.** 3 short paragraphs: the problem in the customer's words, what's new, how to try it today. Headline is the roof sentence or close to it.
4. **Write the customer email.** Our default lengths: subject under 50 characters naming the capability, not "Big news". Body under 120 words, one CTA button that goes to the feature itself.
5. **Write the in-app message.** Our default: title under 40 characters, body under 140 characters, one action. Shown only to users who can use the feature; say who should see it.
6. **Write social posts.** LinkedIn: hook from the most specific pillar, 50 to 150 words (our default), link in the post. X: under 280 characters. Our default: 2 hashtags at most.
7. **Check consistency.** Every piece names the feature the same way, states the same availability, and makes no claim outside the house.

## Output format

```markdown
# Launch kit — [feature], [launch date]
**Tier:** [1 / 2 / 3] — [why]

## Message house
- **Roof:** [one sentence, user as subject, under 20 words]
- **Pillar 1:** [benefit] — proof: [metric, outcome, or quote; or "to collect"]
- **Pillar 2:** [benefit] — proof: [...]
- **Pillar 3:** [benefit] — proof: [...]
- **Facts:** [availability, plans, price, limits]

## Blog intro
**[Headline]**
[3 short paragraphs]

## Email
- Subject: [under 50 chars]
- Preheader: [under 90 chars]
- Body: [under 120 words]
- Button: [verb-first label] → [link]

## In-app
- Audience: [who sees it]
- Title: [under 40 chars]
- Body: [under 140 chars]
- Action: [label] → [location]

## Social
**LinkedIn:** [50–150 words]
**X:** [under 280 chars]

## Open items
- [proof, link, or approval needed]
```

## Example

**Input:** "Shiftly (rota app for cafés) now lets staff swap shifts themselves, manager approves with one tap. All paid plans, 12 May. Beta: Bean There cafés cut rota messages by about half [from the user]."

**Output:**

```markdown
# Launch kit — Shift swaps, 12 May
**Tier:** 2 — a long-requested feature on all paid plans; no reason to brief press.

## Message house
- **Roof:** Café staff can now swap shifts themselves, and managers approve with one tap.
- **Pillar 1:** Fewer rota messages — proof: Bean There cut rota messages by about half in beta.
- **Pillar 2:** Managers stay in control — proof: no swap applies without approval.
- **Pillar 3:** On every paid plan — proof: live on all paid plans from 12 May.
- **Facts:** All paid plans from 12 May; price [check: extra cost or included].

## Blog intro
**Café staff can now swap shifts themselves**
Most rota changes start as a text: "Can anyone take Saturday?" Then the manager rewrites the rota by hand.
From today, staff swap shifts in Shiftly. A colleague accepts, the manager approves with one tap, and everyone's schedule updates.
Shift swaps are on all paid plans now. Open the rota and tap any shift to try it.

## Email
- Subject: Staff can now swap shifts themselves
- Preheader: You approve with one tap. The rota updates for everyone.
- Body: Rota changes used to mean a group text and a rewrite. Now staff offer a shift, a colleague accepts, and you approve with one tap. At Bean There, rota messages dropped by about half during the beta. Shift swaps are live on your plan today.
- Button: Open your rota → [link: rota page]

## In-app
- Audience: managers and staff on paid plans
- Title: Swap shifts without the group text
- Body: Tap a shift to offer it. A colleague accepts, your manager approves, and the rota updates.
- Action: Try it → rota page

## Social
**LinkedIn:** At Bean There cafés, rota messages dropped by about half once staff could swap shifts themselves. From today, every café on a paid Shiftly plan can do the same. A staff member offers a shift, a colleague accepts, and the manager approves with one tap. No more chasing swaps for staff. [link: blog]
**X:** Café staff can now swap shifts in Shiftly. Colleague accepts, manager approves with one tap, rota updates for everyone. Live on all paid plans. [link: blog]

## Open items
- Bean There's approval to be named, and the exact figure — [check: beta data]
- Blog and rota links
- Whether swaps cost extra on any plan — [check: pricing]
```

## Checks before you send

- [ ] The roof sentence's key phrase appears in the blog headline, email subject, and in-app title.
- [ ] Availability and price are identical in every piece.
- [ ] No piece makes a claim that isn't in the message house.
- [ ] Each piece has one action, and its link goes to the feature, not the homepage.
- [ ] Length limits are met: subject 50, in-app title 40, in-app body 140, X 280.
- [ ] Customer names and numbers are in the input or listed under open items.

## Common mistakes

- Writing "We're excited to announce". The reader cares what they can do, so start there.
- Naming the feature 3 ways ("Swaps", "Shift trading", "Rota exchange").
- Announcing to users who can't use it, such as free-plan users seeing a paid-only banner.
