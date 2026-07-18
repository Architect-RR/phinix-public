<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX 公開總覽

PHINIX 是一個探索 local-first、policy-gated agent system 的私人工程原型。

這個公開 repository 只包含文件與抽象 JSON schema，不包含可直接執行的 PHINIX 發行版、部署套件、裝置橋接、模型資產、憑證或私有審計資料。

Languages: [English](README.md) | **繁體中文**

## 目前狀態

PHINIX 的私人工程 repository 內已有原始碼、針對性測試、有限範圍的 sandbox demo，以及部分本機整合測試紀錄。

這些證據有工程參考價值，但範圍有限。目前仍不足以證明外部使用者可以自行安裝、整體端到端可靠運作、在多次真實情境中穩定恢復，或普遍支援硬體與正式部署。

目前適合公開的判斷是：

> 工程原型已有局部內部證據；整體運作可靠性與外部可重現性尚未證實。

Runtime truth label：`bounded_internal_evidence_only`

## 證據邊界

| 領域 | 目前已有證據 | 尚未證實 |
|---|---|---|
| 治理與訊息流程 | 私有原始碼與針對性自動測試 | 外部重現與長時間持續運作 |
| 本地模型整合 | 部分本地 provider 與延遲檢查 | 穩定長時間服務與正式模型選型 |
| Companion 與穿戴路徑 | 特定裝置的有限測試紀錄 | 一般裝置相容性與無人值守運作 |
| Sandbox simulation 與 viewer | 可重複的計算與 HTML demo 檢查 | 完整碰撞物理、數位分身精度或真實世界控制 |
| 自我修正流程 | Proposal、review 與狀態保留結構 | 自主修改程式或未經監督的 promotion |

此表只說明證據範圍，不代表產品成熟度。

## 公開 Repository 內容

- [架構方向](ARCHITECTURE_OVERVIEW.zh-TW.md)
- [目前證據狀態](CURRENT_STATUS.zh-TW.md)
- [公開文件 Roadmap](ROADMAP.zh-TW.md)
- [公開與私有範圍](PUBLIC_SCOPE.zh-TW.md)
- [抽象介面 Schema](interfaces/README.md)
- [貢獻說明](CONTRIBUTING.zh-TW.md)
- [安全回報](SECURITY.md)

抽象 schema 只描述可能的資料形狀；檔案存在不代表已有對等的公開 runtime endpoint。

## 不宣稱

這個 repository 不宣稱：

- 已有可下載或可普遍使用的 PHINIX 應用程式
- 整體端到端能可靠運作
- 已獲正式部署批准
- 能持續自主執行
- 能自動修改自身程式
- 普遍支援硬體或穿戴裝置
- 已具備經驗證的數位分身或完整物理引擎
- 公開提供私有 runtime

## 公開規則

公開更新只應涵蓋架構、介面形狀、有限證據、已知限制與協作材料。私有實作細節、原始 log、本機路徑、憑證、裝置識別資訊、模型資產與未審查輸出必須保留在私有範圍。

## 協作

Issue 與 pull request 應聚焦於文件清晰度、介面設計、可測試的低風險範例、風險檢視與可重現性。請勿提交 secret、私有裝置細節、部署憑證、原始模型資產或本機審計紀錄。
<!-- # ⭐ 修改結束 ⭐ -->
