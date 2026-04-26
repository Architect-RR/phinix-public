# Public Scope

Languages: [English](PUBLIC_SCOPE.md) | **繁體中文**

這份文件定義哪些內容適合放在公開 GitHub repo，哪些應留在 private repo。

## 適合公開的內容

### 文件

- 專案願景
- 高層架構圖
- 路線圖
- 公開協作規則
- 非敏感 checkpoint 摘要

### 抽象介面

- runtime 分層接口
- memory / world state 結構
- stuck issue / proactive suggestion 模型
- embodiment adapter 抽象接口

### 低風險範例

- mock data
- 非敏感測試骨架
- 不綁硬體的 simulation stubs
- 公開開發筆記與輔助腳本

### 社群材料

- issue 模板
- PR 模板
- 設計討論
- 專家回饋入口

## 應保留 private 的內容

### 憑證與設定

- token
- API keys
- bridge credentials
- 本機環境設定

### 私有操作資料

- 原始對話紀錄
- 原始語音資料
- 裝置識別資訊
- 硬體白名單與授權細節

### 大型產物與 vendor blobs

- APK build outputs
- SDK / JDK archives
- vendor binaries
- reverse-engineered artifacts

### 敏感實作細節

- 直接具身控制鏈細節
- 尚未穩定的治理內核
- 容易被濫用的 device control 路徑

## 建議拆分方式

### Public repo

- 公開文件
- 清理後的抽象接口
- 可重用的低風險骨架

### Private repo

- 完整運作 runtime
- 敏感 bridge
- 訓練與評測資料
- build toolchains
- 部署設定
- 硬體專屬實作

## 發布原則

公開內容應該符合：

- 可理解
- 可討論
- 可安全協作
- 對未完成能力保持誠實
