# PHINIX Public Starter

Languages: **English** | [繁體中文](README.zh-TW.md)

PHINIX is a local-first AI runtime aimed at embodied companion systems, AR interfaces, and a future cognition layer for humanoid robots.

This public repository is intentionally limited. It does not expose the full private runtime or deployment chain. It exists to share:

- project vision
- architecture direction
- collaboration rules
- public-safe interfaces
- roadmap and open questions

## Positioning

PHINIX is best described as:

**a local-first, governance-aware, embodied AI runtime that may evolve into a long-lived companion core**

Near-term focus:

- a stable core runtime
- safe autonomy boundaries
- memory and issue-tracking primitives
- device-agnostic cognition interfaces

## Why this repo is public-safe

The full private repo still contains material that should not be published directly:

- bridge credentials and deployment details
- raw interaction and training logs
- hardware-specific bridge details
- large build artifacts and vendor binaries
- evolving governance internals

This public repo shares the direction without exposing those parts.

## What is in this repo

- `README.md` — project overview
- `ARCHITECTURE_OVERVIEW.md` — high-level system design
- `README.zh-TW.md` — Traditional Chinese overview
- `ARCHITECTURE_OVERVIEW.zh-TW.md` — Traditional Chinese architecture overview
- `PUBLIC_SCOPE.md` — what belongs in public vs private repos
- `PUBLIC_SCOPE.zh-TW.md` — Traditional Chinese public-scope guide
- `CONTRIBUTING.md` — how to participate
- `CONTRIBUTING.zh-TW.md` — Traditional Chinese contribution guide
- `CALL_FOR_EXPERTS.md` — where expert feedback is most useful
- `CALL_FOR_EXPERTS.zh-TW.md` — Traditional Chinese expert invitation
- `ROADMAP.md` — staged evolution plan
- `ROADMAP.zh-TW.md` — Traditional Chinese roadmap
- `interfaces/` — public interface directions

## What PHINIX may become

### 1. AR cognitive copilot

A low-latency assistance layer for glasses and other wearable devices.

### 2. Local-first digital companion

A long-lived companion core with memory, follow-up reasoning, and proactive reminders.

### 3. Humanoid robot cognition layer

A portable cognition and governance layer that can outlive any one device body.

Likely roles:

- memory
- issue tracking
- proactive reasoning
- governance
- long-term consistency

## Public collaboration principles

- local sovereignty first
- honest capability boundaries
- no public release of sensitive embodiment chains
- document and interface before risky implementation
- expand access only after validation

## Recommended repo strategy

Keep the full operational system private for now. Use this public repo for:

- architecture review
- interface design
- expert discussion
- low-risk public collaboration
