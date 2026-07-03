<!-- # ⭐ 修改開始 ⭐ -->
# Public Roadmap

Languages: [English](ROADMAP.md) | **繁體中文**

這份 roadmap 只描述 public-safe 的工程方向。private deployment details、local audit outputs、credentials、device-specific paths、raw benchmark output 與未審核自動化產物刻意排除。

## P0：公開專案基線

目標：

- 維持清楚的 public overview
- 定義 public/private boundaries
- 讓文件保持專業、工程化、可審查

產出：

- README
- public scope
- architecture overview
- roadmap
- security and contribution guidance

## P1：Runtime architecture interfaces

目標：

- 描述核心 runtime layers
- 讓 client entry point 保持 thin-client
- 分離 live interaction、background state、policy 與 validation
- 先公開抽象資料形狀，再考慮實作細節

產出：

- runtime state model
- event flow model
- stuck issue model
- proposal model

## P2：Governed improvement flow

目標：

- 將 failure 與 low-quality state 轉成可審核 proposal
- 在 promotion 前先經 sandbox 或 worktree validation
- 每個 change 都保留 tests、rollback plan 與 audit record

產出：

- proposal schema
- sandbox validation interface
- audit summary interface
- promotion status model

## P3：Read-only observability

目標：

- 在不暴露 private audit data 的前提下顯示有限 runtime health status
- 讓 observability 與 execution 分離
- 保留 evidence、readiness 與 runtime enablement 的差異

產出：

- stats-only status summary
- maintenance smoke summary
- viewer / panel display model

## P4：Proactive companion behavior

目標：

- 支援有用的 proactive suggestion，但避免產生噪音
- reminder 必須可審核、rate-limited、可取消
- suggestion 不得繞過 policy 或 human review

產出：

- proactive suggestion model
- cooldown policy
- notification boundary

## P5：Embodiment adapter abstraction

目標：

- 定義 companion devices、wearables 與 future hardware integrations 的安全介面
- 分離 cognition / governance 與 low-level control
- device-specific bridge path 不進 public repository

產出：

- embodiment adapter interface
- device capability descriptor
- authorized-device boundary model

## P6：Controlled maintenance automation

目標：

- 允許 bounded lab-only maintenance loop
- automation 預設停用
- 需要 status checks、stop conditions 與 audit output

產出：

- auto maintenance contract
- dry-run report
- bounded runner configuration

## P7：Boundary hardening and memory governance

目標：

- 在任何高風險 runtime surface 前，先讓 non-harm semantic boundary 可測試
- 讓 private workspace hygiene 與 public release material 分離
- 除非後續 gated phase 實作 runtime support，否則 memory 與 speculative capability notes 都視為人類治理文件

產出：

- harm-boundary regression summary
- public/private release checklist
- human-readable memory governance summary

## P8：Human-supervised operating surface

目標：

- 描述 review、批准、駁回與 follow-up 如何表示，但不公開 private console data
- 讓操作面可追溯，但不把它變成公開 automation
- 在 interface 層保留 append-only review semantics

產出：

- review journal entry schema
- operator decision summary
- human-supervised console boundary notes

## P9：Public-safe evidence and model evaluation summaries

目標：

- 摘要 local evaluation evidence，但不公開 raw benchmark output 或 model assets
- 分離 cold-start、steady-state、provider-overhead 與 execution-scope claims
- 避免 evaluation evidence 被寫成 production selection claim

產出：

- model evaluation summary schema
- runtime truth label guidance
- evidence caveat checklist

## P10：Credential and release-boundary hygiene

目標：

- 讓 credentials、provisioning details、device identifiers 與 local secrets 留在 public history 外
- 描述 public mirror checks，但不公開 private remediation details
- 將 credential rotation 與 provisioning 視為 private operator tasks

產出：

- credential boundary summary schema
- public release checklist
- security posture notes

## Public repo 非目標

- Production deployment guide
- Secret or credential handling
- Device-specific bridge implementation
- Local audit logs
- Full private runtime mirror
- High-risk execution paths
- Machine-loadable private runtime configuration
- Raw model benchmark output
- Device provisioning instructions
<!-- # ⭐ 修改結束 ⭐ -->
