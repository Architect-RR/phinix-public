# Public Roadmap

Languages: [English](ROADMAP.md) | **繁體中文**

這份路線圖只描述適合公開討論的方向，不揭露 private deployment 細節。

## P0：公開最小包

目標：

- 定義公開定位
- 定義協作規則
- 定義 public/private 邊界

輸出：

- README
- scope 文件
- roadmap
- expert call

## P1：三層 runtime 骨架

目標：

- 即時層
- 緩衝層
- 思考層

輸出：

- 公開架構圖
- 抽象接口
- 最小事件流模型

## P2：Stuck issue queue

目標：

- 把失敗與不確定性轉成結構化狀態
- 支援延後重試與背景回看

輸出：

- `StuckIssue`
- `RetryPlan`
- `EscalationCandidate`

## P3：Proactive companion

目標：

- 在不等待下一個 prompt 的前提下，主動提出有用的新結論
- 同時維持低打擾、低干擾

輸出：

- reminder policy
- proactive suggestion flow
- notification channel abstraction

## P4：Embodied companion

目標：

- 從眼鏡與 companion devices 擴展到更廣的 embodiment layer

輸出：

- embodiment adapter interface
- multi-device context model
- safety boundary design

## P5：Humanoid robot cognition layer

目標：

- 讓 PHINIX 成為未來人形機器人的可攜式 cognition architecture

可能角色：

- 記憶
- 情境
- 主動推理
- 治理
- 長時一致性

不等同於：

- 低階馬達控制
- 硬即時控制
- 單純機器人 SDK wrapper

## 真正重要的里程碑

PHINIX 要從概念走向成熟，至少要逐步完成：

1. 清楚的 public/private 邊界
2. live interaction 與 background cognition 分流
3. 能運作的 stuck-issue queue
4. 可控的 proactive reminders
5. 可抽象化的 embodiment layer
6. 可跨多裝置或多身體延續
