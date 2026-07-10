# Security Policy

## Scope

This repository (`lafiya-docs`) contains documentation only — no application
or contract code lives here. There is nothing here to have a code-level
vulnerability, but the design decisions in this repo (the
[data model](docs/data-model.md), [threat model](docs/threat-model.md), and
[privacy design](docs/privacy-design.md)) shape the security posture of every
other Lafiya repo, so design-level reports are welcome and taken seriously.

The full bug bounty program specification is documented in
[docs/bug-bounty-program.md](docs/bug-bounty-program.md).

## Bug Bounty Program

Lafiya operates a formal bug bounty program for all repositories in the
Lafiya ecosystem. See the [program specification](docs/bug-bounty-program.md)
for:

- **In-scope vs. out-of-scope targets** (1.2–1.3)
- **Reward tiers by severity** (2.1) — from 50 XLM (Informational) to 5,000 XLM (Critical)
- **Disclosure timeline** (3.2) — 90-day private disclosure period
- **How to report** (4.1) — via GitHub Security Advisory or `security@lafiya.xyz`

## Reward Tiers (Summary)

| Severity | Testnet Reward | Mainnet Equivalent (USD est.) |
|---|---|---|
| Critical | 5,000 XLM | ~$1,500 |
| High | 2,000 XLM | ~$600 |
| Medium | 500 XLM | ~$150 |
| Low | 100 XLM | ~$30 |
| Informational | 50 XLM | ~$15 |

## How to Report

Please report vulnerabilities via a **GitHub Security Advisory** on this
repository (or the relevant application repository) rather than a public
issue. Security reports should include:

- Clear description of the vulnerability
- Steps to reproduce (with PoC where possible)
- Impact assessment
- Suggested fix (optional)

**Do not** create public issues for security vulnerabilities. See
[docs/bug-bounty-program.md](docs/bug-bounty-program.md) §4 for details.

## Disclosure Timeline

- **Triage**: 5 business days
- **Private disclosure period**: 90 days (60 days for Critical)
- **Public disclosure**: After coordinated fix + advisory release

See [docs/bug-bounty-program.md](docs/bug-bounty-program.md) §3 for the
full timeline.

## Reporting vulnerabilities in the running application or contracts

Once `lafiya-web` and `lafiya-contract` ship code, vulnerabilities should
be reported in their respective `SECURITY.md` files. The bug bounty program
applies to all Lafiya repositories.

## Supported versions

Lafiya is pre-alpha, Stellar **testnet** only. No production deployment
exists yet. Post-mainnet, the latest stable release will be the only
supported version.
