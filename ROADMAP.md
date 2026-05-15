# Public Roadmap

Languages: **English** | [繁體中文](ROADMAP.zh-TW.md)

This roadmap covers only public-safe engineering direction. Private deployment details, local audit outputs, credentials, device-specific paths, and unreviewed automation artifacts are intentionally excluded.

## P0: Public project baseline

Goal:

- Maintain a clear public overview
- Define public/private boundaries
- Keep documentation professional and engineering-focused

Outputs:

- README
- public scope
- architecture overview
- roadmap
- security and contribution guidance

## P1: Runtime architecture interfaces

Goal:

- Document the core runtime layers
- Keep client entry points thin
- Separate live interaction, background state, policy, and validation

Outputs:

- runtime state model
- event flow model
- stuck issue model
- proposal model

## P2: Governed improvement flow

Goal:

- Convert failures and low-quality states into reviewable proposals
- Validate improvements in sandbox or worktree before promotion
- Keep tests, rollback plans, and audit records attached to each change

Outputs:

- proposal schema
- sandbox validation interface
- audit summary interface
- promotion status model

## P3: Read-only observability

Goal:

- Surface limited runtime health status without exposing private audit data
- Keep observability separate from execution

Outputs:

- stats-only status summary
- maintenance smoke summary
- viewer / panel display model

## P4: Proactive companion behavior

Goal:

- Support useful proactive suggestions without creating noise
- Keep reminders reviewable, rate-limited, and cancellable

Outputs:

- proactive suggestion model
- cooldown policy
- notification boundary

## P5: Embodiment adapter abstraction

Goal:

- Define safe interfaces for companion devices, wearables, and future hardware integrations
- Keep cognition and governance separate from low-level control

Outputs:

- embodiment adapter interface
- device capability descriptor
- authorized-device boundary model

## P6: Controlled maintenance automation

Goal:

- Allow bounded lab-only maintenance loops
- Keep automation disabled by default
- Require status checks, stop conditions, and audit output

Outputs:

- auto maintenance contract
- dry-run report
- bounded runner configuration

## Non-goals for the public repo

- Production deployment guide
- Secret or credential handling
- Device-specific bridge implementation
- Local audit logs
- Full private runtime mirror
- High-risk execution paths
