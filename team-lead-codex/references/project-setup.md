# Optional project setup

Load when a user wants reusable project preferences or a standing Team Lead rule.
The current task can proceed without either. This is project setup, not a personal
profile or an installation/configuration workflow.

## Offer once, then prepare a reviewable change

First inspect existing project guidance and any referenced Team Lead preferences.
Reuse equivalent setup. Remember a decline for this conversation; do not save a
decline marker or repeat the offer during the same conversation. A later chat
cannot know an unsaved preference, so it may offer again if no saved setup exists.

When an offer is appropriate, ask one question, for example:

> Would you like me to prepare project preferences and a standing Team Lead rule
> for review, or keep this session temporary?

Let the user choose preferences only, the rule only, both, or skip. Offer at the
handoff for a small task rather than interrupting its execution. If the user
already requested saved setup, proceed to the preview without asking this again.

Use facts already supplied. Ask one question at a time for a missing decision
that affects what will be saved. Do not request personal history, a knowledge
base or accounts. Do not fill unknown fields with invented preferences.

## Choose project-scoped destinations

Use an existing appropriate project document for preferences when available.
Otherwise propose `TEAM_LEAD.md` at the project root; it is optional. Record only
useful project defaults: scope, model constraints, acceptance checks, review and
action boundaries, and existing progress-record locations. Omit unknown fields,
credentials, personal figures and copied conversation transcripts.

For the standing rule, inspect the effective project instruction chain, including
`AGENTS.override.md` and nested scopes. Normally propose a small addition to the
project's `AGENTS.md`. An active override can make that file ineffective; explain
the scope and propose the effective project instruction file instead. Do not edit
both automatically or touch global instructions. Resolve symlinks before proposing
a write; a project path does not authorize editing an external target.

Identify whether a proposed destination is shared/tracked or local. Keep private
answers in the conversation or a user-chosen private location. Hiding a filename
does not make it private. Any needed ignore-file change belongs in the preview
and approval too. Saving setup does not authorize committing or publishing it.

## Show exact contents and get approval

Show the exact file paths and diff, or full contents for new files. Preserve
existing guidance; do not replace a whole rules file to add a short section.
For both options, a standing section can look like this, using the actual relative
path to the approved preferences file:

```markdown
## Team Lead

Before substantive project work, use the installed `team-lead-codex` skill to
decide SOLO or LEAD. Read `TEAM_LEAD.md` for approved project preferences.
Keep task-specific workflows and review requirements in force. If the skill is
unavailable, say so and continue under the existing project rules.
```

For the rule-only option, omit the preferences-file sentence. For preferences
only, do not change any agent rules; explain that the file will be reused when
the skill is invoked and reads it, but does not itself trigger activation. The
skill should inspect an existing root `TEAM_LEAD.md` when it is selected, even
without a standing rule. Do not search unrelated folders for a preferences file.

Ask one direct question: "Apply these exact project changes?" Wait for explicit
approval before writes, including creation of a new `AGENTS.md`. If the displayed
changes are already approved, apply them without asking again. Approval for one
file is not approval for another; if the user approves only part, apply only that
part. Materially changed content needs a new preview and approval.

Before writing, re-read the target files. If they changed since the preview,
prepare a revised diff and obtain approval for it. Preserve unrelated content,
avoid duplicate equivalent sections and write only the approved scope.

## Verify reuse, not just file creation

Re-read the saved files. Verify the approved additions, preserved existing
instructions, relative paths and absence of private material. An equivalent
setup on a repeat run needs no write and no new setup offer. An adjustment
requested later follows the same preview-and-approval process.

On future invocations, load the approved preferences from the instruction link
or root `TEAM_LEAD.md`. Reuse them without repeating answered setup questions.
Current task instructions and applicable project rules take precedence; saved
preferences never grant new permissions or make unavailable models usable.

Report the exact files changed and scope. Explain that the standing rule is
durable guidance for future Codex sessions in that project, subject to the
runtime's instruction discovery. It is not an enforced startup hook or a promise
that every message will invoke this skill. The skill must be installed and
available there. A new session may be needed to load changed project guidance.
For a chat-only project or unavailable filesystem, show the proposed text in chat
and state that it has not been saved. Never claim cross-chat persistence without
saved files or claim a fresh-session activation test that was not performed.
