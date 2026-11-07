---
name: intro-email
description: >
  Draft warm introduction emails connecting two people. Use this skill whenever the user says "introduce", "connect", "intro email", "put them in touch", "they should meet", or names two people who should know each other. Also trigger when the user pastes context about two people and asks for an email, or references a meeting where an introduction was promised. This skill generates specific, structured introductions, not generic "you should meet" emails.
---

# Intro Email Skill

## Purpose

Generate a warm, specific introduction email that connects two people and makes it immediately clear why they should know each other. The email should be ready to send with minimal editing.

---

## Step 1: Gather Context on Both Parties

For each person, identify:

- **Name** (first name is sufficient for the greeting)
- **What they do** (one sentence: role, company, or project)
- **Why they're relevant to the other person** (the connection point)
- **Optional: a personal or timely detail** (recent move, upcoming trip, shared community, new role)

**Where to get this context:**
- User provides it directly ("introduce Mira to Jonas, Mira does X, Jonas does Y")
- Search past chats for prior mentions of either person
- Search email/Drive for prior correspondence
- Web search for professional context if names + orgs are given
- If context is too thin, ask: "What should each person know about the other?"

---

## Step 2: Identify the Connection Type

The framing shifts based on why these two should meet:

| Connection Type | Framing | Example |
|----------------|---------|---------|
| **Professional overlap** | Their work intersects | "You're both building in the longevity space" |
| **Geographic proximity** | They'll be in the same place | "Jonas is relocating to Palo Alto next month" |
| **Shared community** | Both connected to the same network | "Mira is a core member of our founder community" |
| **Complementary expertise** | One has what the other needs | "Mira's experience in impact ventures could be really relevant to what you're building" |
| **Mutual interest surfaced in conversation** | Someone asked to be connected | "You mentioned wanting to meet people in the European VC space" |

---

## Step 3: Draft the Email

### Structure (5 parts, in order):

**1. Greeting.** Address both by first name on the same line.

**2. Intent.** One sentence: why you're making this introduction.

**3. Person A context.** 1-2 sentences about what Person A does and why they're interesting. Include a specific, current detail, not just their job title.

**4. Person B context.** Same treatment. 1-2 sentences, specific and current.

**5. Warm close.** Express confidence they'll find common ground. Hand off the conversation to them. Optionally mention looking forward to seeing them.

### Template:

```
Hi [First Name A], Hi [First Name B],

I wanted to introduce you to each other, as I believe you'll have [plenty of valuable insights to share / a lot of common ground / some great opportunities to explore together].

[First Name A] [1-2 sentences: what they do, why they're relevant, a current detail].

[First Name B] [1-2 sentences: what they do, why they're relevant, a current detail].

[Warm close: confidence in the connection + hand-off + optional personal touch].

Best,
Lucas
```

---

## Tone Rules

- **Warm but not effusive.** "I'm certain you'll find great opportunities" not "OMG you HAVE to meet!!!"
- **Specific, not generic.** Every intro email must contain at least one detail about each person that couldn't apply to anyone else in their role.
- **Connector, not salesperson.** You're facilitating, not selling either person. The email should feel like a gift, not a pitch.
- **Hand off cleanly.** "I'll leave it up to you two to connect." Don't over-orchestrate the next step.
- **Short.** The entire email should be readable in under 30 seconds. 5-8 sentences total.
- **Internationally fluent.** Many contacts are Swiss, European, or otherwise international. No slang, no overly American idioms. Keep it professional and warm across cultures.

---

## Quality Checklist

Before delivering, verify:

- [ ] Both people are named in the greeting
- [ ] Each person gets 1-2 specific sentences (not just a title)
- [ ] The reason for the introduction is stated in the first sentence
- [ ] At least one current/timely detail per person (new role, upcoming trip, recent project, relocation)
- [ ] The email is under 120 words
- [ ] No "I hope this email finds you well"
- [ ] No generic phrases: "two amazing people", "incredible work", "thought leaders"
- [ ] The close hands off to them without prescribing how they should meet
- [ ] Tone works for both a 25-year-old startup founder and a 55-year-old university dean

---

## Reference Example

This follows the structure of an introduction Lucas sends regularly. The names and details are invented. Match this level of specificity and warmth:

> Hi Mira, Hi Jonas,
>
> I wanted to introduce you to each other, as I believe you'll have plenty of valuable insights to share.
>
> Mira runs an early-stage climate fund that invests across Europe and the United States. She opened its first San Francisco office this autumn.
>
> Jonas co-founded a payments startup and now invests at a Zurich-based venture firm. Next month, he'll be relocating to Palo Alto, and we couldn't be more excited to welcome him to the Bay Area.
>
> I am certain you'll find many great opportunities for productive exchanges. I'll leave it up to you two to connect for now, but I am very much looking forward to seeing both of you soon!
>
> Best,
> Lucas

**What makes this work:** Each person gets a specific, current detail (a new San Francisco office; relocating to Palo Alto next month). The connection rationale is implicit (both invest across Europe and the Bay Area). The close is warm but not oversteering.

---

## What This Skill Does NOT Do

- Does not send the email (just drafts it)
- Does not decide whether an introduction should happen (that's the user's judgment)
- Does not BCC or CC: introductions are always open with both parties visible
- Does not add context the user hasn't provided or approved. Don't invent details about people
