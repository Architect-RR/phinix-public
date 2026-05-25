# Security Policy

## Scope

This public repository is intended for:

- architecture discussion
- public-safe documentation
- low-risk interface design
- public collaboration on boundaries and validation

It is not intended to expose private deployment details, credentials, device-specific bridge internals, or local maintenance artifacts.

## Do Not Disclose

- Tokens or API keys
- Private bridge credentials
- Device identifiers
- Raw user interaction logs
- Local audit reports
- Hardware allowlists
- Unreviewed automation outputs
- Device-specific execution paths
- Sensitive prompt corpora or private boundary-test probes
- Private workspace inventories, vault paths, or local memory archives

## Reporting Security Concerns

Do not open a public issue with sensitive details.

Start with a high-level description and wait for maintainer guidance before sharing technical detail. If a concern involves credentials, private device paths, or local audit files, keep those details out of public channels.

## Current Posture

PHINIX is under active engineering development. Public materials describe architecture direction and public-safe status, not production deployment guarantees.

Contributors should assume:

- boundaries may change
- hardening is ongoing
- private implementation is intentionally not mirrored
- high-risk execution paths are outside public scope
- boundary-hardening summaries do not imply runtime actuation is enabled

## Contribution Rule

Security-related contributions are welcome. Changes that weaken governance, auditability, device boundaries, or public/private separation should not be proposed as convenience improvements.
