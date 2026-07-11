<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX 目前狀態

更新日期：2026-07-11

Languages: [English](CURRENT_STATUS.md) | **繁體中文**

PHINIX 是一個 private-first、local-first 的受治理 agent runtime 專案。公開 repo 只保留 public-safe 的方向、架構摘要與狀態說明；完整 runtime、硬體橋接、部署細節、憑證設定、原始審計資料與私有維護文件仍保留在 private repo。

## 對外用詞

公開文件統一採用工程語言：

- 「受治理自動化」而不是不受控自動化。
- 「sandbox validation」而不是直接修改主線。
- 「read-only status」而不是公開完整審計內容。
- 「proposal-based improvement」而不是未審核變更。
- 「local-first runtime」而不是單一聊天機器人或模型 wrapper。
- 「plan / schema layer」不等於 runtime execution 已公開或啟用。
- 「policy / test layer」不等於 real hardware、real LLM 或 autonomous actuation 已公開或啟用。

## 現階段定位

PHINIX 不是單純聊天機器人，也不是單一模型 wrapper。比較準確的說法是：

> 一個本地主權優先、具治理邊界、面向 companion / wearable / long-horizon tool use 的 agent runtime。

核心方向：

- 多模型可替換，不綁死單一 provider。
- 本地 runtime 優先，外部 API 作為可替換能力。
- 工具與行動必須經過 policy gate。
- 高風險動作需要審計、回滾與人工確認。
- 維護與能力提升流程必須可測、可關閉、可追蹤。
- 公開描述必須區分「已完成治理結構」與「尚未公開或尚未啟用 runtime layer」。

## 最近完成的主要能力

### 2026-07 public-safe update

私有工程線在 2026-06 到 2026-07 期間，主要補強了治理可觀測性、credential hygiene、人工監督入口與 proposal-only 修復候選流程。公開 repo 只記錄這些能力的工程方向與邊界，不公開 runtime source、device bridge 細節、token、原始 log 或本機審計資料。

目前可公開描述的新增進度：

- Human-supervised console / journal：私有端新增受控 console 與 append-only journal 類資料層，用於把 review、批准、駁回與回溯線索整理為可審計紀錄。這不等於公開 autonomous execution。
- Error / repair candidate tracking：私有端新增錯誤紀錄與壓力情境修復候選資料層，用於 proposal-only 的維護建議。候選不會自動套用到 production。
- Repair assist packaging：私有端新增 proposal-only 的修復協助請求形狀，用於把已審查的修復意圖交給協作者檢視。它本身不執行、不 patch、不 merge，也不 promotion。
- Companion credential hygiene：私有端補強 companion / wearable bridge 的 credential boundary、log hygiene 與 public/private 分離規則。credential、token、device-specific build artifact 與本機設定仍保持 private。
- Local model evaluation boundary：私有端建立本地模型 smoke / provider E2E 類驗證流程，用於比較 latency、cold start 與 provider overhead。公開 repo 不發布模型權重、vendor asset、完整 benchmark raw output 或 production 選型宣稱。
- Sandbox calculation kernels：私有端新增小型、測試支撐的 world-model 類計算核心。公開用詞只把它視為 sandbox calculation，不宣稱 public physics engine、deployment path 或 hardware-control runtime。
- Sandbox viewer and access policy：private work 新增保守的 demo/export 與 access-policy 文件，用於 sandbox-only simulation preview，並補上 agent-safe 的 inventory/smoke 健康檢查流程與 usage-audit/總結文件。公開說法只把它視為 preview 與 governance guidance，不稱為 public simulator service、AR deployment 或 hardware-control runtime。
- Gated runtime probes：私有端補充 gated probe 與 evidence summary，用於檢查 runtime chain 的候選路徑。這些仍是 gated / operator-supervised evidence，不是公開 production runtime。
- Public interface skeletons：公開 repo 已補上抽象 JSON schema skeleton，用於描述可審查的狀態、proposal、review、model evaluation 與 credential boundary summary。這些 schema 是公開文件，不是 private runtime deployment contract。

