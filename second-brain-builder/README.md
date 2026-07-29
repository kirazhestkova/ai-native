# second-brain-builder

**An AI interviews you about how you actually work, then hands you a build plan your own agent can execute.**

Not a template. The structure comes out of your answers — what's live this week, where your ideas land now, how much organising you'll realistically do.

Built and used by [Kira Zhestkova](https://www.linkedin.com/in/kira-zhestkova-ainative/), ex-CMO at Skyeng, now building an AI product solo with agents. The plan this skill produced for her proposed 13 automations. Eleven weeks later she runs 26 skills off that structure.

It doesn't create folders or write your documents. It asks, designs, and hands over two files: a **plan PDF** for your agent, and a one-screen **architecture card** of your structure.

## What you're actually building

Plain Markdown files in plain folders, on your own disk. Nothing proprietary, nothing to be locked into, readable by any editor and by any AI agent with file access.

**No particular app is required.** [Obsidian](https://obsidian.md) is what I'd recommend if you have no preference — it's free for personal use, opens a folder of Markdown files, and adds linking, search and mobile capture on top. But VS Code, Logseq, iA Writer or plain Finder all work, and the plan doesn't change.

## Why an interview instead of a template

Most people start a knowledge system by copying someone else's folder tree. It rots within a month, because a structure that matches how someone else thinks will quietly fight how you think.

There's no universal template. So the only honest first step is a conversation about how you actually work.

The second reason it stops at a plan: implementation belongs on your files, in your environment, under your supervision. A plan is reviewable *before* anything happens.

## How it runs

| Phase | What happens |
|-------|--------------|
| 1 · Discovery interview | One question at a time — your active projects, where ideas land now, what you read, how much organising you'll realistically do |
| 2 · Architecture design | A PARA-inspired structure shaped from your answers, not a copied tree |
| 3 · The plan | A proposal PDF: folder structure, core document skeletons, automation roadmap, and a step-by-step implementation list tagged `AGENT` / `USER` and `NOW` / `THIS WEEK` / `LATER`. Plus a one-screen card of your architecture |

Then you hand the PDF to your own agent and it builds, one confirmed step at a time.

## What the plan looks like

The folder tree is the part you'll recognise yourself in. A rough shape, before it's adapted to you:

```
!Inbox/          quick capture — anything you can't file in 30 seconds
_Core/           who you are and where you're going (your agents read this first)
1 Projects/      work with a finish line
2 Areas/         responsibilities with no end date
3 Resources/     material you'll want again
4 Education/     courses, if you take them
5 Archive/       everything inactive, still searchable
```

Underneath it, the implementation list — the part your agent actually executes:

```
AGENT · NOW         create the folder tree in section 4
USER  · NOW         choose where the vault lives and how it syncs
AGENT · THIS WEEK   draft About Me by interviewing you section by section
AGENT · LATER       build the first automation from the roadmap
```

## Three principles behind every plan

1. **Start from Zero.** Archive everything first. Bring forward only what's alive right now. The archive stays searchable, so nothing is lost.
2. **Machines Read This Too.** Every important document is written so both you and your agents can use it.
3. **Minimum Viable Structure.** Exactly as many folders as are useful, not one more. The golden rule: if it takes more than 30 seconds to decide where something goes, it goes in Inbox.

## Four questions worth answering before you install anything

From Phase 1 — useful on their own, even if you never run the skill:

- What are you working on this week? Not someday — this week.
- When an idea arrives, where does it go right now, and what happens to it after?
- How much time will you actually spend organising? Be honest.
- If this system worked perfectly, what would be different in your life?

## Requirements

- **An AI agent that supports skills** — Claude Code, Cowork, or similar. That's the only hard requirement.
- **A Markdown editor**, once you implement the plan. [Obsidian](https://obsidian.md) is free and recommended; any editor works.
- About an hour for the interview and the plan. Implementation comes after, at your pace.

You don't need to write any code, and you don't need a terminal.

## Install

**The easy way — no terminal.** Paste this to your AI agent:

> Install the skill at https://github.com/kirazhestkova/ai-native/tree/main/second-brain-builder for me, then run it.

Most agents will fetch it and set it up themselves. If yours can't, use the green **Code → Download ZIP** button at the top of the repo, unzip it, and hand your agent the `second-brain-builder` folder.

**If you're comfortable with a terminal:**

```bash
git clone https://github.com/kirazhestkova/ai-native.git
```

Then copy the `second-brain-builder` folder into your agent's skills directory — for Claude Code that's `~/.claude/skills/`. For Cowork, drop the folder into your Cowork skills directory, or zip it with a `.skill` extension and install it. Other agents vary; check your tool's docs for where skills live.

Then ask your agent to plan you a second brain, or invoke the skill by name.

## Credits

Inspired by the PARA method (Tiago Forte), adapted for a world where humans and AI agents share one knowledge base.

Created by **Kira Zhestkova** · [LinkedIn](https://www.linkedin.com/in/kira-zhestkova-ainative/)

## License

MIT — see [LICENSE](./LICENSE).
