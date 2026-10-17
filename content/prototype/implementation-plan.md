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
- [ ] Fix the BrewTrack example vault links (they currently route back to the homepage).

## Phase 8: Docs Quality (Current)
- [x] Remove personas-as-design-constraint from the methodology (2026-05-06, commit `e520e8b`).
- [x] Remove source-project examples from `sources.md` (2026-05-06, commit `af4e23b`).
- [x] Tighten README, website pages, and template docs against [[writing-discipline]] (2026-10-17).
- [x] Add "What the Vault Enables" to Design & Goals (2026-10-17).
- [x] Remove the dead `personas-as-constraint.md` entry from `mkdocs.yml` nav (2026-10-17).
- [x] Remove source-domain leftovers from template `AGENTS.md` and `SYSTEM.md` ("pedagogy," "learning science") (2026-10-17).
- [x] Fix `SYSTEM.md` "7-point" checklist reference; the checklist has 10 points (2026-10-17).
- [ ] Rework the example vault. See [[ideas/rework-example-vault]].
- [ ] Verify the MCDP-7 citation. Sources lists it for Commander's Intent, but MCDP-7 covers learning; Commander's Intent is usually sourced to MCDP 1 or MCDP 6.
- [ ] Decide whether the template's master file should move from `SYSTEM.md` to `AGENTS.md`, which more tools now read by default and which the source vault adopted.
- [ ] Add a session-history file and checkpoint routine to the template that match this meta-vault's.
- [ ] Commit the 2026-10-17 docs pass in both repos.
