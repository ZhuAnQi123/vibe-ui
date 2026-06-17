---
id: spatial-glass-ui
name: Spatial Glass UI
cover_image: ""
domain: ["AI 工具", "媒体应用", "沉浸式产品", "高级控制面板"]
aesthetic: ["空间 UI", "玻璃态", "VisionOS style", "半透明层级"]
color_scheme: "Dark"
website: "https://www.apple.com.cn/os/macos/"
description: >
  Spatial Glass UI 通过磨砂玻璃、多层半透明容器、细白边框和柔和光晕制造物理空间中的悬浮层级感。它强调背景深度、透光材质、轻微折射和克制的动态反馈，适合营造高端、沉浸、未来感界面。触发词：spatial UI, VisionOS style, frosted glass, deep background blur, translucent layers, thin white borders
---

# Spatial Glass UI 规范说明书

## 1. Overview (概览)

- **核心基调**：沉浸、高级、未来、轻盈悬浮。
- **视觉特征**：磨砂玻璃背景、多层半透明面板、1px 高光边框、背景光斑、柔和景深。
- **适用场景**：AI 控制台、媒体播放器、浮窗面板、空间计算概念页、复杂设置面板。
- **不适用场景**：低性能移动页面、极强可读性要求的长表格、印刷感品牌页。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：使用 `rounded-3xl`、`rounded-[2rem]`，浮窗可用 `rounded-[2.5rem]`。
- **阴影策略 (Shadow)**：使用大范围柔和阴影 `shadow-[0_30px_100px_rgba(0,0,0,0.35)]` 搭配内高光。
- **边框策略 (Border)**：使用 `border border-white/20` 和 `ring-1 ring-white/10` 创建玻璃边缘。
- **间距与留白 (Spacing)**：面板内部使用 `p-6 md:p-8`，悬浮元素之间使用 `gap-4 md:gap-6`，避免过密。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#A5B4FC` - 用于光晕、选中态和重要按钮。
- **Background/Canvas (画布背景)**：`#080B16` - 深色空间背景。
- **Surface (容器背景)**：`#FFFFFF1A` - 半透明玻璃容器，Tailwind 可写 `bg-white/10`。
- **Border/Hairline (线条/描边)**：`#FFFFFF33` - 玻璃高光边框。
- **Text/Ink (主要文本)**：`#F8FAFC` - 深色玻璃上的主文本。
- **Muted (弱化文本)**：`#CBD5E1` - 辅助说明和标签。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：使用轻盈现代无衬线，示例：`font-semibold tracking-tight leading-tight text-white`。
- **正文字体 (Body)**：使用 `text-sm md:text-base leading-relaxed text-slate-300`，避免过细导致玻璃背景上不可读。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div class="relative overflow-hidden rounded-[2.5rem] bg-[#080B16] p-8">
  <div class="absolute -left-24 -top-24 h-72 w-72 rounded-full bg-[#A5B4FC]/30 blur-3xl"></div>
  <div class="absolute -bottom-28 right-0 h-80 w-80 rounded-full bg-cyan-400/20 blur-3xl"></div>
  <div class="relative rounded-[2rem] border border-white/20 bg-white/10 p-8 shadow-[0_30px_100px_rgba(0,0,0,0.35)] backdrop-blur-2xl ring-1 ring-white/10">
    <span class="text-sm font-medium text-[#A5B4FC]">Spatial Panel</span>
    <h3 class="mt-4 text-4xl font-semibold tracking-tight text-white">Control floats above the canvas.</h3>
    <p class="mt-4 leading-relaxed text-slate-300">Layer translucent surfaces with soft background glow and thin white highlights.</p>
    <button class="mt-8 rounded-full border border-white/20 bg-white/15 px-6 py-3 font-medium text-white backdrop-blur-xl transition hover:bg-white/25">Open panel</button>
  </div>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：元素应像浮在空间里，面板之间保留明确空气感，背景需要有可见但不抢眼的深度线索。

## 7. Elevation & Depth (层级与深度)

- 通过 `backdrop-blur-2xl`、半透明背景、细边框、背景光斑和大范围阴影叠加表达深度。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：保持玻璃透明度、边缘高光和背景景深之间的平衡。
- **Don't**：不要在玻璃层上放低对比文字；不要叠加过多彩色光斑导致廉价霓虹感。
