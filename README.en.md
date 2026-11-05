# DSH Plugin Dev

[中文](README.md) | English

All four skills in this repository come from **DeepSeek's official open-source project, [DSH (DeepSeek Harness)](https://github.com/deepseek-ai/deepseek-harness)**. This repository only reorganizes them for use in other development tools. The skill instructions, reference materials, and templates retain their original upstream contents.

This is a community-maintained collection and is not affiliated with DeepSeek. See [LICENSE](LICENSE) for the original copyright notice and MIT license.

## Included skills

| Skill | Purpose |
|---|---|
| [cordis-plugin-development](cordis-plugin-development/SKILL.md) | Main workflow for developing DSH plugins and bundles, with Host, Client UI, and MCP references and templates |
| [cordis-composition-reference](cordis-composition-reference/SKILL.md) | Cordis Loader YAML syntax and a list of installable plugin packages |
| [editing-cordis-compositions](editing-cordis-compositions/SKILL.md) | Creating, changing, and validating Agent presets and Cordis compositions |
| [agent-experience](agent-experience/SKILL.md) | Tool definitions, skill design, and on-demand context loading |

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

All 33 upstream skill files are preserved, including the complete reference materials, UI and MCP templates, and all template locale resources. `cordis-plugin-development` references the other Cordis skills, so keep all four directories with their original names rather than copying a single `SKILL.md`.

## Usage

Clone or download this repository, then add the skill directories you need using your development tool's skill import mechanism. You can also ask an Agent to start with `cordis-plugin-development/SKILL.md` and read the relevant references and templates as needed.

These skills originally run in DSH's creator mode. The complete workflow uses DSH's `cordis_inspect_list`, `cordis_inspect_query`, and `plugin_manager` tools to inspect actual APIs, install bundles, and verify results.

In other development tools, the documentation and templates can guide plugin development, but importing the skills does not provide those DSH tools. Runtime inspection, installation, and verification require a connection to the target DSH environment or adaptation to the capabilities of your development tool. Interpret the original profile, permission, and Desktop `app.asar` access conventions in the context of your environment.

## Upstream source

- Project: [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)
- Original directory: [packages/preset/agent-preset/skills](https://github.com/deepseek-ai/deepseek-harness/tree/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159/packages/preset/agent-preset/skills)
- Source commit: [`fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159`](https://github.com/deepseek-ai/deepseek-harness/commit/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159)
- Reorganized on: 2026-11-05

This directory contains the runtime skill resources used by the official creator mode. The loading path can be checked in the official [cordis preset configuration](https://github.com/deepseek-ai/deepseek-harness/blob/fcc0ad462172522aaf5c93a7b2e01f6b9f0b0159/packages/bundle/web-app/presets/cordis.patch.yml#L122-L138).

[SOURCE.json](SOURCE.json) records the source, file mappings, Git blob SHA-1 values, and SHA-256 hashes. Every skill file remains byte-for-byte identical to the pinned upstream commit. This repository only changes the outer directory layout and accompanying documentation; automatic synchronization with future upstream changes is not guaranteed.

## Integrity check

Run from the repository root:

```sh
shasum -a 256 -c SHA256SUMS
```

## License

Distributed under the upstream [MIT License](LICENSE), retaining `Copyright (c) 2026 DeepSeek` and the complete license text.
