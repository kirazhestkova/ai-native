---
name: team-lead-codex
description: >-
  Plan and coordinate Codex project work: builds, refactors, migrations, research
  or document batches, multi-step tasks and team lead mode. Also use to configure
  saved Team Lead project preferences and standing invocation rules. Choose SOLO
  or bounded delegation using available models only when total token use is
  expected not to increase at unchanged quality and safety. Other task skills
  retain ownership of their workflows.
license: MIT
metadata:
  author: "Kira Zhestkova"
  version: "1.2.0"
  last-updated: "2026-10-17"
  platform: codex
---

# Team Lead for Codex

Coordinate who does the work, what each task needs, and how the result is checked.
This skill works with an ordinary project folder and the user's existing process.
It needs no personal knowledge base, profile files, other skills or named personas.
An applicable task skill keeps ownership of its workflow and required reviews.

Priority: preserve quality and safety, then reduce total tokens without a planned
increase. Keep the lead's context clear within that constraint. Lower model prices
or a smaller main conversation do not prove fewer total tokens.

## 1. Establish the project context

Use the current workspace, the user's request and context already supplied. Read
applicable project instructions, such as `AGENTS.md`, and the relevant parts of
the README or existing plan. Load context once and reuse it. Inspect only the
files needed for the task; do not search a user's home directory for background.

On first use in a project, resolve the following from existing evidence:

| Need | Default when the task makes it clear |
| --- | --- |
| Project and permitted scope | The current workspace and the requested changes |
| Outcome and acceptance | The user's stated result and relevant project checks |
| Models and delegation | Current chat model leads; select workers from the runtime's available models only if the token gate passes |
| Reviews and sensitive actions | Applicable project rules and the user's existing authorization |
| Continuation records | Existing plan, task tracker or handoff document, when available |

Ask only about missing information that changes the next decision, one question
at a time. Start with the most consequential gap, for example: "Which project
should I work in?" Ask about the outcome next only if it remains unclear. A complete
task brief needs no setup interview. An absent optional plan, reviewer preference
or model preference does not block ordinary work.

Read project preferences referenced by the applicable instructions or a root
`TEAM_LEAD.md` when present. Reuse approved defaults, subject to current
instructions and the user's current task.
When no equivalent saved setup is present, offer optional persistence once in
the conversation, at a point that does not interrupt the requested work. The
user can save project preferences, add a standing invocation rule, choose both,
or keep the session temporary. Declining creates no files and does not block work.

Before preparing or applying saved setup, load
[Optional project setup](references/project-setup.md). Show the exact proposed
file paths and changes, then obtain explicit approval before writing. Approval
to discuss setup does not approve an unseen agent-rule edit. Reuse a prior
approval of the displayed changes without asking again. Never silently change
personal/global agent rules, install hooks, alter model settings or connect an
account. Keep unrelated personal information out of project records.

For a project outside the current workspace, resolve the intended location before
writing. Work without a filesystem can use the documents supplied in the chat.

## 2. Announce SOLO or LEAD

Before substantive execution, state `team-lead-codex v1.2.0`, complexity, risk and
the decision in one line:

- C0: one step; C1: bounded routine work; C2: several work packages; C3: a program.
- R0: reversible private work; R1: shared or user-facing work; R2: money,
  credentials, personal data, production or destructive actions.

Use SOLO when the task is small, tightly coupled or fails the token gate. For
LEAD, add a compact map: package → executor/model/effort → acceptance check.
State a runtime limitation when it affects the decision. Complexity alone never
forces delegation. Continue work already authorized; ask for approval only when
needed by applicable rules or a step exceeds the authorized scope.

## 3. Apply the total-token gate

1. Use deterministic tools for searches, counts, diffs and transformations when
   they can complete the task reliably. Bound output before bringing it into chat.
2. Compare solo work with the complete delegation route: copied context, briefs,
   model input/output and reasoning, steering, summaries, lead verification,
   required independent review and likely retries. Count cached input as input;
   do not count reasoning twice when it is already included in output totals.
3. Delegate only with a credible, conservative expectation of no more total tokens
   at the same quality and safety. Prefer a clear saving. If uncertain, stay SOLO.
   Parallel speed or less lead context alone does not pass this gate.
4. Use prior evidence for similar tasks when available. A first useful pilot can
   establish whether a route works; do not duplicate full tasks to manufacture a
   baseline. Inspect the first artifact before extending delegation.
5. If observed overhead or corrections invalidate the estimate, stop expanding
   that route and complete the remaining work through a better route. Retain the
   required checks and report any observed overrun.

