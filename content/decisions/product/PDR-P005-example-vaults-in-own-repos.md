---
doctype: PDR
id: PDR-P005
domain: product
status: accepted
date: 2026-10-17
tags: [example, repository-structure, website]
constitution-clause: O1
supersedes: "[[decisions/product/PDR-P002-three-example-vaults]]"
superseded-by: null
---
# PDR-P005: Two Example Vaults, Each in Its Own Repo

## Context
Night Post outgrew the other examples ([[decisions/product/PDR-P004-night-post-flagship-example|PDR-P004]]), and every template change had to be applied to three vaults. Readers also couldn't see an example the way they'd see their own vault: as a repo they clone and open in Obsidian.

## Decision
Keep two examples, Night Post (creative) and Curbside Cycles (business), each in its own public repo with its own Quartz site: `adamcee/night-post-vault` and `adamcee/curbside-cycles-vault`. The vault sits at the repo root, and the publishing setup lives in a hidden `.site/` folder. The main docs link out to both; Brigade (software) is dropped.

## Alternatives Considered
- **Keep all three in the main repo.** Rejected. Readers can't see a vault as a standalone repo, and upkeep triples.
- **Keep only Night Post.** Rejected. A business vault shows the method on a project with no software and no creative work, which Night Post can't.

## Consequences
- Template changes must be applied to both example repos by hand.
- The main repo drops `examples/`, the Quartz build, and the MkDocs wikilink hook.
- Each example README uses plain markdown links so it works on GitHub, in Quartz, and in Obsidian.
