---
name: second-brain-builder
description: |
  Interviews a person about how they actually work, then produces a personalised Second Brain implementation plan as a PDF — architecture, core documents, and an automation roadmap — that their own AI agent can implement afterwards. Inspired by the PARA method, adapted for a world where humans and AI agents share one knowledge base. Triggers when the user mentions: second brain, PARA method, Obsidian vault setup, knowledge management system, organize my digital life, personal knowledge base, building a second brain, Tiago Forte, or wants to structure their notes/ideas/projects so AI agents can use them. Also triggers when someone asks to audit or redesign an existing vault. This skill plans; it does not build.
---

# Second Brain Builder

Interview a person, then hand them a plan.

This skill produces **one deliverable: a proposal PDF** — a personalised architecture for a Second Brain, written so the user's own AI agent can implement it step by step afterwards.

It does not create folders. It does not write their documents. It asks, then designs, then hands over.

## What you're actually building (no app required)

A Second Brain here is **plain Markdown files in plain folders on their own disk**. Nothing proprietary, nothing to be locked into, readable by any editor and by any AI agent with file access.

That matters for the whole design: the system has to survive whichever tool they use this year.

**Obsidian is the recommended reader, not a requirement.** It's a free app that opens a folder of Markdown files and adds linking, search and a graph view on top — [obsidian.md](https://obsidian.md), free for personal use, on Mac, Windows, Linux, iOS and Android. Its paid Sync service is optional; any file-sync method works, with one exception noted below for code.

If someone already lives in VS Code, Logseq, iA Writer, or just Finder, the plan works unchanged. Recommend Obsidian when they have no preference, because mobile capture and backlinks are the two things that make the system stick — but never make the plan depend on it. If they'd rather not install anything, say so plainly in the plan and describe the structure as folders.

## Why the plan comes first

Most people start a knowledge system by copying someone else's folder tree. It rots within a month, because a structure that matches how someone else thinks will quietly fight how you think.

There is no universal template. So the only honest first step is an interview.

The second reason for stopping at a plan: implementation belongs in the user's own environment, on their own files, under their supervision. A plan is reviewable before anything happens. A build is reviewable only once it already has.

## What problems this solves

Present these early — people recognise themselves in several, and it clarifies what the plan is for.

- **Ideas die between capture and action.** An idea arrives while walking. A week later it's gone.
- **You repeat yourself to every AI agent.** Every new session, you re-explain who you are and what you're working on.
- **Your knowledge is scattered across ten apps.** Finding something you wrote is harder than writing it again.
- **You organise instead of creating.** You build a perfect folder system, then never use it.
- **Your projects have no memory.** You finish something and the research, decisions and mistakes vanish into a folder you'll never reopen.
- **AI agents can't see your bigger picture.** An agent can write a good email without knowing your goals, or whether the task even serves them.
- **You don't follow through on what you learn.** Books, talks, courses — consumed, then nothing changes.

Trace every design decision in the plan back to one of these. If a folder doesn't solve a problem they actually named, don't propose it.

## Three principles behind every plan

1. **Start from Zero.** Archive everything first. Bring forward only what is alive right now. The archive stays searchable, so nothing is lost. This prevents the classic trap of organising old clutter instead of building something usable.
2. **Machines Read This Too.** Every important document is written so both the person and their agents can use it. Core documents become the context an agent loads before it acts.
3. **Minimum Viable Structure.** Exactly as many folders as are useful, not one more. No elaborate tagging, no maintenance rituals. The golden rule: if it takes more than 30 seconds to decide where something goes, it goes in Inbox.

---

## Process

```
Phase 1: Discovery interview   → understand how this person actually works
Phase 2: Architecture design   → shape a structure from their answers
Phase 3: Produce the plan PDF  → the deliverable, written for their agent to implement
```

---

## Phase 1 — Discovery interview

Understand how the person thinks, works and creates *before* proposing anything.

**Ask one question at a time.** Never dump a list. Use structured choices where they help, and let them free-type where the answer is personal. Follow the thread when something interesting surfaces — this is a conversation, not a form.

### Questions to cover

**Projects — what's active right now?**
- What are you actively working on this week? Not someday projects — real, current work.
- Which of these have a clear goal and deadline? Which are ongoing?
- Any creative projects — writing, content, courses?

**Code — do you build anything?**

Ask this properly if the answer to "do you write code, or work with agents that do?" is yes. It changes the architecture, not just a folder.

- Where do your repos live on disk, and are they in Git?
- Are any of them inside a cloud-synced folder like iCloud Drive, Dropbox or OneDrive?
- Do your coding agents have any project context today, or do you re-explain the project each session?
- Do you keep project decisions, research and diaries anywhere, or do they live in the code and your head?

