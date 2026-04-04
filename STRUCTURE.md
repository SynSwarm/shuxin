# 书信 (shuxin) — 目录结构（意图）

代码尚未全部落地时，本文只约定 **方向**。与 `ARCHITECTURE.md` 一致：**公开仓库以 iOS 客户端为开源主体**；**网关源码在独立私有仓库**，不在本目录下维护（见 `ARCHITECTURE.md` §2）。

---

## 目标布局（占位已建，随实现填充）

```
.
├── .github/
│   ├── dependabot.yml
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml
│   │   ├── config.yml
│   │   └── feature_request.yml
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── workflows/
│       └── ci.yml              # 当前：必备文件等元数据检查
├── CHANGELOG.md                # 版本与变更记录
├── CODE_OF_CONDUCT.md          # 社区准则
├── CONTRIBUTING.md             # 贡献流程与仓库边界（必读）
├── SECURITY.md                 # 漏洞披露方式
├── README.md
├── ARCHITECTURE.md
├── STRUCTURE.md
├── PROGRESS.md
├── LICENSE
├── ios/
│   ├── README.md
│   ├── Resources/              # 资产等（.gitkeep 占位）
│   └── Sources/
│       ├── Application/
│       ├── Domain/
│       ├── Infrastructure/
│       └── Presentation/
└── docs/
    ├── README.md
    ├── adr/                      # ADR（.gitkeep 占位）
    └── api/
        └── README.md             # 对外 API 契约摘要占位
```

### 根目录文件分工（速查）

| 路径 | 用途 |
|------|------|
| `CONTRIBUTING.md` | 贡献步骤、Issue/PR、**本仓 vs 私仓网关**边界 |
| `SECURITY.md` | 安全报告渠道（勿在公开 Issue 贴细节） |
| `CODE_OF_CONDUCT.md` | 参与者行为约定 |
| `CHANGELOG.md` | 面向使用者的版本变更 |
| `ARCHITECTURE.md` / `STRUCTURE.md` / `PROGRESS.md` | 架构、目录意图、阶段决策与待办 |

**私有网关仓**（另库）：建议同样包含 `ARCHITECTURE.md`（可引用本文）、`STRUCTURE.md`、实现侧 ADR；与本文冲突时以 **先改公开边界文档再改实现** 为准。

---

## 依赖方向（简述）

- **ios/**：Presentation → Application → Domain；Infrastructure 经协议对接 **网关 HTTP API**，不直接散落飞书 REST 细节。
- **网关（私有仓）**：路由 / handler → 应用服务 → 领域 → Feishu / DB 适配器；目录树见该仓 `STRUCTURE.md`。

---

## 变更记录

| 日期 | 说明 |
|------|------|
| 2026-04-04 | 初版：占位与公开范围说明。 |
| 2026-04-04 | 网关已决为独立私有仓；本仓不再列可选 `gateway/`。 |
| 2026-04-04 | 建立 `ios/` 分层占位、`docs/`、`docs/adr/`、`docs/api/`。 |
| 2026-04-04 | 对齐仓库现状：补充 `.github/`、`CONTRIBUTING.md` 等根目录与速查表。 |
