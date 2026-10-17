---
doctype: PDR
id: PDR-P002
domain: product
status: accepted
date: 2026-10-17
tags: [example, documentation, domain-agnostic]
constitution-clause: O1
supersedes: null
superseded-by: null
---
# PDR-P002: Three Example Vaults Replace BrewTrack

## Context
The BrewTrack example showed a vault on day one, with no protocol visibly at work. A single software example also implied the template is for code only. See [[ideas/rework-example-vault]].

## Decision
`example/` becomes `examples/` with three vaults, each a few weeks into its project:
- **`software/`**: a web app.
- **`business/`**: a small service business.
- **`creative/`**: an indie video game.

Each example shows every core protocol leaving a trace: a superseded decision, a rejected decision, research docs with maturity tags, a reweave that weakened an earlier decision, ideas in each resolution state, a draft next to its admitted version, and a session history.

## Alternatives Considered
- **Improve BrewTrack only.** Rejected. One software example can't show that the method works for business and creative projects.
- **One example per protocol.** Rejected. Protocols interact, and isolated demos hide that.

## Consequences
- Research in the examples is the fictional team's own primary research (interviews, pilots, playtests), so the examples cite no invented real-world sources.
- `website/docs/examples/` mirrors `examples/`.
- [[architecture/CONSTITUTION|CONSTITUTION]] O1 names `examples/`.
