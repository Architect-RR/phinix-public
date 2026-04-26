# ⭐ 修改開始 ⭐
# PHINIX 公開範圍

這份文件定義未來公開到 GitHub 時，哪些內容適合放出，哪些內容應保留在 private repo。

---

## 可公開內容

### 文件與定位

- 專案願景
- 高層架構圖
- 路線圖
- 公開協作規則
- 非敏感 checkpoint 摘要

### 抽象介面

- runtime 分層接口
- memory / world state 抽象結構
- stuck issue / proactive suggestion 抽象模型
- embodiment adapter 抽象接口

### 低風險範例

- 假資料示例
- 非敏感測試骨架
- 無硬體綁定的模擬程式
- 開發文件與說明腳本

### 社群內容

- issue 模板
- PR 規範
- 設計討論
- 專家討論題

---

## 不宜公開內容

### 憑證與敏感設定

- token
- API key
- bridge secret
- 本機環境設定

### 私有操作資料

- 原始對話紀錄
- 原始語音資料
- 裝置識別資訊
- 硬體白名單與授權細節

### 大型產物與 vendor blob

- APK build 產物
- SDK / JDK 壓縮包
- vendor 二進位
- 反編譯產物

### 高敏感實作細節

- 直接具身控制鍊的敏感配置
- 尚未穩定的治理核心細節
- 容易被濫用的 bridge / device control 細節

---

## 建議拆分方式

### Public Repo

建議只放：

- `github_public/` 內文件
- 經整理後的抽象接口
- 可重用的低風險模組骨架

### Private Repo

保留：

- 完整主腦實作
- 敏感 bridge
- 訓練與測試資料
- build tools
- 硬體細節
- 真實部署配置

---

## 公開原則

1. 不因為想吸引人就過度公開
2. 不把未驗證能力宣稱為已完成
3. 不把 private deploy 細節混入公開 repo
4. 公開內容應以「可理解、可討論、可安全協作」為目標

# ⭐ 修改結束 ⭐
