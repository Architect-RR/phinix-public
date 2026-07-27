<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX Public Overview

PHINIX is a private engineering prototype exploring local-first, policy-gated agent systems.

This public repository contains documentation and abstract JSON schemas only. It does not contain a runnable PHINIX distribution, deployment package, device bridge, model assets, credentials, or private audit data.

Languages: **English** | [繁體中文](README.zh-TW.md)

## Current Status

PHINIX has source code, targeted tests, bounded sandbox demonstrations, local-first retrieval and memory components, agent control-plane work, and records from selected local integration sessions in its private engineering repository.

That evidence is useful but limited. It does **not** yet establish that the project can be installed by an external user, operate reliably end to end, recover across repeated real-world sessions, or support general hardware and production deployment.

Current public assessment:

> Engineering prototype with bounded internal evidence. Overall operational reliability and external reproducibility remain unproven.

Runtime truth label: `bounded_internal_evidence_only`

## Evidence Boundary

| Area | Evidence currently available | What remains unproven |
|---|---|---|
| Governance and message flow | Private source and targeted automated tests | Independent reproduction and sustained operation |
| Agent capability control | Bounded catalog, authorization, proposal, and tool-loop tests in the private repository | General task completion, natural interaction quality, and unattended operation |
| Local knowledge, memory, and search | Private local-index, bounded connector, persistent-store component, and synthetic restart tests | Public data import, encrypted durable user memory with real data, and reliable live search |
| Local model integration | Selected local provider and latency checks | Stable long-running service and production model selection |
| Companion and wearable path | Selected session, UI, build, private-network, bounded relay, and first-leg pinned-transport implementation records | Cable-free use, live pinned ingress, end-to-end transport hardening across both relay legs, general compatibility, and unattended operation |
| Vision path | Selected bounded single-frame local-model evidence | Robust multi-frame perception across varied scenes and conditions |
| Sandbox simulation and viewer | Deterministic calculation and HTML demo checks | Full collision physics, digital-twin accuracy, or real-world control |
| Self-correction workflow | Proposal, review, and retained-state structures | Autonomous code mutation or unsupervised promotion |

The table reports evidence scope, not product readiness.

## Public Repository Contents

- [Architecture direction](ARCHITECTURE_OVERVIEW.md)
- [Current evidence status](CURRENT_STATUS.md)
- [Public documentation roadmap](ROADMAP.md)
- [Public/private scope](PUBLIC_SCOPE.md)
- [Abstract interface schemas](interfaces/README.md)
- [Contribution guidance](CONTRIBUTING.md)
- [Security reporting](SECURITY.md)

The abstract schemas document possible data shapes. Their presence is not proof that an equivalent public runtime endpoint exists.

## Not Claimed

This repository does not claim:

- a downloadable or generally usable PHINIX application
- reliable end-to-end operation
- production deployment approval
- continuous autonomous execution
- automatic self-modification
- general hardware or wearable compatibility
- a validated digital twin or complete physics engine
- public access to the private runtime

## Public Release Rule

Public updates should stay limited to architecture, interface shape, bounded evidence, known limitations, and collaboration material. Private implementation details, raw logs, local paths, credentials, device identifiers, model assets, and unreviewed outputs must remain private.

## Collaboration

Issues and pull requests should focus on documentation clarity, interface design, testable low-risk examples, risk review, and reproducibility. Do not submit secrets, private device details, deployment credentials, raw model assets, or local audit records.
<!-- # ⭐ 修改結束 ⭐ -->