Estimates are not measurements. Without suitable usage telemetry and a comparable
baseline, report savings as unverified. Never invent a percentage or guarantee.
Required independent review belongs in both routes and cannot be dropped to save
tokens. A mandatory review still needs an independent reviewer when the work is
otherwise SOLO.

## 4. Choose executors from the actual runtime

| Role | Selection | Responsibility |
| --- | --- | --- |
| Lead | The user's current chat model | Decisions, ambiguity, design judgment, sensitive steps and final acceptance |
| Bounded worker | An available model suited to the task | Well-specified implementation, reasoning or synthesis |
| Mechanical worker | An available model adequate for narrow, verifiable work | Extraction and repetitive work that tools alone cannot finish |

Respect explicit user preferences. A skill cannot switch the lead model. Do not
claim to know the actual model from a preference or role label alone. Resolve a
known mismatch with the user before work that depends on that model choice.

For workers, inspect exposed runtime tools and supported model/effort choices.
Use subagent tools, not new user-owned chats. Select model and reasoning effort
explicitly and give only the context the task needs. Use a fresh context when
supported. Follow the exposed schema rather than assuming a particular tool name.
If explicit worker selection or delegation is unavailable, stay SOLO and disclose
the limitation; a required independent gate remains unresolved if no reviewer is
available. Never silently substitute an unavailable requested model.

Start with one worker. Add workers only for independent packages that separately
pass the token gate; use at most three concurrent workers, within runtime limits.
Workers do not spawn more agents. Shared mutable files are handled sequentially;
give writers separate files or worktrees when isolation is needed.

## 5. Brief, execute and inspect

- Give each worker one self-contained brief: objective, bounded inputs, permitted
  actions, forbidden side effects, output location/shape, acceptance checks and
  stop conditions. Supply facts with evidence; do not preload a reviewer's verdict.
- Follow the project's existing requirements and planning process. When no formal
  process exists, use a short task plan and concrete acceptance checks; do not
  require a new framework, expert roster or documentation hierarchy.
- Pass only necessary data. Keep credentials and sensitive operations in the
  lead. A worker inherits no additional permission from its brief. Avoid secrets
  and unnecessary personal information in prompts, logs and outputs.
- Save requested artifacts and meaningful checkpoints before reporting back. A
  worker returns results, evidence locations, checks, uncertainty and remaining
  work. Keep raw logs and large datasets out of the lead's context unless needed.
- Inspect the actual result, not just the worker's account. Use machine checks
  where useful, then inspect the relevant content or user path. Resolve any
  discrepancy with more evidence before accepting it.
- Keep acceptance criteria constant across models. Mechanical work must be exact;
  qualitative requirements must all pass. Investigate input, tool and instruction
  failures before attributing a failure to the model.
- Check a material model or workflow change against the existing acceptance
  contract. After a worker failure, inspect saved state before resuming. Retry a
  justified infrastructure failure at most once; the same failure twice ends
  delegation of that task class.

## 6. Preserve review and approval boundaries

Keep money, credentials, personal data, publishing, deployment, merges and
destructive steps in the lead, within existing authorization and access limits.
Preparing a result does not authorize publishing it. Avoid putting private inputs
into shared artifacts, even when the working conversation can access them.

Preserve independent gates required by the project or owning task skill. Give
the judge the artifact, requirements and captured evidence, separately from the
author's conclusions. Preserve the actual criteria and hard failures; do not
invent a passing score or treat self-review as an independent pass.

For engineering, production or visual work, load
[Engineering and visual checks](references/engineering-gates.md). Otherwise keep
that reference out of context.

After three failed review rounds on the same issue, surface the unresolved
decision to the user with evidence and options. A retry limit or budget limit
does not make a failed gate pass. Stop redundant reviews after independent
acceptance, or when the affected scope is explicitly removed or deferred.

## 7. Close with evidence and useful state

Report briefly: item/status → actual executor → verification → unresolved work.
Include fallbacks and required decisions. Report measured lead/worker token
totals only when exposed, counting overlapping fields once; otherwise state that
totals are unavailable. Never infer usage from item counts or text length.

Use existing project records for continuation state when their maintenance is in
scope. A handoff records completed work, remaining work, evidence and required
approvals. Do not create another tracking system just for this skill.

Suggest reusable improvements when a run exposes one. Keep learning local to the
project; do not silently edit this skill, the user's agent rules or installed
copies. Review such changes with the user and maintain one canonical source.

Copyright (c) 2026 Kira Zhestkova. Released under the [MIT License](LICENSE).
