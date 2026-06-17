---
id: copula-neo-brutalism
name: Copula Agency Bold Neo-Brutalism
name_zh: "Copula 高饱和新粗野主义"
cover_image: "../assets/copula.webp"
domain: ["Agency", "Portfolio", "Creative"]
aesthetic: ["Neo-Brutalism", "High Contrast", "Bold"]
color_scheme: "Light"
website: https://copula.agency/contact
description: >
  这是一种充满活力、高冲击力的创意代理商风格（Neo-Brutalism 的现代变体）。它通过极具视觉侵略性的高饱和度朱红与群青蓝，搭配温和的米白色进行大块面的色彩撞击。排版极具杂志感与街头感，采用超粗、紧凑的无衬线压缩字体作为视觉核心。整体情绪基调自信、张扬、具有现代创意的先锋感，打破了传统扁平化设计的沉闷，适合需要强烈品牌个性和情感连接的创意机构、数字化工作室或潮流品牌。
  触发词：Copula、高饱和撞色、新粗野主义、先锋创意
---

# Copula Agency Bold Neo-Brutalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：张扬个性的创意代理商风格、现代新粗野主义（Neo-Brutalism）变体、高情绪价值。
- **视觉特征**：极端对比、高压排版、特色图形、硬核极简（1px 炭黑细线描边）。
- **适用场景**：数字创意机构官网、艺术家个人作品集、潮流时尚品牌、先锋设计工作室。
- **不适用场景**：严肃的企业级 SaaS 平台、医疗政务系统、需要长时间沉浸阅读的工具型产品。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：
  - 按钮/卡片：使用 `rounded-2xl` 或 `rounded-3xl`
  - 胶囊/标签：使用 `rounded-full`
  - 容器/通栏：使用 `rounded-none`
- **阴影策略 (Shadow)**：**绝对不要使用任何弥散阴影（Blur Shadow）**。完全不使用阴影，或者使用纯色硬阴影。
- **边框策略 (Border)**：使用 `border border-[#1A1A1A]` (1px) 来实现输入框和普通标签的硬朗线条。
- **间距与留白 (Spacing)**：Section 之间使用 `gap-y-[120px]` 或 `py-[120px]`，模块直接无缝硬切。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#FF4500` (Copula Red) - 核心品牌色，用于第一屏大背景、核心行动点按钮。
- **Secondary (次要主色)**：`#0000FF` (Copula Blue) - 次要撞色，用于大背景、博客卡片背景。
- **Background/Canvas (画布背景)**：`#F4F1EA` (Warm Canvas) - 核心全局背景色，带有报纸/杂志感的米白色。
- **Surface (容器背景)**：`#FFFFFF` (Pure Surface) - 用于表单输入框背景、次要卡片容器。
- **Border/Hairline (线条/描边)**：`#1A1A1A` (Brutalist Border) - 1px 的硬朗线条。
- **Text/Ink (主要文本)**：`#1A1A1A` (Ink Charcoal) - 主要文本颜色，带一点点暖调的炭黑。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：大标题使用 `font-black tracking-tighter leading-none uppercase` (如 Impact 或类似压缩超粗无衬线体)。行高必须小于 1.0，字距为负值。
- **正文字体 (Body)**：正文使用 `font-medium leading-relaxed tracking-normal` (如 Inter 或 system-ui)。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<!-- 示例：一个标准的 Copula 风格按钮 -->
<button class="bg-[#FF4500] text-[#F4F1EA] px-7 py-3 rounded-2xl font-medium tracking-normal hover:bg-[#CC3700] transition-colors">
  Let's Bond
</button>

<!-- 示例：一个标准的 Copula 风格输入框 -->
<input type="text" class="bg-[#FFFFFF] border-b border-[#1A1A1A] px-0 py-3 text-[#1A1A1A] placeholder-[#888888] focus:outline-none focus:border-b-2 transition-all" placeholder="Enter your email" />

<!-- 示例：一个标准的 Copula 风格标签 -->
<span class="bg-transparent border border-[#1A1A1A] text-[#1A1A1A] px-4 py-1.5 rounded-full text-sm font-medium">
  Creative
</span>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：采用“极端”两极化的留白。在内容展示区（如表单、正文），留白非常开阔，具有极强的呼吸感；而在纯文字视觉冲击区，字块堆叠极其紧凑。

## 7. Elevation & Depth (层级与深度)

该风格属于典型的新粗野主义平面化表达，**完全抛弃渐变与柔和阴影**，通过纯色块的覆盖关系、极具张力的超大圆角形变来表达层级。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：坚持使用大面积饱和色块（朱红、群青蓝）与柔和米白的对撞。标题必须使用全大写（Uppercase）且字距紧凑。保持线条（Border）的极致纤细（1px）。
- **Don't**：绝对不要使用任何弥散阴影（Blur Shadow）或渐变色。正文部分切勿使用 Impact 等展示型压缩字体。不要加入第三种高饱和度有色相的颜色（如明黄或翠绿）。