**Capture — how do ideas arrive?**
- When you have an idea, where does it go right now?
- Do you use voice capture? When, and with what?
- What happens to ideas after you capture them? Do they get lost?
- How do your files sync between devices today — iCloud, Dropbox, Google Drive, something paid, nothing at all? Ask everyone, not only people who code. The plan has to name a sync method, and guessing it produces a plan that quietly doesn't fit.

**Knowledge sources — what do you consume?**
- Books? Do you take notes from them?
- YouTube, podcasts, newsletters, social media? In which languages?
- Courses? How do you capture what you learn?
- Newsletters or subscriptions worth mining?

**Work style — how do you think?**
- Rigid structure or organic mess?
- How much time will you actually spend organising? Be honest.
- What note-taking tool do you use now, and what's wrong with it?
- Do you work with AI agents? Do you want them reading your knowledge?

**Life areas — what matters beyond work?**
- What ongoing responsibilities do you maintain? Health, finance, relationships, learning.
- Any personal development practices — journalling, goals tracking?
- Do you track personal data?

**Collaboration — who else is involved?**
- Teams? Shared documents?
- Cloud tools that should link in?
- Call recording or meeting transcription?

**Goals — what's the dream?**
- If this system worked perfectly, what would be different in your life?
- What's the biggest frustration with your current approach?

### Interview tips

- Listen for the difference between **Projects** (has a deadline) and **Areas** (ongoing responsibility). Most people conflate them. Clarify gently.
- Watch for **Education** as a separate category — many people take courses and want them tracked apart from projects.
- Note any inner-work or personal-development practice. These usually need their own space.
- "I hate organising" is a design constraint, not a complaint. Build for minimum maintenance and maximum automation.
- Identify the tools they already have strong habits with. Don't fight those habits — integrate them.
- Watch for the **over-organiser trap**. If someone is excited about categories and subcategories, redirect. Every folder they create is a folder they maintain.

---

## Phase 2 — Architecture design

Design a PARA-inspired structure adapted to the answers you just heard.

### The starting template

Adapt this. Don't ship it as-is.

```
!Inbox/          ← quick capture, always at the top
_Core/           ← identity documents for humans and AI agents
    About Me.md
    Goals.md
1 Projects/      ← active work with goals and deadlines
2 Areas/         ← ongoing responsibilities, no end date
3 Resources/     ← reference material by topic
4 Education/     ← courses and structured learning (optional)
5 Archive/       ← everything inactive, fully searchable
```

### Adaptation rules

- **Projects** — only genuinely active work. "Someday" belongs as a line in Goals, not a folder. Subfolders one level deep are fine when they match how the person naturally splits the work.
- **Areas** — order by importance to them, never alphabetically. Only areas they actually maintain. No aspirational folders.
- **Resources** — organise by how they consume information. Books, podcasts, people, plus their own domains.
- **Education** — a separate top-level category only if they take multiple courses and want them tracked apart. Ask.
- **Archive** — everything else, out of the way and searchable.

### Two layers, if they write code

If the interview surfaced code projects, the plan needs a two-layer architecture. Notes and repos should not live in the same place, but they must know about each other.

- **Layer 1 — the brain.** The Markdown vault: ideas, plans, knowledge, decisions.
- **Layer 2 — the hands.** Code repos: live locally, synced with Git. **Never inside iCloud, Dropbox or OneDrive** — cloud sync corrupts `.git` folders. Flag this explicitly if the interview found repos in a synced folder; it is the single most damaging thing in a typical setup.

Three bridges connect them:

- **Portal notes** — one note in the vault per code project, with frontmatter carrying the local path, the repo URL and current status. This is how the vault can talk about a project it doesn't contain.
- **An agent file in each repo** (`CLAUDE.md`, `AGENTS.md`, or whatever their tool reads) pointing back at the vault for context, so a coding agent starts informed.
- **A gitignored project folder** inside the repo for project-specific knowledge — decisions, research, a build diary — that belongs with the code rather than in the vault.

The rule underneath: the vault holds *why*, the repo holds *what*, and each points at the other.

### The core documents

The plan specifies these with a skeleton for each. It does **not** write their contents — that's implementation.

**About Me.md** — a machine-readable profile any agent reads before starting work. Their "API documentation." Sections: identity, professional background, current projects, online presence, tone of voice per platform, interests, work style, life context.

**Goals.md** — the living translation of direction into action. A yearly vision cascaded to the current month. Yearly goals should read like directions ("build financial independence"), not tasks ("apply to ten jobs").

### The automation roadmap

From the frictions they named in the interview, propose 2–3 automations to build first and list the rest as later candidates. Every automation gets a status: **ON AIR** or **IN PLAN**.

Common patterns, as illustrations only — every person's list differs:

