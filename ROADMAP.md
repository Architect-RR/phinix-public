<!-- # ⭐ 修改開始 ⭐ -->
# Public Documentation Roadmap

Languages: **English** | [繁體中文](ROADMAP.zh-TW.md)

This roadmap is a sequence of evidence goals, not a delivery promise. Private implementation details and schedules are intentionally excluded.

## Current: Honest Public Baseline

- Keep the public repository limited to documentation and abstract schemas.
- Separate private implementation evidence from public availability.
- State known limitations before describing future capability.
- Remove duplicated or promotional wording.

## Next: Reproducibility

- Define a clean-machine setup checklist for a low-risk public example.
- Define an externally reproducible mock flow for capability selection and local evidence retrieval without private data.
- Add a public-safe restart/restore example that uses synthetic records only and makes persistence, promotion, and deletion boundaries explicit.
- Publish a non-sensitive smoke test only when it can be reproduced outside the private workspace.
- Pin dependencies and document supported environments.
- Record failure and recovery behavior, not only successful output.

Status: not yet delivered.

## Later: Bounded Public Demonstration

- Provide a small demo with mock data and no device, credential, or private runtime dependency.
- Keep all side effects disabled by default.
- Publish acceptance criteria and expected failure modes.
- Distinguish calculation output from real-world truth.

Status: design direction only.

## Deferred: Runtime and Device Release Decisions

- Evaluate whether any runtime subset is safe and maintainable enough for release.
- Require an explicit support matrix, security review, and rollback path.
- Keep hardware, wearable, model, and external API integrations separately gated.
- Require separate evidence before describing companion memory, wireless wearable transport, or live search as reliable.
- Treat first-leg pinned-transport implementation evidence as narrower than live transport proof; require upstream-leg hardening and bounded dual-leg live evidence before deployment-oriented claims.
- Require encryption-at-rest decisions for durable memory and bounded shutdown behavior for non-returning resource cleanup before reliability claims.
- Require repeated cable-free sessions and multi-condition vision evidence before describing wearable or perception paths as generally usable.

Status: no public release decision.

## Non-goals

- Mirroring the private runtime
- Publishing credentials, local paths, raw logs, or device identifiers
- Claiming autonomous self-modification
- Presenting sandbox output as validated real-world behavior
- Publishing deployment instructions before reproducibility and security evidence exist
<!-- # ⭐ 修改結束 ⭐ -->
