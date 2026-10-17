# Implementation Plan: Agentic Vault Template
*Updated: 2026-10-17*

This is the vault ledger for building the Agentic Vault template project.

## Phase 1: Meta-Vault Initialization (Current)
- [x] Create project directory structure (`project_vault/`, `template/`, `example/`, `website/`).
- [x] Seed `project_vault/` with `CLAUDE.md`, `CONSTITUTION.md`, and this `implementation-plan.md`.

## Phase 2: Template Structure Creation
- [x] Create core directories in `template/` (`decisions/`, `strategy/`, `architecture/`, `research/`, `ideas/`, `drafts/`, `journal/`, `vault-guide/`).
- [x] Draft a model-agnostic master context file (e.g., `SYSTEM.md` or `CLAUDE.md`).
- [x] Translate Chameleon's `vault-guide/` (Philosophy, Writing Discipline, Protocols) into domain-agnostic template files.
- [x] Draft `AGENTS.md` equivalent with placeholders.
- [x] Create `decisions/` schema and index bases.

## Phase 3: Setup Automation & Skills
- [x] Port `.claude/skills/` from Chameleon, adapting instructions to be graceful if missing.
- [x] Write `init-vault.sh` or a Python setup script to scaffold a new vault from the template.
- [x] Add `.gitignore` and recommended `.obsidian/` configurations.

## Phase 4: README & Interactive Guide
- [x] Write the Tiered `README.md` (Web App, Desktop App, CLI).
- [x] Draft the Interactive AI Onboarding Prompt (The "Wizard").

## Phase 5: Example Repo Creation
- [x] Clone the finalized `template/` into `example/`.
- [x] Invent a fictional project (e.g., Local Coffee Shop App).
- [x] Populate `example/` with realistic ADRs, PDRs, a `CONSTITUTION.md`, and an `implementation-plan.md` to demonstrate the methodology in action.

## Phase 6: Website/Documentation
- [x] Build a simple landing page or MkDocs site in `website/` explaining the philosophy and linking to the template and example.

## Phase 7: Next Session Priorities
- [ ] Setup GitHub Pages for the main site (MkDocs deployment verification).
- [ ] Add a best-practice research doc (written by Claude) on the vault methodology, principles, and how it works to the project.
- [x] Extract the `project_vault/` into a separate repository and build a public Quartz site for it. Link it back to the main repository. (Done 2026-04-21: `agentic-vault-meta`.)
- [x] Research and document a good Windows alternative to Obsidian, other general Obsidian alternatives, and a web-based note-taking alternative to give users multiple tooling options. (Done: `website/docs/installation/tooling-alternatives.md`.)
- [x] Fix the BrewTrack example vault links. (Superseded: BrewTrack removed; the new examples use the wikilink hook.)

## Phase 8: Docs Quality (Current)
- [x] Remove personas-as-design-constraint from the methodology (2026-05-06, commit `e520e8b`).
- [x] Remove source-project examples from `sources.md` (2026-05-06, commit `af4e23b`).
- [x] Tighten README, website pages, and template docs against [[writing-discipline]] (2026-10-17).
- [x] Add "What the Vault Enables" to Design & Goals (2026-10-17).
- [x] Remove the dead `personas-as-constraint.md` entry from `mkdocs.yml` nav (2026-10-17).
- [x] Remove source-domain leftovers from template `AGENTS.md` and `SYSTEM.md` ("pedagogy," "learning science") (2026-10-17).
- [x] Fix `SYSTEM.md` "7-point" checklist reference; the checklist has 10 points (2026-10-17).
- [x] Rework the example vault: three examples (software, business, creative) replace BrewTrack ([[decisions/product/PDR-P002-three-example-vaults|PDR-P002]], 2026-10-17).
- [x] MCDP-7 citation reviewed; Adam kept it as is (2026-10-17).
- [x] Move the template's master file from `SYSTEM.md` to `AGENTS.md` ([[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]], 2026-10-17). The meta-vault's own master file moved too.
- [x] Add `session-history.md` and a Last Session Checkpoint to the template (2026-10-17).
- [x] Commit the 2026-10-17 docs pass in both repos (branch `docs-pass-2026-10`).
- [x] Add ISO 24495-1 plain language to the writing discipline ([[decisions/product/PDR-P003-iso-plain-language|PDR-P003]], 2026-10-17).
- [x] Fix website wikilinks in example vaults with an MkDocs hook; replace `mkdocs-roamlinks-plugin` (2026-10-17).
- [x] Rebuild `website/.venv` from `requirements.txt` (2026-10-17).
- [x] Merge `docs-pass-2026-10` into `main` in both repos (2026-10-17).
- [ ] Push `main` in both repos. This deploys both public sites.
- [ ] Revisit [[ideas/quartz-for-example-site]] now that there are three examples.

## Phase 9: Source-Vault Parity (Current)
- [x] Gap report: compare the source vault with the template (2026-10-17, read-only).
- [x] Port protocol pages, style guides, and the research-paper discipline to `template/vault-guide/` ([[decisions/technical/ADR-T002-port-source-vault-protocols|ADR-T002]]).
- [x] Port link checker, autolinker, lint, review scan, and tag aligner; upgrade `vault-start` and `prompt-architect`.
- [x] Template structure: folder READMEs, human task list, weekly logs, `prompts/`, `.link-check-ignore`, `.gitignore` that tracks `drafts/`.
- [x] Docs site: Session Logs and Vault Maintenance pages; Obsidian setup page.
- [~] Bring the three examples up to the new template.
- [ ] Push `main` in both repos once Adam approves. This deploys both sites, including Night Post at `/night-post/`.
- [ ] Decide whether this meta-vault adopts the full template structure (folder READMEs, human task list, scripts).

