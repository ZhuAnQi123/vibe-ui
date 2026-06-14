# Vibe UI

**UI Design Systems, Translated for AI.**

Vibe UI 是一个专为 AI 辅助编程（Vibe Coding）打造的开源设计风格库。它将各大顶级产品的视觉风格、小众创意设计，转换成了 AI（如 Cursor, Windsurf, Claude, GPT-4）能直接读懂并完美执行的纯文本设计说明书（Prompt/Skill）。

## 🌟 为什么需要 Vibe UI？

在使用 AI 编程时，AI 写逻辑很强，但默认生成的 UI 往往是千篇一律的“默认 Tailwind 风”或“Bootstrap 风”。如果你只给 AI 模糊的提示（如“好看一点”、“极简风”），生成的界面通常不尽如人意。

Vibe UI 通过提供**结构化的 Design Tokens** 和**硬核的工程约束**（具象化的 Tailwind 字典、色彩变量映射、基准组件示例），让 AI 能够“一键注入设计灵魂”，完美还原你想要的视觉氛围。

## 📂 目录结构

本库采用 **Cursor Skill 标准结构**：扁平 `references/` + YAML 元数据标签，与 [vibe-motion-md](https://github.com) 动效库保持一致，方便脚本生成 catalog 并供 [vibe-ui-web](https://github.com) 线上展示。

文件命名规范：`[产品名]-[核心风格].md`

```text
vibe-ui/
└── skills/
    └── ui-style-library/
        ├── SKILL.md                              # 路由大脑：风格索引与输出模板
        ├── assets/                               # 风格预览图 / 截图（可选）
        └── references/
            ├── copula-neo-brutalism.md           # 创意代理商 / 新粗野主义
            ├── tiimo-organic-minimalism.md       # 医疗健康 / 有机极简主义
            ├── units-playful-brutalism.md        # 青年社区 / 趣味粗野主义
            └── _template.md                      # 风格文件贡献模板
```

## 🚀 如何使用

1. 下载本仓库中的 `skills/ui-style-library` 文件夹。
2. 将其复制到你项目的 `.cursor/skills/` 目录下（没有则新建）。
3. 在 Cursor 聊天框中 @ `SKILL.md` 或具体 reference 文件，例如：“按 Tiimo 有机极简风格实现这个页面。”
4. 也可以只复制某个 `references/*.md` 的内容，作为独立 Prompt 发给 AI。

## 🛠️ 贡献指南

我们非常欢迎你提交自己发现的小众风格和调优好的 prompt！

1. 复制 `skills/ui-style-library/references/_template.md`。
2. 按照 `[产品名]-[核心风格].md` 的规范重命名并放入 `references/`。
3. 填写顶部的 YAML 元数据（`id`、`domain`、`aesthetic`、触发词等）。
4. 严格按照模板提供**具象化的 Tailwind 字典**、**色彩变量映射**和**基准组件示例**。
5. 在 `SKILL.md` 的「风格索引」表中追加一行。
6. 提交 Pull Request。

## 💡 核心设计原则

- **视觉展示给人看，精准 Token 给机器看**。
- 拒绝模糊形容词，用具体的 Tailwind 类名和 Hex 色值约束 AI。
- 提供基准组件（Anchor Component），利用 AI 强大的上下文模仿能力推导全局风格。

---

*Built for the Vibe Coders.*