### 2026-07-11 里程碑紀錄

近期 private work 收口 sandbox simulation 與 viewer 文件線。公開摘要只限 sandbox-only 計算、保守 viewer-demo 邊界、inventory/smoke 健康檢查與 access-policy 文件；不代表 public simulator service、AR deployment、hardware-control runtime、real-time digital twin 或 production autonomous execution。Runtime truth：`public_safe_milestone_summary`。

見 [公開里程碑](MILESTONES.zh-TW.md)。

這些更新共同目標是提高「可觀測、可審核、可回滾」能力，而不是擴大未審核自動化。

### Human review escalation

私有 runtime 已建立人工審核升級路徑。當模型供應器或 runtime 偵測到重大失敗、連續錯誤或疑似低品質回應時，系統可以建立升級請求，交由人類決定後續方向。

### Upgrade proposal workflow

系統可以把升級請求轉成工程提案。每個提案包含問題來源、嚴重度、建議方向、預期修改檔案、禁止修改檔案、測試命令、風險與 rollback plan。

### Sandbox upgrade pipeline

私有 runtime 已具備受控 sandbox pipeline：

- dry-run executor
- worktree executor
- patch validation
- test verification
- auto-advancement gate
- local branch materialization
- guard ref reference safety

這條線仍以本地、可審計、可回滾為前提；公開 repo 不包含完整實作細節。

### Lab-only maintenance workflow

私有 runtime 已建立 lab-only 維護流程：

- lab stress harness
- private audit writer
- manual CLI entry
- read-only status summary
- viewer / commander card 的 stats-only 顯示
- maintainer onboarding checklist

這些能力只輸出有限摘要，不公開 audit 全文，不提供公開執行入口。

### Auto maintenance contract

私有 runtime 已建立可設定的自動維護 runner 契約。它目前只定義 bounded lab-only maintenance loop，不接 boot、不新增 endpoint、不常駐背景執行、不推送或合併公開 repo。

### Model asset boundary

模型權重已從 repo 邊界拉出。權重、adapter、tokenizer、embedding 等大型模型資產由外部模型資料夾管理，repo 只保存 registry、manifest 與 hash 驗證邏輯。

### Companion bridge governance

Companion bridge 已加入授權來源與低風險輸入路徑的治理設計。公開層只描述抽象方向：來源必須由本地設定或使用者明確提供，不做未授權掃描，不輸出明文憑證。

### Non-harm semantic boundary layer

私有工程線已補強 harm-boundary 的 policy / test layer，覆蓋直接傷害、間接傷害、授權覆蓋與裝置媒介型風險敘述。這條線的目的不是讓 PHINIX 執行高風險行為，而是讓治理層在更早的位置拒絕或轉向安全替代方案。

公開邊界：公開 repo 只描述 non-harm boundary 的治理方向與 regression-test 類型；不公開敏感 prompt corpus，不公開 device-control 細節，也不宣稱 real-runtime actuation 已啟用。

### Codebase introspection governance layer

私有工程線已完成 codebase introspection 的 plan / read-model layer，用來描述如何以受控方式讀取既有索引、彙整狀態、避免直接啟動 scanner 或修改 codebase。

公開邊界：這不是公開 scanner，也不是 runtime index 執行入口。公開 repo 只描述 schema-first 的治理方向。

### Source verification governance layer

私有工程線已完成 source verification 的 plan / result-schema layer，用來描述未來 source validation、citation requirement、source authority 與 anti-hallucination guardrails 的治理邊界。

公開邊界：這不是公開 RAG engine、不是 live LLM caller、不是 citation checker，也不是 fact-checking service。runtime RAG / LLM / fetch / citation checking 仍需獨立 gated phase。

### Template reuse and maintenance completion mapping

私有工程線已完成多個 governance template 的二次使用驗證，並建立 maintenance completion map，用來追蹤：

- 哪些 phase 已完成
- 哪些只是 plan / schema / read-model layer
- 哪些 runtime layer deferred
- 哪些 local maintenance state 不應進入公開 repo
- 下一個 phase 的啟動條件

