# AI workflows

I work on partnerships and programs at Swissnex in San Francisco. I build Claude skills for that work. This repo has three of them, with internal details removed, and notes on how they are used. It’s a personal project, not an official Swissnex resource.

## A meeting, end to end

Most of my week is meetings with partners, funders, and prospects, and the useful work happens just before and just after them. These three skills cover that cycle:

- [`meeting-briefing`](skills/meeting-briefing/SKILL.md) prepares a one-screen brief before a meeting, pulling from calendar, email, documents, past notes, and the web.
- [`meeting-debrief`](skills/meeting-debrief/SKILL.md) turns meeting notes (usually from Granola) into decisions, action items with owners, a follow-up email, and notes worth remembering about the people involved.
- [`intro-email`](skills/intro-email/SKILL.md) drafts the introductions I promise in meetings, following the structure of an intro I send regularly.

They hand off to each other: the debrief offers a brief for the next meeting, and the brief offers a debrief template for afterwards.

**The problem:** [One or two sentences in your words: what took time or slipped before you built these.]

**Who uses them and what changed:** [Who besides you, how often, and what changed. Only numbers you measured.]

**What didn't work at first:** [One failure and the fix. If a rule like "don't fabricate warmth" came from a real mistake, tell that story.]

[90-second video: notes in, debrief and follow-up email out]

## Using these skills

Each folder in `/skills` is a Claude skill: a `SKILL.md` file whose short description tells Claude when to use it. Download a folder and add it as a skill in Claude. In `meeting-briefing`, replace the program list with your own.

For this public version I removed my employer's internal details and real names, and replaced the real examples with invented ones.

## License

MIT
