# Glossary

- **Attestation** — an on-chain Soroban record stating that an allowlisted
  health worker verified a patient record, without revealing the record
  itself.
- **Attester** — a health worker approved (allowlisted) to submit
  attestations.
- **CHW** — Community Health Worker; registers and verifies patients, paid in
  USDC per verified registration.
- **DPG** — Digital Public Good, per the Digital Public Goods Standard.
- **Emergency subset** — the minimal set of fields shown on the public,
  unauthenticated emergency page. See [data-model.md](data-model.md).
- **Genotype (AS/SS)** — hemoglobin genotype status relevant to sickle-cell
  risk; one of the highest-priority emergency fields.
- **NDPA** — Nigeria Data Protection Act (2023).
- **Responder** — an emergency responder or clinician scanning a patient's QR
  code; has no login and sees only the emergency subset.
- **RLS** — Row-Level Security, the Postgres/Supabase mechanism enforcing
  per-user data access.
- **Soroban** — Stellar's smart contract platform.
- **Verified indicator** — the UI signal on the public page confirming an
  attestation hash matches the currently displayed record.
