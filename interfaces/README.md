# Public Interface Directions

This directory is reserved for abstract interfaces and data models that are safe to discuss publicly.

The guiding rule is:

```text
publish abstractions first
publish low-risk skeletons second
keep deployment-specific implementations private
```

## Interface Families Worth Exposing First

### 1. Runtime state interface

For session state, event snapshots, and status summaries.

### 2. Stuck issue interface

For unresolved questions, retry conditions, escalation rules, and review states.

### 3. Proposal interface

For turning failures or improvement requests into reviewable engineering proposals.

### 4. Sandbox validation interface

For dry-run results, test results, and promotion readiness.

### 5. Audit summary interface

For stats-only public-safe reporting without exposing private audit details.

### 6. Proactive suggestion interface

For low-risk reminders and suggestions without opening direct control paths.

### 7. Embodiment adapter interface

For connecting a governed runtime to companion devices, wearables, and future authorized hardware surfaces.

## Separation Principles

Public interface work should keep these concerns separate:

- cognition and context
- memory and retention
- policy and permission
- sandbox validation
- audit and observability
- device or embodiment adaptation

The public repository should not contain device-specific execution paths, credentials, private audit logs, or production deployment details.
