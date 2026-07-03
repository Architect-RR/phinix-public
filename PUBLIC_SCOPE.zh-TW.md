<!-- # ⭐ 修改開始 ⭐ -->
# Public Scope

Languages: [English](PUBLIC_SCOPE.md) | **繁體中文**

這份文件定義哪些內容適合放在 PHINIX public repository，哪些必須保留在 private repo。

## 適合公開的內容

### 文件

- 專案概覽
- 高層架構
- 公開 roadmap
- 貢獻規則
- 安全回報流程
- public-safe 狀態摘要
- public-safe boundary-hardening 摘要

### 抽象介面

- runtime state interfaces
- event and message shapes
- stuck issue and retry models
- proposal and audit summary models
- embodiment adapter abstractions
- read-only status summaries
- human-readable memory governance summaries
- 不含 secrets 的 credential boundary summaries
- 不含 raw benchmark output 的 public-safe model evaluation summaries

### 低風險範例

- mock data
- simulation stubs
- interface skeletons
- documentation examples

### 協作材料

- issue templates
- PR template
- architecture discussion prompts
- public-safe review topics

## 必須保留 private 的內容

### 憑證與本機設定

- tokens
- API keys
- bridge credentials
- local machine configuration

### 私有操作資料

- raw conversation logs
- raw audio or image captures
- device identifiers
- hardware allowlists
- local audit reports
- lab maintenance artifacts
- private workspace inventories 或 vault details
- raw model benchmark output

### 大型或 vendor-specific assets

- APK build outputs
- SDK or JDK archives
- vendor binaries
- device analysis artifacts
- model weights

### 敏感實作細節

- device-specific bridge internals
- direct actuation paths
- unreviewed automation outputs
- private maintenance loops
- high-risk domain execution details
- machine-loadable private runtime configuration
- boundary testing 使用的敏感 prompt corpus
- device provisioning instructions

## 公開發布規則

公開內容應該：

- 可理解
- 可審查
- 可安全討論
- 對未完成能力保持誠實
- 不包含憑證與私有操作資料

不確定時，實作細節留在 private，只公開 interface 或 architecture summary。
<!-- # ⭐ 修改結束 ⭐ -->
