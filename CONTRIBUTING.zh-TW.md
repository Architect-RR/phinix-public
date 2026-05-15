# Contributing to PHINIX

Languages: [English](CONTRIBUTING.md) | **繁體中文**

這個公開 repo 歡迎能改善文件、架構清晰度、介面邊界與 public-safe review 的貢獻。

## 適合參與的背景

- Agent runtime architecture
- Local-first systems
- State management and observability
- Human-computer interaction
- Wearable or companion interfaces
- Governance、audit、risk review
- Test and validation design

## 建議貢獻軌道

### A. Architecture

- Runtime layer separation
- State and event interfaces
- Proposal and validation flows
- Read-only observability

### B. Human Interaction

- Companion UX
- Low-interruption proactive behavior
- Viewer or panel information density
- Accessibility and operator workflows

### C. Device and Embodiment Boundaries

- Adapter abstractions
- Authorized-device capability descriptors
- Governed runtime 與 low-level control 的分離

### D. Governance and Safety

- Review workflows
- Public/private scope checks
- Audit summary models
- Low-risk / high-risk boundary definitions

## 貢獻原則

1. 不要誇大未完成能力。
2. 不要提交 secrets、raw logs、local audit files 或 hardware allowlists。
3. 不要把高風險 device control 包裝成便利功能。
4. 優先提交文件、介面與低風險骨架。
5. 每次修改只聚焦單一主題。
6. 若內容是 proposal、interface draft 或 non-runtime example，請明確標示。

## 建議流程

1. 架構或邊界變更先開 issue。
2. 提出最小但有價值的修改。
3. 實作前先討論風險與驗證方式。
4. 若涉及 governance、device 或 automation，採用更高審查標準。

## 初期高價值貢獻

- Public architecture diagrams
- Runtime state interfaces
- Stuck issue and proposal models
- Read-only status summary schema
- Public-safe simulation stubs
- Documentation cleanup
