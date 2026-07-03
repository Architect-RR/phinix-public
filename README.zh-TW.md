<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX 公開總覽

PHINIX 是一個 private-first、local-first 的受治理 agent runtime 專案。

這個公開 repository 只保留工程上適合公開的專案概覽、public/private 邊界、架構說明、roadmap 與抽象介面方向。完整 private runtime、裝置橋接實作、本機憑證、硬體設定、原始審計產物與部署專屬實作不放在此處。

## 目前定位

PHINIX 不是聊天機器人 wrapper。此專案採用受治理 runtime 模式：

```text
輸入
-> runtime state
-> policy 與 risk gate
-> proposal generation
-> sandbox validation
-> audit
-> human or operator review
```

實務目標是讓 agent 行為在影響高風險系統前，先具備可觀測、可審核、可測試、可回滾的工程邊界。

## 已完成的公開安全能力區塊

private engineering track 已完成下列能力區塊；此處只以 public-safe 層級描述，不公開 private implementation details。

| 區塊 | 已完成能力 | 公開邊界 |
|---|---|---|
| 人工審核升級 | failure、低品質輸出與風險訊號可以轉成可審核 escalation item。 | 公開 repo 只描述治理模式；private review data 與 audit records 不公開。 |
| Proposal-based improvement flow | 改善請求可以表示為結構化 proposal，包含 scope、禁止修改、測試、風險與 rollback expectation。 | 不公開 private patch 內容或本機維護報告。 |
| Sandbox validation workflow | 變更可經 dry-run、worktree validation、patch checks、tests 與 promotion-readiness gates 評估。 | 這不是公開 production execution，也不是部署批准。 |
| Read-only observability | runtime 與 maintenance 狀態可透過 stats-only view 摘要。 | 不公開完整 audit logs、raw results、本機 errors 或 branch details。 |
| Lab-only maintenance contract | private lab use 的 bounded maintenance loop 已定義 stop conditions 與 audit expectations。 | 不提供公開 auto-runner、scheduler、push、merge 或 release automation。 |
| Model asset boundary | 大型模型資產維持在 repo 邊界外，透過 registry / manifest / hash 類治理追蹤。 | 不公開 weights、adapters、tokenizers、embeddings 或 vendor assets。 |
| Companion / wearable governance | 裝置面方向被視為 thin-client 或 adapter boundary，需本機授權治理。 | device-specific bridge details、credentials、allowlists 與 hardware paths 保持 private。 |
| Non-harm semantic boundary layer | private policy/test coverage 已涵蓋直接、間接、授權覆蓋與裝置媒介型的 harm-boundary wording。 | 這是 governance 與 regression-test layer；不是公開 autonomous actuation 或部署批准。 |
| Codebase introspection schema layer | private 端已有 codebase index 類 introspection 的 plan/read-model layer。 | 只到 schema/read-model；不公開 private scanner outputs，也不在公開 repo 啟動 runtime scanner。 |
| Source verification schema layer | private 端已有 source verification 與 citation-aware governance 的 plan/result-schema layer。 | 只到 plan/schema；runtime RAG、live LLM calls、source fetching 與 citation checking 仍留給獨立 gated phases。 |
| Maintenance completion mapping | private 專案已建立 completion、maintenance-state、runtime-deferred 與 next-action maps。 | 公開文件只摘要 operating model，不公開 private maintenance notes。 |
| Private workspace hygiene | private-only notes、本機 artifacts 與 public mirror content 透過明確 inventory 與 release-boundary rules 分離。 | 公開文件只描述規則；private vault paths、raw checkpoints 與 local artifact names 不公開。 |
| Memory governance policy | 長期記憶、工程計算邊界案例與 research notes 以人類治理文件記錄。 | 這不是 machine-loadable runtime configuration，也不代表相關能力已實作。 |

## 不宣稱已完成的部分

這個公開 repository 不宣稱 PHINIX 目前提供：

- production-grade autonomous actuation
- 公開 runtime RAG 或 live LLM execution
- production deployment instructions
- device-specific bridge implementation
- 完整 private runtime source
- raw audit logs 或本機維護資料
- model weights 或 model asset manifests
- 未審核的 automation outputs
- 可執行高風險物理、金融、醫療或裝置控制行為的公開批准

若某項能力被描述為 plan、schema、read-model 或 governance-hint layer，意思是目前 artifact 定義了可審核結構與邊界；不代表 runtime execution layer 已公開或啟用。

## 公開 repository 內容

- 高層架構摘要
- public/private scope 規則
- 公開 roadmap
- 貢獻與安全說明
- 抽象介面方向
- public-safe 狀態報告

此 repository 刻意不包含：

- private deployment code
- device credentials 或 bridge tokens
- hardware allowlists
- local audit logs
- model weights 或模型資產 manifest
- 未審核的自動化輸出
- private maintenance reports

## 目前工程重點

private 專案目前聚焦：

- runtime 與 side-effect observability
- proposal-based improvement flow
- promotion 前的 sandbox validation
- human-supervised console 與 append-only journal 類審計面
- error-ledger 與 repair-candidate tracking（proposal-only maintenance）
- companion / wearable credential hygiene 與 log minimization
- schema-first 與 plan-first capability governance
- source verification 與 citation boundary planning
- non-harm semantic boundary regression testing
- private workspace hygiene 與 memory-governance documentation
- lab-only maintenance smoke tests
- read-only status summaries
- 嚴格 public/private boundary control

公開更新會維持在架構、介面形狀與可驗證工程狀態層級。private implementation details 只會摘要，不會鏡像公開。

最新 public-safe 狀態：2026-07-03。近期 private 工作補強了人工監督 review surface、append-only audit-style record、companion credential hygiene 與本地模型評估邊界。這不代表 autonomous production execution 已公開或啟用。

## 文件

- [架構總覽](ARCHITECTURE_OVERVIEW.zh-TW.md)
- [公開範圍](PUBLIC_SCOPE.zh-TW.md)
- [Roadmap](ROADMAP.zh-TW.md)
- [目前狀態](CURRENT_STATUS.zh-TW.md)
- [貢獻說明](CONTRIBUTING.zh-TW.md)
- [Security](SECURITY.md)

## 協作邊界

Issue 與 PR 應聚焦：

- 架構回饋
- 介面設計
- public-safe 文件
- 風險與治理審查
- 低風險範例或 simulation stubs

請勿提交 secrets、private device details、production credentials、local audit files、raw model assets 或未審核的 automation outputs。
<!-- # ⭐ 修改結束 ⭐ -->
