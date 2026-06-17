---
id: ultra-minimalist-swiss-design
name: Ultra-Minimalist Swiss Design
name_zh: "超极简瑞士设计体系"
cover_image: "../assets/apracticeforeverydaylife.webp"
domain: ["作品集", "建筑设计", "高端品牌", "编辑内容"]
aesthetic: ["绝对极简", "Swiss design", "黑白灰", "网格排版"]
color_scheme: "Light"
website: "https://apracticeforeverydaylife.com/"
description: >
  Ultra-Minimalist Swiss Design 以大量留白、严格网格、黑白灰配色和强排版秩序建立克制、理性、永不过时的界面气质。它拒绝装饰性边框、复杂渐变和多余阴影，让文字尺度、对齐关系和空间比例成为主要视觉表达。触发词：ultra-minimalist, Swiss design, huge typography, lots of white space, monochromatic, grid-based typography
---

# Ultra-Minimalist Swiss Design UI 规范说明书

## 1. Overview (概览)

- **核心基调**：克制、理性、冷静、高级、精确。
- **视觉特征**：大面积留白、黑白灰单色系统、超大排版、严格左对齐、几乎无装饰。
- **适用场景**：建筑事务所、设计作品集、高端顾问、艺术展览、极简产品落地页。
- **不适用场景**：需要强情绪色彩的娱乐产品、儿童应用、复杂后台和高密度数据看板。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：默认使用 `rounded-none`，必要卡片最多使用 `rounded-sm`。
- **阴影策略 (Shadow)**：完全不使用阴影，使用 `shadow-none`。
- **边框策略 (Border)**：仅使用细线 `border-t border-black` 或 `border-neutral-200` 做结构分割。
- **间距与留白 (Spacing)**：Section 使用 `py-28 md:py-40`，网格使用 `gap-8 md:gap-16`，容器最大宽度使用 `max-w-7xl`。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#000000` - 标题、CTA 和关键线条。
- **Background/Canvas (画布背景)**：`#FAFAF7` - 轻微暖调白色画布。
- **Surface (容器背景)**：`#FFFFFF` - 内容块背景，尽量少用独立卡片。
- **Border/Hairline (线条/描边)**：`#D4D4D4` - 辅助分割线。
- **Text/Ink (主要文本)**：`#111111` - 主文本。
- **Muted (弱化文本)**：`#737373` - 说明文字和元信息。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：使用巨大无衬线标题，示例：`text-6xl md:text-9xl font-semibold tracking-[-0.08em] leading-[0.9] text-[#111111]`。
- **正文字体 (Body)**：正文使用 `text-base md:text-lg leading-relaxed text-[#737373]`，保持清晰和节制。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<section class="bg-[#FAFAF7] px-6 py-32 text-[#111111]">
  <div class="mx-auto grid max-w-7xl gap-16 md:grid-cols-12">
    <p
      class="border-t border-black pt-4 text-sm uppercase tracking-wide md:col-span-3"
    >
      Selected System
    </p>
    <div class="md:col-span-9">
      <h1
        class="text-6xl font-semibold leading-[0.9] tracking-[-0.08em] md:text-9xl"
      >
        Less interface. More intent.
      </h1>
      <p class="mt-10 max-w-2xl text-lg leading-relaxed text-[#737373]">
        Use scale, alignment, and whitespace as the entire visual system.
      </p>
      <button
        class="mt-12 border border-black px-8 py-4 text-sm font-medium uppercase tracking-wide transition hover:bg-black hover:text-white"
      >
        View index
      </button>
    </div>
  </div>
</section>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：留白是主要视觉材料。让内容之间有明显距离，避免用卡片、阴影或装饰填满空间。

## 7. Elevation & Depth (层级与深度)

- 不使用三维层级。靠字号、网格位置、黑白对比和分割线建立信息层级。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：使用严格对齐、大字号、单色系统和极少元素。
- **Don't**：不要使用多彩渐变、玻璃拟态、复杂插画、厚重阴影或花哨动效。
