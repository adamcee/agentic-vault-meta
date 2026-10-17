# [[CLAUDE]].md — Agentic Vault Meta-Project
*Load this file first in every AI session for the `agentic-vault` meta-project. Updated: 2026-10-17.*

## Last Session Checkpoint
On 2026-10-17, tightened every user-facing doc in the `agentic-vault` repo against [[writing-discipline]], added a "What the Vault Enables" section to Design & Goals, and removed source-project references ([[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]). Logged the example-vault critique in [[ideas/rework-example-vault]]. Full log: [[session-history]].

## What This Project Is

This is the meta-vault used to build and organize the **Agentic Vault Template**. 

The goal is to distill the highly effective structure, protocols, and discipline of the `chameleon_vault` into a domain-agnostic, reusable "Agentic Knowledge Base" template. This template is designed for both non-technical founders/writers and developers who want to manage context efficiently with AI agents (Claude Code, Gemini CLI, Obsidian MCP).

## Current Phase

**Phase 8: Docs Quality.** Template, example, and website are published. Current work is tightening the docs and reworking the example vault. See [[prototype/implementation-plan]].

## Project Structure

Two repos, checked out side by side in `~/ai/agentic-vault/`:

```text
agentic-vault-meta/   ← This repo. The meta-vault, published with Quartz. Vault files live in content/.
agentic-vault/        ← The public product.
├── template/         ← The domain-agnostic vault template.
├── example/          ← A filled-in example vault (BrewTrack).
└── website/          ← MkDocs site. website/docs/example/ is a copy of example/; keep them in sync.
```

## Hard Constraints

- **Domain Agnostic:** Nothing in the `agentic-vault` repo names or describes the source project: no name, domain, stack, or personas ([[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]).
- **Graceful Degradation:** The template must be usable by non-technical people who just copy/paste text into a web app, all the way up to devs using CLI agents. Instructions in the template's `CLAUDE.md` must account for missing skills or CLI tools.
- **Progressive Enhancement:** Documentation (READMEs and guides) must be tiered (Tier 1: Web App, Tier 2: Desktop App + MCP, Tier 3: CLI tools).
- **Dogfooding:** Any structural decision or protocol we plan to put in the `template/` should first be implemented or documented in this meta-vault.
- **Writing Discipline:** Every doc written or edited, in either repo, passes the tightening checklist in [[writing-discipline]].

## Standing Decisions

- **Naming:** Temporary working title is "Agentic Vault" or "AI-Native Vault Template". Final name pending.
- **Architecture:** The template mirrors the `chameleon_vault` directory structure (`decisions/`, `strategy/`, `architecture/`, `research/`, `ideas/`, `drafts/`, `journal/`, `vault-guide/`).

## Task-Specific Context Loading

- **Template Generation Session:** Load `architecture/CONSTITUTION.md` and the relevant phase in `prototype/implementation-plan.md`. Read the original `chameleon_vault` equivalents to ensure no structural nuance is lost.
- **Documentation Session:** Load the target `README.md` or guide, [[writing-discipline]], and `strategy/` for the target audience.

## Decision Records

- [[decisions/product/PDR-P001-no-source-project-in-public-docs|PDR-P001]]: No source-project references in the public repo.

## Session History

[[session-history]]