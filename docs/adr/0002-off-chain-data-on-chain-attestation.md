# ADR 0002: Off-chain data, on-chain attestation only

## Status

Accepted

## Context

Putting health data on a public, immutable ledger is both a privacy risk
(data can never truly be deleted) and, in most jurisdictions, a compliance
non-starter.

## Decision

Personal health data lives exclusively in an encrypted, access-controlled
off-chain database (Supabase). Only a hash of the record, the attester's
identity, and a timestamp are ever written to Soroban.

## Consequences

- Deletion requests can be honored for the actual data; the on-chain hash
  reveals nothing on its own and needs no deletion.
- A responder can still verify integrity: re-hash the fetched record and
  compare it to the on-chain value.
- This makes NDPA 2023 compliance tractable — see
  [privacy-design.md](../privacy-design.md#ndpa-2023-compliance-mapping).
- Tradeoff: if the off-chain database is compromised, on-chain attestations
  for those records become historical artifacts pointing at data that may
  have changed; this is accepted because the alternative (health data
  on-chain) is strictly worse.
