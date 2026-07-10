# AI.md — Lafiya Organization Map

A single entry point for an AI agent (or a new contributor) to understand how
the `lafiya-xyz` repos relate before making a change in any one of them.
Read this before touching a shared contract in any Lafiya repo.

## Repos

| Repo | Purpose | Priority |
|------|---------|----------|
| [`lafiya-web`](https://github.com/lafiya-xyz/lafiya-web) | Patient + responder web app (Next.js). Public emergency page, authed profile editor, QR generation. | **Build first** |
| [`lafiya-contracts`](https://github.com/lafiya-xyz/lafiya-contracts) | Soroban smart contracts (Rust): attestation registry + attester allowlist. Testnet first. | **Build next** |
| [`lafiya-docs`](https://github.com/lafiya-xyz/lafiya-docs) _(this repo)_ | Concept note, data model, threat model, privacy design, funding/DPG materials, references. | Start now (lightweight) |
| [`.github`](https://github.com/lafiya-xyz/.github) | Organization profile README and contribution guidelines. | Start now |
| `lafiya-verifier` | CHW verification tool. Begins as a route inside `lafiya-web`; split out only if it grows. | Later |

## Where to start in each repo

- **`lafiya-web`** — not yet scaffolded. When it exists, start at its own
  README, then read this repo's [data model](docs/data-model.md) and
  [API surface sketch](docs/api-surface-sketch.md) before writing profile or
  public-page code.
- **`lafiya-contracts`** — not yet scaffolded. Start at this repo's
  [attestation record schema](docs/data-model.md#attestation-record-on-chain-soroban),
  the [Soroban interface sketch](docs/api-surface-sketch.md#lafiya-contracts-soroban-interface-sketch),
  and [docs/adr/](docs/adr/README.md) for why the trust model looks the way
  it does.
- **`lafiya-docs`** (this repo) — start at [docs/README.md](docs/README.md).
  This is the source of truth every other repo builds against.
- **`.github`** — org-wide templates and the org profile README; not yet
  scaffolded.
- **`lafiya-verifier`** — no separate repo yet; CHW verification currently
  lives as a planned route inside `lafiya-web` (see
  [Core Components](README.md#core-components)).

## Shared contracts (must stay in sync across repos, once they exist)

- **Emergency data model** — [docs/data-model.md](docs/data-model.md) is the
  source of truth; `lafiya-web`'s profile schema must mirror it
  field-for-field.
- **Attestation record shape** — hash of record + attester identity +
  timestamp; specified here before `lafiya-contracts` implements the Soroban
  struct.
- **Environment/config keys** — none exist yet; the first will be Supabase
  and Stellar testnet keys needed by `lafiya-web`.

## Data flow

```
lafiya-docs ──(data model, threat model, privacy design)──▶  lafiya-web
                                                                  │
                                                     patient profile + QR
                                                                  │
                            lafiya-contracts (Soroban) ◀── attestation hash ── CHW verifies record
                                     │
                                     ▼
                          verified flag on public page
                                     │
                                     ▼
                          USDC payout to CHW (on Stellar)
```

## Conventions for AI agents working in any Lafiya repo

- Treat `lafiya-docs` as the source of truth for cross-repo contracts. Each
  repo's own README covers repo-local conventions once it exists.
- `lafiya-docs` currently contains **documentation only** — do not assume
  application or contract code lives there.
- No personal health data, secrets, or private keys belong in `lafiya-docs`,
  ever — only specs, models, and public materials.
- If a change in one repo touches a shared contract above, say so explicitly
  and open a matching issue in the affected repo(s) — don't let the repos
  drift silently out of sync.
- Don't invent URLs, contact details, or people. If a fact isn't confirmed,
  leave a clearly marked placeholder instead of a fabricated one.
