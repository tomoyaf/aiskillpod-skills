---
name: landing-page-house-style
description: Builds a landing page or campaign page the team's house way, whoever's AI makes it - the brand voice and words to avoid, a fixed section order, one call to action with fixed wording, only the form fields the team allows, every claim that needs a source flagged, alt text on every image, readable contrast - and returns a preview, never publishing unless the person asks. Use when someone asks an AI to make, draft or update a landing page, campaign page, sign-up page or event page for the team.
---

# Landing page house style

Share this skill with everyone on the team who makes pages, so every teammate's AI works from one house style. When several people ask their own AI for a landing page, each AI invents its own: a different call to action, a longer form, a claim nobody can prove. This skill holds the team's one way. Fill in the blanks in "Our house style" once; after that, every page any teammate's AI builds has the same order, the same button, the same form and the same checks. It works for any host or a plain HTML file.

## Our house style

Fill these in once for the team. Until a line is filled, follow the default after it.

- **Voice:** [3 traits, "this, not that"]. Default: plain, specific, no hype.
- **Words we avoid:** [list]. Default: "revolutionary", "world-class", "next-generation", "effortless".
- **Section order:** [list]. Default: headline and one-line promise with the button; the problem in the reader's words; how it works in 3 steps; proof; what it costs or what they get; 3 to 5 questions; the button again.
- **The one call to action:** [wording, such as "Book a 20-minute demo"]. Default: a verb and what happens next.
- **Form fields we ask:** [list]. Default: name and work email. **Never ask:** [list]. Default: date of birth, home address, anything the reply doesn't need.
- **Proof we hold:** [the numbers, customer quotes with permission, and logos we may use, each with its source].
- **Who approves publishing:** [name or role].

## When to use

- Someone asks their AI to make or update a landing page, campaign page, sign-up page or event page.
- A page made by one teammate's AI needs to match the others before it goes live.
- Not for reviewing finished copy line by line (use landing-copy-review) or for checking claims alone (use marketing-claims-check).

## What you need

- The brief: the offer, who it's for, the one action, and the date or deadline if there is one.
- The facts the page may state: prices, numbers, customer quotes with permission. Anything else stays out.
- Images, and what each one shows.
- Where the page will live: a host's preview, or an HTML file.

## Steps

1. **Read the brief against the house style.** Note the one action, and check it matches "The one call to action". If the brief asks for a second button, keep one and list the other as a text link.
2. **Write in the house voice.** Use "Voice" and drop every word on "Words we avoid". Lead the headline with what the reader gets, not with the company.
3. **Build the sections in the house order.** Keep the order even when a section is short. Leave out a section only when the brief has nothing true to put in it, and say so.
4. **Use the one call to action everywhere.** Same words on every button. One primary button style on the page.
5. **Build the form from the house list.** Only the fields in "Form fields we ask"; nothing from "Never ask". Label every field, mark optional ones "(optional)", and say under the button what happens next and how the data is used, with a link to the privacy policy. If the form also signs people up for email, say so beside the button and don't pre-tick it.
6. **Flag every claim that needs a source.** Numbers, comparisons ("fastest", "#1"), results, testimonials, "free", guarantees: keep them only if they're in "Proof we hold" or the brief, and mark the rest "[source needed: what]". Never invent a statistic, quote, logo or review. Run marketing-claims-check on the page before it's published.
7. **Write alt text.** Every image that carries meaning gets alt text saying what it shows and why it's there; decorative images get an empty alt. No text that exists only inside an image.
8. **Check accessibility.** Text contrast at least 4.5:1, or 3:1 for large text, as WCAG 2.2 sets for level AA; headings in order; every field has a label; link and button text says where it goes.
9. **Preview, don't publish.** Return the page as a preview (the host's private preview link, or the HTML file) with the checklist below. Publish, or replace a live page, only when the person asks to publish in this conversation.

## Output format

```markdown
**Page:** [title] · **Status:** preview only, not published

[The page: sections in the house order, or the HTML]

**Before you publish**
- Call to action: "[wording]" on [n] buttons
- Form: [fields] · never asked: [list]
- Claims needing a source: [list, or "none"]
- Images: [n] with alt text, [n] decorative
- Contrast: [checked / to check]
- Preview: [link or file] · Publish when [approver] says so
```

## Example

**Input:** House style filled in for Harbor Payroll (fictional): voice "plain, not stiff; specific, not technical"; avoid "revolutionary", "effortless"; section order as the default; call to action "Book a 20-minute demo"; form fields name, work email, company size; never ask phone number or job title; proof held: "used by 300 restaurants" (CRM count, October). Brief: a page for restaurant groups hiring seasonal staff for the summer; the one action is booking a demo. The draft from the brief says "Cut payroll time in half" and "the #1 payroll app for restaurants". Hero photo: a manager checking a tablet in a kitchen.

**Output:**

```markdown
**Page:** Payroll for seasonal staff · **Status:** preview only, not published

- Headline: Run payroll for seasonal staff without the Sunday spreadsheet
- Promise: See how to pay every seasonal hire from one screen, in a 20-minute demo.
- [Button: Book a 20-minute demo]
- ...
- Proof: Used by 300 restaurants.
- Form: Name · Work email · Company size (optional)
- Under the button: We'll email you a time that suits you. Privacy policy.

**Before you publish**
- Call to action: "Book a 20-minute demo" on 2 buttons
- Form: name, work email, company size · never asked: phone, job title
- Claims needing a source: "Cut payroll time in half" [source needed: a study or customer data]; "#1 payroll app for restaurants" removed (no source)
- Images: 1 with alt text ("A restaurant manager approving the week's hours on a tablet"), 0 decorative
- Contrast: checked, button text 8.7:1 (white on #1F4E79)
- Preview: private preview link · Publish when the marketing lead says so
```

## Checks before you send

- [ ] The sections follow the house order, and the call to action uses the house wording on every button.
- [ ] The form has only allowed fields, each labeled, with what happens next and the privacy link.
- [ ] Every number, comparison, testimonial and "free" is in the proof list or marked "[source needed]".
- [ ] Every meaningful image has alt text; decorative ones have an empty alt.
- [ ] Text contrast is at least 4.5:1 (3:1 for large text).
- [ ] The status says "preview only", and nothing was published without the person asking.

## Common mistakes

- Two buttons that ask for different things. Readers pick neither.
- A form that asks for a phone number "just in case". Every extra field costs sign-ups and holds data you must protect.
- A claim kept because the AI wrote it confidently. Confidence isn't a source.
- Publishing straight from the chat. The preview is where the team catches the rest.
