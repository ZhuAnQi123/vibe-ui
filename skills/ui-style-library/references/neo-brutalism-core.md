---
id: neo-brutalism-core
name: Neo-Brutalism Core
cover_image: ""
domain: ["创意产品", "作品集", "教育工具", "独立开发者"]
aesthetic: ["新粗野主义", "粗黑描边", "硬阴影", "高饱和色块"]
color_scheme: "Light"
website: "https://brutalistwebsites.com/"
description: >
  Neo-Brutalism Core 用粗重黑色边框、高饱和纯色、无模糊硬阴影和直白强势的排版打破传统精致感。它看起来直接、叛逆、像可点击的实体拼贴，适合需要强个性、强记忆点和年轻化表达的界面。触发词：neo-brutalism, thick black borders, hard shadows, high saturation colors, bold stark typography
---

# Neo-Brutalism Core UI 规范说明书

## 1. Overview (概览)

- **核心基调**：叛逆、直接、粗粝、年轻、强视觉冲击。
- **视觉特征**：2-4px 黑色粗描边、无模糊硬阴影、高饱和背景色、粗体标题、可见网格拼贴。
- **适用场景**：创意工具、教育游戏、个人品牌、独立开发者落地页、活动页。
- **不适用场景**：医疗、银行、政企、需要安静信任感或高级克制感的品牌。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：默认 `rounded-none` 或 `rounded-md`，也可用 `rounded-2xl` 制造玩具感，但必须搭配粗边框。
- **阴影策略 (Shadow)**：使用硬阴影 `shadow-[6px_6px_0px_0px_#000000]`，禁止模糊阴影。
- **边框策略 (Border)**：核心组件使用 `border-2 border-black` 或 `border-4 border-black`。
- **间距与留白 (Spacing)**：模块使用 `p-6 md:p-8`，Section 可用 `py-20 md:py-28`，元素排布可以紧凑但必须清楚。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#FFDD00` - 明亮黄色，用于主卡片、CTA 或重点背景。
- **Background/Canvas (画布背景)**：`#F5F0E8` - 复古纸面背景。
- **Surface (容器背景)**：`#FFFFFF` - 内容卡片底色。
- **Border/Hairline (线条/描边)**：`#000000` - 所有主要边框和硬阴影。
- **Text/Ink (主要文本)**：`#000000` - 标题和正文。
- **Muted (弱化文本)**：`#4B4B4B` - 次级说明。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：标题使用粗黑字重，示例：`font-black uppercase tracking-tight leading-none text-black`。
- **正文字体 (Body)**：正文可使用系统无衬线或等宽字体，示例：`font-bold leading-snug text-black`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div class="border-4 border-black bg-[#FFDD00] p-8 shadow-[8px_8px_0px_0px_#000000]">
  <span class="inline-block border-2 border-black bg-white px-3 py-1 font-mono text-xs font-bold uppercase">New drop</span>
  <h3 class="mt-6 text-5xl font-black uppercase leading-none tracking-tight text-black">Build loud. Ship fast.</h3>
  <p class="mt-4 max-w-md text-lg font-bold leading-snug text-black">Use thick outlines, hard shadows, and saturated blocks to make every interaction feel physical.</p>
  <button class="mt-8 border-2 border-black bg-white px-6 py-3 font-black uppercase shadow-[4px_4px_0px_0px_#000000] transition hover:translate-x-1 hover:translate-y-1 hover:shadow-none">Smash it</button>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：可以大胆拥挤，但必须保持清晰块面。用粗边框把区域切开，用高饱和色块制造节奏。

## 7. Elevation & Depth (层级与深度)

- 只使用硬边错位投影和纯色块叠放表达层级，阴影必须无模糊、像印刷套色一样直接。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：使用粗黑边框、硬阴影、全大写标题、高饱和纯色。
- **Don't**：不要使用柔和玻璃、低对比粉彩、细腻弥散阴影或过度圆润的 SaaS 卡片感。
