# PHINIX 目前狀態

更新日期：2026-05-15

PHINIX 是一個 private-first、local-first 的受治理 agent runtime 專案。公開 repo 只保留 public-safe 的方向、架構摘要與狀態說明；完整 runtime、硬體橋接、部署細節、憑證設定、審計資料與私有維護文件仍保留在 private repo。

## 對外用詞

公開文件統一採用工程語言：

- 「受治理自動化」而不是不受控自動化。
- 「sandbox validation」而不是直接修改主線。
- 「read-only status」而不是公開完整審計內容。
- 「proposal-based improvement」而不是未審核變更。
- 「local-first runtime」而不是單一聊天機器人或模型 wrapper。

## 現階段定位

PHINIX 不是單純聊天機器人，也不是單一模型 wrapper。比較準確的說法是：

> 一個本地主權優先、具治理邊界、面向 companion / wearable / long-horizon tool use 的 agent runtime。

核心方向：

- 多模型可替換，不綁死單一 provider。
- 本地 runtime 優先，外部 API 作為可替換能力。
- 工具與行動必須經過 policy gate。
- 高風險動作需要審計、回滾與人工確認。
- 維護與能力提升流程必須可測、可關閉、可追蹤。

## 最近完成的主要能力

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

- Lab stress harness
- Private audit writer
- Manual CLI entry
- Read-only status summary
- Viewer / commander card 的 stats-only 顯示
- Maintainer onboarding checklist

這些能力只輸出有限摘要，不公開 audit 全文，不提供公開執行入口。

### Auto maintenance contract

私有 runtime 已建立可設定的自動維護 runner 契約。它目前只定義 bounded lab-only maintenance loop，不接 boot、不新增 endpoint、不常駐背景執行、不推送或合併公開 repo。

### Model asset boundary

模型權重已從 repo 邊界拉出。權重、adapter、tokenizer、embedding 等大型模型資產由外部模型資料夾管理，repo 只保存 registry、manifest 與 hash 驗證邏輯。

### Companion bridge governance

Companion bridge 已加入授權攝影機來源清單與低風險取像路徑的治理設計。公開層只描述抽象方向：來源必須由本地設定或使用者明確提供，不做未授權掃描，不輸出明文憑證。

## 目前能力邊界

已具備：

- runtime / bridge / governance / audit 的骨架
- 模型供應器失效偵測與人工審核升級
- proposal-based improvement flow
- sandbox dry-run / worktree / patch / local-branch promotion 的受控流程
- lab-only smoke test 與 private audit
- stats-only read-only status
- public/private 分離策略

尚未公開或尚未完成：

- production-grade live actuation gate
- 高風險 domain package 的完整 policy layer
- public-safe interface package
- 完整公開 demo
- production deployment guide

刻意不做：

- 未經確認的高風險外部執行
- 隱藏式自動修改
- 直接修改 production main
- 未審核的 push / PR / release
- 把使用者資料無邊界送入訓練或外部模型
- 未授權掃描、撞庫或憑證繞過

## 近期路線

短期路線：

1. 持續清理 public/private 邊界。
2. 把適合公開的抽象 interface 從 private runtime 中萃取出來。
3. 補足 public-safe 的事件模型、狀態模型與提案模型。
4. 將 lab-only 維護流程維持在 private repo，公開層只保留摘要。

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
