---
id: units-playful-brutalism
name: Units Student Housing Playful Brutalism
cover_image: "../assets/units.webp"
domain: ["Real Estate", "Community", "Youth"]
aesthetic: ["Neo-Brutalism", "Playful", "Grid"]
color_scheme: "Light"
website: https://units.gr/en/homepage/
description: >
  这是一种充满朝气、玩味十足且极具互动感的新粗野主义（Neo-Brutalism）风格。专为现代学生公寓设计，它巧妙地在报纸质感的米色画布上，通过高饱和度的电网蓝、活力黄、热烈红和香芋紫等大块纯色进行拼贴。设计融合了像素风网格、加粗的黑描边、独特的几何ICON和趣味错位动画。整体情绪基调充满活力、包容性、安全感以及社区的归属感，非常适合面向 Z 世代的青年社区、创意住宿或互动生活平台。
  触发词：Units、像素网格、大色块拼接、青春玩味、新粗野
---

# Units Student Housing Playful Brutalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：玩味十足、高互动性、专为 Z 世代打造的硬核扁平新粗野主义。
- **视觉特征**：像素与网格、左侧独立多色导航、高反差色彩积木、透视错位交互、2px 纯黑描边。
- **适用场景**：学生公寓官网、青年旅舍、联合办公空间、互动潮流品牌、潮流艺术展。
- **不适用场景**：冷淡风极简主义产品、传统房产中介、纯文字密集型的严谨资讯网站。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：
  - 核心卡片：使用 `rounded-2xl`
  - 弹窗/大透视：使用 `rounded-3xl`
  - 胶囊按钮：使用 `rounded-full`
- **阴影策略 (Shadow)**：**绝对不要使用轻薄、朦胧的灰色阴影**。完全不使用阴影，或者使用硬核纯黑偏移阴影（如 `shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]`）。
- **边框策略 (Border)**：使用 `border-2 border-black` 来实现标志性的硬核描边。
- **间距与留白 (Spacing)**：Section 之间使用 `gap-y-[100px]` 或 `py-[100px]`，模块直接无缝硬切。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#0066FF` (Electric Blue) - 代表科技、现代与年轻活力。
- **Accent Yellow (点缀黄)**：`#FFBB00` - 用于呈现特色服务、地图大色块。
- **Accent Red (点缀红)**：`#CC1111` - 多用于召唤行动（CTA）按钮。
- **Accent Purple (点缀紫)**：`#9933FF` - 次要功能、点缀色。
- **Background/Canvas (画布背景)**：`#F4EDE2` (Warm Paper) - 全局主体背景底色，略带温度的灰米色。
- **Surface (容器背景)**：`#FFFFFF` - 卡片/容器纯白。
- **Border/Hairline (线条/描边)**：`#000000` - 2px 标志性硬核描边（纯黑）。
- **Text/Ink (主要文本)**：`#000000` (Units Black) - 核心文字与结构线。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：大标题使用 `font-black tracking-tighter leading-none` (如 Inter Black 或带有独特几何切割感的无衬线字体)。
- **正文字体 (Body)**：正文使用 `font-medium leading-relaxed` (如 system-ui)。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<!-- 示例：一个标准的 Units 风格按钮 -->
<button class="bg-[#000000] text-[#FFFFFF] px-7 py-3.5 rounded-full font-medium border-2 border-[#000000] hover:bg-[#1E1E1E] transition-colors">
  Book your Unit
</button>

<!-- 示例：一个标准的 Units 风格卡片 -->
<div class="bg-[#FFFFFF] rounded-2xl p-6 border-2 border-[#000000]">
  <h3 class="text-3xl font-extrabold text-[#000000] mb-4 tracking-tight leading-tight">Our way of Living</h3>
  <p class="text-[#1E1E1E] leading-relaxed font-medium">Experience the best community life.</p>
</div>

<!-- 示例：一个多色拼接导航块 -->
<div class="bg-[#FFBB00] border-2 border-[#000000] p-4 flex items-center justify-center cursor-pointer hover:bg-[#0066FF] transition-colors">
  <span class="font-bold text-[#000000]">Community</span>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：局部极为紧凑（如左侧导航和卡片内部无缝排列），整体又通过极大的通栏大色块保证视觉上不容易迷失。典型的多栏非对称布局，不同大小的彩色卡片像俄罗斯方块一样紧密塞满屏幕。

## 7. Elevation & Depth (层级与深度)

拒绝任何伪三维的阴影和渐变，完全依赖厚重的**纯黑线条**与**高对比度纯色**进行层级区分。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：大胆使用纯黑（#000000）作为结构描边与线条。将多色拼接（黄、红、蓝、紫）与大面积米色（Canvas）相结合。允许标题中混入像素、箭头和简单的几何符号。
- **Don't**：绝对不能使用轻薄、朦胧的灰色阴影。严禁加入色彩渐变（Gradient），所有色彩表现必须是 100% 纯色。正文说明部分不要使用全大写或过粗的特粗体。