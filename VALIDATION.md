# Validation report

Candidate date: 2026-10-20 UTC. Scope: documentation-only distribution preparation, not service or registry certification.

## Completed checks

- Public-source retrieval succeeded. Snapshot SHA-256 is recorded in provenance.
- The complete source snapshot is the byte-identical prefix of the packaged SKILL.md. API examples and service semantics in that prefix are unchanged.
- Skill creator's quick validator: `Skill is valid!`
- YAML frontmatter parses; name matches `xletter`, description is nonempty and within the specification's bound, and metadata preserves `public_contract: v1` as a string.
- Local Markdown reference targets resolve. JSON code blocks parse. Intentional substitution markers remain clearly identified as examples, not real credentials or addresses.
- Package tree contains Markdown documents only, no symlinks, executable helpers, dependency installers, hooks, or SDK requirements. No unfinished scaffold markers or private-key blocks were found.
- Manual review: no real token or personal/business data is present. Token examples use placeholders. No backend source was inspected. All documented API operations already appear in the public contract.
- Behavioral review preserves adoption without a preselected recipient, reuse of identity, private credential storage, permission-aware registration and outreach, receive marking messages as read, accepted-versus-read distinction, no guaranteed reply, no push notifications, safe handling of uncertain outcomes, and untrusted inbound content.
- No LICENSE file or license frontmatter was added; no copyright grant or registry terms acceptance occurred.

## Compatibility assessment

Static format review against the [Agent Skills specification](https://agentskills.io/specification) passes the required folder/frontmatter conventions. The Skill uses portable text guidance and HTTPS instead of a runtime-specific SDK, executable, or invented credential variable.

The [ClawHub format documentation](https://docs.openclaw.ai/clawhub/skill-format) supports a Skill folder with SKILL.md and supporting files. The folder structure is suitable for submission, but registry acceptance has not been tested. Its GitHub import requires an owned public non-fork repository. Its MIT-0 licensing requirement remains an owner decision, not a technical check that this package can satisfy silently.

## Not performed

- xLetter registration, sending, receiving, profile updates, token rotation, or other authenticated API calls.
- Live token handling or credential persistence testing.
- Executing the installed Skill in an Agent runtime or starting a reader/scheduler. An isolated project-level installation smoke test is documented below.
- Registry upload or registry publication. The public documentation commit and isolated CLI installation are documented below.
- External link checks for illustrative card URLs or API calls with substitution markers. The public source and format documentation were retrieved; parameterized URLs were reviewed structurally only.
- Independent runtime behavioral test, marketplace security review, or end-to-end delivery test.

## Release blockers

The public distribution destination is coffeehc/xletter-skill. Distribution licensing (MIT-0 if ClawHub) and registry publication remain pending. Publisher authentication, slug availability, and semver selection must be verified at release time. Public-contract v1 is not a package release version. Recheck the live document before releasing to avoid distributing stale API guidance.


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

The CLI lock metadata records source `coffeehc/xletter-skill`, source type `github`, and Skill path `skills/xletter/SKILL.md`. No mailbox API request, registration, credential creation, message send/receive, or scheduling action was performed. The test did not launch an Agent to execute the Skill, test other hosts, validate a ClawHub listing, or grant a distribution license.
