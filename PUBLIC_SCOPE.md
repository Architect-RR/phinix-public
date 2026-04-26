# Public Scope

This document defines what should live in the public GitHub repository and what should remain private.

## Safe to publish

### Documentation

- project vision
- architecture overviews
- roadmaps
- public collaboration rules
- non-sensitive checkpoint summaries

### Abstract interfaces

- runtime layer interfaces
- memory and world-state schemas
- stuck-issue and proactive-suggestion models
- embodiment adapter interfaces

### Low-risk examples

- mock data
- non-sensitive test skeletons
- simulation stubs without hardware coupling
- public developer notes and helper scripts

### Community materials

- issue templates
- PR templates
- design discussions
- expert feedback prompts

## Keep private

### Secrets and credentials

- tokens
- API keys
- bridge credentials
- local environment configuration

### Private operational data

- raw dialogue logs
- raw voice data
- device identifiers
- hardware allowlists and authorization details

### Large artifacts and vendor blobs

- APK build outputs
- SDK and JDK archives
- vendor binaries
- reverse-engineered artifacts

### Sensitive implementation details

- direct embodiment control chain details
- unstable governance internals
- device control paths that are easy to misuse

## Suggested split

### Public repo

- public documentation
- cleaned interface definitions
- low-risk reusable skeletons

### Private repo

- operational runtime
- sensitive bridge logic
- training and evaluation data
- build toolchains
- deployment configuration
- hardware-specific implementation

## Release rule

Public content should be:

- understandable
- discussable
- safe to collaborate on
- honest about what is not yet implemented
