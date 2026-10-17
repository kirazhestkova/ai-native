# Engineering and visual checks

Load for engineering, production or visual acceptance. Use the target project's
requirements, test commands, reviewer roles and release process. These checks
work without another skill or a prescribed project layout.

## Match checks to the change

- Use the project's requirements, implementation plan and acceptance criteria.
  When none exist, state the intended behavior and a proportionate verification
  plan before implementation. A small change does not need a new planning system.
- Run checks capable of detecting the relevant defect. For a new validation rule,
  demonstrate a failing case in an isolated fixture and a valid case that passes.
  Tests that repeat the implementation's wording do not establish behavior.
- Exercise the route and state transition the user uses. Check content and
  behavior as well as schemas; a fallback can parse correctly while losing data.
  If a failure reveals a class of defects, check related cases within scope.
- For visual work, inspect the rendered result at its intended size. Text searches
  and screenshots that were never inspected do not establish visual acceptance.
  Design judgment and acceptance remain lead responsibilities.

## Keep required review independent

Production changes and engineering involving money, authentication, credentials or
personal data require independent review. Use the project's reviewer and criteria
when specified; otherwise identify a separate qualified reviewer and give them
the requirements, artifact and evidence. The reviewer may be another agent with
a fresh context or an appropriate human. No named expert persona is required.

Provide durable evidence, reproduction steps, the build or commit identity when
applicable, and any changes since the tested version. Refresh the plan, statuses
and handoff that the judge will read. Derive claims from the captured evidence.

If a required reviewer is unavailable, identify an alternative that meets the
same criteria. If none is available, report the unmet gate and continue only
unaffected work. The author cannot provide their own independent approval.

## Verify previews and releases

Before asking the user to test a preview, reproduce the target path on that
deployment. Use equivalent configuration or disclose meaningful differences.
Use an appropriate test identity and respect rate limits. Give the user the
location, steps, expected result and known limitations. A failed preview check
needs new evidence before asking them to try it again.

If the project or user requires a manual preview or release approval, preserve
that requirement. Automated checks do not replace an explicitly required user
walkthrough. Apply authorization already given; ask only for missing approval or
changes beyond its scope. Use the project's promotion process and verify the
actual deployed behavior afterward.

A passing local check is evidence about that tested artifact. State separately
whether it was reviewed, published or verified in production. Instructions in a
skill do not install hooks or prove that automatic enforcement is active.
