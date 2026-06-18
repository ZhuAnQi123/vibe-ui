---
id: smat-organic-grain-editorial
name: SMAT Organic Grain Editorial
name_zh: "SMAT 有机颗粒人文刊物风"
cover_image: "../assets/smat-organic-grain-editorial.webp"
domain: ["健康与公益", "心理戒断支持", "生活方式倡导", "人文艺术媒体"]
aesthetic:
  [
    "有机渐变 (Organic Gradient)",
    "复古刊物 (Editorial Serif)",
    "自然柔和 (Natural & Muted)",
  ]
color_scheme: "Auto"
website: https://smat.ca/
description: >
  该风格融合了经典纸质刊物的优雅排版与现代数字化有机美学。核心视觉由柔和细腻的低饱和度渐变、高质感的复古噪点颗粒（Grain）以及流畅自然的 3D 抽象有机形态共同构成。排版上极为大胆地使用优雅高贵的衬线体（Serif）作为核心视觉锤，传递出极具人文关怀、温暖而包容的情绪基调，非常适合强引导、重文本阅读且需要建立深度信任感的产品。
  触发词：smat-organic-editorial-style
---

# SMAT Organic Grain Editorial UI 规范说明书

## 1. Overview (概览)

- **核心基调**：温暖治愈、包容平和、人文质感、克制优雅。
- **视觉特征**：微噪点自然有机渐变底色、大字重有衬线体（Serif）带来的传统报刊印刷感、拟真圆角气泡对话框（强化亲切感）、轻量化的微拟物 3D 抽象图形与趣味性浮动标签网格。
- **适用场景**：心理健康与戒断服务、公益组织官网、数字杂志与内容社区、注重情感连接的人文科技产品。
- **不适用场景**：硬核暗黑风游戏界面、高冷冷调工业风后台、快节奏强刺激的电商大促活动页。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：常规功能卡片和模态弹窗使用亲和力较强的 `rounded-2xl` 到 `rounded-3xl`；按钮及悬浮气泡标签使用更柔软圆润的 `rounded-xl` 或 `rounded-full`。
- **阴影策略 (Shadow)**：极为克制，常规内容完全不使用物理阴影（`shadow-none`）。仅在模拟现实对话气泡卡片层级或强提示弹窗时，使用微弱的硬边缘投影或柔和的一体化阴影，如 `shadow-[0_4px_20px_rgba(0,0,0,0.03)]`。
- **边框策略 (Border)**：不使用强硬的深色实线。卡片边界或输入框通常采用低对比度的细描边（如 `border border-black/10` 或 `border border-amber-900/10`），或直接通过色块拼接分割，拒绝粗暴的线条感。
- **间距与留白 (Spacing)**：倡导高呼吸感的“段落式”杂志排版。Section 之间使用极其宽裕的 `py-20` 到 `py-32`，组件内部则通过大文字间距和自然行高（`leading-relaxed`）营造出不急不躁的阅读节奏。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#000000` (或 `#1A1A1A`) - 用于大字重的有衬线标题和核心正文，复刻纸质油墨印刷的尊贵质感。
- **Background/Canvas (基础画布)**：`#FFFEE0` (明亮米黄/暖奶白) - 作为全站最底层的环境底色，相比纯白更具纸张的温度与阅读舒适感。
- **Organic Gradient (有机渐变色谱)**：采用从绿色 `#1F996B`、温暖粉橘 `#F2B89D` 到柔和蓝紫 `#A1C6D9` 的大面积多色流体渐变，并叠加微细噪点。
- **Surface (容器/卡片背景)**：`#FFFDD0` (低饱和度浅暖黄) 或 `#FFFFFF` (纯白) - 用于文字对话框和通栏信息板块，与背景形成微妙且舒适的层级差。
- **Accent/Alert (强调/公告色)**：`#F9FA62` (高明度柠檬黄) - 用于顶部重要公告 Banner 或全局强提示弹窗，起到吸睛作用但不带侵略性。
- **Text/Ink (油墨正文)**：`#1A1A1A` - 保证高品质的阅读体验。
- **Muted (弱化说明)**：`#555555` - 用于次要辅助文本。

