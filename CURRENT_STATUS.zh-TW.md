# PHINIX 目前狀態

更新日期：2026-05-10

PHINIX 目前是一個 private-first、local-first 的具身 AI runtime 專案。公開 repo 只保留 public-safe 的方向、架構摘要與狀態說明；完整 runtime、硬體橋接、部署細節與敏感治理資料仍留在 private repo。

## 現階段定位

PHINIX 不是單純聊天機器人，也不是單一模型 wrapper。比較準確的說法是：

> 一個本地主權優先、具治理邊界、面向 companion / wearable / long-horizon agent 的 AI runtime。

核心方向：

- 多模型可替換，不綁死單一 provider
- 本地 runtime 優先，外部 API 作為可替換能力
- 工具與行動必須經過 policy gate
- 高風險動作需要審計、回滾與人工確認
- 長期目標、記憶、觀察、提醒與自我升級都要可測、可關閉、可追蹤

## 最近完成的主要能力

### Human review escalation

PHINIX 已建立人工審核升級路徑。當模型供應器或 runtime 偵測到重大失敗、連續錯誤或疑似低品質回應時，系統可以建立升級請求，交由人類決定後續方向。

目前重點不是自動呼叫外部工具或自動修復，而是先把問題整理成可審核事件。

### UpgradeProposal

系統可以把升級請求轉成 `UpgradeProposal`。每個 proposal 會包含問題來源、嚴重度、建議方向、預期修改檔案、禁止修改檔案、測試命令、風險與 rollback plan。

這讓 PHINIX 的自我升級流程從「發現問題」前進到「提出可審核工程提案」。

### Autonomy governance

PHINIX 已加入自主性治理骨架。

目前所有自動化模式都以安全邊界為前提：

- 僅建立提案
- sandbox 內乾跑
- 低風險變更審核後推進
- 實驗室模式下的隔離測試

實驗室模式只代表未來可在隔離 sandbox / worktree 內進行測試，不代表可直接修改 production 主線。

### ModelAssetRegistry

模型權重已從 repo 邊界拉出。權重、adapter、tokenizer、embedding 等大型模型資產由外部模型資料夾管理，repo 只保存 registry、manifest 與 hash 驗證邏輯。

這讓 repo 保持輕量，也避免模型資產與程式碼版本混在一起。

### Sandbox Upgrade 基礎

目前已完成 `SandboxRun`、`SandboxRunStore`、`SandboxTestResult` 與檔案邊界檢查。`UpgradeProposal` 可以被轉成可審計的 sandbox run。

這一層目前仍是資料契約，不建立 worktree、不執行 shell、不自動 patch。下一步會先做 dry-run executor，再往真正 worktree executor 前進。

## 目前能力邊界

已具備：

- runtime / bridge / governance / audit 的骨架
- 模型供應器失效偵測與人工審核升級
- proposal-based upgrade flow
- autonomy governance scaffolding
- model asset boundary
- sandbox upgrade data contract

尚未完成：

- 真正的 sandbox worktree executor
- 自動 patch / test / rollback 閉環
- low-risk auto-promotion
- production-grade live actuation gate
- 高風險 domain package 的完整 policy layer

刻意不做：

- 未經確認的高風險外部執行
- 隱藏式自我修改
- 直接修改 production main
- 把使用者資料無邊界送入訓練或外部模型

## 近期路線

短期路線：

1. `63A-2`：Sandbox dry-run executor contract
2. `63A-3`：Workspace / Session / Permission 資料契約
3. `63A-4`：Tool Registry + Permission Scope
4. `63A-5`：ActionRiskLevel / Policy Gate 通用化
5. `63B`：Execution Simulation / Dry-run Gate

中期路線：

- 將高風險行動統一進 `proposed_action -> policy check -> dry-run/simulation -> human gate -> execution adapter -> audit`
- 把 self-improvement 侷限在 sandbox / worktree，通過測試與審核後才 promotion
- 將眼鏡、companion、CLI、dashboard 都視為 thin client，共用同一個 PHINIX core

## 產品方向

PHINIX 的黏著度應該來自實際價值，而不是刺激式互動。

預期使用者會留下來，是因為 PHINIX 能：

- 記得長期目標與上下文
- 在低打擾的時機提醒
- 把問題整理成下一步
- 幫人節省時間
- 對高風險動作保持誠實邊界
- 每次行動都可追溯、可取消、可回滾

## 總結

PHINIX 的主線不是「更會聊天」，而是讓 AI runtime 能可靠地觀察、記憶、建議、使用工具、提出升級、接受審核，並逐步進入可控的 sandbox 自我改進。

目前最重要的工程方向是：

> 把能力擴張放在治理、審計、權限、回滾與 sandbox 之後。
