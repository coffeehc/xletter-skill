# Distribution channel synchronization · 2026-10-22

| Channel | Observed version/source | Required next action |
| --- | --- | --- |
| GitHub `coffeehc/xletter-skill` | Before update: main `75287877f891434eb77449458fbf203ca318a4cf`, Oct 20 snapshot | This package updates main to 0.2.0; verify committed files and hashes after the write. |
| [ClawHub](https://clawhub.ai/coffeehc/skills/xletter) | Public page still v0.1.0; current session shows Sign in with GitHub, no authenticated publisher verified | Authorized owner publishes `skills/xletter/` as 0.2.0; preserve SKILL.md, examples and LICENSE. Verify version, file hashes and installation before claiming completion. The old audit is not a new-version audit. |
| [AgentSkillHub](https://agentskillhub.dev/u/coffeehc/sk/xletter) | Browser verified current v2026.10.20, source `7ade369f4599e6a6b6449fe7cece6efb3a50c2aa`, tree `3698de8`; still the old content | Authenticated owner refreshes/imports the final new GitHub commit; verify actual registry version/source and downloads. Do not assume it follows main automatically. |
| [Agent Skill Exchange](https://github.com/agentskillexchange/skills/blob/main/skills/xletter/SKILL.md) | Public catalog copy points at `75287877f891434eb77449458fbf203ca318a4cf`; old Skill lacks current directory/contact semantics | Catalog maintainer updates the pinned source and copied Skill from the new commit, retaining catalog-specific metadata. No third-party write or outreach performed. |
| [skills.sh](https://skills.sh/coffeehc/xletter-skill/xletter) | HTTP 200 wrapper renders “404 / xletter isn’t available in this repository” | Verify indexing after GitHub synchronization; the documented Skills CLI repository-install path is separate from catalog availability. No indexed listing is claimed. |

## Release checklist for authorized publishers

1. Use the final GitHub commit, not an old imported snapshot. The bundle root is `skills/xletter/`; preserve its three files and MIT-0 license.
2. Check source/SHA256SUMS and confirm Skill prefix against the current canonical https://xletter.51apis.com/skill.md.
3. Publish with the channel's own version convention. Do not confuse package 0.2.0, public-contract v1 and the server content revision.
4. Read the public listing and downloadable files back. Verify all six send states, no-ID/no-delivery/no-queue ignored handling, directory opt-in, blacklist and valid history.peer alias.
5. Test installation only in an authorized test environment. A registry audit or installation does not prove identity adoption, mail retrieval or real collaboration.

No publisher credentials were created or expanded. No registry publication is claimed by this GitHub update.
