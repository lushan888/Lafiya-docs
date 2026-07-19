# Security Policy

## Scope

This repository (`lafiya-docs`) contains documentation only — no application or contract code lives here. There is nothing here to have a code-level vulnerability, but the design decisions in this repo (the [data model](docs/data-model.md), [threat model](docs/threat-model.md), and [privacy design](docs/privacy-design.md)) shape the security posture of every other Lafiya repo, so design-level reports are welcome and taken seriously.

## What to report here

- A gap or incorrect assumption in the [threat model](docs/threat-model.md)
- A flaw in the proposed attestation scheme or the on-chain/off-chain boundary described in [privacy-design.md](docs/privacy-design.md)
- A privacy issue in the [data model](docs/data-model.md) — e.g. a field proposed for the public emergency subset that shouldn't be there

## How to report

Please report privately via a **GitHub Security Advisory** on this repository rather than a public issue, so the report can be reviewed before any sensitive detail is public.

## Reporting vulnerabilities in the running application or contracts

Once `lafiya-web` and `lafiya-contract` exist and ship code, report vulnerabilities in those systems in their own repositories, following their respective `SECURITY.md` files.

## Supported versions

Lafiya is pre-alpha, Stellar **testnet** only. No production deployment exists yet, so there is no supported-version matrix to publish.

## Researcher Acknowledgement Policy

### Security Hall of Fame

We value and recognize the contributions of security researchers who help strengthen Lafiya's security posture. A permanent `Security Hall of Fame` section will be maintained in this document to honor researchers who submit valid reports in good faith.

### Conditions for Acknowledgment

To qualify for recognition in the Security Hall of Fame, a report must meet the following criteria:

- The report identifies a valid security issue or design flaw in scope of this repository or the broader Lafiya project
- The report includes a clear description and, where applicable, a proof-of-concept demonstrating the issue
- The report is submitted privately via designated channels (GitHub Security Advisory for this repository)
- The researcher adheres to responsible disclosure practices and does not publicly disclose the issue before a patch or mitigation is deployed
- The researcher's disclosure does not violate any laws or cause harm to Lafiya users or systems

Acknowledgment is added after the report has been validated and the issue has been remediated, mitigated, or formally accepted by the maintainers.

### Monetary Reward Differentiation

Inclusion in the Security Hall of Fame is credential-based recognition and is separate from financial compensation. Any monetary reward decisions are handled through the official bug bounty tracker, `Lafiya Bug Bounty Campaign #5`.

## Security Hall of Fame

_We look forward to acknowledging our first good-faith security researchers here!_

- **[Slot Open]** — Awaiting the first verified responsible disclosure.
