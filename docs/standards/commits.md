# Commit and branch standard

## Commits

Use Conventional Commits:

```text
type(scope): imperative summary

Why this change is needed. Wrap the body at 72 columns.

Refs: #123
```

### Types

| Type | Use for |
| --- | --- |
| `feat` | New capability. |
| `fix` | Bug fix. |
| `docs` | Documentation only. |
| `refactor` | Behavior-preserving code change. |
| `test` | Tests only. |
| `perf` | Performance improvement. |
| `build` | Build system or dependency changes. |
| `ci` | CI configuration. |
| `chore` | Maintenance that does not fit another type. |
| `security` | Security hardening or vulnerability fix. |

### Rules

- Summary in the imperative mood: `add`, not `added` or `adds`.
- Lowercase after the type and scope. No trailing period.
- Keep the summary under 72 characters.
- Use a scope when it clarifies the area: `feat(worker): ...`, `fix(store): ...`.
- The body explains **why**, not a line-by-line restatement of the diff.
- Reference issues in the footer: `Refs: #123` or `Closes: #123`.
- Mark breaking changes explicitly:

```text
feat(protocol)!: require protocol version in every envelope

BREAKING CHANGE: v0 clients without protocol_version are rejected.
```

- One logical change per commit. Do not mix a refactor, a feature, and a formatting
  change.
- Never commit secrets, tokens, local state, or generated files that should be ignored.
- Do not create `WIP` commits on the default branch. Squash or fix up before merge.

## Branches

Use `type/short-slug`:

```text
feat/worker-snapshot-channel
fix/stale-snapshot-sequence
docs/issue-breakdown
chore/labels
```

Rules:

- Lowercase kebab-case after the type.
- No personal names or dates.
- Keep branches short-lived.
- Rebase on the default branch before requesting final review when the repository uses
  squash merges.
- Delete the branch after merge.

## Reverts

Use `revert: <original summary>` and include the original commit hash and the reason in
the body. Do not rewrite published history to hide a bad merge.
