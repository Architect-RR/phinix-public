<!-- # ⭐ 修改開始 ⭐ -->
# 公開文件 Roadmap

Languages: [English](ROADMAP.md) | **繁體中文**

這份 roadmap 是證據目標的先後順序，不是交付承諾。私有實作細節與時程刻意不公開。

## 目前：誠實的公開基線

- 公開 repository 只保留文件與抽象 schema。
- 將私有實作證據與公開可用性分開。
- 先說明已知限制，再描述未來能力。
- 移除重複或偏宣傳的用語。

## 下一步：可重現性

- 為低風險公開範例定義乾淨環境設定清單。
- 定義不含私有資料、可由外部重現的 capability selection 與本機證據 retrieval mock 流程。
- 新增只使用 synthetic records 的 public-safe restart/restore 範例，並明確標示 persistence、promotion 與 deletion 邊界。
- 只有在私有 workspace 之外可以重現時，才發布不含敏感資訊的 smoke test。
- 固定依賴版本並記錄支援環境。
- 記錄失敗與恢復行為，不只記錄成功輸出。

狀態：尚未交付。

## 後續：有限範圍的公開 Demo

- 提供使用 mock data，且不依賴裝置、憑證或私有 runtime 的小型 demo。
- 所有 side effect 預設關閉。
- 公開 acceptance criteria 與預期 failure mode。
- 清楚區分計算輸出與真實世界事實。

狀態：只有設計方向。

## 延後：Runtime 與裝置發布決策

- 評估是否有任何 runtime 子集具備足夠安全性與可維護性，可考慮公開。
- 必須先有明確 support matrix、security review 與 rollback path。
- 硬體、穿戴、模型與外部 API 整合分別管理與 gate。
- 在把 companion memory、無線穿戴 transport 或 live search 描述為可靠前，分別取得獨立證據。
- 在任何 deployment-oriented 宣稱前，先完成耐久記憶的 at-rest 加密決策，以及 relay 路徑的 application-layer transport review。
- 在把穿戴或感知路徑描述為一般可用前，先取得可重複 cable-free session 與多條件 vision 證據。

狀態：尚無公開發布決策。

## 非目標

- 鏡像私有 runtime
- 公開憑證、本機路徑、原始 log 或裝置識別資訊
- 宣稱能自主修改自身程式
- 把 sandbox 輸出當成經驗證的真實世界行為
- 在缺少可重現性與安全證據前發布部署說明
<!-- # ⭐ 修改結束 ⭐ -->
