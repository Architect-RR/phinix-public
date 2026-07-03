<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX Public Overview

PHINIX is a private-first, local-first governed agent runtime project.

This public repository contains the engineering-safe project overview, public/private boundaries, architecture notes, roadmap, and abstract interface direction. The private runtime, device bridge implementation, credentials, hardware configuration, raw audit artifacts, and deployment-specific implementation remain outside this repository.

Languages: **English** | [繁體中文](README.zh-TW.md)

## Current Position

PHINIX is not a chatbot wrapper. It is organized around a governed runtime pattern:

```text
input
-> runtime state
-> policy and risk gate
-> proposal record
-> sandbox or dry-run validation
-> human or operator review
-> audit summary
```

The practical goal is to make agent behavior observable, reviewable, testable, and reversible before it can affect higher-risk systems.

## What Makes This Different

PHINIX is being built around a conservative operating model:

- Governed runtime over direct automation.
- Proposal-before-action instead of silent mutation.
- Human-supervised review surfaces before promotion.
- Append-only review traces for accountable decisions.
- Public/private release discipline for local-first systems.
- Thin-client device and companion boundaries rather than device-specific control paths in public.

These are engineering boundaries, not marketing claims. Public artifacts describe architecture, interface shape, and status. They do not expose the private runtime or assert production autonomous execution.

## Completed Public-Safe Capability Areas

The private engineering track has completed the following capability areas at a public-safe level of description:

| Area | Completed capability | Public boundary |
|---|---|---|
| Human review escalation | Failure, low-quality output, and risk signals can be converted into reviewable escalation items. | Public repo describes the pattern only; private review data and audit records stay private. |
| Proposal-based improvement flow | Improvement requests can be represented as structured proposals with scope, forbidden edits, tests, risk notes, and rollback expectations. | Public repo does not expose private patch content or local maintenance reports. |
| Sandbox validation workflow | Work can be evaluated through dry-run, worktree validation, patch checks, tests, and promotion-readiness gates. | This is not public production execution or deployment approval. |
| Human-supervised console pattern | Review, approval, rejection, and follow-up can be represented as supervised operating records. | Public repo exposes only abstract interface shape, not private console data. |
| Append-only journal pattern | Review traces can be represented as append-only records for accountability. | Raw journals, local operator notes, and private audit entries are not mirrored publicly. |
| Error and repair candidate tracking | Error states and repair ideas can be represented as proposal-only candidates. | Candidates are not automatically applied and do not imply production mutation. |
| Read-only observability | Runtime and maintenance status can be summarized through stats-only views. | Full audit logs, raw results, local errors, and branch details are not mirrored publicly. |
| Lab-only maintenance contract | Bounded maintenance loops are defined for private lab use with stop conditions and audit expectations. | No public auto-runner, scheduler, push, merge, or release automation is exposed here. |
| Local model evaluation boundary | Local model checks can be summarized as evaluation evidence with cold-start, latency, and provider-overhead boundaries. | The public repo does not publish model weights, raw benchmark output, vendor assets, or production model selection. |
| Model asset boundary | Large model assets are kept outside the repository boundary and tracked through registry / manifest / hash-style governance. | Weights, adapters, tokenizers, embeddings, and vendor assets are not published here. |
| Companion / wearable governance | Device-facing directions are treated as thin-client or adapter boundaries governed by local authorization. | Device-specific bridge details, credentials, allowlists, and hardware paths remain private. |
| Credential hygiene boundary | Credential handling, log minimization, and public/private release checks are treated as a separate security surface. | Public docs state the posture only; secrets, rotation data, and provisioning details stay private. |
| Non-harm semantic boundary layer | Private policy/test coverage includes direct, indirect, authorization-override, and device-mediated harm-boundary wording. | This is a governance and regression-test layer; it is not public autonomous actuation or deployment approval. |
| Codebase introspection schema layer | A private plan/read-model layer exists for codebase index style introspection. | It is schema/read-model only; it does not expose private scanner outputs or invoke runtime scanners from this public repo. |
| Source verification schema layer | A private plan/result-schema layer exists for source verification and citation-aware governance. | It is plan/schema only; runtime RAG, live LLM calls, source fetching, and citation checking remain deferred to separate gated phases. |
| Private workspace hygiene | Private-only notes, local artifacts, and public-mirror content are separated through explicit inventory and release-boundary rules. | Public docs describe the rule; private vault paths, raw checkpoints, and local artifact names stay private. |
| Memory governance policy | Long-term memory, engineering calculation edge cases, and research notes are documented as human-governance policy. | It is not a machine-loadable runtime configuration and does not imply those capabilities are implemented. |

## What Is Not Claimed

This public repository does not claim that PHINIX currently exposes:

- production-grade autonomous actuation
- public runtime RAG or live LLM execution
- production deployment instructions
- device-specific bridge implementation
- complete private runtime source
- raw audit logs or local maintenance data
- model weights or model asset manifests
- unreviewed automation outputs
- public approval to execute high-risk physical, financial, medical, or device-control actions

When a capability is described as plan, schema, read-model, proposal-only, or governance-hint level, it means the current artifact defines reviewable structure and boundaries. It does not mean the runtime execution layer is publicly available or enabled.

## Public Repository Contents

- High-level architecture summaries
- Public/private scope rules
- Public roadmap
- Contribution and security guidance
- Abstract interface schemas
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

- runtime and side-effect observability
- proposal-based improvement flow
- sandbox validation before promotion
- human-supervised console and append-only journal style audit surfaces
- error-ledger and repair-candidate tracking for proposal-only maintenance
- companion / wearable credential hygiene and log minimization
- local model evaluation boundaries
- schema-first and plan-first capability governance
- source-verification and citation-boundary planning
- non-harm semantic boundary regression testing
- private workspace hygiene and memory-governance documentation
- lab-only maintenance smoke tests
- read-only status summaries
- strict public/private boundary control

Public updates stay at the level of architecture, interface shape, and verifiable engineering status. Private implementation details are intentionally summarized rather than mirrored.

Latest public-safe status: 2026-07-03. Recent private work strengthened human-supervised review surfaces, append-only audit-style records, companion credential hygiene, local model evaluation boundaries, and gated runtime probes. This does not mean autonomous production execution is publicly available or enabled.

## Documentation

- [Architecture Overview](ARCHITECTURE_OVERVIEW.md)
- [Public Scope](PUBLIC_SCOPE.md)
- [Roadmap](ROADMAP.md)
- [Current Status](CURRENT_STATUS.md)
- [Current Status, Traditional Chinese](CURRENT_STATUS.zh-TW.md)
- [Public Interfaces](interfaces/README.md)
- [Contributing](CONTRIBUTING.md)
- [Security](SECURITY.md)

## Collaboration Boundary

Issues and pull requests should focus on:

- architecture feedback
- interface design
- public-safe documentation
- risk and governance review
- low-risk examples or simulation stubs

Do not submit secrets, private device details, production credentials, local audit files, raw model assets, or unreviewed automation outputs.
<!-- # ⭐ 修改結束 ⭐ -->
