---
doctype: ADR
id: ADR-T002
domain: technical
status: accepted
date: 2026-10-17
tags: [template, protocols, tooling, vault-guide]
constitution-clause: D3
supersedes: null
superseded-by: null
---
# ADR-T002: Port the Source Vault's Newer Protocols and Tooling

## Context
The source vault added protocols and scripts after the template was cut in April: append-only weekly logs with a lint check, vault review, plan triage, review-before-write for decisions, reweave backfill, link-rewriting promotion out of `drafts/`, and a research paper workflow. A read-only gap report on 2026-10-17 found none of these in the template.

## Decision
Port every gap that applies to any project, described generically:
- **Protocol pages.** Each protocol gets a canonical page in `vault-guide/`. `AGENTS.md` keeps the short checklist and links the page; if the two differ, the page wins and `AGENTS.md` is corrected.
- **Structure.** Weekly logs in `prototype/implementation-logs/`, a human task list the AI never writes, a `prompts/` folder, a README in every top-level folder, `.link-check-ignore`, and `archive/` folders exempt from scans.
- **Rules.** Decisions are reviewed in chat before they are written. Research sessions may widen scope but don't draft decisions. `drafts/` is tracked in git.
- **Tooling.** Link checker, autolinker, lint, review scan, and tag aligner, ported as generic scripts with manual fallbacks (constitution D3).

## Alternatives Considered
- **Port only the protocols, not the scripts.** Rejected. The append-only rule and the zero-broken-links rule hold only because scripts check them.
- **Keep everything inline in `AGENTS.md`.** Rejected. The master file would grow past what some CLIs read in one call.

## Consequences
- The three examples are updated to the new template, including weekly logs and folder READMEs.
- The session-history line format gains `(agent, session type)`.
- The template's `.gitignore` stops ignoring `drafts/`.
