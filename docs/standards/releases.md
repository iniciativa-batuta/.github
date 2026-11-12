# Release standard

## Versioning

Use Semantic Versioning for products and libraries:

- `MAJOR` for incompatible public changes.
- `MINOR` for backward-compatible features.
- `PATCH` for backward-compatible fixes.

Before `1.0.0`, minor versions may include breaking changes, but they must still be
called out in the release notes. Do not use `0.x` as an excuse to break users silently.

The protocol has its own major version (`protocol_version: "1"`). Product version and
protocol version are independent. A product release that changes protocol compatibility
must state the supported protocol versions.

## Tags

- Format: `vMAJOR.MINOR.PATCH`, for example `v0.3.1`.
- Annotated tags are preferred.
- Tags are immutable. Never move or reuse a published tag.
- Sign tags when the maintainer has a signing key configured.

## Release notes

Every release includes:

- A short summary of the user-visible change.
- Breaking changes and migration steps.
- New configuration, commands, or protocol fields.
- Fixed defects, especially security-relevant ones.
- Known limitations.
- Supported protocol versions.
- Checksums for published artifacts.

Do not publish a release note that says "various fixes" without listing the relevant
changes.

## Process

1. Confirm the default branch is clean and all required checks pass.
2. Confirm documentation and examples match the release.
3. Run the full validation suite from a clean checkout.
4. Update the changelog or release notes.
5. Create the annotated tag.
6. Build artifacts from the tagged commit.
7. Generate and publish checksums.
8. Publish the release.
9. Verify the published artifacts can be downloaded and the checksum matches.

Do not build release artifacts from a dirty working tree.

## Artifacts

- Publish reproducible binaries for supported platforms.
- Include version, commit, and build date in `batuta version`.
- Publish SHA-256 checksums alongside artifacts.
- Do not attach secrets, local configuration, debug binaries, or test data.
- State the minimum supported Go version when source builds are supported.

## Compatibility

- Additive protocol/API changes may ship in a minor release.
- Removing or changing the meaning of a field requires a protocol major version.
- Deprecations are announced before removal and documented.
- Database migrations must be forward-only and tested from the previous release.

## Security releases

A security release follows the same process but may be prepared privately. Coordinate
disclosure through GitHub Security Advisories. Do not publish exploit details before a
fix is available. See [security](security.md).
