# Public Roadmap

This roadmap describes the direction that is safe to discuss in public. It does not expose private deployment details.

## P0: Public starter package

Goal:

- define the public position
- define collaboration rules
- define the public/private split

Outputs:

- README
- scope document
- roadmap
- expert call

## P1: Three-layer runtime skeleton

Goal:

- real-time layer
- buffer layer
- thinking layer

Outputs:

- public architecture diagram
- abstract interfaces
- minimum event-flow model

## P2: Stuck issue queue

Goal:

- turn failure and uncertainty into structured state
- support deferred retry and background revisit

Outputs:

- `StuckIssue`
- `RetryPlan`
- `EscalationCandidate`

## P3: Proactive companion

Goal:

- surface useful new conclusions without waiting for another prompt
- keep reminders low-friction and low-disruption

Outputs:

- reminder policy
- proactive suggestion flow
- notification channel abstraction

## P4: Embodied companion

Goal:

- expand from glasses and companion devices to a broader embodiment layer

Outputs:

- embodiment adapter interface
- multi-device context model
- safety boundary design

## P5: Portable cognition layer

Goal:

- make PHINIX a cognition architecture that can carry context across companion apps, wearables, desktop tools, and future embodied systems

Likely roles:

- memory
- context
- proactive reasoning
- governance
- long-term consistency

Not the same as:

- low-level motor control
- hard real-time control
- a thin robot SDK wrapper

## P6: Governed capability improvement

Goal:

- turn runtime failures, low-quality responses, and stuck issues into reviewable improvement proposals
- validate changes inside sandbox / worktree boundaries instead of modifying production directly
- retain test evidence, audit records, and rollback plans

Outputs:

- codebase self-indexing
- side-effect map
- sandbox dry-run / worktree validation
- local branch materialization
- human review workflow

## Milestones that matter

PHINIX becomes mature only if it can progressively achieve:

1. a clear public/private boundary
2. separation between live interaction and background cognition
3. an operating stuck-issue queue
4. controlled proactive reminders
5. an abstract embodiment layer
6. continuity across multiple devices or bodies
7. reviewable and rollback-capable improvement workflows
