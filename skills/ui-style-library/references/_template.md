---
id: [如 tiimo-organic-minimalism]
name: [风格官方名称]
name_zh: "[中文展示标题，可选]"
cover_image: "../assets/your-image-name.png"
# 例如 移动应用，品牌官网 等
domain: ["行业标签1", "行业标签2"]
# 例如 情绪价值产品 等
aesthetic: ["风格标签1", "风格标签2"]
color_scheme: "Light/Dark/Auto"
website: [原设计来源网站 URL]
description: >
  详细描述该风格的情绪基调、核心特点、关键色彩策略和排版原则。
  这段描述会被注入到 AI 的 prompt 中，对 AI 把握整体氛围非常重要。
  触发词：[填入触发词]
---

# [风格官方名称] UI 规范说明书

## 1. Overview (概览)

- **核心基调**：[例如：安静内敛、张扬叛逆、温暖治愈]
- **视觉特征**：[列出 3-4 个核心视觉视觉锚点，如：2px 纯黑描边、杂志感留白、像素网格]
- **适用场景**：[推荐应用的业态]
- **不适用场景**：[极度不推荐应用的边界]

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：[如：使用 `rounded-2xl` 或 `rounded-3xl`，不要使用 `rounded-sm`]
- **阴影策略 (Shadow)**：[如：使用 `shadow-[0_8px_30px_rgb(0,0,0,0.04)]` 来实现弥散阴影，或完全不使用阴影]
- **边框策略 (Border)**：[如：使用 `border-2 border-black` 来实现粗野主义描边]
- **间距与留白 (Spacing)**：[如：Section 之间使用 `gap-16` 或 `gap-24`]

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#HexCode` - [用途说明]
- **Background/Canvas (画布背景)**：`#HexCode` - [用途说明，如：大面积底色]
- **Surface (容器背景)**：`#HexCode` - [用途说明，如：卡片底色]
- **Border/Hairline (线条/描边)**：`#HexCode` - [用途说明]
- **Text/Ink (主要文本)**：`#HexCode` - [用途说明]
- **Muted (弱化文本)**：`#HexCode` - [用途说明]

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：[大标题的字体选型与间距压缩原则，如：使用 `font-black tracking-tighter leading-none`]
- **正文字体 (Body)**：[正文可读性保障，如：使用 `font-medium leading-relaxed`]

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<!-- 示例：一个标准的 [风格名称] 按钮 -->
<button class="bg-[#FF4500] text-[#F4F1EA] px-7 py-3 rounded-xl font-bold tracking-tight border-2 border-[#1A1A1A] hover:-translate-y-1 transition-transform">
  Let's Bond
</button>

<!-- 示例：一个标准的 [风格名称] 卡片 -->
<div class="bg-white rounded-3xl p-8 shadow-[0_8px_30px_rgb(0,0,0,0.04)] border border-gray-100">
  <h3 class="text-2xl font-bold text-gray-900 mb-2">Card Title</h3>
  <p class="text-gray-500 leading-relaxed">Card description goes here.</p>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：[如：紧凑的仪表盘数据流风格，或是呼吸感极强的杂志留白排版]

## 7. Elevation & Depth (层级与深度)

[描述元素悬浮或层次的表达方式，如：不使用阴影、仅靠纯色块层叠、或使用硬核 3D 错位投影]

## 8. Do's and Don'ts (设计禁忌)

- **Do**：[必须坚持的做法]
- **Don't**：[绝对不能犯的视觉错误]
