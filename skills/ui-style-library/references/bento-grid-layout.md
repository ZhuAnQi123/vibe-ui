---
id: bento-grid-layout
name: Bento Grid Layout
cover_image: "../assets/notion.webp"
domain: ["SaaS", "产品展示", "仪表盘", "个人主页"]
aesthetic: ["便当盒布局", "模块化网格", "Apple-like widgets", "整洁信息架构"]
color_scheme: "Light"
website: "https://www.notion.com/"
description: >
  Bento Grid Layout 是一种将内容拆分为严格对齐、大小错落的圆角矩形模块的 UI 风格。它强调清晰的信息层级、稳定的网格节奏和高度可扫描的卡片化结构，适合把多个功能、数据或卖点组织成像日本便当盒一样紧凑但有秩序的界面。触发词：bento grid layout, bento box layout, rounded distinct cards, strict grid alignment, Apple-like widgets, modular dashboard UI
---

# Bento Grid Layout UI 规范说明书

## 1. Overview (概览)

- **核心基调**：整洁、理性、高级、产品感强，像精心排列的现代 SaaS 或 Apple 小组件界面。
- **视觉特征**：严格网格对齐、大小不一的圆角卡片、统一间距系统、清晰的图标/数据/文案层级。
- **适用场景**：SaaS 落地页、数据看板、个人主页、功能介绍页、AI 产品能力展示页。
- **不适用场景**：强叙事长文页面、需要高度随机感或艺术破坏性的品牌视觉、密集表格后台。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：卡片使用 `rounded-3xl` 或 `rounded-[2rem]`，内部小元素使用 `rounded-2xl`，避免尖锐直角。
- **阴影策略 (Shadow)**：使用轻微扩散阴影 `shadow-[0_16px_50px_rgba(15,23,42,0.08)]`，避免厚重硬阴影。
- **边框策略 (Border)**：使用 `border border-slate-200/80` 或深色模式下 `border-white/10` 强化模块边界。
- **间距与留白 (Spacing)**：网格使用 `grid gap-4 md:gap-6`，卡片内使用 `p-6 md:p-8`，Section 外围使用 `py-20 md:py-28`。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#2563EB` - 用于 CTA、关键数据、选中态和重点图标。
- **Background/Canvas (画布背景)**：`#F8FAFC` - 大面积浅冷灰背景，保持科技产品感。
- **Surface (容器背景)**：`#FFFFFF` - 卡片和模块主底色。
- **Border/Hairline (线条/描边)**：`#E2E8F0` - 卡片边界、分割线和小组件轮廓。
- **Text/Ink (主要文本)**：`#0F172A` - 标题和核心数据文本。
- **Muted (弱化文本)**：`#64748B` - 说明文字、标签和辅助指标。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：使用现代无衬线粗字重，强调清晰层级。示例：`font-bold tracking-tight leading-none text-slate-950`。
- **正文字体 (Body)**：正文保持紧凑可读。示例：`text-sm md:text-base leading-relaxed text-slate-500`。
- **数据字体 (Metrics)**：数据和短标签可使用 `font-semibold tabular-nums tracking-tight`，保证看板式稳定感。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<section class="bg-[#F8FAFC] py-24 px-6">
  <div class="mx-auto grid max-w-6xl grid-cols-1 gap-5 md:grid-cols-4">
    <div class="rounded-[2rem] border border-[#E2E8F0] bg-white p-8 shadow-[0_16px_50px_rgba(15,23,42,0.08)] md:col-span-2 md:row-span-2">
      <span class="text-sm font-semibold text-[#2563EB]">Analytics</span>
      <h3 class="mt-4 text-4xl font-bold tracking-tight text-[#0F172A]">One grid for every signal.</h3>
      <p class="mt-4 max-w-md text-base leading-relaxed text-[#64748B]">Group metrics, actions, and summaries into distinct rounded modules.</p>
    </div>
    <div class="rounded-[2rem] border border-[#E2E8F0] bg-white p-6">
      <p class="text-sm text-[#64748B]">Revenue</p>
      <p class="mt-3 text-3xl font-bold tabular-nums text-[#0F172A]">$48.2K</p>
    </div>
    <div class="rounded-[2rem] border border-[#E2E8F0] bg-[#2563EB] p-6 text-white">
      <p class="text-sm text-white/70">Active users</p>
      <p class="mt-3 text-3xl font-bold tabular-nums">12,408</p>
    </div>
  </div>
</section>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：页面整体保持宽松，模块内部保持紧凑。用大小不同的卡片承载层级，而不是靠杂乱装饰制造变化。

## 7. Elevation & Depth (层级与深度)

- 主要依靠卡片尺寸、背景色差、轻边框和柔和阴影建立层级。重要模块可以跨列跨行，次要模块保持标准尺寸。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：坚持统一的 `gap`、统一圆角半径和严格网格线；让每张卡片只承载一个明确主题。
- **Don't**：不要随意错位、旋转卡片或混用过多圆角；不要把所有卡片做成同等视觉权重。
