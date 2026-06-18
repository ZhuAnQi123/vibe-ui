````markdown
---
id: kawe-ski-pixel-art
name: Kawe.ski Pixel Art
name_zh: "Kawe.ski 复古像素画风"
cover_image: "../assets/kawe.webp"
domain:
  [
    "个人作品集 (Portfolio)",
    "独立开发者/设计师官网",
    "创意设计工作室",
    "系统架构文档",
  ]
aesthetic:
  [
    "新粗野主义 (Neo-Brutalism)",
    "复古像素 (Pixel Art)",
    "柔和高饱和 (Muted High-Saturation)",
  ]
color_scheme: "Light"
website: https://kawe.ski/
description: >
  该风格是新粗野主义与复古低保真（Lo-Fi）美学的完美结合。它保留了新粗野主义标志性的纯黑高对比度描边（High-contrast stroke）、硬边缘无渐变投影（Hard shadows），但摒弃了传统粗野主义刺眼扎眼的荧光色，转而采用一种更具亲和力的、高饱和度却略带粉质感的柔和复古色块（如奶油黄、薰衣草紫、复古绿）。搭配像素艺术（Pixel Art）头像和精致的圆角微卡片，既有极客的硬核态度，又兼具设计师的细腻人文。
  触发词：kaweski-brutalism-style
---

# Kawe.ski Neo-Brutalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：个性张扬、极客复古、率真幽默、克制规范。
- **视觉特征**：1.5px 至 2px 的纯黑刚性描边、清晰的无渐变硬化位移投影、高饱和度但视觉舒适的粉质纯色块、像素风头像/ICON 与规整的网格双栏/三栏布局。
- **适用场景**：个人求职作品集、独立品牌概念店、开发工具/Design System 官方主页、先锋科技博客。
- **不适用场景**：强调奢侈品的高级微光质感界面、需要大面积图片沉浸式留白的摄影网站、高度严肃的医疗或金融风控后台。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：区别于完全直角的新粗野主义，此风格更具亲和力。外层大卡片与核心功能块使用中等圆角 `rounded-2xl`（或 `rounded-[20px]`），内部小标签或状态组件采用 `rounded-lg` 或 `rounded-full`。
- **阴影策略 (Shadow)**：绝对不使用任何模糊、渐变的弥散阴影。必须使用硬边缘的黑色位移投影来制造板块的立体系悬浮感，典型类名如 `shadow-[4px_4px_0px_0px_#000000]` 或 `shadow-[6px_6px_0px_0px_#1A1A1A]`。
- **边框策略 (Border)**：全员标配描边，用来作为图形和卡片的分界线。统一使用纯黑（或极深灰）的实体边框：`border-2 border-black` 或 `border-[1.5px] border-neutral-900`。
- **间距与留白 (Spacing)**：布局极其规整，像杂志格子般严丝合缝。 Section 之间使用标准的 `gap-6` 或 `gap-8` 紧凑排列；卡片内部通常使用对称的 `p-6` 或 `p-8` 保证充实的图文呼吸感。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Background/Canvas (基础画布)**：`#F3F3F3` (或带一点点米调的 `#EFEFEF`) - 极为干净、理性的浅灰色大背景，用于衬托上层的多彩卡片。
- **Primary/Accent (核心提亮色组)**：
  - **复古芒果黄**：`#F2C94C` - 用于最核心的项目卡片、重点高亮标签或悬浮切换按钮。
  - **低饱和紫萝兰**：`#D3C2F7` - 用于次要重点板块、按钮背景或设计系统标签。
  - **清新草绿**：`#6FCF97` - 用于“战略”、“经验”等正向状态标签。
  - **柔和珊瑚粉**：`#EB5757` - 用于特定分类或趣味性装饰元素。
- **Surface (卡片背景)**：`#FFFFFF` - 标准卡片底色，配合黑色粗边框，确保极佳的内容可读性。
- **Border/Text (边框与绝对油墨)**：`#000000` (或 `#111111`) - 用于所有的文字、图标描边、卡片边框以及硬投影。

