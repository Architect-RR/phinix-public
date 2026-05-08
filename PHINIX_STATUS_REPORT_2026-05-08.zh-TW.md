# PHINIX 公開狀態報告（2026-05-08）

- 日期：2026-05-08
- 範圍：public-safe 摘要，不包含私有 repo 原始碼、憑證、硬體部署細節或敏感具身控制鏈
- 最新穩定內部基線：Phase 62Y-1 至 62Z-3
- 驗證摘要：內部完整回歸於 62Z-3 後達 `921 PASS / 1 SKIP / 48 subtests`

## 一句話定位

PHINIX 目前不是 AGI，也不以公開宣稱 AGI 為目標。

更準確的定位是：

> **PHINIX 是一個 local-first、governance-first 的具身 AI runtime，用來承載模型、記憶、工具、感知、審計與可控自主升級流程。**

換句話說，PHINIX 的核心價值不是單一模型，而是讓不同模型與本地設備能在可治理、可追蹤、可回滾的環境中協作。

## 近期完成重點

### 1. Mentor escalation：模型失效時先問人

PHINIX 已建立 LINE-based mentor escalation path。當 GeminiProvider 遇到重大問題時，可以把問題整理成升級請求，由人類選擇後續方向。

目前已支援的觸發類型：

- Gemini key 全部 cooldown 或不可用
- 單次請求所有 key 嘗試失敗
- 回應疑似低品質或不符合任務複雜度

治理邊界：

- 不自動呼叫 Claude / Codex
- 不自動修改程式
- 不自動執行 shell
- 不在 log 或 payload 洩漏 API key / bridge token / LINE token

### 2. UpgradeProposal：把求救訊號變成可審核升級提案

PHINIX 現在可以把 mentor escalation 轉成 `UpgradeProposal`，讓每個升級請求具備可審核結構。

每筆 proposal 包含：

- 問題來源與嚴重度
- 建議導師方向
- 預期修改檔案
- 禁止修改檔案
- 測試命令
- 風險等級
- rollback plan
- 人工審核狀態

這代表 PHINIX 不只是「發現錯誤」，而是開始能把錯誤整理成工程提案。

### 3. AutonomyPolicy：先設計自動閉環的治理邊界

PHINIX 已預留 `AutonomyMode` / `AutonomyPolicy`，但目前不啟動任何自動 patch。

模式設計：

- `off`
- `proposal_only`
- `sandbox_auto`
- `low_risk_auto_promote`
- `full_auto_lab`

公開重點是：即使未來進入更高自動化模式，仍必須受限於：

- sandbox / worktree
- audit log
- rollback plan
- forbidden paths
- max cycles
- human / policy gates

`full_auto_lab` 是內部實驗室模式的治理旗標，不代表可直接修改 production 主線。

### 4. ModelAssetRegistry：權重檔外部化

PHINIX 已把模型權重治理拉出 repo 邊界。

設計原則：

- 權重檔不進 Git repo
- repo 只保存 registry / manifest / hash 驗證邏輯
- 實際模型資產由 `PHINIX_MODEL_ROOT` 指向外部資料夾
- 支援 sha256 驗證與狀態檢查
- 自主升級 proposal 不得修改 repo 內權重路徑

這讓 PHINIX 未來可以接本地模型、adapter、embedding 或 vision weight，同時保持 Git repo 乾淨、可審查、可公開。

## 目前完成度判斷

以下為 public-safe 粗估，不等同 AGI 完成度。

| 目標層級 | 目前估計 | 判斷 |
|---|---:|---|
| 可展示的 governed companion runtime | 90-92% | 核心 pipeline、bridge、治理與審計已具備清楚輪廓 |
| 具身 autonomous operator | 60-65% | 已有 vision / camera / bridge / actor path，但真實 actuation 仍需更完整壓測 |
| AGI-compatible shell / cognition host | 82-85% | mentor escalation、proposal、autonomy policy、model asset boundary 已成形 |
| 真正 AGI | <5% | PHINIX 是 runtime / shell，不是 frontier cognition model 本身 |

## 為什麼這個進度重要

多數 agent 系統的風險不是「不會做事」，而是「做事時缺乏治理」。

PHINIX 的近期路線選擇是先把下列能力做成可測契約：

- 發現模型失效
- 向人類升級
- 產生工程提案
- 檢查修改邊界
- 外部化模型權重
- 預留 sandbox 自動升級

這些設計讓 PHINIX 更接近一個可以長期運行的 AI runtime，而不是一次性 demo。

## 下一步

下一階段會進入 Sandbox Upgrade Layer。

短期目標：

1. 建立 `SandboxRun` / `SandboxRunStore`
2. 建立 sandbox file boundary
3. 把 `UpgradeProposal` 轉成可審計 sandbox run
4. 先做資料契約，再做 worktree executor
5. 任何自動 patch 都必須先在隔離環境測試


