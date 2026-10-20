# Release notes

## 0.1.0 · 2026-10-20

Distribution version: 0.1.0, published on [ClawHub](https://clawhub.ai/coffeehc/skills/xletter). Public-contract label: v1. These are separate version identifiers.

Prepared the xletter Skill folder from the live public contract, preserving its complete API and behavioral guidance. Added three non-executing workflows covering adoption, a research handoff, and session continuity. Included source provenance, checksum, validation results, and the documented Skills CLI repository-install syntax.

The public distribution repository is [coffeehc/xletter-skill](https://github.com/coffeehc/xletter-skill). No private server code is included. The owner approved MIT-0 licensing for this public Skill documentation package only. Added the canonical license text at the repository root and inside the standalone Skill folder; the license does not cover the backend or hosted service. ClawHub publication, anonymous public listing access, and download/hash verification of all three bundle files are complete. The security audit reports Pass for 0.1.0 (2026-10-20 06:55 UTC). No install count, registration count, or runtime certification is claimed.

## AgentSkillHub distribution · 2026-10-20

[xLetter is listed on AgentSkillHub](https://agentskillhub.dev/u/coffeehc/sk/xletter) as version `2026.10.20`, imported from source commit `7ade369`. The public import and listing details were verified. The displayed install command is `npx skhub add coffeehc/xletter`; it has not been executed or tested. This date-based registry version is independent of ClawHub `0.1.0` and public-contract `v1`. No Skill bundle content changed for this documentation update.

## For subsequent releases

- MIT-0 licensing for this documentation package is approved. Preserve the license and its documentation-only scope in the published bundle.
- Re-fetch the live public contract, compare its SHA-256, and reconcile changes.
- Verify publisher authentication and slug availability; assign a semver package version separately from the public-contract label.
- Re-run structural checks and review the file set. The registry package root is `skills/xletter/`.
- After authorized publication, verify the registry version, rendered description, downloadable file set, checksum, and installation behavior in an authorized clean test environment.

## Verification limits

Static validation, public-file checksum verification, CLI discovery, and an isolated project-level Codex installation passed with Skills CLI 1.7.4. ClawHub publication and its public audit result were verified separately. No live account operation, Agent execution of the Skill, OpenClaw runtime installation, scheduler integration, or end-to-end mail delivery test has been performed. Static compatibility does not guarantee registry approval or successful execution on every Agent runtime.
