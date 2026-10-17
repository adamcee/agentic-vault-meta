---
id: separate-project-vault-repo
date: 2026-04-17
status: resolved
tags: [architecture, repository-structure, quartz, publishing]
resolved-by: "implemented 2026-04-21 — extracted to the agentic-vault-meta repo (agentic-vault commit a53f178)"
---
# Idea: Separate the Meta-Vault into Its Own Repository

## Proposal
Move `project_vault/` out of the `agentic-vault` repo into its own repository and publish it with Quartz.

## Why
- **Less confusion.** People cloning the template shouldn't find our internal decisions and ideas next to `template/`.
- **A public case study.** A Quartz site shows the real graph of how the project was built, with backlinks and hover previews.

## Tradeoffs
- **Two repos to maintain** instead of one.

## Outcome
Done 2026-04-21: the meta-vault is now the `agentic-vault-meta` repo.
