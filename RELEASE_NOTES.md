# Release notes

## Initial distribution · 2026-10-20

Proposed initial distribution version: 0.1.0, not yet published to a registry. Public-contract label: v1. These are separate version identifiers.

Prepared the xletter Skill folder from the live public contract, preserving its complete API and behavioral guidance. Added three non-executing workflows covering adoption, a research handoff, and session continuity. Included source provenance, checksum, validation results, and the documented Skills CLI repository-install syntax.

The public distribution repository is [coffeehc/xletter-skill](https://github.com/coffeehc/xletter-skill). No private server code is included. The owner approved MIT-0 licensing for this public Skill documentation package only. Added the canonical license text at the repository root and inside the standalone Skill folder; the license does not cover the backend or hosted service. ClawHub publication and listing verification remain pending. There is no claimed registry version, install count, registration count, or runtime certification.

## Before a registry release

- MIT-0 licensing for this documentation package is approved. Preserve the license and its documentation-only scope in the published bundle.
- Re-fetch the live public contract, compare its SHA-256, and reconcile changes.
- Verify publisher authentication and slug availability; assign a semver package version separately from the public-contract label.
- Re-run structural checks and review the file set. The registry package root is `skills/xletter/`.
- After authorized publication, verify the registry version, rendered description, downloadable file set, checksum, and installation behavior in an authorized clean test environment.

## Verification limits

Static validation, public-file checksum verification, CLI discovery, and an isolated project-level Codex installation passed with Skills CLI 1.7.4. No live account operation, Agent execution of the Skill, scheduler integration, registry upload, marketplace review, or end-to-end mail delivery test has been performed. Static compatibility does not guarantee registry approval or successful execution on every Agent runtime.
