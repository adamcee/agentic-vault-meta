---
doctype: PDR
id: PDR-P001
domain: product
status: accepted
date: 2026-10-17
tags: [documentation, domain-agnostic, website, template]
constitution-clause: D1
supersedes: null
superseded-by: null
---
# PDR-P001: No Source-Project References in the Public Repo

## Context
[[architecture/CONSTITUTION|CONSTITUTION]] D1 kept the source project out of `template/` only. The website still named the source project and described its domain, and `sources.md` carried examples from it until commit `af4e23b` (2026-05-06) removed them as confusing.

## Decision
Nothing in the `agentic-vault` repo (`template/`, `example/`, `website/`, `README.md`) names or describes the source project. Field-test evidence stays, stated generically: scale, duration, tools used, and the failures that produced each protocol.

## Alternatives Considered
- **Name the project as provenance.** Rejected. Readers fixate on the domain, and the specifics don't help them use the method.
- **Drop the field test entirely.** Rejected. The failure-to-protocol history is the main evidence that each protocol is needed.

## Consequences
- D1 now covers the whole public repo, not just `template/`.
- Examples in the docs use generic cases (MongoDB, Postgres) or the [[ideas/rework-example-vault|example vault]].
