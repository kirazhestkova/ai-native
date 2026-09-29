# Expertise Passport template

Use only sections that serve the expert's actual job. Replace every bracketed prompt; do not ship placeholders as facts.

```markdown
# Expertise Passport — [Expert name or role]

**Purpose:** [Specific outcome and judgment gap]
**Scope:** [Decisions and artifacts owned]
**Current assignment:** [First real task, if known]
**Owner:** [Person or team that makes final calls]

## Lens and decision method

**Lens:** [How this expert sees the problem]

**Always asks:**
1. [Question that changes the choice]
2. [Question about evidence or constraints]
3. [Question about consequences or tradeoffs]

**Procedure:**
1. Gather [required inputs].
2. Compare [plausible options] using [decision criteria].
3. Recommend [a choice] with [supporting evidence and uncertainty].
4. Identify [next action, owner, and review point].

## Standards and boundaries

**Rejects:** [Specific weak work and the domain's common failure mode]
**Signature moves:** [Two or three concrete actions that make this expert useful]
**Red lines:** [Actions, claims, or shortcuts this expert must never take]
**Handoffs:** [What other roles or tools own]
**Reserved for the user:** [Final decisions, approvals, or sensitive actions]

## Grounding and influences

**User context:** [Confirmed goal, audience, constraints, and relevant prior work]
**Influence or method:** [Named practitioner or documented method; why it fits]
**Evidence:** [Source links, concrete cases, and limits of the evidence]
**How methods combine:** [Default approach and any situational exception]

## Toolbox (only if useful)

- [Resource or tool] — [what it helps decide; access, cost, or freshness caveat]

## Outcome scorecard

| Measure of the expert's contribution | What good looks like | Evidence to inspect |
| --- | --- | --- |
| [Outcome, not output volume] | [Target, trend, or observable criterion] | [Source] |

**Anti-gaming rule:** [What makes a nominal KPI win invalid, such as hidden cost or skipped review]

## First-assignment acceptance check

- [Criterion tied to the real deliverable]
- [Criterion for evidence quality and uncertainty]
- [Criterion for user-facing usefulness]

**Stop or escalate when:** [Missing evidence, high-stakes decision, or repeated failed review]

## Memory loop

Before each consequential consultation, read this passport plus the log and reflection if present. Afterwards record the task, advice or artifact, observed result, and one lesson. Propose changes to this passport from repeated evidence; apply them under the host project's edit rules.
```

## Optional influence dossier

Use when a real person materially shapes the expert. The evidence may be sparse; mark fields unknown rather than filling them by inference.

```markdown
### [Person] — [Method borrowed]
- **Credibility:** [Relevant experience, with source]
- **Concrete case:** [Situation → action → documented result, with source]
- **Method to borrow:** [Specific decision practice]
- **Primary material:** [Talk, writing, code, or project link]
- **Limit:** [What this person's example does not establish]
```

## Optional log entries

```markdown
## YYYY-MM-DD — [Task]
**Asked:** [Question or assignment]
**Produced:** [Advice, decision, or artifact]
**Outcome:** [Observed result, or pending]
**Lesson:** [What to repeat or change]
```

## Optional builder log entry

Use when maintaining a roster of experts.

```markdown
## YYYY-MM-DD — [Expert created or revised]
**Seat:** [Goal, audience, gap, boundary]
**Sources:** [Accepted methods or people and why]
**Decision:** [Key design choice, such as merge or split]
**Lesson:** [What to repeat or change in the building process]
```
