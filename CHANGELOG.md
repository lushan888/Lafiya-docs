# Changelog

All notable changes to this repository are documented here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- Full documentation set: concept note, data model, threat model, privacy
  design, data retention policy, funding & DPG notes, detailed roadmap,
  personas, FAQ, forward-looking API/contract surface sketch, testing
  strategy, and style guide
- Architecture Decision Records (ADR 0001–0006) covering the Stellar/Soroban
  choice, the on-chain/off-chain boundary, attester governance, the
  `lafiya-web` stack, USDC incentives, and attester key management
- Contributor-facing files: `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`,
  `SECURITY.md`, `LICENSE` (Apache-2.0), PR and issue templates, a
  `CODEOWNERS` placeholder
- Markdown lint CI workflow and configuration
- README restructured to a professional, org-wide format covering overview,
  architecture, trust model, repository structure, roadmap, and cross-repo
  conventions
- README's Lafiya Organization section gained a linked repo table, a
  "Where to Start (per repo)" guide, and expanded AI-agent conventions
- License badge; Roadmap section now links to `docs/roadmap.md` instead of
  duplicating it silently; Tech Stack choices link to their ADRs

### Fixed

- Markdown lint findings across the repo (table style, missing fenced-code
  languages, inconsistent emphasis markers, bold text used as headings, a
  bare URL, and stray blank lines) — CI's markdown-lint workflow now passes
  cleanly
- `docs/funding-and-dpg.md`'s DPG licensing checklist row, which still said
  "planned" after `LICENSE` was added to this repo

### Removed

- `AI.md` — its cross-repo map was folded into README's Lafiya Organization
  section instead of living as a separate file
