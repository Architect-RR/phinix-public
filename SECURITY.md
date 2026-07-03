<!-- # ⭐ 修改開始 ⭐ -->
# Security Policy

## Scope

This public repository is intended for:

- architecture discussion
- public-safe documentation
- low-risk interface design
- public collaboration on boundaries and validation

It is not intended to expose private deployment details, credentials, device-specific bridge internals, local maintenance artifacts, raw benchmark output, or provisioning instructions.

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
- Raw model benchmark output
- Device provisioning details

## Credential Hygiene Posture

The public repository should only describe credential boundaries at a policy level.

Acceptable public content:

- credential boundary summaries without values
- public/private release checklist items
- general log-minimization posture
- high-level security review expectations

Not acceptable public content:

- secret values
- token prefixes or suffixes
- rotation records
- provisioning commands
- private device package names or identifiers
- local file paths used for secret storage

Credential rotation, device provisioning, and local secret storage remain private operator tasks.

## Reporting Security Concerns

Do not open a public issue with sensitive details.

Start with a high-level description and wait for maintainer guidance before sharing technical detail. If a concern involves credentials, private device paths, local audit files, or deployment details, keep those details out of public channels.

## Current Posture

PHINIX is under active engineering development. Public materials describe architecture direction and public-safe status, not production deployment guarantees.

Contributors should assume:

- boundaries may change
- hardening is ongoing
- private implementation is intentionally not mirrored
- high-risk execution paths are outside public scope
- boundary-hardening summaries do not imply runtime actuation is enabled
- abstract schemas do not imply the private runtime exposes a public API

## Contribution Rule

Security-related contributions are welcome. Changes that weaken governance, auditability, device boundaries, or public/private separation should not be proposed as convenience improvements.
<!-- # ⭐ 修改結束 ⭐ -->
