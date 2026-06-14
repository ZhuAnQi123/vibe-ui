# Vibe UI

**UI Design Systems, Translated for AI.**

Vibe UI 是一个专为 AI 辅助编程（Vibe Coding）打造的开源设计风格库。它将各大顶级产品的视觉风格、小众创意设计，转换成了 AI（如 Cursor, Windsurf, Claude, GPT-4）能直接读懂并完美执行的纯文本设计说明书（Prompt/Skill）。

## 🌟 为什么需要 Vibe UI？

在使用 AI 编程时，AI 写逻辑很强，但默认生成的 UI 往往是千篇一律的“默认 Tailwind 风”或“Bootstrap 风”。如果你只给 AI 模糊的提示（如“好看一点”、“极简风”），生成的界面通常不尽如人意。

Vibe UI 通过提供**结构化的 Design Tokens** 和**硬核的工程约束**（具象化的 Tailwind 字典、色彩变量映射、基准组件示例），让 AI 能够“一键注入设计灵魂”，完美还原你想要的视觉氛围。

## 📂 目录结构

所有的风格文件统一存放在 `/library` 目录下。我们采用扁平化存储 + 元数据标签（Metadata Tags）的方式进行管理，方便后续通过脚本生成多维度的筛选器。

文件命名规范：`[产品名]-[核心风格].md`

```text
vibe-ui/
├── library/
│   ├── copula-neo-brutalism.md       # 创意代理商 / 新粗野主义
│   ├── tiimo-organic-minimalism.md   # 医疗健康 / 有机极简主义
│   └── units-playful-brutalism.md    # 青年社区 / 趣味粗野主义
├── _template.md                      # 风格文件贡献模板
└── requirement.md                    # 产品需求文档 (PRD)
```

## 🚀 如何使用

1. 在 `/library` 目录中寻找你喜欢的风格。
2. 复制对应 `.md` 文件中的内容。
3. 将内容粘贴到你的 Cursor 的 `.cursorrules` 文件中，或者作为独立指令发送给 AI。
4. 让 AI 开始为你生成带有该设计灵魂的代码！

## 🛠️ 贡献指南

我们非常欢迎你提交自己发现的小众风格和调优好的 prompt！

1. 复制根目录下的 `_template.md` 文件。
2. 按照 `[产品名]-[核心风格].md` 的规范重命名。
3. 填写顶部的 YAML 元数据（领域、风格、触发词等）。
4. 严格按照模板中的要求，提供**具象化的 Tailwind 字典**、**色彩变量映射**和**基准组件示例**。
5. 提交 Pull Request。

## 💡 核心设计原则

- **视觉展示给人看，精准 Token 给机器看**。
- 拒绝模糊形容词，用具体的 Tailwind 类名和 Hex 色值约束 AI。
- 提供基准组件（Anchor Component），利用 AI 强大的上下文模仿能力推导全局风格。

---

*Built for the Vibe Coders.*
