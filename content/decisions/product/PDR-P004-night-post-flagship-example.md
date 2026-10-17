---
doctype: PDR
id: PDR-P004
domain: product
status: accepted
date: 2026-10-17
tags: [example, website, quartz, game]
constitution-clause: O1
supersedes: null
superseded-by: null
---
# PDR-P004: Night Post Is the Flagship Example, Published With Quartz

## Context
Adam judged the three examples from [[decisions/product/PDR-P002-three-example-vaults|PDR-P002]] better but still thin, and asked for a full game vault that readers can explore interactively. [[ideas/quartz-for-example-site]] had proposed Quartz for this in April.

## Decision
The creative example becomes **Night Post**, an adventure RPG vault covering six months and about 90 files: decisions, research of every kind the project needs, a world bible, game design docs, and production plans. CI builds it with Quartz and publishes it at `/night-post/` next to the MkDocs docs, so the docs stay in one repo and one Pages site.

## Alternatives Considered
- **Keep Low Tide and expand it.** Rejected. A puzzle game has too few kinds of research to show breadth.
- **A separate repo, like the meta-vault.** Rejected for now. It adds a repo to maintain; the in-repo build pins Quartz `v4.5.2` and overlays two config files.
- **Render the game vault with MkDocs only.** Rejected. MkDocs has no graph view or backlinks, which are the point of exploring a vault.

## Consequences
- `website/quartz/` holds the Quartz config and `build.sh`, used by both CI and local preview.
- Software and business examples stay small and MkDocs-only.
- Resolves [[ideas/quartz-for-example-site]].
