# Pull request standard

A pull request is a reviewable change, not a dump of a branch.

## Size and scope

- One concern per pull request. If the description needs "and" to explain the purpose,
  split it.
- Prefer a change under roughly 400 changed lines. This is a guideline, not a license to
  hide unrelated changes in a large PR.
- Refactors that are not required by the behavior change belong in a separate PR.
- Do not mix formatting-only changes with logic changes.

## Title

Use the same convention as commits: `type(scope): imperative summary`.

Examples:

- `feat(worker): request snapshots through the control channel`
- `fix(store): reject stale snapshot sequences`
- `docs(protocol): clarify cancellation fallback`

## Description

Use the organization pull request template. It requires:

- **Summary:** what changed and why.
- **Scope:** what is included and what is not.
- **Validation:** exact commands run and their results.
- **Related issues:** `Closes #...` or `Refs #...`.
- **Breaking changes:** protocol, configuration, CLI, or data changes.
- **Security:** impact on auth, secrets, execution boundaries, or inputs.
- **Documentation:** which docs and examples changed.

Do not claim a check passed unless it was run.

## Before opening

- Rebase or merge the default branch as required by the repository.
- Run the documented build, test, vet, and format commands.
- Add or update tests for behavior changes.
- Update documentation and examples in the same change.
- Review your own diff.
- Remove debug output, commented-out code, secrets, and unrelated files.
- Confirm no generated or local state is included.

## Review

- CI must be green before merge.
- Resolve every conversation or explicitly explain why it is deferred.
- A reviewer checks behavior, failure paths, boundaries, tests, and documentation.
- The author does not approve their own PR. With a single maintainer, use the checklist
  and self-review; add a second reviewer when one exists.
- Security-sensitive changes require an explicit security review note, even if the
  reviewer is the author.

## Merge

- Squash merge by default.
- Delete the branch after merge.
- Keep the default branch history linear.
- Do not force-push the default branch.
- Do not merge with failing required checks or unresolved blocking comments.
- A draft PR may be opened early for feedback. Do not request final review while it is
  still a draft.

## Stacked work

If a change depends on another unmerged PR, state the dependency and keep the diff
minimal. Rebase the stack after the base merges. Do not merge a stack out of order.

## Rollback

If a change is risky, document how to revert it or disable it. A feature flag is not a
substitute for a correct default.