| Automation | What it does |
|---|---|
| Inbox Sorter | Files captured notes into the right folder |
| Book Harvest | Turns reading notes into reusable assets |
| Call Intelligence | Extracts promises and follow-ups from transcripts |
| News Digest | Curates newsletters and channels by topic |
| Media Journal | Summarises what they watched or listened to |
| Language Coach | Analyses their real speech or writing for improvement |

Rules: automations come from the user's frictions, not from the machine. Start with two or three. They suggest actions rather than take them, and the user approves before anything runs.

---

## Phase 3 — Produce the plan PDF

This is the deliverable. Write it for **two readers**: the person, who needs to understand and approve it, and their **AI agent**, which needs to implement it without making them repeat the interview.

### Structure of the proposal

1. **Vision** — one paragraph, in their words, on what this system is for.
2. **At a glance** — a short table: sync method, structure, core docs, capture method, automations planned.
3. **Philosophy** — the three principles, tied to the problems *they* named.
4. **Vault structure** — the full folder tree, one line per folder on what it does and why it's there for them.
5. **Core documents** — skeletons for About Me and Goals, with the sections they need.
6. **Active projects** — the actual project folders to create, from the interview.
7. **Areas, Resources, Education, Archive** — contents, in their order of importance.
8. **Automation roadmap** — the first 2–3 builds plus later candidates, each ON AIR or IN PLAN.
9. **What changes day to day** — concrete before-and-after for their real routines.
10. **Implementation plan** — ordered steps, each tagged with who does it and when.

### The implementation plan matters most

This is what their agent picks up. Every step should be unambiguous and independently executable, tagged `AGENT` or `USER` and `NOW`, `THIS WEEK` or `LATER`. For example:

- `AGENT · NOW` — create the folder tree exactly as specified in section 4.
- `USER · NOW` — set up sync. If the vault sits in an iCloud-watched folder, move it somewhere iCloud ignores. Two sync services on the same files will corrupt data.
- `USER · NOW` — set up capture on their phone. Obsidian mobile if they chose Obsidian; otherwise any editor that can reach the same folder.
- `AGENT · THIS WEEK` — draft About Me by interviewing the user section by section.
- `AGENT · THIS WEEK` — archive existing notes, keeping them searchable.
- `AGENT · LATER` — build the first automation from the roadmap.

Close the plan with a short "how to hand this to your agent" note: point the agent at the PDF, ask it to start with the first `AGENT · NOW` step, and have it confirm each step before moving on.

### The second deliverable — the architecture card

Alongside the PDF, render **one image**: their folder tree plus the one-paragraph vision, on a single screen, 4:5 or square.

This exists because a personalised structure is a portrait of how someone thinks, and people post those. The PDF is private admin; the card is the thing they show a colleague. Without it the skill can be downloaded but not passed on.

Put a small attribution line at the foot of both the card and the PDF:

```
Planned with second-brain-builder · github.com/kirazhestkova/ai-native
```

Then say this once, plainly, when you hand over the files — not as a marketing ask, as an offer:

> If you post your structure, other people can steal the parts that fit them. One line of context is usually enough: *"This is how my work actually splits up — an AI asked me about twenty questions and drew it."*

Never nag. Say it once and let it go.

### Producing the files

Write the proposal as Markdown first, in the conversation, and revise it there until the user is happy. Nothing is saved to disk until they approve it — then write the final Markdown, the PDF and the card together.

Render with whatever the environment offers — a PDF skill if one is available, otherwise `pandoc` or `weasyprint`.

**Fallback that always works:** write a single self-contained HTML file with inline CSS, and tell the user to open it in their browser and use Print → Save as PDF. Assume nothing is installed. The person running this may never have opened a terminal, and the skill's only deliverable must not depend on a toolchain they don't have.

Keep the design plain: readable headings, real tables, nothing decorative that survives badly across renderers. Name the files `Second Brain Plan — <name or date>` and save them where the user asked.

---

## Rules for whoever runs this skill

1. **Never propose structure without understanding the person first.** The interview is the most important phase. A beautiful structure that doesn't match how someone thinks is worse than no structure.
2. **One question at a time.** A list of questions gets a list of shallow answers.
3. **Plan, don't build.** Creating folders, writing their documents and running automations all happen afterwards, by their agent, in their environment.
4. **Listen for hidden categories.** Education, inner work and people/CRM are common needs PARA doesn't name.
5. **Minimum viable structure.** If it takes more than 30 seconds to decide where something goes, it goes in Inbox.
6. **Don't over-engineer the proposal.** A plan they act on this week beats a perfect one they read once.
7. **The system serves the person, not the reverse.** If their natural workflow conflicts with PARA, adapt the system. Never ask them to change how they think.

## After this skill — reflect

When the plan is delivered, reflect briefly with the user: did the interview reach the right things, is anything in the plan wrong for them, what would they tune. Capture recurring lessons somewhere durable, and change this skill only on their explicit yes.
