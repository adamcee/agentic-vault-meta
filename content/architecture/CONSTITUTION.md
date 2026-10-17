---
id: CONSTITUTION
date: 2026-04-17
status: Active
tags: [architecture, invariants, template-design]
---
# [[CONSTITUTION]].md — Agentic Vault Invariants

*This document defines the non-negotiable rules for building the Agentic Vault template. Violating any invariant requires creating an ADR.*

## Part I — Design Invariants

- **D1 — Strict Domain Agnosticism**
The `template/` directory must be a blank slate structurally. No file in the `agentic-vault` repo (`template/`, `example/`, `website/`, `README.md`) may name or describe the source project, including its product, personas, or stack. Amended 2026-10-17 by [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]. Placeholders must clearly indicate where the user should inject their own domain knowledge (e.g., `[Insert Project Name Here]`).

- **D2 — AGENTS.md Primacy**
The template's `AGENTS.md` is the single source of truth. Tool-specific files (`CLAUDE.md`, `GEMINI.md`, `.cursorrules`, `.windsurfrules`) only point to it. Amended 2026-10-17 by [[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]].

- **D3 — Tiered Accessibility (Graceful Degradation)**
The template must not break if a user lacks technical skills. Protocols must offer a "manual" or "web app" fallback. For instance, if an automated script or a `.claude/skill/` isn't available, the documentation must explain how to manually verify links or update indexes.

- **D4 — Principle over Tooling**
The vault methodology (Decision Records, Reweave Protocols, Research Traceability, Writing Discipline) is more important than the specific markdown editor. The template should recommend Obsidian (for its graph and linking features) but must remain fundamentally editor-agnostic markdown.

## Part II — Output Invariants

- **O1 — Three Distinct Outputs**
The project must produce:
1. `template/` — The blank, reusable directory structure.
2. `examples/` — Three populated demonstration vaults: software, business, and creative ([[decisions/product/PDR-P002-three-example-vaults|PDR-P002]]).
3. `website/` or `docs/` — The tiered installation and philosophy guide.

- **O2 — The Interactive Setup Guide**
We must produce an interactive AI prompt that acts as an onboarding wizard. It will ask the user about their environment and context, then fill in their `AGENTS.md` and `CONSTITUTION.md`.