## 4. Typography (排版系统原则)

- **展示字体 (Display/Heading)**：大标题和核心口号。必须选用高阶、带有经典人文美感的**有衬线体（Serif）**，字重极粗，字距微调。典型类名组合：`font-serif font-bold text-4xl md:text-6xl text-neutral-900 tracking-tight leading-tight`。
- **正文字体 (Body)**：正文与细则说明。为了保障屏幕长文本的极佳可读性，切换为高清晰度的**无衬线体（Sans-serif）**。典型类名组合：`font-sans font-medium text-base text-neutral-800 leading-relaxed`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div
  class="bg-[#F9FA62] rounded-[24px] p-8 max-w-md border border-black/5 text-center relative shadow-[0_12px_40px_rgba(0,0,0,0.04)]"
>
  <button class="absolute top-4 right-4 text-neutral-700 hover:text-black">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M6 18L18 6M6 6l12 12"
      />
    </svg>
  </button>

  <h3 class="font-serif font-bold text-2xl text-neutral-950 leading-snug mb-4">
    Les inscriptions au SMAT sont mises en pause pour une durée indéterminée.
  </h3>
  <p class="font-sans font-medium text-sm text-neutral-800 mb-6">
    Besoin de soutien ou de plus d'infos?
  </p>
  <button
    class="bg-[#D6C5FF] text-neutral-950 font-sans font-semibold px-6 py-2.5 rounded-full border border-black/10 hover:bg-[#c3aeff] transition-colors"
  >
    En savoir plus
  </button>
</div>

<div
  class="flex flex-wrap gap-3 p-6 bg-[#FFFEE0] rounded-3xl justify-center items-center"
>
  <span
    class="px-5 py-2.5 bg-[#FCD8A5] text-neutral-900 font-sans font-medium text-sm rounded-full border border-black/5 cursor-pointer hover:scale-105 transition-transform"
  >
    Substituts nicotiniques
  </span>
  <span
    class="px-5 py-2.5 bg-[#FBCBB5] text-neutral-900 font-sans font-medium text-sm rounded-full border border-black/5 cursor-pointer hover:scale-105 transition-transform"
  >
    Santé physique
  </span>
  <span
    class="px-5 py-2.5 bg-[#E1E5AC] text-neutral-900 font-sans font-medium text-sm rounded-full border border-black/5 cursor-pointer hover:scale-105 transition-transform"
  >
    Préparation
  </span>
  <span
    class="px-5 py-2.5 bg-[#F7C5A9] text-neutral-900 font-sans font-medium text-sm rounded-full border border-black/5 cursor-pointer hover:scale-105 transition-transform"
  >
    Soutien
  </span>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：采用如同高端生活方式画报般的自然留白。模块与模块之间通过超宽的间距（如 `space-y-32`）来减缓信息密度，绝不让用户在浏览时产生压迫感，从而提供一个让人静下心来阅读和倾听的舒适底色。

## 7. Elevation & Depth (层级与深度)

- **平面层叠与气泡悬浮**：该风格不追求前卫的 3D 纵深。它主要采用“纸张层叠”的伪 2D 层级：底层是有机多色微噪点画布，中层是干净纯色的对话气泡卡片，最表层则是通过趣味性微错位、乱序排列的悬浮胶囊标签，形成一种轻松、灵动、不刻板的手工拼贴刊物感。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：
- 核心大标题必须坚定不移地使用优雅、粗重的衬线体（Serif）来奠定人文基调。
- 大量使用明度适中、带有一点点灰调或奶调的自然保护色（如米黄、淡绿、暖橘），减少刺眼的纯白色。
- 细节处要注重人情味，多采用对话气泡或者略带俏皮的圆角标签形式。

- **Don't**：
- 绝对不要使用极具科技冷冽感的纯黑白冷调或高饱和度荧光渐变（如科技蓝、赛博紫）。
- 标题严禁使用过于死板、毫无个性的标准黑体或几何无衬线体。
- 避免引入大面积错综复杂的物理强阴影或生硬刺眼的工业化粗描边，那会彻底破坏这种温润治愈的人文氛围。
