---
doctype: ADR
id: ADR-T001
domain: technical
status: accepted
date: 2026-10-17
tags: [template, master-file, agents-md, session-protocol]
constitution-clause: D2
supersedes: null
superseded-by: null
---
# ADR-T001: AGENTS.md Is the Template's Master File

## Context
The template split its master context across two files: `SYSTEM.md` (constraints, decisions, protocols) and `AGENTS.md` (directory map, stack). Agents had to read both, and each file called itself the single source of truth. `AGENTS.md` is a cross-tool convention that Codex, Cursor, and other agents read by default, and the source vault already moved its master context there.

## Decision
The template merges `SYSTEM.md` into `AGENTS.md` and deletes `SYSTEM.md`. `CLAUDE.md`, `GEMINI.md`, `.cursorrules`, and `.windsurfrules` stay as short pointers to `AGENTS.md` that hold only tool-specific notes. The template also gains an append-only `session-history.md`; its last `## YYYY-MM-DD` heading is the last session date the Session Start Protocol reads.

## Alternatives Considered
- **Keep `SYSTEM.md` as the master and `AGENTS.md` as the map.** Rejected. Two files claiming authority is the drift the vault exists to prevent.
- **Rename `SYSTEM.md` to `AGENTS.md` without merging.** Rejected. It would leave the directory map in a second file that agents might skip.

## Consequences
- Every doc, skill, script, and example that names `SYSTEM.md` changes to `AGENTS.md`.
- The website page "SYSTEM.md Primacy" becomes "AGENTS.md Primacy" at a new URL.
- [[architecture/CONSTITUTION|CONSTITUTION]] D2 names `AGENTS.md`.
