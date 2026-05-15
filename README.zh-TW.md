# PHINIX 公開總覽

PHINIX 是一個 private-first、local-first 的受治理 agent runtime 專案。

這個公開 repository 只保留工程上適合公開的專案概覽、架構說明、協作邊界與抽象介面方向。完整 private runtime、裝置橋接細節、本機憑證、硬體設定、審計產物與部署專屬實作不放在此處。

## 目前定位

PHINIX 不是聊天機器人 wrapper。此專案採用受治理 runtime 模式：

```text
輸入
-> runtime state
-> policy 與 risk gate
-> proposal generation
-> sandbox validation
-> audit
-> human or operator review
```

實務目標是讓 agent 行為在影響高風險系統前，先具備可觀測、可審核、可測試、可回滾的工程邊界。

## 公開 repository 內容

- 高層架構摘要
- public/private scope 規則
- 公開 roadmap
- 貢獻與安全說明
- 抽象介面方向
- public-safe 狀態報告

此 repository 刻意不包含：

- private deployment code
- device credentials 或 bridge tokens
- hardware allowlists
- local audit logs
- model weights 或模型資產 manifest
- 未審核的自動化輸出
- private maintenance reports

## 目前工程重點

private 專案目前聚焦：

- runtime 與 side-effect observability
- proposal-based improvement flow
- promotion 前的 sandbox validation
- lab-only maintenance smoke tests
- read-only status summaries
- 嚴格 public/private boundary control

公開更新會維持在架構、介面與可驗證工程狀態層級。private implementation details 只會摘要，不會鏡像公開。

## 文件

- [架構總覽](ARCHITECTURE_OVERVIEW.zh-TW.md)
- [公開範圍](PUBLIC_SCOPE.zh-TW.md)
- [Roadmap](ROADMAP.zh-TW.md)
- [目前狀態](CURRENT_STATUS.zh-TW.md)
- [貢獻說明](CONTRIBUTING.zh-TW.md)
- [Security](SECURITY.md)

## 協作邊界

Issue 與 PR 應聚焦：

- 架構回饋
- 介面設計
- public-safe 文件
- 風險與治理審查
- 低風險範例或 simulation stubs

請勿提交 secrets、private device details、production credentials、local audit files 或未審核的自動化輸出。
