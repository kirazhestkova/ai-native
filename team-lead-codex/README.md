# Team Lead for Codex

I built this skill to make delegation a decision an agent has to justify. It
checks the task, chooses SOLO or LEAD, gives each worker a bounded brief, and
verifies the result before calling the work done.

The priority is quality and safety, followed by total token use. A cheaper model
alone does not prove a saving. Worker context, instructions, review and retries
all count. If the comparison is uncertain, the agent stays solo.

This public edition works with your own project folder, documents and team
process. It requires no Second Brain, personal profile, external expert library
or particular folder structure.

## First use

Open the project you want to work on and describe the outcome:

```text
Use $team-lead-codex to help with this project.
I want to [describe the result]. Done means [acceptance criteria].
Read the project instructions first, then decide SOLO or LEAD.
```

The skill reads the relevant project instructions and uses what you have already
told it. If essential context is missing, it asks one question at a time. Questions
can cover which project to use, what counts as done, model constraints, and any
required reviews or approval boundaries. A complete brief skips the interview.

You can supply preferences in the same message:

```text
Work in the current folder. Keep the current chat model as lead.
Use workers only if the total-token comparison supports it.
Keep deployment for my review. Record progress in the existing project plan.
```

Answers stay in the conversation unless you approve saving project setup. On
first use without existing setup, the skill offers to prepare project preferences
and a standing Team Lead rule. For a small task, it can offer this after finishing
the work. You can save preferences, add the rule, choose both, or skip.

## Reuse setup in new chats

If you opt in, the skill shows the exact file paths and proposed changes before
writing anything. It uses an existing project document for preferences or proposes
`TEAM_LEAD.md` at the project root. Preferences cover the project, model choices,
checks, reviews and action boundaries. Personal profiles and secrets stay out.

The standing rule goes in the project's effective `AGENTS.md` or equivalent
instruction file. A typical addition is:

```text
Before substantive project work, use the installed team-lead-codex skill
to decide SOLO or LEAD. Read TEAM_LEAD.md for approved project preferences.
```

After you approve the displayed changes, the skill saves and checks them. Future
invocations reuse the preferences. Existing equivalent setup is left in place,
and the setup offer is skipped. If you decline, no files are created; the choice
is remembered for this conversation. A later chat cannot remember an unsaved
choice and may offer again.

Saving preferences alone does not activate the skill. Adding the standing rule
provides durable project guidance for future Codex sessions; activation remains
instruction-based and requires the skill to be installed and available. It is
not an enforced startup hook or a guarantee for every message. A new session may
be needed to load updated project instructions. See
[OpenAI's project-instruction documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

The setup is scoped to your project. It preserves existing rules, shows a new
preview if the files change before approval, and never modifies global agent
settings or publishes preferences without separate authorization. A chat without
file access can receive the setup text to save later, but no persistence is claimed.

## What to expect

| Stage | Result |
| --- | --- |
| Triage | Complexity, risk and a one-line SOLO or LEAD decision with a reason |
| Delegation, when justified | Work packages, actual models/efforts and acceptance checks |
| Verification | Inspection of artifacts and relevant user paths; independent review where required |
| Handoff | Completed work, checks, actual executors, unresolved decisions and available usage totals |

Small tasks stay in the main conversation. Delegated work starts with one worker
and uses at most three at once, within runtime limits. The lead keeps judgment,
sensitive actions and final acceptance. Other task skills keep their workflows.

Savings are unverified unless comparable usage evidence supports them. The skill
cannot guarantee a lower bill, fewer tokens or faster completion.

## Install in Codex

Download this repository or clone it:

```bash
git clone https://github.com/kirazhestkova/ai-native.git
```

Copy the complete `team-lead-codex` folder into one of these locations:

- Your project: `<project>/.agents/skills/team-lead-codex/`.
- Your personal skills: `~/.agents/skills/team-lead-codex/`.

For a fresh personal installation, from the cloned repository:

```bash
mkdir -p ~/.agents/skills
cp -R -n team-lead-codex ~/.agents/skills/
```

If a copy already exists, review and update that copy deliberately. Avoid multiple
installed versions with the same skill name. Codex detects skill changes; if it
doesn't appear in the selector, restart Codex. These locations follow
[OpenAI's skill documentation](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills).

This folder is a standalone skill package. It includes `SKILL.md`, this README,
`LICENSE`, optional Codex display metadata and the engineering/setup references. Copy
the whole folder so relative links continue to work.

## Models and tools

The current chat model leads. Workers use models available in your runtime,
selected explicitly for the task. No particular model family is required.

Delegation needs exposed subagent tools and explicit worker model/effort selection.
If those capabilities are unavailable, the skill works solo and explains the
limitation. It cannot enable tools, switch the lead model or grant permissions.
See [OpenAI's subagent documentation](https://learn.chatgpt.com/docs/agent-configuration/subagents)
for runtime configuration.

Independent review required by your project remains required in solo mode.
Production changes and engineering involving money, authentication, credentials
or personal data also require an independent reviewer under this skill. If no
qualified reviewer is available, the skill reports that gate as unresolved.

## Privacy and maintenance

Use project context relevant to the task. Keep credentials and unnecessary
personal information out of worker briefs, shared evidence and deliverables.
Setup answers belong in your conversation or your chosen project records.

Maintain one canonical copy and review changes before updating installations.
The skill can suggest improvements after a run; it does not rewrite its own
instructions or your project rules without your approval.

## Copyright and license

Copyright (c) 2026 Kira Zhestkova.

Released under the [MIT License](LICENSE), matching the other skills in this
repository. You may use, modify and share it while retaining the copyright and
license notice.

Created by [Kira Zhestkova](https://www.linkedin.com/in/kira-zhestkova-ainative/).
Public edition: 1.2.0.
