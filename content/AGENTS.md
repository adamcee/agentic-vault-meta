# AGENTS.md — Agentic Vault Meta-Project
*Single source of truth for every AI agent in the `agentic-vault` meta-project. Load this file first in every session. Updated: 2026-10-17.*

## Last Session Checkpoint
On 2026-10-17, the template's master file became `AGENTS.md`, three example vaults replaced BrewTrack, and the writing discipline adopted ISO 24495-1. Both repos are merged to `main` but not pushed.

Full log: [[session-history]].

## What This Project Is

This meta-vault manages the building of the **Agentic Vault**, a reusable vault template distilled from the source vault's structure and protocols. The template serves anyone working with AI over a long project, from writers and founders using web chat to developers using CLI agents.

## Current Phase

**Phase 8: Docs Quality.** Template, examples, and website are published. Remaining work is pushing `main` and the open items in the plan. See [[prototype/implementation-plan]].

## Project Structure

Two repos, checked out side by side in `~/ai/agentic-vault/`:

```text
agentic-vault-meta/   ← This repo. The meta-vault, published with Quartz. Vault files live in content/.
agentic-vault/        ← The public product.
├── template/         ← The domain-agnostic vault template.
├── examples/         ← Three filled-in example vaults: software/, business/, creative/.
└── website/          ← MkDocs site. website/docs/examples is a symlink to examples/.
```

## Hard Constraints

- **Domain Agnostic:** Nothing in the `agentic-vault` repo names or describes the source project: no name, domain, stack, or personas ([[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]).
- **Graceful Degradation:** The template must be usable by non-technical people who just copy/paste text into a web app, all the way up to devs using CLI agents. Instructions in the template's `AGENTS.md` must account for missing skills or CLI tools.
- **Progressive Enhancement:** Documentation (READMEs and guides) must be tiered (Tier 1: Web App, Tier 2: Desktop App + MCP, Tier 3: CLI tools).
- **Dogfooding:** Any structural decision or protocol we plan to put in the `template/` should first be implemented or documented in this meta-vault.
- **Writing Discipline:** Every doc written or edited, in either repo, passes the tightening checklist in [[writing-discipline]].

## Standing Decisions

- **Naming:** Temporary working title is "Agentic Vault" or "AI-Native Vault Template". Final name pending.
- **Master file:** `AGENTS.md` ([[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]]).
- **Architecture:** The template mirrors the source vault's directory structure (`decisions/`, `strategy/`, `architecture/`, `research/`, `ideas/`, `drafts/`, `journal/`, `vault-guide/`).

## Task-Specific Context Loading

- **Template Generation Session:** Load `architecture/CONSTITUTION.md` and the relevant phase in `prototype/implementation-plan.md`. Compare against the source vault's equivalents so no structure is lost.
- **Documentation Session:** Load the target `README.md` or guide, [[writing-discipline]], and `strategy/` for the target audience.

## Decision Records

- [[decisions/technical/ADR-T001-agents-md-master-file|ADR-T001]]: `AGENTS.md` is the template's master file.
- [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]: No source-project references in the public repo.
- [[decisions/product/PDR-P002-three-example-vaults|PDR-P002]]: Three example vaults (software, business, creative) replace BrewTrack.
- [[decisions/product/PDR-P003-iso-plain-language|PDR-P003]]: Writing discipline adopts ISO 24495-1 plain language.
- [[decisions/product/PDR-P004-night-post-flagship-example|PDR-P004]]: Night Post is the flagship example, published with Quartz.

## Session History

[[session-history]]