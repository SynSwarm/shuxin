# iOS 客户端（SwiftUI）

Xcode 工程可置于此目录或子目录；落地后把本说明换成真实工程入口与构建方式。

## 占位目录（与架构分层一致）

| 目录 | 职责 |
|------|------|
| `Sources/Presentation/` | SwiftUI 视图、导航、本地 UI 状态 |
| `Sources/Application/` | 用例编排（寄信、同步策略等） |
| `Sources/Domain/` | 领域模型与领域服务（纯逻辑、可测） |
| `Sources/Infrastructure/` | 网关 HTTP 客户端、Keychain、系统能力适配；**不**直接散落飞书原始 JSON 拼装 |
| `Resources/` | 资产、本地化等（随工程调整） |

网关实现见 **独立私有仓库**（`../ARCHITECTURE.md` §2）。
