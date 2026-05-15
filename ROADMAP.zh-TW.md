# Public Roadmap

Languages: [English](ROADMAP.md) | **繁體中文**

這份 roadmap 只描述 public-safe 的工程方向。private deployment details、local audit outputs、credentials、device-specific paths 與未審核自動化產物刻意排除。

## P0：公開專案基線

目標：

- 維持清楚的 public overview
- 定義 public/private boundaries
- 讓文件維持專業、工程化、可審查

輸出：

- README
- public scope
- architecture overview
- roadmap
- security and contribution guidance

## P1：Runtime architecture interfaces

目標：

- 文件化核心 runtime layers
- 保持 client entry points thin
- 分離 live interaction、background state、policy 與 validation

輸出：

- runtime state model
- event flow model
- stuck issue model
- proposal model

## P2：Governed improvement flow

目標：

- 把 failure 與 low-quality state 轉成可審核 proposal
- 在 sandbox 或 worktree 中驗證改善，不直接 promotion
- 每次變更保留 tests、rollback plan 與 audit record

輸出：

- proposal schema
- sandbox validation interface
- audit summary interface
- promotion status model

## P3：Read-only observability

目標：

- 在不暴露 private audit data 的前提下顯示有限 runtime health status
- 讓 observability 與 execution 分離

輸出：

- stats-only status summary
- maintenance smoke summary
- viewer / panel display model

## P4：Proactive companion behavior

目標：

- 支援有用的主動建議，但避免變成噪音
- reminder 必須可審核、rate-limited、可取消

輸出：

- proactive suggestion model
- cooldown policy
- notification boundary

## P5：Embodiment adapter abstraction

目標：

- 定義 companion devices、wearables 與 future hardware integrations 的安全介面
- 讓 cognition / governance 與 low-level control 分離

輸出：

- embodiment adapter interface
- device capability descriptor
- authorized-device boundary model

## P6：Controlled maintenance automation

目標：

- 允許 bounded lab-only maintenance loop
- 自動化預設關閉
- 需要 status check、stop condition 與 audit output

輸出：

- auto maintenance contract
- dry-run report
- bounded runner configuration

## Public repo 非目標

- Production deployment guide
- Secret or credential handling
- Device-specific bridge implementation
- Local audit logs
- Full private runtime mirror
- High-risk execution paths
