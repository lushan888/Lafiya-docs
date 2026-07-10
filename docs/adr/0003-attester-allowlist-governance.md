# ADR 0003: Attester allowlist governed by committee

## Status

Accepted

## Context

Anyone able to submit an attestation would make the "verified" indicator
meaningless — it must map to a real, accountable, licensed health worker.

## Decision

Only addresses on a governance-managed allowlist can call `attest`. Adding or
removing an attester requires committee action, not a CHW- or patient-level
credential.

## Consequences

- Verification integrity depends on allowlist integrity — this is now a
  governance problem as much as a technical one; see
  [threat-model.md](../threat-model.md#residual-risk).
- Onboarding a new health worker has a process cost (committee review)
  instead of being instant.
- A compromised or coerced attester is a known residual risk, mitigated by
  the [dispute process](../../README.md#attestation--trust-model), not by the
  allowlist itself.
