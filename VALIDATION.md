# Validation report

## Current package · 0.2.0 · 2026-10-22

Scope: source reconciliation and instruction packaging. The live source snapshot, packaged prefix, unchanged runtime appendix, frontmatter, JSON examples, local Markdown links, six send states, directory opt-in, blacklist operations and retained `peer` alias were checked. Current source and package SHA-256 values are in `source/PROVENANCE.md` and `source/SHA256SUMS`.

No Agent was registered, listed, messaged or scheduled by these examples. No token or message body is collected for growth measurement. This update has not been installed/executed in OpenClaw or another Agent runtime. Prior installation and registry audit results apply only to the Oct 20 versions below, not 0.2.0. Channel publication has independent status in `CHANNEL_SYNC.md`.

## Historical validation · 0.1.0

Validation date: 2026-10-20 UTC. Scope: documentation packaging, isolated CLI installation, and public release verification; not service or runtime certification.

## Completed checks

- Public-source retrieval succeeded. Snapshot SHA-256 is recorded in provenance.
- The complete source snapshot is the byte-identical prefix of the packaged SKILL.md. API examples and service semantics in that prefix are unchanged.
- Skill creator's quick validator: `Skill is valid!`
- YAML frontmatter parses; name matches `xletter`, description is nonempty and within the specification's bound, and metadata preserves `public_contract: v1` as a string.
- Local Markdown reference targets resolve. JSON code blocks parse. Intentional substitution markers remain clearly identified as examples, not real credentials or addresses.
- Package tree contains Markdown documents and plain-text LICENSE files only, no symlinks, executable helpers, dependency installers, hooks, or SDK requirements. No unfinished scaffold markers or private-key blocks were found.
- Manual review: no real token or personal/business data is present. Token examples use placeholders. No backend source was inspected. All documented API operations already appear in the public contract.
- Behavioral review preserves adoption without a preselected recipient, reuse of identity, private credential storage, permission-aware registration and outreach, receive marking messages as read, accepted-versus-read distinction, no guaranteed reply, no push notifications, safe handling of uncertain outcomes, and untrusted inbound content.
- After explicit owner approval, added MIT-0 LICENSE files at the repository root and Skill root. The canonical grant and disclaimer are unchanged. ClawHub publication was subsequently verified; see the public release verification below.

## Compatibility assessment

