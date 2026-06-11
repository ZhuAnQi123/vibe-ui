---
version: alpha
name: style-name-analysis
description: >
  详细描述该风格的情绪基调、核心特点、关键色彩策略和排版原则。
  这段描述会被注入到 AI 的 prompt 中，对 AI 把握整体氛围非常重要。
  例如：“这是一种安静、内敛的开发者工具风格，使用米色背景和暖黑色文字，排版带有杂志感...”
  触发词：[填入触发词，如 Tiimo、有机极简等]

# 以下是结构化的 Design Tokens（供 AI 直接读取应用）
colors:
  primary: "#hex"
  primary-active: "#hex"
  ink: "#hex"
  body: "#hex"
  muted: "#hex"
  canvas: "#hex"
  surface-card: "#hex"
  hairline: "#hex"

typography:
  display-lg:
    fontFamily: "..."
    fontSize: 36px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.02em
  body-md:
    fontFamily: "..."
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0

rounded:
  none: 0px
  sm: 4px
  md: 8px
  lg: 12px
  pill: 9999px

spacing:
  xs: 8px
  sm: 12px
  base: 16px
  md: 24px
  lg: 32px
  section: 80px

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.canvas}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "8px 16px"
---

# [风格名称] UI 规范

> 本规范参考 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 结构，包含可被 AI 严格执行的结构化 Tokens 与设计原则。

## 1. Overview (概览)
- **核心基调**：[例如：冷静的开发者工具、治愈系手账、高端奢侈品等]
- **视觉特征**：[列出 3-5 点最核心的特征，如是否用阴影、线条粗细、饱和度等]
- **适用场景**：[什么产品类型最适合]
- **不适用**：[什么场景不要用]

## 2. Colors (色彩系统)
### Brand & Accent (品牌与点缀色)
- **[颜色名]** (`{colors.primary}` — #hex)：[使用场景说明]

### Surface (表面与背景色)
- **[背景色名]** (`{colors.canvas}` — #hex)：[使用场景说明]
- **[卡片色名]** (`{colors.surface-card}` — #hex)：[使用场景说明]

### Text & Lines (文本与线条)
- **[主文本色]** (`{colors.ink}` — #hex)：[使用场景说明]
- **[分隔线]** (`{colors.hairline}` — #hex)：[使用场景说明]

## 3. Typography (排版系统)
### Font Family (字体族)
- **主字体**：[如 Inter, Roboto, 或某款展示型字体]
- **等宽字体**：[如 JetBrains Mono]

### Hierarchy (层级)
| Token | Size | Weight | Line Height | Letter Spacing | Use |
|---|---|---|---|---|---|
| `{typography.display-lg}` | 36px | 600 | 1.2 | -0.02em | 页面大标题 |
| `{typography.body-md}` | 16px | 400 | 1.5 | 0 | 默认正文 |

### Principles (排版原则)
- [如：标题不用粗体、正文字号偏小、负字距等]

## 4. Layout & Spacing (布局与空间)
### Spacing System (间距系统)
- **Base unit (基准单位)**: [如 4px 或 8px]
- **Section padding (区块间距)**: [如 80px]

### Whitespace Philosophy (留白理念)
- [如：紧凑的仪表盘数据流风格，或是呼吸感极强的杂志留白排版]

## 5. Elevation & Depth (层级与深度)
> 描述元素悬浮或层次的表达方式（如阴影、纯线条、色块层叠）。

| Level | Treatment | Use |
|---|---|---|
| Flat | `{colors.canvas}` | 页面底色 |
| Card | 1px border `{colors.hairline}` | 内容卡片，无阴影 |
| Floating | Drop shadow `0 4px 12px rgba(...)` | 弹窗、下拉菜单 |

## 6. Shapes (形态与圆角)
| Token | Value | Use |
|---|---|---|
| `{rounded.sm}` | 4px | 小标签、Badge |
| `{rounded.md}` | 8px | 核心操作按钮、输入框 |
| `{rounded.lg}` | 12px | 内容卡片主体 |

## 7. Components (核心组件模式)
### Buttons (按钮)
- **Primary**：背景 `{colors.primary}`，圆角 `{rounded.md}`，文字反白。
- **Secondary**：背景透明，边框 1px `{colors.hairline}`，文字 `{colors.ink}`。

### Cards (卡片)
- **Feature Card**：内边距 24px，无阴影，带边框。

### Animations / Micro-interactions (动效与微交互)
- **时长与缓动**：[如 300ms ease-out]
- **关键反馈**：[如 点击时的缩放、加载动画特点]

## 8. Do's and Don'ts (设计禁忌)
### Do
- [坚持使用什么]
- [推荐什么]

### Don't
- [绝对不能用纯黑纯白]
- [不要使用超过 2 种点缀色]
- [不要叠加多层阴影]

## 9. Responsive & Accessibility (响应式与无障碍)
### Breakpoints (断点)
| Name | Width | Key Changes |
|---|---|---|
| Mobile | < 640px | 布局折叠、大字号缩小、导航收起为汉堡菜单 |

### Accessibility (可访问性)
- 动效降级：如何处理 `prefers-reduced-motion`（如关闭弹簧动效）
- 色彩对比度：核心内容要求 ≥ 4.5:1
