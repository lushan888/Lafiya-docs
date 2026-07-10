# Roadmap (detail)

This expands the milestone list in the
[root README](../README.md#roadmap). Each milestone is a working increment,
not a sprint — M(n+1) does not start in earnest until M(n) has a working
demo.

## Phase 0 — Documentation foundation

**Goal:** every design decision M0 depends on is written down before any app
or contract code exists. Status: **done**, entirely within this repo.

- [x] Concept note, data model, threat model, and privacy design specified
- [x] Architecture Decision Records for the Stellar/Soroban trust model, the
      `lafiya-web` stack, and CHW incentives (see [adr/](adr/README.md))
- [x] Contributor infrastructure: `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`,
      `SECURITY.md`, `LICENSE` (Apache-2.0), issue/PR templates, and
      markdown-lint CI
- [ ] `lafiya-web` and `lafiya-contract` repos scaffolded — not started;
      this is what M0 below actually requires next

## M0 — Public card (testnet)

**Goal:** one patient can create a profile and expose a working read-only
emergency page via QR. **Status: not started** — blocked on scaffolding
`lafiya-web`.

- Patient signup/login (`lafiya-web`)
- Profile editor covering the full [data model](data-model.md)
- Public emergency page rendering the emergency subset only
- QR generation pointing at the public page
- No attestation yet — page shows "unverified"

## M1 — Attestation

**Goal:** an allowlisted attester can verify a record; the card shows a
verified indicator.

- Soroban attestation registry contract (`lafiya-contract`), Testnet
- Attester allowlist (governance-managed)
- `lafiya-web` submits the record hash on attestation and checks it on page
  load

## M2 — Incentives

**Goal:** CHWs are paid in USDC per verified registration.

- USDC-on-Stellar payout flow tied to a completed attestation
- CHW-facing view of registrations and payouts (may live in
  `lafiya-verifier`)

## M3 — Pilot

**Goal:** a small, supervised field pilot.

- Metrics: verified cards created, scan events (see
  [concept-note.md](concept-note.md#success-metrics))
- Dispute process exercised at least once end-to-end

## M4 — Mainnet + funding

**Goal:** launch on mainnet; open a transparent funding pool.

- Mainnet deployment of `lafiya-contract`
- Public, on-chain-traceable funding pool for CHW incentives
- DPG Standard registration (see [funding-and-dpg.md](funding-and-dpg.md))