## 4. Typography (排版系统原则)

- **展示字体 (Display/Heading)**：主标题与导航 LOGO。采用极为粗重、硬朗的无衬线黑体，字距略微压缩，大开大合。典型类名组合：`font-black text-3xl md:text-5xl text-black tracking-tight leading-none uppercase`。
- **正文字体 (Body)**：正文与卡片描述。采用字形方正、间距适中的现代无衬线体，字重适中，确保在粗边框包围下依然拥有极高、极清晰的视觉传达。典型类名组合：`font-semibold text-neutral-800 text-sm md:text-base leading-relaxed`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div
  class="bg-[#F2C94C] rounded-[24px] p-6 border-2 border-black shadow-[6px_6px_0px_0px_#000000] hover:translate-x-[-2px] hover:translate-y-[-2px] hover:shadow-[8px_8px_0px_0px_#000000] transition-all duration-200 max-w-sm"
>
  <div
    class="w-full h-40 bg-white rounded-xl border-2 border-black mb-4 flex items-center justify-center font-black text-4xl"
  >
    Y
  </div>
  <h3 class="font-black text-2xl text-black uppercase tracking-tight mb-2">
    Yorgute
  </h3>
  <p class="font-medium text-sm text-neutral-900 leading-relaxed mb-4">
    Projeto autoral que explora uma alternativa às redes sociais atuais,
    priorizando vínculos humanos e memória digital.
  </p>
  <a
    href="#"
    class="inline-flex items-center font-bold text-sm text-black underline underline-offset-4 hover:text-neutral-700"
  >
    Ver projeto ↗
  </a>
</div>

<div
  class="flex flex-wrap gap-3 p-4 bg-white border-2 border-black rounded-2xl shadow-[4px_4px_0px_0px_#000000]"
>
  <span
    class="px-3 py-1 bg-[#6FCF97] text-black text-xs font-bold rounded-lg border-2 border-black"
  >
    Estratégia
  </span>
  <span
    class="px-3 py-1 bg-[#D3C2F7] text-black text-xs font-bold rounded-lg border-2 border-black"
  >
    Design Inteligente
  </span>
  <button
    class="ml-auto px-4 py-1 bg-black text-white text-xs font-bold rounded-lg border-2 border-black hover:bg-white hover:text-black transition-colors"
  >
    Contato
  </button>
</div>
```
````

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：严谨的几何主义。整体界面就像是由一个个被框起来的“信息集装箱”拼接而成。它不依赖无边界的空气感留白，而是通过卡片与卡片之间标准的、等距的物理缝隙（如 `space-y-6`）来形成天然的视觉秩序。

## 7. Elevation & Depth (层级与深度)

- **位移差与硬投影**：该风格的纵深感完全由“黑色实体投影”和“反向位移（Translate）”来决定。背景是 0 层，卡片通过 `shadow-[4px_4px_0px_0px_#000000]` 拔高至 1 层。当用户 Hover 悬停时，卡片向左上微调 `hover:-translate-y-0.5 hover:-translate-x-0.5` 且投影变大，形成极为纯粹的机械式物理反弹质感。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：
- 必须坚持为所有的卡片、按钮、标签添加刚性纯黑边框（`border-2 border-black`）。
- 阴影必须是硬边无渐变色块（`shadow-[Xpx_Xpx_0px_0px_#000]`），禁止带有任何模糊度（`blur`）。
- 卡片底色可以大胆尝试复古粉质色彩，但文字必须保持绝对的纯黑高可读性。

- **Don't**：
- 绝对不要引入任何现代化的渐变色、色彩斑斓的发光或弥散阴影（`blur-xl`）。
- 不要使用纤细、软糯、带有过多装饰性的花体衬线字作为大标题。
- 严格禁止在同一个组件内同时出现圆角、直角、粗边框、无边框混杂的情况，粗野主义的灵魂在于全站视觉规范的绝对高度统一。
