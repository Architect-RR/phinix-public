<!-- # ⭐ 修改開始 ⭐ -->
# PHINIX 目前證據狀態

更新日期：2026-07-27

Languages: [English](CURRENT_STATUS.md) | **繁體中文**

## 整體判斷

PHINIX 目前應描述為私人工程原型，不應描述為已證實可正常運作的產品。

私有 repository 內已有多個實作模組、自動測試、有限範圍的 sandbox demo，以及部分本機整合證據。這些資料能證明特定路徑在受控條件下可運作，但不能證明整個專案具有穩定可靠性。

Runtime truth label：`bounded_internal_evidence_only`

## 已在有限範圍內確認

- 這個公開 repository 的文件與抽象 schema 可在不接觸私有 runtime 的情況下檢閱。
- 私有端的針對性測試涵蓋治理、policy、訊息流程、proposal/review 結構、sandbox 計算與 viewer demo。
- Sandbox demo 產生流程曾以可重複、不開瀏覽器的方式測試。
- 私有端 bounded-agent 工作涵蓋 capability catalog、授權、proposal、sandbox coding 與 local-first retrieval 路徑的針對性測試。
- 部分本地模型與 companion/device 路徑已有受控 session 的紀錄。
- 私有記憶工作已有 in-process governance、持久化 store 元件、synthetic restart/restore 測試與 bounded runtime-wiring 檢查；真實使用者資料的耐久性與 at-rest 加密仍未證實。
- Companion 互動模式已有針對性多輪與本地模型 session 證據；私人網路與跨網 relay 的 bounded data path 也曾在 operator-controlled 條件下觀察。
- 私有 relay hardening 現已有第一段 pinned HTTPS 實作與 build/test 證據；尚未觀察 pinned ingress live session，upstream relay leg 也仍在該 TLS 邊界之外。
- 部分單幀 vision 路徑已有 structured local-model 證據，quality gate 也曾正確拒絕不適合的低光輸入。
- 私有 runtime lifecycle 測試已涵蓋部分背景、麥克風、暫存狀態、logging 與記憶資源的 cancellation-safe ownership/cleanup；單一 cleanup 永久不返回時仍未 bounded。
- 自我修正工作限制在 proposal、review、test 與狀態保留機制。

以上只代表局部證據，不是完整驗收。

## 尚未證實

- 外部使用者可在乾淨環境自行安裝與設定
- 可重現私有 runtime 的公開 demo
- 經過長時間 session 與多次重啟後仍能可靠端到端運作
- 跨電腦、模型、companion 裝置或穿戴裝置的一般相容性
- 使用真實資料的耐久加密個人記憶，以及持續自然的多輪伴侶互動
- 不需纜線的穿戴 session、pinned ingress live、relay 兩段端到端 application-layer TLS，以及可重複的可靠跨網運作
- 單一資源 cleanup 永久不返回時仍可 bounded shutdown
- 跨光線、動態、多幀與不同場景的穩健視覺理解
- 適合部署的安全性、效能與故障恢復能力
- 第三方獨立驗證
- 未經監督的自我修改或自主 promotion

## 能力成熟度

| 能力領域 | 目前公開判斷 |
|---|---|
| 架構與治理 | 私有端已有設計與部分實作；公開內容只有文件 |
| Policy 與 review 流程 | 私有端有針對性測試；完整運作覆蓋尚未證實 |
| Bounded agent 控制 | Catalog、授權、proposal 與 tool-loop 路徑有私有測試；一般能力尚未證實 |
| 本機知識、記憶與搜尋 | 私有端有本機索引、bounded connector、持久化 store 元件與 synthetic restart 檢查；真實資料耐久性、at-rest 加密與可靠 live search 尚未證實 |
| 本地 LLM 路徑 | 有部分本機檢查；穩定服務能力尚未證實 |
| Companion 與穿戴路徑 | 有特定 session、UI、build、bounded relay 與第一段 pinned transport 實作證據；pinned ingress live、cable-free、雙段 transport hardening 與一般支援尚未證實 |
| Vision 路徑 | 私有端有 bounded 單幀 local-model 證據；穩健感知與一般場景理解尚未證實 |
| Sandbox simulation 與 viewer | 有有限且可重複的 demo；不是經驗證的物理環境 |
| 自我修正 | 只提供 proposal 與 review 協助；不宣稱自主修改 |
| 公開發行版 | 尚未提供 |

## 提高可信度所需證據

1. 具固定依賴版本的乾淨環境安裝流程。
2. 外部使用者可重現、且不含敏感資訊的公開 smoke test。
3. 涵蓋啟動、失敗、恢復與關閉的重複端到端測試。
4. 作業系統、模型與裝置的支援矩陣。
5. 對安全邊界與故障處理的獨立檢視。

在取得上述證據前，公開描述應使用 `prototype`、`bounded test evidence`、`sandbox`、`proposal_only` 與 `not externally reproduced` 等有限範圍用語。
<!-- # ⭐ 修改結束 ⭐ -->
