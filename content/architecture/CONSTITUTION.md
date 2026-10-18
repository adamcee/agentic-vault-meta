---
id: CONSTITUTION
date: 2026-04-17
status: Active
tags: [architecture, invariants, template-design]
---
# CONSTITUTION.md — Agentic Vault Invariants

*Rules for building the Agentic Vault. Breaking one requires a decision record that supersedes the clause.*

## Part I — Design Invariants

- **D1 — Domain agnostic.** The template is a structural blank slate with clear placeholders. No file in the `agentic-vault` repo (`template/`, `examples/`, `website/`, `README.md`) names or describes the source project, its product, personas, or stack. Amended 2026-10-17 by [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]].
- **D2 — AGENTS.md primacy.** The template's `AGENTS.md` is the single source of truth. Tool-specific files (`CLAUDE.md`, `GEMINI.md`, `.cursorrules`, `.windsurfrules`) only point to it. Amended 2026-10-17 by [[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]].
- **D3 — Works without tools.** Every protocol has a manual fallback. If a script or skill isn't available, the docs say how to do the step by hand.
- **D4 — Method over tooling.** The protocols matter more than the editor. The template recommends Obsidian but stays plain markdown that works anywhere.

## Part II — Output Invariants

- **O1 — Three outputs.** The project produces:
  1. `template/`: the blank, reusable vault.
  2. Example vaults: Night Post and Curbside Cycles, each in its own repo with its own site ([[decisions/product/PDR-P005-example-vaults-in-own-repos|PDR-P005]]).
  3. `website/`: the setup and methodology docs.
- **O2 — Setup wizard.** An AI prompt asks about the user's project and fills in their `AGENTS.md` and `CONSTITUTION.md`.
