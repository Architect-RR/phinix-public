<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX 公開里程碑

本檔只記錄 public-safe 里程碑。內容刻意保持簡短，不鏡像 private runtime source、本機審計 log、裝置專屬設定、憑證、原始 benchmark output 或部署細節。

## 2026-07-11 — Sandbox viewer 邊界與 access policy

Public-safe 摘要：

- private work 新增保守的 world-viewer demo flow，用於 sandbox-only calculation preview。
- green/yellow/red access-policy note 將 agent 可自助使用的 sandbox calculation，與需要使用者明確要求或另開 gated phase 的行動切開。
- 公開價值是清楚邊界：可以討論 simulation-style preview，但不暗示 runtime deployment、AR support、hardware control 或 production automation。
- 不鏡像 private runtime source、device bridge details、raw output、本機路徑、憑證或 model assets。

Runtime truth label：

`public_safe_milestone_summary`

不宣稱：

- production autonomous execution
- public simulator service
- AR deployment
- public live hardware control
- automatic code mutation
- STL/STEP collision truth
- raw local test output、private commit history、device bridge code、credentials 或 local audit files

## 2026-07-10 — 提案封包與可驗證 sandbox 計算核心

Public-safe 摘要：

- Self-correction 工作新增 proposal-only 的協助請求形狀，用於把已審查的修復意圖交給人類或 AI 協作者。它仍然不可執行，也不會自動套用程式修改。
- Sandbox world-model 工作新增小型、可驗證的計算核心，涵蓋點質量運動、場方程求解與相對論參考計算。這些是 sandbox calculation，不是公開 simulator，也不是硬體控制 runtime。
- 公開用詞持續區分「已驗證的計算核心」與「部署宣稱」。此 repo 不鏡像 private runtime source、device bridge details、raw benchmark output、本機路徑或憑證。
- 本次公開價值在工程紀律：修復意圖可以封裝供審查，模型式計算以測試支撐，而不是敘事能力宣稱。

Runtime truth label：

`public_safe_milestone_summary`

不宣稱：

- production autonomous execution
- public live hardware control
- public physics engine deployment
- automatic code mutation
- raw local test output、private commit history、device bridge code、credentials 或 local audit files

## 2026-07-09 — 治理與操作介面整理

Public-safe 摘要：

- Human-supervised operation 仍是預設邊界：review、approval、rejection、follow-up 與 rollback expectation 都必須明確。
- Self-correction 工作以可觀測的 error state、reflection record、repair candidate 與 proposal evidence 留存方式描述。這不等於自動套用 production 變更。
- Companion / wearable 工作仍描述為 thin-client boundary，核心是本地受治理 runtime。公開文件不揭露 bridge internals、token、provisioning steps 或 device identifiers。
- Local model 工作以 evaluation evidence 描述，保留 cold-start、latency、provider-overhead 與 runtime-scope caveat。這不等於 production model selection claim。
- Vision / world-state 工作以 state/context wiring 與 reviewable evidence flow 描述，不等於 public autonomous actuation。
- Public/private release discipline 仍是產品表面的一部分：公開 artifact 描述架構、interface shape 與 boundary；private implementation details 保留在私有側。

Runtime truth label：

`public_safe_milestone_summary`

不宣稱：

- production autonomous execution
- public deployment instructions
- public live hardware control
- public runtime RAG 或 live LLM source-verification service
- public model weights、benchmark logs、device bridge code、credentials 或 local audit files

## 2026-07-03 — 公開表面整理

Public-safe 摘要：

- 整理 public overview、architecture notes、scope boundaries、roadmap、status page 與 abstract interface skeletons。
- 釐清 plan、schema、dry-run、read-only 與 proposal-only artifact 不等於 runtime enablement claim。
- 補上 runtime state、proposal、review journal entry、local model evaluation summary 與 credential boundary summary 的 public-safe interface direction。

Runtime truth label：

`public_schema_and_documentation_refresh`
<!-- # ⭐ 修改結束 ⭐ -->