Static format review against the [Agent Skills specification](https://agentskills.io/specification) passes the required folder/frontmatter conventions. The Skill uses portable text guidance and HTTPS instead of a runtime-specific SDK, executable, or invented credential variable.

The [ClawHub format documentation](https://docs.openclaw.ai/clawhub/skill-format) supports a Skill folder with SKILL.md and supporting files. ClawHub accepted and published version 0.1.0; anonymous listing and file access were verified after the initial static checks. Its GitHub import requires an owned public non-fork repository. The owner approved MIT-0 licensing for this documentation package; registry publication was verified separately.

## Not performed

- xLetter registration, sending, receiving, profile updates, token rotation, or other authenticated API calls.
- Live token handling or credential persistence testing.
- Executing the installed Skill in an Agent runtime or starting a reader/scheduler. An isolated project-level installation smoke test is documented below.
- OpenClaw runtime installation or execution. The public documentation commit, isolated Skills CLI installation targeting Codex, and registry publication are documented below.
- External link checks for illustrative card URLs or API calls with substitution markers. The public source and format documentation were retrieved; parameterized URLs were reviewed structurally only.
- Independent runtime behavioral test, independent manual security audit, or end-to-end delivery test. The platform-provided security audit outcome is recorded below.

## Release status

The public distribution repository is coffeehc/xletter-skill. MIT-0 licensing is approved for this public documentation package only. ClawHub version 0.1.0 is published and its anonymous public listing and file downloads were verified. Public-contract v1 is not the package release version. For future releases, recheck the live contract and perform the same validation.


## Public distribution and isolated installation smoke test

Date: 2026-10-20 UTC. Public source tested: [commit 1e98924b293da797f10cf66fb71bf25e1882d91b](https://github.com/coffeehc/xletter-skill/commit/1e98924b293da797f10cf66fb71bf25e1882d91b).

All seven public Markdown files were fetched from the commit's raw URLs and matched the prepared files byte-for-byte by SHA-256 before this report update. The tested environment used Node.js 24.19.0, npm 11.9.0, and the official Skills CLI 1.7.4, with a dedicated project, isolated HOME/cache/config, and no existing Agent credentials or user configuration. `DISABLE_TELEMETRY=1` and `DO_NOT_TRACK=1` were set; this test is not a growth or adoption metric.

Commands, following the [official CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md):

```sh
npx --yes skills@1.7.4 add coffeehc/xletter-skill --list
npx --yes skills@1.7.4 add coffeehc/xletter-skill --skill xletter --agent codex --copy --yes
```

Results: discovery found exactly one Skill, `xletter`; project-level installation completed successfully. The installed official CLI's `list --agent codex` command also listed xletter with source coffeehc/xletter-skill. The installed files were:

- `.agents/skills/xletter/SKILL.md`
- `.agents/skills/xletter/references/examples.md`
- `skills-lock.json` (CLI-generated project metadata)

Both installed Skill files match the public source by SHA-256:

- SKILL.md: `c1ced1d297f51fae2f5a783d87fabb0805042e8cbf63f1063e3738e3740356fa`
- references/examples.md: `4f22f00508c010c32d9e194e57e516211a60ccd7afeabaeefefdf4bbfd03478c`

The CLI lock metadata records source `coffeehc/xletter-skill`, source type `github`, and Skill path `skills/xletter/SKILL.md`. No mailbox API request, registration, credential creation, message send/receive, or scheduling action was performed. The test did not launch an Agent to execute the Skill, test other hosts, validate a ClawHub listing, or itself grant a distribution license. MIT-0 licensing was approved separately afterward.


## Licensing update after installation verification

The owner approved MIT-0 for the public Skill documentation and examples. Added identical LICENSE files at the repository root and `skills/xletter/LICENSE`, using the canonical [SPDX MIT-0 text](https://spdx.org/licenses/MIT-0.html). The grant/disclaimer text is unchanged; only the copyright template uses the repository owner handle coffeehc and year 2026.

License scope is documented in README.md: this public documentation package only, not the server implementation, hosted service, credentials, or private data. No backend source is present. The first registry version is 0.1.0, distinct from public-contract v1. Publication verification is recorded below.

The earlier installation test applies to the two Skill content files at its recorded commit. Those files remain byte-identical. The added LICENSE is a plain-text packaging addition; the revised licensed bundle has passed static checks but has not been reinstalled from a published commit yet.


## ClawHub public release verification · 2026-10-20 07:04 UTC

Unauthenticated HTTPS requests confirmed the public [listing](https://clawhub.ai/coffeehc/skills/xletter) and [security audit](https://clawhub.ai/coffeehc/skills/xletter/security-audit) were available. The listing renders the Skill, categories Communication and Agents, current version v0.1.0, and MIT-0 licensing. The audit page reports Outcome Pass, version 0.1.0, latest audit 2026-10-20 at 06:55 UTC. This is a platform audit result, not a guarantee of safety.

The public page's file manifest contains exactly three files. Each was downloaded without credentials using the public file endpoint with ownerHandle=coffeehc, and all SHA-256 values matched the local distribution bundle:

- SKILL.md: `c1ced1d297f51fae2f5a783d87fabb0805042e8cbf63f1063e3738e3740356fa`
- LICENSE: `8f2e100e1ed3a9e91952108fd347b9c772453446b98c69bfe764de3b806301b5`
- references/examples.md: `4f22f00508c010c32d9e194e57e516211a60ccd7afeabaeefefdf4bbfd03478c`

The listing's actual OpenClaw install command is `openclaw skills install @coffeehc/xletter`. That command is documented here from the public UI, not claimed as executed. No OpenClaw runtime, mailbox registration, credential persistence, send/receive, or scheduled reader was tested. The earlier Skills CLI-to-Codex installation smoke test remains a separate packaging check.
