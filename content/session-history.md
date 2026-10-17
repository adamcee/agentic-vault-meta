# Session History

One line per session, `- (agent, session type) what changed`, under its date heading, oldest first; append only and never rewrite. Entries before 2026-10-17 are reconstructed from git history.

## 2026-04-17
- Meta-vault initialized. Built `template/`, `example/` (BrewTrack), and the MkDocs site. See [[prototype/implementation-plan]] Phases 1–6.

## 2026-04-21
- Extracted the meta-vault into the `agentic-vault-meta` repo with a Quartz site and GitHub Pages deploy. Moved MkDocs deployment to GitHub Actions. Resolves [[ideas/separate-project-vault-repo]].

## 2026-05-06
- Removed personas-as-design-constraint from the methodology and source-project examples from `sources.md` (Adam, outside a vault session).

## 2026-10-17
- (Claude Code, documentation) Writing-discipline pass on every user-facing doc in `agentic-vault`. Added "What the Vault Enables" to Design & Goals, fixed the dead personas nav entry and source-domain leftovers, and wrote [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]. Logged [[ideas/rework-example-vault]]. Committed on branch `docs-pass-2026-10`.
- (Claude Code, documentation) Merged the template's `SYSTEM.md` into `AGENTS.md` and added `session-history.md` ([[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]]). Moved this vault's own master file to [[AGENTS]] with a `CLAUDE.md` pointer.
- (Claude Code, documentation) Replaced BrewTrack with three example vaults: software (Brigade), business (Curbside Cycles), creative (Low Tide) ([[decisions/product/PDR-P002-three-example-vaults|PDR-P002]]). `website/docs/examples` is now a symlink, and an MkDocs hook replaced the roamlinks plugin so example wikilinks resolve.
- (Claude Code, documentation) Added ISO 24495-1 plain language to the writing discipline ([[decisions/product/PDR-P003-iso-plain-language|PDR-P003]]).
- (Claude Code, documentation) Merged `docs-pass-2026-10` into `main` in both repos and rebuilt `website/.venv`. Not pushed.
- (Claude Code, documentation) Added `website/README.md` with local run instructions.
- (Claude Code, documentation) Moved the docs site to uv (`pyproject.toml`, `uv.lock`, Python 3.13); CI uses `astral-sh/setup-uv`.
- (Claude Code, documentation) Built Night Post as the flagship example with a Quartz site ([[decisions/product/PDR-P004-night-post-flagship-example|PDR-P004]]); added the Obsidian setup page; slop pass on everything.
- (Claude Code, vault maintenance) Ported source-vault protocols, structure, and scripts to the template ([[decisions/technical/ADR-T002-port-source-vault-protocols|ADR-T002]]); started weekly logs at [[prototype/implementation-logs/2026-W42]].
