---

## id: nvrmnd-editorial-neo-brutalism

name: Neo-Brutalist Editorial
name_zh: "NVRMND 编辑感新粗野主义"
domain: ["创意设计", "数字工作室", "个人品牌", "出海独立开发者"]
aesthetic: ["新粗野主义", "先锋杂志风", "像素波普", "极高对比度"]
color_scheme: "Light"
cover_image: "../assets/nvrmndstudio.webp"
website: [https://www.nvrmndstudio.com/](https://www.nvrmndstudio.com/)
description: >
该风格融合了现代新粗野主义（Neo-Brutalism）的硬朗骨架与高端时尚杂志的排版肌理。通过极具张力的超大非衬线紧凑字体、粗重的线条分割，配合复古的低保真像素（Pixelated）交互元素和高饱和度的荧光绿/宝蓝色作为点缀，营造出一种既专业又带有些许叛逆、极具视觉冲击力的先锋数字艺术氛围。
触发词: nvrmnd-editorial-neo-brutalism style, ultra-bold typography, neo-brutalist layouts, high contrast neon accents, pixelated interactive elements

# Neo-Brutalist Editorial UI 规范说明书

## 1. Overview (概览)

- **核心基调**：张扬叛逆、先锋自信、具有极强视线侵略性的时尚杂志感。
- **视觉特征**：超大字重标题且字距极度紧凑（Tracking-tighter）、4px 粗黑边界线与网格基底、荧光绿高亮色块、低保真像素风（Pixelated）功能性文本与互动元素。
- **适用场景**：设计工作室、独立创意人作品集、极客品牌官网、极具个性化的产品落地页（Landing Page）。
- **不适用场景**：传统政企官网、医疗健康、需要提供极高安稳感和中庸信任感的理财或银行类应用。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：整体采用完全直角 `rounded-none` 或极小圆角 `rounded-sm`。但在特定交互组件（如实体优惠券卡片、门票）上可使用 `rounded-3xl` 或 `rounded-full` 形成结构冲突。
- **阴影策略 (Shadow)**：绝不使用渐变弥散阴影。若要表达层级，使用硬核无模糊的黑边错位投影 `shadow-[4px_4px_0px_0px_#000000]` 或纯色块直接层叠。
- **边框策略 (Border)**：高频使用粗线进行区域分割。使用 `border-t-2 border-black` 或 `border-b` 进行 Section 级别划分；网格系统使用细线 `border-gray-300` 形成后台草稿感。
- **间距与留白 (Spacing)**：Section 之间采用呼吸感极强的超大留白（`py-24` 至 `py-36`），但在元素组内部（如标题与副标题之间）采用极度紧凑的间距（`space-y-2` 或 `mt-1`）。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (高亮/主色)**：`#99FF00`（荧光冷绿）- 用于高光选中背景、核心行动点（CTA）悬浮反馈。
- **Secondary (次高亮)**：`#1043FF`（宝蓝色）- 用于重要功能区块底色、标签背景或特定微交互。
- **Background/Canvas (画布背景)**：`#E3E3E3` 或 `#EDEDED`（低饱和冷灰）- 模拟实体纸张或高级水泥画板大面积底色。
- **Surface (容器背景)**：`#FFFFFF`（纯白）- 用于卡片、内容主干区域，与冷灰底色形成清晰切分。
- **Border/Hairline (线条/描边)**：`#000000`（纯黑）- 用于粗分割线、文字描边或硬核投影。
- **Text/Ink (主要文本)**：`#1A1A1A`（墨黑）- 承载大标题和主视觉文案，确保绝对的高对比度。
- **Muted (弱化文本)**：`#666666`（中灰）- 用于副标题、时间戳、说明文本。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：大标题必须拥有极致的视觉压迫感。使用超重字重、极致压缩的字距与行距。示例：`font-black text-6xl md:text-8xl uppercase tracking-tighter leading-[0.85] text-[#1A1A1A]`。
- **功能交互字体 (Interactive)**：在导航菜单序号、标签、提交按钮等功能性节点上，使用像素风字体或等宽字体。示例：`font-mono font-bold tracking-widest`。
- **正文字体 (Body)**：正文需要回归理性和极高可读性，采用无衬线中文字体或现代无衬线英文字体，保障视线流畅。示例：`font-normal text-base leading-relaxed text-[#333333]`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<button
  class="relative group bg-[#1043FF] text-white px-8 py-4 font-mono font-bold tracking-wider text-sm flex items-center gap-4 transition-all duration-200 active:scale-95"
>
  LET'S BUILD YOURS
  <span
    class="inline-block border border-white p-1 text-xs group-hover:translate-x-1 group-hover:-translate-y-1 transition-transform"
    >↗</span
  >
</button>

<div class="relative inline-block cursor-pointer py-2 group">
  <span
    class="relative z-10 text-4xl font-black tracking-tighter uppercase transition-colors group-hover:text-black"
  >
    DREAM CLIENTS
  </span>
  <div
    class="absolute inset-x-0 bottom-1 h-8 bg-[#99FF00] -z-0 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"
  ></div>
</div>

<div
  class="w-full border-b border-black/10 py-6 flex justify-between items-end group cursor-pointer hover:border-black transition-colors"
>
  <div class="flex items-baseline gap-6">
    <span class="font-mono text-xs text-[#1043FF]">[ 01 ]</span>
    <h3 class="text-5xl font-black uppercase tracking-tighter leading-none">
      HOME
    </h3>
  </div>
  <span
    class="font-mono text-xs opacity-0 group-hover:opacity-100 transition-opacity"
    >➔ VIEW SECTION</span
  >
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：采用“极空与极满”的剧烈反差。版面四周留出大面积的纯灰色块不放任何元素，给视觉以呼吸感；而核心文案区块则通过超大字号将空间近乎塞满，形成如同海报般的排版张力。

## 7. Elevation & Depth (层级与深度)

- 界面彻底抛弃伪物主义的三维阴影。完全依赖**高饱和度色块的对撞**（如灰底上放白卡片，白卡片上放蓝按钮）以及**硬边缘线条的堆叠**来划分前后层级。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：
- 大胆使用全大写（UPPERCASE）英文标题。
- 在页面边缘加入像素化（Pixelated）或者点阵（Dot-matrix）风格的巨型 LOGO 作为视觉底纹。
- 保持边框和线条的纯黑高对比度。

- **Don't**：
- **绝对不要**使用任何带有渐变色（Gradient）的背景或按钮。
- 不要使用柔和、带有模糊（Blur）的毛玻璃效果或弥散阴影。
- 严禁在大标题上使用大字距（Tracking-wide），这会彻底破坏新粗野主义的紧凑感和压迫力。
