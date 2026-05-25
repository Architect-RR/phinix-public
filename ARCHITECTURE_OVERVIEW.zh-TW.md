# Architecture Overview

Languages: [English](ARCHITECTURE_OVERVIEW.md) | **繁體中文**

本文件只描述適合公開討論的高層架構，不包含 private deploy 細節、硬體橋接設定、憑證、審計全文或本機維護資料。

## 核心概念

PHINIX 是 local-first governed agent runtime。它的重點不是單次回答，而是把長時任務、背景狀態、工具使用、提案、驗證與審計放在同一個可治理流程中。

## 公開架構層

### 1. Client entry layer

職責：

- 接收文字、語音、viewer、companion 或 wearable 入口請求
- 顯示受控結果
- 保持 thin client

此層不應直接做高風險決策。

### 2. Runtime state layer

職責：

- 管理 session
- 管理短期事件與狀態快照
- 保存卡關、延後處理與待審核項目
- 將背景狀態整理成可觀測資料

### 3. Policy and proposal layer

職責：

- 判斷請求風險
- 在考慮任何高風險 execution 前，先套用 non-harm semantic boundary
- 建立工程提案
- 標示禁止修改範圍
- 決定是否進入 sandbox
- 產生 rollback / test / audit 要求

### 4. Sandbox validation layer

職責：

- dry-run
- worktree 驗證
- patch validation
- test execution
- local branch materialization
- private audit

此層仍不代表 production approval。

### 5. Read-only observability layer

職責：

- 顯示 DANGLE / promotion / lab smoke 摘要
- 僅輸出 stats-only summary
- 不暴露 audit 全文
- 不提供執行、restore、push、merge 動作

## Stuck issue queue

PHINIX 把「卡關」視為可追蹤狀態，而不是一次性錯誤。

這讓系統可以：

- 記住失敗位置
- 記住已嘗試方案
- 在新線索出現時再回看
- 在適當時機提出低打擾提醒

## Proactive behavior

主動性不等於持續打擾。

較健康的流程是：

1. 背景產生候選結論
2. 轉成可審核候選
3. 套用 policy / cooldown
4. 由使用者選擇是否展開

## Embodiment boundary

如果未來接上更多裝置，PHINIX 比較適合扮演：

- memory
- context
- governance
- risk review
- proposal generation
- audit

而不是直接取代低階控制器或硬即時控制器。

## Engineering rule

所有高風險能力都應遵循：

```text
proposed action
-> policy check
-> dry-run or simulation
-> human/operator gate
-> execution adapter
-> audit
```

Design-only notes、memory policies 與 speculative capability ideas 在獨立 gated phase 實作、測試並文件化 runtime behavior 前，都應維持為人類可讀的治理材料。
