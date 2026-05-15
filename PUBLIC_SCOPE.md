# Public Scope

Languages: **English** | [繁體中文](PUBLIC_SCOPE.zh-TW.md)

This document defines what belongs in the public PHINIX repository and what must remain private.

## Suitable for Public Release

### Documentation

- Project overview
- High-level architecture
- Public roadmap
- Contribution rules
- Security contact and reporting process
- Public-safe status summaries

### Abstract Interfaces

- Runtime state interfaces
- Event and message shapes
- Stuck issue and retry models
- Proposal and audit summary models
- Embodiment adapter abstractions
- Read-only status summaries

### Low-Risk Examples

- Mock data
- Simulation stubs
- Interface skeletons
- Documentation examples

### Collaboration Material

- Issue templates
- PR template
- Architecture discussion prompts
- Public-safe review topics

## Must Stay Private

### Credentials and Local Configuration

- Tokens
- API keys
- Bridge credentials
- Local machine configuration

### Private Operational Data

- Raw conversation logs
- Raw audio or image captures
- Device identifiers
- Hardware allowlists
- Local audit reports
- Lab maintenance artifacts

### Large or Vendor-Specific Assets

- APK build outputs
- SDK or JDK archives
- Vendor binaries
- Device analysis artifacts
- Model weights

### Sensitive Implementation Details

- Device-specific bridge internals
- Direct actuation paths
- Unreviewed automation outputs
- Private maintenance loops
- High-risk domain execution details

## Public Release Rule

Public content should be:

- understandable
- reviewable
- safe to discuss
- honest about incompleteness
- free of credentials and private operational data

When in doubt, keep implementation details private and publish only the interface or architecture summary.
