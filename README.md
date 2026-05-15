# PHINIX Public Overview

PHINIX is a private-first, local-first governed agent runtime project.

This public repository contains only the engineering-safe project overview, architecture notes, collaboration boundaries, and interface direction. The complete private runtime, device bridge details, local credentials, hardware configuration, audit artifacts, and deployment-specific implementation remain outside this repository.

## Current Position

PHINIX is not a chatbot wrapper. The project is organized around a governed runtime pattern:

```text
inputs
-> runtime state
-> policy and risk gates
-> proposal generation
-> sandbox validation
-> audit
-> human or operator review
```

The practical goal is to make agent behavior observable, reviewable, testable, and reversible before it can affect higher-risk systems.

## Public Repository Contents

- High-level architecture summaries
- Public/private scope rules
- Public roadmap
- Contribution and security guidance
- Abstract interface directions
- Public-safe status reports

This repository intentionally does not include:

- Private deployment code
- Device credentials or bridge tokens
- Hardware allowlists
- Local audit logs
- Model weights or model asset manifests
- Unreviewed automation outputs
- Private maintenance reports

## Current Engineering Focus

The private project is currently focused on:

- Runtime and side-effect observability
- Proposal-based improvement flow
- Sandbox validation before promotion
- Lab-only maintenance smoke tests
- Read-only status summaries
- Strict public/private boundary control

Public updates will stay at the level of architecture, interfaces, and verifiable engineering status. Private implementation details are intentionally summarized rather than mirrored.

## Documentation

- [Architecture Overview](ARCHITECTURE_OVERVIEW.md)
- [Public Scope](PUBLIC_SCOPE.md)
- [Roadmap](ROADMAP.md)
- [Current Status](CURRENT_STATUS.zh-TW.md)
- [Contributing](CONTRIBUTING.md)
- [Security](SECURITY.md)

Traditional Chinese documents are available for key public pages where useful.

## Collaboration Boundary

Issues and pull requests should focus on:

- Architecture feedback
- Interface design
- Public-safe documentation
- Risk and governance review
- Low-risk examples or simulation stubs

Do not submit secrets, private device details, production credentials, local audit files, or unreviewed automation outputs.
