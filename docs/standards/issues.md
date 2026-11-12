# Issue standard

An issue is a unit of reviewable work, not a place to think out loud.

## Principles

- One deliverable per issue.
- Small enough to review in one sitting. If it cannot be completed in a few focused days,
  split it.
- Acceptance criteria describe observable behavior, not files created.
- Dependencies are explicit. Do not start an issue whose foundation is undefined.
- Use a tracking issue only for coordination. The actual work stays in small issues.

## Title

- Imperative and specific: `Implement snapshot reconciliation`, not `Snapshots`.
- No issue number in the title.
- No vague titles such as `Improve stuff` or `Refactor`.
- Prefix with a type only when the tracker benefits from it, for example `[Bug]` for
  bugs. The `type:*` label is the canonical classification.

## Required sections

```markdown
## Context

Why this work exists. What is broken, missing, or risky. Link to the relevant design.

## Objective

One paragraph describing the outcome.

## Scope

What will be changed. Include interfaces, commands, data, and documentation.

## Out of scope

What this issue deliberately does not do. This is as important as the scope.

## Acceptance criteria

- [ ] Observable behavior.
- [ ] Failure path or edge case.
- [ ] Documentation and examples updated.
- [ ] Tests added or updated.

## Dependencies

- Blocked by: #...
- Blocks: #...

## Technical notes

Constraints, decisions, traps, and links. Not a full implementation plan.

## Validation

Exact commands that must pass, and any manual check that cannot be automated.
```

## Definition of ready

An issue is ready to start when:

- The objective and scope are unambiguous.
- Dependencies are complete or explicitly stubbed.
- Acceptance criteria can be verified.
- The relevant architecture decision exists or the issue explicitly asks for one.
- Labels are set.

## Definition of done

- Acceptance criteria are met.
- Tests cover the behavior and the failure path.
- The documented validation commands were run and the results are reported.
- Documentation and examples are updated.
- No secrets, generated files, or unrelated changes are included.
- The issue and pull request are linked.
- Known limitations are recorded.

## Bugs

A bug report must include:

- What happened.
- What was expected.
- Steps to reproduce, with the smallest input that triggers it.
- Environment, version, and relevant configuration with secrets redacted.
- Whether it is a security issue. Security issues go through the private process, not
  the public tracker.

Do not mark a bug as fixed without a regression test when the behavior is testable.

## Tracking issues

A tracking issue may list sub-issues and a milestone. It must not contain implementation
work that belongs in a sub-issue. Close the tracking issue when all sub-issues are closed
or explicitly moved.

## Labels

Use exactly one `type:*` label, one or more `area:*` labels only when needed, one
`priority:*` label, and a `status:*` label only when the status is true. See
[labels](labels.md).

## Duplicates and stale work

- Search before creating.
- Link duplicates and close the newer one with a reason.
- If an issue is no longer valid, close it with an explanation and, when useful, a link
  to the replacement.
- Do not leave an issue open as a permanent maybe.
