# ⭐ 修改開始 ⭐
# PHINIX 公開路線圖

這份路線圖只描述適合公開討論的方向，不等於 private 主線的所有內部細節。

---

## P0：公開最小包

目標：

- 建立公開定位
- 建立公開協作規則
- 定義 public / private 邊界

輸出：

- README
- scope 文件
- roadmap
- expert call

---

## P1：三層 runtime 骨架

目標：

- 即時層
- 緩衝層
- 思考層

輸出：

- 公開架構圖
- 抽象接口
- 最小事件流模型

---

## P2：Stuck Issue Queue

目標：

- 把卡關做成正式資料結構
- 支援延後重試與背景回看

輸出：

- `StuckIssue`
- `RetryPlan`
- `EscalationCandidate`

---

## P3：Proactive Companion

目標：

- 有新結論時可低打擾提醒
- 不必等使用者再次開口

輸出：

- reminder policy
- proactive suggestion flow
- notification channel abstraction

---

## P4：Embodied Companion

目標：

- 從眼鏡 / companion device 擴展到更多具身節點

輸出：

- embodiment adapter interface
- multi-device context model
- safety boundary design

---

## P5：Humanoid Robot Cognition Layer

目標：

- 將 PHINIX 作為未來人形機器人的可移植主腦架構

可能角色：

- 記憶層
- 情境層
- 主動提醒層
- 治理層
- 長時一致性層

不直接等同於：

- 低階馬達控制器
- 硬即時控制器
- 單純的機器人 SDK wrapper

---

## 核心里程碑判準

只有在以下條件逐步完成後，PHINIX 才能從概念走向成熟：

1. public / private 邊界清楚
2. live 主鏈與 background cognition 分流
3. stuck issue queue 可運作
4. proactive reminder 可控
5. embodiment layer 可抽象化
6. 主腦可跨裝置延續

# ⭐ 修改結束 ⭐
