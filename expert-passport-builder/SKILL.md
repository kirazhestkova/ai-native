---
name: expert-passport-builder
description: Build or revise a reusable AI expert with a specific decision method, evidence-backed influences, clear boundaries, acceptance criteria, and a learning log. Use when someone asks to create, hire, design, or improve an AI expert, advisor, specialist, or persona. Do not use for ordinary one-off advice from an existing expert.
---

# Expert Passport Builder

Create an expert that can make and defend domain decisions, rather than a generic role prompt. The deliverable is an **Expertise Passport** that explains the expert's mandate, reasoning method, standards, boundaries, and how its work will be judged. The same passport can later be adapted into an agent instruction, a skill, or a prompt.

Read [the passport template](references/passport-template.md) when drafting an expert. Adapt its headings to the user's actual use case; keep the decision method, evidence, boundaries, and evaluation explicit.

## 1. Define the seat

Use the user's request and available project material to establish:

- **Goal:** the outcome this expert should help achieve.
- **Work:** the decisions or artifacts it owns, plus a realistic first assignment.
- **Audience:** who uses its work or is affected by it.
- **Gap:** the judgment or capacity the user needs from this expert.
- **Boundary:** what remains with the user, other experts, or other tools.

Read any supplied job description, contract, project plan, or example before inferring the mandate. Distinguish documented facts from assumptions. Ask only for missing information that would materially change the design. If two disciplines overlap, decide whether one expert can own the whole outcome or whether separate experts need a handoff. Confirm ambiguous numbers before using them as targets.

Summarize the seat briefly. If the user has already given a clear brief or asked for immediate execution, proceed; do not force a discovery interview.

Check that the seat will be used often enough to justify standing instructions. For a single small task, a focused prompt may serve the user better; say so and still build the passport if they want one.

## 2. Build the method from evidence

Identify the domain's useful methods, cases, and sources. When the user wants an expert inspired by named practitioners, research their published work and documented results. Model **methods and decisions**, never a person's identity or purported private thoughts. Do not impersonate a living person or invent quotes.

For each proposed influence, capture the method worth borrowing, a concrete case or artifact, and source links. Label weak or unavailable evidence. Verify time-sensitive claims, such as current roles, before including them. If research access is unavailable, say which claims remain unverified and avoid presenting them as established. Let the user approve proposed people before making them standing influences. People the user named are already part of the brief; any additional people remain proposals until accepted. A named influence is optional when a well-supported discipline method is a better fit.

Keep the influence set coherent. If several approaches conflict, state which one governs routine decisions and when another is used. Do not treat reputation alone as proof that a method works.

## 3. Write the passport

Build the passport around the **discipline** when the craft is reusable. Put the current project in a separate assignment section. Make these elements operational:

1. A one-sentence lens and the questions the expert checks before acting.
2. A decision procedure: inputs → options → choice → evidence → uncertainty → next action.
3. Signature moves, standards, and a guard against the domain's common failure mode.
4. Red lines, handoffs, and decisions reserved for the user.
5. A small outcome scorecard measuring the expert's own usefulness, with anti-gaming safeguards. Do not invent baseline values or targets.
6. Acceptance criteria for its first real deliverable. Match the review effort to the stakes; a separate reviewer is useful for consequential work but is not a universal requirement.

If a source library, method, or tool genuinely improves the expert's decisions, link it as a toolbox. Mark costs, access requirements, and stale-source risks. Avoid adding tools merely to make the persona look sophisticated.

## 4. Save and use it

Follow the user's specified repository or workspace layout. If none exists, offer a self-contained folder such as `experts/<expert-name>/` with:

- `passport.md` — operating specification and source links.
- `log.md` — dated tasks, advice or artifacts, and observed outcomes.
- `reflection.md` — recurring failures and candidate passport improvements.

If the user is building several experts, keep a roster index and a short **builder log** alongside the expert folders. The builder log records discovery choices, sources accepted or rejected, and lessons about the *creation method*. Each expert's own log records how that expert performs. Read the relevant log before repeating either kind of work.

Create files only when the user asked for a durable expert or repository artifact. Otherwise deliver the passport in the requested format. Add an index entry only if the host project already uses one. Do not create or modify agent-wide rules, publish, install, or deploy without the user's authorization.

On later consultations, read the passport and any available log and reflection first. Record what happened after consequential use. Suggest passport changes when evidence warrants them; apply changes under the host project's normal edit rules. Keep observations distinct from edits to the expert's standing instructions.

## Quality check

Before handing off, try the passport against the first assignment. Can another agent tell what evidence to gather, how to choose between plausible options, what to reject, when to defer to the user, and how success will be measured? If the answer is only “act like a senior expert,” revise it. Check that all influence claims have sources or uncertainty labels and that no private project details were copied into a reusable package.
