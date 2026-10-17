---
id: rework-example-vault
date: 2026-10-17
status: resolved
tags: [example, documentation, website]
resolved-by: "[[decisions/product/PDR-P002-three-example-vaults]]"
---
# Idea: Rework the Example Vault

## Context
Adam called the BrewTrack example weak. It shows a vault on day one: one ADR, one PDR, a constitution, and a plan. `research/`, `ideas/`, `concepts/`, `strategy/`, and `drafts/` are empty.

## Problems
- **No protocol is shown working.** There is no rejected or superseded decision, no research doc with maturity tags, no `## Reweave Triggers` section, no resolved idea, no draft promotion, and no session history.
- **It breaks its own rules.** PDR-P001 cites the "endowed progress effect" with no research link or `[unsourced]` flag.
- **Its README is the template README.** It tells readers to run `./scripts/init-vault.sh`, which doesn't exist in `example/`.
- **The domain is a toy.** A coffee-shop loyalty app never produces the long-running relitigation the vault exists to stop.

## Proposal
Show a vault a few weeks in. Keep it small, but make each protocol leave a visible trace:
- One ADR superseded by a later one, plus one record in `decisions/rejected/`.
- Two or three research docs with maturity tags, one of which triggered a reweave that weakened an earlier decision.
- An `ideas/` note for each resolution: promoted, rejected, absorbed, open.
- A draft in `drafts/` next to its tightened, admitted version and its `_source-` original.
- A `session-history.md` with several entries and a filled-in checkpoint.
- A README written for the example, explaining what to look at.

The domain could stay a software product or switch to non-code work (a nonfiction book, a research project) to show the template isn't code-only. Adam to choose.

## Related
- [[prototype/implementation-plan]] Phase 7 lists broken BrewTrack links on the website.
- [[ideas/quartz-for-example-site]] proposes rendering the example with Quartz.
