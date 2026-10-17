# Idea: Use Quartz for the Example Vault Site

## Proposal
Keep MkDocs for the linear docs (landing page, methodology, setup) and render an example vault with Quartz.

## Why
The vault's value is a linked graph of notes, and MkDocs presents books and chapters. Quartz renders Obsidian vaults directly:
- **Graph view** shows decisions connected to research and strategy.
- **Backlinks** on every page show how a reweave finds affected docs.
- **Hover previews** let readers follow a link without leaving the page.
- **Obsidian syntax** (callouts, tags, frontmatter) works without plugins.

## Tradeoffs
- **Two build tools.** MkDocs runs on Python and Quartz on Node.
- **Two looks.** The docs and the example vault use different themes.

## Outcome
Resolved by [[decisions/product/PDR-P004-night-post-flagship-example|PDR-P004]]: Night Post is built with Quartz inside the docs deploy.
