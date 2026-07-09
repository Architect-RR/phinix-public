<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX Current Status

Updated: 2026-07-09

Languages: **English** | [繁體中文](CURRENT_STATUS.zh-TW.md)

PHINIX is a private-first, local-first governed agent runtime project. The public repository contains only public-safe status, architecture direction, public/private boundary notes, and abstract interface shapes. The private runtime, device bridge implementation, credentials, hardware setup, raw audit artifacts, and deployment-specific implementation remain private.

## Public Wording Rules

Use the following distinctions when describing the project:

- "Governed runtime" does not mean production autonomous execution.
- "Sandbox validation" does not mean deployment approval.
- "Read-only status" does not mean public access to raw audit data.
- "Proposal-based improvement" does not mean automatic mutation.
- "Plan / schema layer" does not mean runtime execution is public or enabled.
- "Policy / test layer" does not mean real hardware, real LLM, or autonomous actuation is public or enabled.

## Current Position

PHINIX is best described as:

> A local-first, governed agent runtime for companion, wearable, and long-horizon tool-use scenarios.

Its current engineering direction prioritizes:

- observable state
- explicit risk boundaries
- policy gates
- reviewable proposals
- validation before promotion
- human-supervised operation
- reversible changes
- public/private release discipline

## 2026-07 Public-Safe Update

The private engineering track strengthened governance observability, credential hygiene, human-supervised operation surfaces, and proposal-only repair candidate flows during 2026-06 to 2026-07. The public repository records only the engineering direction and boundaries. It does not publish runtime source, device bridge details, tokens, raw logs, or local audit records.

Current public-safe summaries:

- Human-supervised console / journal: private work added supervised console and append-only journal style data layers for review, approval, rejection, and follow-up traces. This is not public autonomous execution.
- Error / repair candidate tracking: private work added error records and repair candidate data layers for proposal-only maintenance suggestions. Candidates are not automatically applied to production.
- Companion credential hygiene: private work strengthened companion / wearable credential boundaries, log hygiene, and public/private separation rules. Credentials, tokens, device-specific build artifacts, and local settings remain private.
- Local model evaluation boundary: private work added local model smoke and provider E2E style evaluation flows for latency, cold start, and provider overhead. The public repository does not publish model weights, vendor assets, raw benchmark output, or production selection claims.
- Gated runtime probes: private work added gated probes and evidence summaries for runtime-chain candidates. These remain operator-supervised evidence, not public production runtime.
- Public interface skeletons: this public repository now includes abstract JSON schema skeletons for reviewable status and boundary summaries. These schemas are public documentation, not private runtime deployment contracts.

### 2026-07-09 milestone note

The latest public-safe milestone records incremental progress around operator-supervised self-correction, retained proposal evidence, companion / wearable credential boundaries, local model evaluation caveats, and vision / world-state context wiring. This is a low-key status update, not a production runtime announcement.

See [Public Milestones](MILESTONES.md).

## Current Public Capability Boundary

Currently appropriate to discuss publicly:

- runtime / bridge / governance / audit architecture direction
- proposal-based improvement flow
- sandbox dry-run / worktree / patch validation concepts
- lab-only smoke and maintenance status summaries
- stats-only read-only status
- public/private boundary strategy
- plan-first / schema-first capability governance
- non-harm semantic boundary regression direction
- private workspace hygiene and memory governance as human policy
- public-safe interface shapes

Not public:

- production-grade live actuation gate
- real hardware or full local-control runtime details
- autonomous actuation
- device-specific bridge implementation
- public runtime RAG or live LLM source verification
- production deployment guide
- raw audit logs
- local benchmark output
- credentials or provisioning details

## Near-Term Public Direction

Next public-safe work should focus on:

1. Keeping public/private boundaries clean.
2. Extracting abstract interfaces from private runtime concepts.
3. Expanding public-safe event, state, proposal, review, and evidence summary schemas.
4. Keeping lab-only maintenance flows private while publishing only summaries.
5. Separating plan / schema / read-model artifacts from runtime execution.
6. Maintaining non-harm and release-boundary regression checks before broader public claims.

## Product Direction

The product direction is deliberately conservative:

- Treat companion, wearable, CLI, and dashboard surfaces as thin clients around a governed core.
- Keep high-risk actions behind policy, validation, human review, rollback, and audit.
- Keep local-first ownership and public/private boundaries explicit.
- Use public artifacts to communicate architecture and collaboration surfaces, not private deployment internals.

## Summary

PHINIX is moving toward a runtime where AI behavior can be observed, reviewed, tested, rolled back, and audited before promotion into higher-risk contexts.

Current public status:

> Governed architecture and public-safe interface shape are visible; private runtime execution and deployment details remain intentionally private.
<!-- # ⭐ 修改結束 ⭐ -->
