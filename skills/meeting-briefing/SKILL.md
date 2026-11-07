---
name: meeting-briefing
description: >
  Prepare context briefings before meetings. Use this skill whenever the user mentions "prep me for a meeting", "brief me on", "who am I meeting", "what do I need to know about", "meeting prep", "get me ready for", or names a specific person, organization, or meeting they're about to have. Also trigger when the user shares a calendar entry, a name they're meeting, or asks "what's on my calendar." This skill pulls relevant context, surfaces past interactions, and delivers a structured pre-meeting brief so you walk in informed, not cold.
---

# Meeting Briefing Skill

## Purpose

Generate a focused pre-meeting brief that gives you exactly what you need to walk into any meeting prepared. Not a dossier, a cheat sheet. The goal is: you glance at this 2 minutes before the call and you're oriented.

---

## Step 1: Identify Meeting Type

Determine the meeting type from context (calendar entry, user description, or ask). The type determines what context to pull and how to structure the brief.

| Type | Signal | Priority Context |
|------|--------|-----------------|
| **New prospect** | First-time meeting, external org | Who they are, what they do, how they connect to your organization, which of your programs might fit |
| **Partner check-in** | Recurring, known org (university, foundation, corporate) | Last interaction, open commitments, relationship temperature |
| **Program kick-off** | Named program (a lab, a camp, a study tour) | Program scope, participant list, deliverables, timeline |
| **Study tour / delegation** | Visiting group, multi-day, logistics involved | Group composition, agenda, logistics status, speaker confirmations |
| **Corporate / foundation pitch** | Potential sponsor, funder, or co-producer | Their portfolio, past support, alignment with your mission, ask amount |
| **Cross-functional internal** | Programs × Comms, team sync | Open items from last meeting, shared deadlines, blockers |
| **1-on-1 (direct report)** | Associate meeting | Their current projects, recent wins, blockers mentioned last time, development goals |
| **1-on-1 (manager)** | Meeting with your manager or leadership | Your priorities, what you need from them, team pulse, culture items |
| **Finance / accounting** | Budget review, invoicing | Open invoices, budget vs actuals, upcoming expenses |
| **All-hands / retreat** | Whole team, quarterly or biannual | Agenda, pre-reads, any items you're presenting |
| **Webinar / public event** | External-facing presentation | Audience profile, run of show, tech setup, key talking points |

If the type is ambiguous, ask one clarifying question.

---

## Step 2: Pull Context

Based on meeting type, gather the following. Use available tools (calendar, email, Drive, past chats, web search) as appropriate.

### For External Meetings (prospects, partners, pitches)

**About the person:**
- Name, title, organization
- LinkedIn summary (if available via web search)
- How the connection was made (intro, inbound, event?)
- Any prior interactions with your organization (search past chats, Drive, email)

**About the organization:**
- What they do (one paragraph max)
- Connection to your organization: shared geography, funders, partners, or interests
- Overlap with your organization's focus areas
- Recent news (funding round, leadership change, new initiative): web search if name is specific enough

**Program fit:**
- Which of your programs or offerings could be relevant? Replace this list with your own:
  - [Accelerator or camp] (for startups going global)
  - [Innovation tour] (for corporates exploring new technology)
  - [Residency or sabbatical] (for researchers and faculty)
  - [Training lab] (for media professionals)
  - Custom study tours (for visiting delegations)

### For Internal Meetings

**About the meeting:**
- Agenda (from calendar invite or past pattern)
- Open action items from the last occurrence of this meeting
- Any relevant documents shared since last meeting

**For 1-on-1s specifically:**
- What the person is currently working on
- Any blockers or concerns they've raised recently
- Career development topics in progress

### For Program Meetings

**About the program:**
- Current phase (planning, recruitment, active, wrap-up)
- Key dates and deadlines approaching
- Participant or partner status
- Budget status if relevant
- Any decisions needed

---

## Step 3: Format the Brief

Output a structured brief. Keep it scannable: this gets read in 2 minutes, not 20.

```
## Meeting Brief: [Person/Group], [Date, Time]

### Context
[1-2 sentences: who they are, why you're meeting, how the connection was made]

### Key Background
- [3-5 bullets: the most important things to know going in]

### Last Interaction
[1-2 sentences: when you last spoke, what was discussed, any open threads]
OR
[First meeting: no prior interaction on record]

### Relevant Programs / Opportunities
- [Which of your programs or offerings could be relevant and why]

### Their Likely Questions or Needs
- [2-3 things they're probably hoping to get out of this meeting]

### Your Agenda
- [What do YOU want to get out of this meeting? Ask the user if unclear]

### Prep Actions
- [ ] [Anything to do before the meeting: review a doc, forward an intro, check a detail]
```

**Formatting rules:**
- No section should exceed 5 bullets
- Total brief should fit on one screen (roughly 200-300 words)
- Bold the single most important thing to know
- If there's a personal detail worth remembering (they mentioned a trip, a milestone, a concern), surface it: this is the "unreasonable hospitality" data

---

## Step 4: Offer Follow-Up

After delivering the brief, offer:
- "Want me to draft an opening message or agenda to send ahead of the meeting?"
- "Should I set up a debrief template for after?" (hand off to the meeting-debrief skill)

---

## Tool Usage

- **Google Calendar**: Pull meeting details, attendees, time
- **Google Drive**: Search for past briefs, proposals, shared docs related to the person/org
- **Email/Gmail**: Search for prior correspondence
- **Web search**: For external people/orgs: LinkedIn, company site, recent news
- **Past chats**: Search for prior conversations about this person/org
- **Granola notes**: If past meeting notes exist, surface key takeaways and open items

---

## What This Skill Does NOT Do

- Does not generate meeting agendas (that's a separate ask; just offer to draft one)
- Does not do post-meeting processing (hand off to meeting-debrief)
- Does not write the talking points for a presentation (hand off to relevant program or event skill)
- Does not replace the user's judgment about relationship dynamics: surface facts, let them decide tone
