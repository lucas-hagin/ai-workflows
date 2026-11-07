---
name: meeting-debrief
description: >
  Process meeting notes into structured follow-ups after any meeting. Use this skill whenever the user shares Granola notes, a meeting transcript, raw meeting notes, or says "debrief this meeting", "process my notes", "what did we decide", "draft the follow-up", "summarize that call", or pastes in notes from a call they just had. Also trigger when the user mentions Granola by name, shares a granola.ai link, or asks to "turn my notes into action items." This skill extracts decisions, action items, relationship signals, and drafts follow-up communications, turning raw meeting output into structured next steps.
---

# Meeting Debrief Skill

## Purpose

Take raw meeting notes (typically from Granola: structured markdown with topical headers, bullet takeaways, a "Next Steps" section, and a transcript link) and produce: a clean summary, owned action items, a follow-up email draft, and relationship notes worth remembering. The output should make the 30 minutes after a meeting productive instead of scattered.

---

## Step 1: Ingest the Notes

Accept input in any of these formats:
- **Granola export** (most common): structured markdown with topic headers, bullet points, and "Next Steps" section with transcript link
- **Raw paste**: unstructured notes the user typed during the meeting
- **Transcript excerpt**: longer verbatim text from a recording
- **User summary**: "I just met with X and we discussed Y"

If the input is sparse, ask: "Anything else discussed that isn't in the notes? Any commitments made verbally that might not be captured?"

---

## Step 2: Identify Meeting Type and Tailor Output

The output emphasis shifts based on meeting type:

| Meeting Type | Primary Output | Secondary Output |
|-------------|---------------|-----------------|
| **New prospect / intro call** | Follow-up email + relationship notes | Program fit assessment |
| **Partner check-in** | Action items + follow-up email | Relationship notes, items for internal reporting |
| **Program kick-off** | Decision log + action items with owners | Timeline updates, participant notes |
| **Study tour planning** | Logistics action items + shared doc updates | Speaker/visit pipeline status |
| **Corporate / foundation pitch** | Follow-up email + proposal next steps | Budget/scope notes |
| **Cross-functional internal** | Action items with owners + decisions | Blockers to escalate |
| **1-on-1 (direct report)** | Action items + development notes | Wins to celebrate, concerns to monitor |
| **1-on-1 (manager)** | Your action items + decisions made | Topics to revisit next time |
| **Finance / accounting** | Action items + budget decisions | Open invoices, deadline tracking |
| **Webinar / event debrief** | Attendee feedback + what worked/didn't | Content to repurpose, follow-up with speakers |

---

## Step 3: Extract and Structure

Parse the notes and produce these sections:

### 3a. Summary
2-3 sentences. What was this meeting about, who was there, what was the headline outcome. Written so that someone who wasn't in the room (a colleague, your manager, headquarters) immediately understands what happened.

### 3b. Decisions Made
Bullet list of anything that was agreed, confirmed, or ruled out. Each decision should be stated as a clear fact:
- ✅ "Workshop dates confirmed: week of March 9"
- ✅ "Speaker fee split 50/50 between the two partners"
- ✅ "Anna will present at the July session"
- ❌ Not: "We talked about dates" (that's a topic, not a decision)

If no decisions were made, say so explicitly; that itself is useful information.

### 3c. Action Items
Each action item must have:
- **What** (specific, verifiable task)
- **Who** (owner: use names, not "we")
- **When** (deadline, or "next meeting" if no date set)

Format:
```
- [ ] [Task description]: **[Owner]** by [deadline]
```

Separate into "Your actions" and "Their actions" so the user knows what they owe vs what they're waiting on.

### 3d. Relationship Notes
Surface any personal or contextual details worth remembering for future interactions. These are the "unreasonable hospitality" signals, the details that make the next interaction feel human:

- Travel plans mentioned ("In Zurich for two weeks in July")
- Personal milestones ("Just changed jobs", "first time visiting the city")
- Interests or passions beyond work ("interested in privacy-first AI", "working with a local science museum")
- Concerns or sensitivities ("budget is tight this quarter", "new to AI tooling")
- Connections offered or requested ("looking for speaking opportunities in Europe")

If nothing personal surfaced, skip this section. Don't fabricate warmth.

### 3e. Follow-Up Email Draft
Draft a follow-up email appropriate to the meeting type:

**For external meetings:**
- Warm but professional tone
- Reference one specific thing from the conversation (not generic)
- Restate any commitments made on both sides
- Clear next step with a date or trigger
- Offer to share relevant resources (program info, past reports, introductions)

**For internal meetings:**
- Brief, action-oriented
- Focus on "here's what we agreed, here's who owns what"
- Flag any blockers or decisions needed from others

**Tone calibration:** The work sits in a diplomatic-adjacent context. Emails should feel warm, competent, and internationally fluent: not overly casual (no "Hey!") but not stiff either. Match the formality level of the person you're writing to.

### 3f. Reporting Extract (when relevant)
For external meetings, partnerships, and program milestones, generate a 2-3 line extract formatted for internal reporting to headquarters or your manager:

```
[Date]: [Meeting type] with [Org/Person]
[One-line outcome]
[Status: Active / Follow-up needed / On hold]
```

---

## Step 4: Deliver and Offer Next Steps

Present the structured debrief, then offer:
- "Want me to send the follow-up email?" (if email tool available)
- "Should I add these action items to your task tracker?"
- "Want me to save the relationship notes for next time you meet [person]?"
- "Need a brief for the next meeting with them?" (hand off to the meeting-briefing skill)

---

## Granola-Specific Parsing Notes

Granola exports follow a consistent pattern:
- **Topic headers** (## or bold text) group related discussion points
- **Bullet points** under each topic are concise takeaways (not raw transcript)
- **"Next Steps"** section at the end contains action items, usually with implied owners
- **Transcript link** at the bottom (granola.ai URL): reference it but don't fetch unless asked
- Notes are topical, not chronological. Don't assume bullet order = discussion order

When parsing Granola notes:
- The "Next Steps" bullets often embed ownership in the text (e.g., "Anna to send a short blurb"): extract the owner
- If a bullet under a topic header contains a decision, pull it into the Decisions section even if it's not in "Next Steps"
- Personal/relationship details are often buried in context bullets, not called out separately, so scan for them

---

## What This Skill Does NOT Do

- Does not join or record meetings (Granola handles that)
- Does not replace the user's judgment on tone or relationship dynamics
- Does not auto-send emails without user approval
- Does not generate the pre-meeting brief (hand off to meeting-briefing skill)
