# DSH Plugin Dev

中文 | [English](README.en.md)

本仓库的四个技能均来源于 **DeepSeek 官方开源项目 [DSH（DeepSeek Harness）](https://github.com/deepseek-ai/deepseek-harness)**。这里只做重新整理，方便在其他开发工具中使用；技能正文、参考资料和模板均保留官方原文。

这是社区整理仓库，与 DeepSeek 官方无隶属关系。原始内容的版权和 MIT 许可归属见 [LICENSE](LICENSE)。

## 包含的技能

| 技能 | 用途 |
|---|---|
| [cordis-plugin-development](cordis-plugin-development/SKILL.md) | DSH 插件和 bundle 开发主流程，包含 Host、Client UI、MCP 参考资料与模板 |
| [cordis-composition-reference](cordis-composition-reference/SKILL.md) | Cordis Loader YAML 语法与可安装插件包清单 |
| [editing-cordis-compositions](editing-cordis-compositions/SKILL.md) | 创建、修改和验证 Agent preset 与 Cordis composition |
| [agent-experience](agent-experience/SKILL.md) | 工具定义、技能设计和上下文按需加载原则 |

```text
dsh-plugin-dev/
├── cordis-plugin-development/
│   ├── SKILL.md
│   ├── references/
│   └── templates/
├── cordis-composition-reference/
│   ├── SKILL.md
│   └── references/
├── editing-cordis-compositions/
│   └── SKILL.md
└── agent-experience/
    └── SKILL.md
```

共保留 33 个上游技能文件，包括完整的参考资料、UI 与 MCP 模板，以及模板的全部语言资源。`cordis-plugin-development` 会引用其他 Cordis 技能，请保留四个目录及其原名，不要只复制单个 `SKILL.md`。

## 使用方式

将本仓库克隆或下载到本地，按照所用开发工具的技能导入方式，添加需要的技能目录。也可以直接让 Agent 从 `cordis-plugin-development/SKILL.md` 开始阅读，再按任务读取相应的参考资料和模板。

这些技能原本运行于 DSH 创造模式。完整流程使用 DSH 提供的 `cordis_inspect_list`、`cordis_inspect_query` 和 `plugin_manager`，以查询实际 API、安装 bundle 并验证结果。

在其他开发工具里，文档与模板可以用于插件开发，但导入技能本身不会同时提供上述 DSH 工具。运行时检查、安装和验证需要连接目标 DSH 环境，或按目标工具的能力进行适配。原文中的 profile、权限以及 Desktop `app.asar` 读取约定，应结合实际环境理解。

## 上游来源

- 项目：[deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)
- 原始目录：[packages/preset/agent-preset/skills](https://github.com/deepseek-ai/deepseek-harness/tree/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159/packages/preset/agent-preset/skills)
- 来源提交：[`fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159`](https://github.com/deepseek-ai/deepseek-harness/commit/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159)
- 整理日期：2026-11-05

该目录是官方创造模式使用的运行时技能资源。可从官方的 [cordis preset 配置](https://github.com/deepseek-ai/deepseek-harness/blob/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159/packages/bundle/web-app/presets/cordis.patch.yml#L122-L138) 核对其加载路径。

[SOURCE.json](SOURCE.json) 记录来源、文件映射、Git blob SHA-1 和 SHA-256。所有技能文件均与固定上游提交保持字节一致；本仓库仅调整外层目录和配套说明，不保证自动同步后续上游变化。

## 完整性校验

在仓库根目录运行：

```sh
shasum -a 256 -c SHA256SUMS
```

## 许可

按上游 [MIT License](LICENSE) 分发，并保留 `Copyright (c) 2026 DeepSeek` 及完整许可文本。
