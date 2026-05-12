# PHINIX 目前狀態

更新日期：2026-05-12

PHINIX 是一個 private-first、local-first 的 governed intelligence runtime 專案。公開 repo 只保留 public-safe 的方向、架構摘要與狀態說明；完整 runtime、硬體橋接、部署細節、憑證設定與敏感治理資料仍留在 private repo。

## 對外用詞

公開文件統一採用工程語言：

- 「受治理升級」而不是誇大的能力宣稱。
- 「可審核自動化」而不是不受控自動化。
- 「能力強化」而不是模糊的自我擴張。
- 「風險阻斷與審計」而不是情緒化敘述。
- 「local-first runtime」而不是單一聊天機器人或模型 wrapper。

## 現階段定位

PHINIX 不是單純聊天機器人，也不是單一模型 wrapper。比較準確的說法是：

> 一個本地主權優先、具治理邊界、面向 companion / wearable / long-horizon agent 的 AI runtime。

核心方向：

- 多模型可替換，不綁死單一 provider。
- 本地 runtime 優先，外部 API 作為可替換能力。
- 工具與行動必須經過 policy gate。
- 高風險動作需要審計、回滾與人工確認。
- 長期目標、記憶、觀察、提醒與能力提升流程都要可測、可關閉、可追蹤。

## 最近完成的主要能力

### Human review escalation

PHINIX 已建立人工審核升級路徑。當模型供應器或 runtime 偵測到重大失敗、連續錯誤或疑似低品質回應時，系統可以建立升級請求，交由人類決定後續方向。

目前重點不是自動呼叫外部工具或自動修復，而是先把問題整理成可審核事件。

### UpgradeProposal

系統可以把升級請求轉成 `UpgradeProposal`。每個 proposal 會包含問題來源、嚴重度、建議方向、預期修改檔案、禁止修改檔案、測試命令、風險與 rollback plan。

這讓 PHINIX 的能力提升流程從「發現問題」前進到「提出可審核工程提案」。

### Governed automation policy

PHINIX 已加入受治理自動化骨架。

目前所有自動化模式都以安全邊界為前提：

- 僅建立提案。
- sandbox 內乾跑。
- 低風險變更仍需測試與審核後推進。
- 實驗室模式只代表隔離測試，不代表可直接修改 production 主線。

### ModelAssetRegistry

模型權重已從 repo 邊界拉出。權重、adapter、tokenizer、embedding 等大型模型資產由外部模型資料夾管理，repo 只保存 registry、manifest 與 hash 驗證邏輯。

這讓 repo 保持輕量，也避免模型資產與程式碼版本混在一起。

### Sandbox upgrade pipeline

私有 runtime 已從資料契約推進到受控 sandbox pipeline：

- `SandboxRun` / `SandboxRunStore` / `SandboxTestResult`
- dry-run executor
- worktree executor
- patch application
- auto-advancement orchestrator
- local branch materializer
- guard ref reference safety，避免 materialized commit 在失敗路徑中失去引用

這條線仍以本地、可審計、可回滾為前提；公開 repo 不包含完整實作細節。

### Companion bridge camera governance

Companion bridge 已加入授權攝影機來源清單與低風險取像路徑的治理設計。公開層只描述抽象方向：來源必須由本地設定或使用者明確提供，不做未授權掃描，不輸出明文憑證。

## 目前能力邊界

已具備：

- runtime / bridge / governance / audit 的骨架
- 模型供應器失效偵測與人工審核升級
- proposal-based improvement flow
- governed automation scaffolding
- model asset boundary
- sandbox dry-run / worktree / patch / local-branch promotion 的受控流程
- public/private 分離策略

尚未公開或尚未完成：

- production-grade live actuation gate
- 高風險 domain package 的完整 policy layer
- codebase self-indexing 的正式 public artifact
- runtime state indexing
- 人類維護面板

刻意不做：

- 未經確認的高風險外部執行
- 隱藏式自我修改
- 直接修改 production main
- 未審核的 push / PR / release
- 把使用者資料無邊界送入訓練或外部模型
- 未授權掃描、撞庫或憑證繞過

## 近期路線

短期路線：

1. `63E-1`：Codebase self-indexing，建立唯讀程式碼索引與人類維護手冊 generated artifact。
2. `63E-2`：Runtime state indexing，整理 stores / workers / diagnostics 的狀態快照。
3. `63E-3`：Side-effect map，標記哪些模組會寫檔、跑 shell、碰網路、碰硬體、對外輸出。
4. `63E-4`：World-state evaluator，建立狀態差異、風險與 drift 評估器。
5. `64`：只在 lab / sandbox 中測試多輪受治理改善流程。

中期路線：

- 將高風險行動統一進 `proposed_action -> policy check -> dry-run/simulation -> human gate -> execution adapter -> audit`。
- 把能力提升限制在 sandbox / worktree，通過測試與審核後才 promotion。
- 將眼鏡、companion、CLI、dashboard 都視為 thin client，共用同一個 PHINIX core。

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

> 把能力擴張放在治理、審計、權限、回滾與 sandbox 之後。
