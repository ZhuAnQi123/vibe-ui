---
id: organic-soft-minimalism
name: Organic Soft Minimalism
cover_image: ""
domain: ["健康生活", "习惯养成", "笔记工具", "情绪价值产品"]
aesthetic: ["有机极简", "柔和 UI", "低饱和渐变", "治愈科技感"]
color_scheme: "Light"
website: "https://gumroad.com/"
description: >
  Organic Soft Minimalism 用暖中性色、低饱和粉彩、超大圆角和柔和渐变建立平静、亲近、无压力的界面气质。它弱化硬朗边界与强对比，用温柔的留白、圆润容器和轻盈排版传达治愈、专注和可信赖的情绪。触发词：organic minimalism, soft UI, pastel gradients, warm neutral background, calm tech, rounded aesthetic
---

# Organic Soft Minimalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：温暖、治愈、安静、低压力。
- **视觉特征**：暖米色背景、粉彩渐变、超大圆角、低对比细线、柔软留白。
- **适用场景**：习惯打卡、心理健康、日程管理、女性向消费产品、AI 陪伴或知识工具。
- **不适用场景**：金融交易、重度开发者工具、竞技游戏、需要强警示感的后台系统。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：大量使用 `rounded-3xl`、`rounded-[2rem]` 和 `rounded-full`，避免 `rounded-none`。
- **阴影策略 (Shadow)**：使用极轻柔阴影 `shadow-[0_18px_60px_rgba(120,90,70,0.10)]`，不要使用硬阴影。
- **边框策略 (Border)**：使用 `border border-white/70` 或 `border-[#E8DDD2]`，让边界几乎融入背景。
- **间距与留白 (Spacing)**：采用舒缓节奏，Section 使用 `py-20 md:py-28`，卡片使用 `p-7 md:p-10`，元素间使用 `space-y-5`。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#D98F75` - 用于 CTA、图标高亮和温暖强调。
- **Background/Canvas (画布背景)**：`#F7F1E8` - 暖米色大面积底色。
- **Surface (容器背景)**：`#FFFDF8` - 柔和白色卡片底。
- **Border/Hairline (线条/描边)**：`#E8DDD2` - 低对比容器边界。
- **Text/Ink (主要文本)**：`#2F2A25` - 温暖深棕黑文本。
- **Muted (弱化文本)**：`#8B7E73` - 说明文本和辅助信息。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：标题应柔和但清晰，使用 `font-semibold tracking-tight leading-tight text-[#2F2A25]`，避免过度粗黑。
- **正文字体 (Body)**：正文使用 `text-base leading-relaxed text-[#8B7E73]`，保持慢节奏阅读感。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div class="rounded-[2rem] border border-[#E8DDD2] bg-[#FFFDF8] p-8 shadow-[0_18px_60px_rgba(120,90,70,0.10)]">
  <div class="mb-6 h-28 rounded-[1.5rem] bg-gradient-to-br from-[#F8C8B8] via-[#F6E4B8] to-[#CDE7D8]"></div>
  <span class="rounded-full bg-[#F7F1E8] px-4 py-2 text-sm font-medium text-[#D98F75]">Today</span>
  <h3 class="mt-5 text-3xl font-semibold tracking-tight text-[#2F2A25]">A calmer way to keep momentum.</h3>
  <p class="mt-4 leading-relaxed text-[#8B7E73]">Use soft surfaces, warm neutrals, and gentle gradients to reduce visual pressure.</p>
  <button class="mt-8 rounded-full bg-[#D98F75] px-6 py-3 font-semibold text-white transition hover:scale-[1.02]">Start gently</button>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：保持充足呼吸感，模块之间像漂浮在暖色画布上，不要压缩成工具后台式密度。

## 7. Elevation & Depth (层级与深度)

- 用柔和阴影、浅色边界和渐变色块表达深度。层级应像纸张轻轻叠放，而不是硬朗悬浮。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：使用低饱和颜色、圆润容器、轻柔渐变和温暖文字色。
- **Don't**：不要使用纯黑高对比、荧光色、锐利直角、强烈霓虹或厚重阴影。
