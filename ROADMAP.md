<!-- # ⭐ 修改開始 ⭐ -->
# Public Roadmap

Languages: **English** | [繁體中文](ROADMAP.zh-TW.md)

This roadmap covers only public-safe engineering direction. Private deployment details, local audit outputs, credentials, device-specific paths, raw benchmark output, and unreviewed automation artifacts are intentionally excluded.

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
- Publish abstract data shapes before implementation details

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
- Preserve the difference between evidence, readiness, and runtime enablement

Outputs:

- stats-only status summary
- maintenance smoke summary
- viewer / panel display model

## P4: Proactive companion behavior

Goal:

- Support useful proactive suggestions without creating noise
- Keep reminders reviewable, rate-limited, and cancellable
- Prevent suggestions from bypassing policy or human review

Outputs:

- proactive suggestion model
- cooldown policy
- notification boundary

## P5: Embodiment adapter abstraction

Goal:

- Define safe interfaces for companion devices, wearables, and future hardware integrations
- Keep cognition and governance separate from low-level control
- Keep device-specific bridge paths outside the public repository

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

## P7: Boundary hardening and memory governance

Goal:

- Keep non-harm semantic boundaries testable before any high-risk runtime surface
- Keep private workspace hygiene separate from public release materials
- Treat memory and speculative capability notes as human-governance documents unless a later gated phase implements runtime support

Outputs:

- harm-boundary regression summary
- public/private release checklist
- human-readable memory governance summary

## P8: Human-supervised operating surface

Goal:

- Describe how review, approval, rejection, and follow-up can be represented without publishing private console data
- Keep the operating surface accountable without turning it into public automation
- Preserve append-only review semantics at the interface level

Outputs:

- review journal entry schema
- operator decision summary
- human-supervised console boundary notes

## P9: Public-safe evidence and model evaluation summaries

Goal:

- Summarize local evaluation evidence without publishing raw benchmark output or model assets
- Separate cold-start, steady-state, provider-overhead, and execution-scope claims
- Prevent evaluation evidence from becoming a production selection claim

Outputs:

- model evaluation summary schema
- runtime truth label guidance
- evidence caveat checklist

## P10: Credential and release-boundary hygiene

Goal:

- Keep credentials, provisioning details, device identifiers, and local secrets outside public history
- Document public mirror checks without disclosing private remediation details
- Treat credential rotation and provisioning as private operator tasks

Outputs:

- credential boundary summary schema
- public release checklist
- security posture notes

## Non-goals for the public repo

- Production deployment guide
- Secret or credential handling
- Device-specific bridge implementation
- Local audit logs
- Full private runtime mirror
- High-risk execution paths
- Machine-loadable private runtime configuration
- Raw model benchmark output
- Device provisioning instructions
<!-- # ⭐ 修改結束 ⭐ -->
