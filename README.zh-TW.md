# PHINIX Public Starter

Languages: [English](README.md) | **繁體中文**

這個公開 repo 是 PHINIX 的 `public-safe` 起點。

它不是完整私有主腦的直接公開版本，而是用來分享：

- 專案願景
- 架構方向
- 協作規則
- 可公開討論的抽象介面
- 路線圖與核心問題

## 專案定位

PHINIX 可以被描述為：

**一個本地主權優先、具治理邊界、面向具身 companion 與未來人形機器人的 AI runtime**

現階段重點：

- 穩定的核心 runtime
- 可控的自主性邊界
- 記憶與問題追蹤能力
- 可跨裝置延展的 cognition interfaces

## 為什麼這個 repo 是 public-safe

完整 private repo 仍包含不適合直接公開的內容：

- bridge 憑證與部署細節
- 原始互動與訓練紀錄
- 硬體橋接細節
- 大型 build 產物與 vendor binaries
- 尚在演進中的治理內核

因此這個公開 repo 的目標，是先公開方向，而不是公開所有運作細節。

## 這個 repo 目前包含

- `README.md` / `README.zh-TW.md`
- `ARCHITECTURE_OVERVIEW.md` / `ARCHITECTURE_OVERVIEW.zh-TW.md`
- `PUBLIC_SCOPE.md` / `PUBLIC_SCOPE.zh-TW.md`
- `CONTRIBUTING.md` / `CONTRIBUTING.zh-TW.md`
- `CALL_FOR_EXPERTS.md` / `CALL_FOR_EXPERTS.zh-TW.md`
- `ROADMAP.md` / `ROADMAP.zh-TW.md`
- `interfaces/`

## PHINIX 未來可能成為什麼

### 1. AR 認知副駕

作為眼鏡與 wearable 裝置上的低延遲輔助層。

### 2. 本地主權數位伴侶

作為具有記憶、回看能力與主動提醒的長時 companion core。

### 3. 人形機器人的 cognition layer

作為可跨不同身體延續的認知與治理核心。

可能扮演：

- 記憶層
- 問題追蹤層
- 主動推理層
- 治理層
- 長時一致性層

## 公開協作原則

- 本地主權優先
- 能力邊界誠實
- 不公開敏感具身控制鏈
- 先公開文件與介面，再逐步公開低風險骨架
- 只有在驗證後才逐步擴大開放範圍

## 建議的 repo 策略

完整運作系統暫時維持 private。這個 public repo 用於：

- 架構審查
- 介面設計
- 專家討論
- 低風險公開協作
