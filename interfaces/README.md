<!-- # ⭐ 修改開始 ⭐ -->
# Public Interface Directions

This directory contains abstract interface and data-model skeletons that are safe to discuss publicly.

The guiding rule is:

```text
publish abstractions first
publish low-risk skeletons second
keep deployment-specific implementations private
```

These schemas are documentation artifacts. They are not a promise that the private runtime exposes the same files, field names, or deployment contract.

## Included Skeletons

| Schema | Purpose | Boundary |
|---|---|---|
| [`runtime_state_summary.schema.json`](runtime_state_summary.schema.json) | Public-safe runtime status shape. | Stats-only; no raw audit logs or private state. |
| [`proposal_record.schema.json`](proposal_record.schema.json) | Reviewable improvement or action proposal shape. | Proposal-only; not automatic execution. |
| [`review_journal_entry.schema.json`](review_journal_entry.schema.json) | Human-supervised review trace shape. | No private console data or raw operator notes. |
| [`model_eval_summary.schema.json`](model_eval_summary.schema.json) | Local model evaluation summary shape. | No model weights, raw benchmark output, or production selection claim. |
| [`credential_boundary_summary.schema.json`](credential_boundary_summary.schema.json) | Public-safe credential boundary posture shape. | No tokens, provisioning details, device IDs, or rotation values. |

## Interface Families Worth Exposing First

### 1. Runtime state interface

For session state, event snapshots, readiness labels, and status summaries.

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

### 8. Credential boundary interface

For recording public-safe security posture without disclosing secrets, provisioning steps, or device-specific implementation details.

## Runtime Truth Labels

Public schemas should use explicit status labels when a field might otherwise be misunderstood:

- `public_schema`
- `plan_only`
- `proposal_only`
- `read_only`
- `gated_evidence`
- `private_runtime`
- `deferred`

Do not use schema presence as proof of runtime enablement.

## Separation Principles

Public interface work should keep these concerns separate:

- cognition and context
- memory and retention
- policy and permission
- proposal and review
- sandbox validation
- audit and observability
- device or embodiment adaptation
- credential and release boundaries

The public repository should not contain device-specific execution paths, credentials, private audit logs, local benchmark output, or production deployment details.
<!-- # ⭐ 修改結束 ⭐ -->
