# Contributing to Lafiya

Thanks for your interest in Lafiya — an open-source Digital Public Good. This
repository (`lafiya-docs`) is documentation only: the concept note, data
model, threat model, privacy design, and funding materials the rest of the
`lafiya-xyz` organization is built against. See the [root README](README.md#lafiya-organization)
for where application and contract code live.

## Before you open a PR

For anything beyond a typo or broken link, please open an issue first using
the **Proposal** template. This is especially important for changes to the
[data model](docs/data-model.md) or [attestation record schema](docs/data-model.md#attestation-record-on-chain-soroban) —
these are shared contracts with `lafiya-web` and `lafiya-contracts`, and
changing them here without warning breaks other repos silently.

## Making the change

1. Fork and branch from `main`.
2. Follow the [docs style guide](docs/style-guide.md).
3. Run the markdown linter locally if you have Node available:
   ```bash
   npx markdownlint-cli2 "**/*.md"
   ```
   CI runs the same check on every PR.
4. Update [docs/README.md](docs/README.md)'s index if you add a new document.
5. If your change affects a shared contract (data model, attestation schema,
   env/config keys), say so explicitly in the PR description using the
   checklist in the PR template, and open a matching issue in the affected
   repo(s).

## Commit and PR style

- Write commit messages that explain *why*, not just *what*.
- Keep PRs scoped to one topic — a data model change and a typo fix belong in
  separate PRs.

## Code of Conduct

By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).

## Reporting a security or privacy issue

Please don't open a public issue for a security or privacy concern — see
[SECURITY.md](SECURITY.md).
