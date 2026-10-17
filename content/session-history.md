# Session History

One line per session under its date, oldest first; append only and never rewrite. The last `## YYYY-MM-DD` heading is the last session date. Entries before 2026-10-17 are reconstructed from git history.

## 2026-04-17
- Meta-vault initialized. Built `template/`, `example/` (BrewTrack), and the MkDocs site. See [[prototype/implementation-plan]] Phases 1–6.

## 2026-04-21
- Extracted the meta-vault into the `agentic-vault-meta` repo with a Quartz site and GitHub Pages deploy. Moved MkDocs deployment to GitHub Actions. Resolves [[ideas/separate-project-vault-repo]].

## 2026-05-06
- Removed personas-as-design-constraint from the methodology and source-project examples from `sources.md` (Adam, outside a vault session).

## 2026-10-17
- Writing-discipline pass on every user-facing doc in `agentic-vault`. Added "What the Vault Enables" to Design & Goals, fixed the dead personas nav entry and source-domain leftovers, and wrote [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]. Logged [[ideas/rework-example-vault]]. Committed on branch `docs-pass-2026-10`.
- Merged the template's `SYSTEM.md` into `AGENTS.md` and added `session-history.md` ([[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]]). Moved this vault's own master file to [[AGENTS]] with a `CLAUDE.md` pointer.
- Replaced BrewTrack with three example vaults: software (Brigade), business (Curbside Cycles), creative (Low Tide) ([[decisions/product/PDR-P002-three-example-vaults|PDR-P002]]). `website/docs/examples` is now a symlink, and an MkDocs hook replaced the roamlinks plugin so example wikilinks resolve.
- Added ISO 24495-1 plain language to the writing discipline ([[decisions/product/PDR-P003-iso-plain-language|PDR-P003]]).
- Merged `docs-pass-2026-10` into `main` in both repos and rebuilt `website/.venv`. Not pushed.