公開邊界：公開層只說明維護方法與完成狀態摘要，不公開 private maintenance notes、內部測試輸出或原始維護資料。

### Private workspace hygiene and memory governance

私有工程線已建立更清楚的 workspace hygiene 與 memory governance 文件：private-only notes、本機 artifacts、public mirror 與 memory policy 各自有分層邊界。這讓公開 repo 能保持乾淨，同時避免把人類治理文件誤當成 machine-loadable runtime config。

公開邊界：公開層只摘要治理原則；不公開 private vault 路徑、raw checkpoint、local artifact name、內部工作指令或本機記憶檔。

## 目前能力邊界

已具備：

- runtime / bridge / governance / audit 的骨架
- 模型供應器失效偵測與人工審核升級
- proposal-based improvement flow
- sandbox dry-run / worktree / patch / local-branch promotion 的受控流程
- lab-only smoke test 與 private audit
- stats-only read-only status
- public/private 分離策略
- plan-first / schema-first 的能力治理方法
- codebase introspection 的 private plan / read-model layer
- source verification 的 private plan / result-schema layer
- maintenance completion / maintenance-state / deferred runtime 的追蹤方法
- harm-boundary 的 private policy / regression-test layer
- private workspace hygiene 與 memory governance 的人類治理文件

尚未公開或尚未完成：

- production-grade live actuation gate
- real hardware / full local-control runtime / autonomous actuation
- 高風險 domain package 的完整 policy layer
- public-safe interface package 實作
- runtime RAG / live LLM source verification
- citation checker / verifier service
- 完整公開 demo
- production deployment guide

刻意不做：

- 未經確認的高風險外部執行
- 隱藏式自動修改
- 直接修改 production main
- 未審核的 push / PR / release
- 把使用者資料無邊界送入訓練或外部模型
- 未授權掃描、撞庫或憑證繞過
- 把 plan/schema 層成果誤寫成 runtime 已啟用
- 把 policy/test layer 誤寫成 real-world execution approval

## 近期路線

短期路線：

1. 持續清理 public/private 邊界。
2. 把適合公開的抽象 interface 從 private runtime 中萃取出來。
3. 補足 public-safe 的事件模型、狀態模型、提案模型與驗證結果模型。
4. 將 lab-only 維護流程維持在 private repo，公開層只保留摘要。
5. 繼續把 plan / schema / read-model 與 runtime execution 明確分層。
6. 維持 non-harm semantic boundary 與 public/private release boundary 的回歸檢查。

中期路線：

- 將高風險行動統一進 `proposed_action -> policy check -> dry-run/simulation -> human gate -> execution adapter -> audit`。
- 把能力提升限制在 sandbox / worktree，通過測試與審核後才 promotion。
- 將 companion、wearable、CLI、dashboard 都視為 thin client，共用同一個 PHINIX core。
- 以獨立 gated phase 逐步處理 runtime RAG、LLM call、citation checking、handler 與 UI surface。
- 在任何 real hardware / local-control runtime / financial or medical action 前，先完成更嚴格的授權、審計、rollback、kill-switch 與非傷害語意邊界。

## 產品方向

PHINIX 的使用黏著度應該來自實際價值，而不是刺激式互動。

預期使用者會留下來，是因為 PHINIX 能：

- 記得長期目標與上下文。
- 在低打擾的時機提醒。
- 把問題整理成下一步。
- 幫人節省時間。
- 對高風險動作保持誠實邊界。
- 每次行動都可追溯、可取消、可回滾。

## 總結

PHINIX 的主線不是「更會聊天」，而是讓 AI runtime 能可靠地觀察、記憶、建議、使用工具、提出改善提案、接受審核，並逐步進入可控的 sandbox 驗證流程。

目前最重要的工程方向是：

> 把能力擴張放在治理、審計、權限、回滾與 sandbox 之後；把 plan / schema 層成果和 runtime execution 清楚分開。
<!-- # ⭐ 修改結束 ⭐ -->
