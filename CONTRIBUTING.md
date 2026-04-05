# 参与贡献 · Contributing

感谢你愿意为 **书信 (shuxin)** 花时间。我们欢迎所有「不着急、可协作、尊重边界」的贡献。

---

## 仓库边界（请先读）

本仓库的定位见 [ARCHITECTURE.md](ARCHITECTURE.md)：

- **本公开仓**：**SwiftUI / iOS 客户端**、产品/架构文档与 API 契约**摘要**。
- **邮局网关（后端）**：在**独立私有仓库**维护，**不**随本仓库开源；贡献服务端实现请在维护者协调下进入私仓流程。

因此：在本仓的 Issue/PR 请聚焦 **iOS 客户端、文档、契约摘要与设计资产**；网关实现与线上密钥相关问题请通过维护者指引的渠道沟通。

---

## 如何开始

1. 阅读 [README.md](README.md)、[STRUCTURE.md](STRUCTURE.md) 与相关 `docs/`。
2. **小修复**（错别字、链接、明显笔误）：可直接提 Pull Request。
3. **较大改动**（新功能、目录结构调整、破坏性 API 契约变更）：建议 **先开 Issue** 对齐方向，避免重复劳动；涉及架构的变更请同步更新 `ARCHITECTURE.md`、`STRUCTURE.md` 与 `PROGRESS.md`（并与维护者在 Issue 中确认是否需补充 ADR）。

---

## Issue

- **Bug**：可复现的步骤、期望与实际行为、环境（iOS 版本、构建方式等）。
- **功能或想法**：使用场景、是否愿意参与实现。
- 尽量用 [Issue 模板](.github/ISSUE_TEMPLATE/)，信息齐了更好处理。

---

## Pull Request

- 一个 PR 尽量只做 **一件事**，便于审查与回滚。
- 在描述中说明 **动机、方案概要、破坏性变更**（若有）。
- 若改动可见 UI，请附 **截图或录屏**（脱敏）。
- 请确保你的提交 **不引入** 密钥、证书、`.env` 或飞书 Secret（参见 [.gitignore](.gitignore)）。

填写 PR 时请使用仓库的 [PR 模板](.github/PULL_REQUEST_TEMPLATE.md)。

---

## 行为准则

参与本仓库即表示你同意遵守 [行为准则](CODE_OF_CONDUCT.md)。

---

## 许可证

向本仓库贡献的代码与文档，将按仓库根目录的 [Apache License 2.0](LICENSE) 授权（除非你另行与维护者约定并书面说明）。
