# ⭐ 修改開始 ⭐
# PHINIX 公開介面方向

這個目錄預留給未來可公開化的抽象接口與資料模型。

原則：

- 先公開抽象
- 後公開低風險骨架
- 最後才考慮公開更多實作

---

## 建議優先公開的接口

### 1. Realtime Runtime Interface

用途：

- 描述即時輸入、即時回覆、低延遲輸出

### 2. Buffer Layer Interface

用途：

- 描述事件沉澱、摘要、狀態快照、暫存記憶

### 3. Thinking Worker Interface

用途：

- 描述背景思考任務、結果產出、取消與冷卻

### 4. Stuck Issue Interface

用途：

- 描述未解問題、重試條件、升級條件

### 5. Proactive Notifier Interface

用途：

- 描述主動提醒，但不直接開放高風險主動控制

### 6. Embodiment Adapter Interface

用途：

- 讓未來眼鏡、手機、機器人等不同身體都能接上同一主腦

---

## 未來方向

若 PHINIX 要成為未來人形機器人的主腦架構，最重要的不是公開所有裝置實作，而是先把：

- cognition
- memory
- governance
- proactive reasoning
- embodiment abstraction

這幾個接口切乾淨。

# ⭐ 修改結束 ⭐
