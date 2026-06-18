---
id: elva-cinematic-dark-minimalism
name: Elva Cinematic Dark Minimalism
name_zh: "Elva 电影感暗黑微光风"
cover_image: "../assets/elvalabs.webp"
domain: ["AI 视频工具", "音视频剪辑", "摄影/摄像应用", "创意设计工具"]
aesthetic:
  [
    "暗黑极简 (Dark Minimalism)",
    "电影质感 (Cinematic)",
    "微光流体 (Glow & Fluid)",
  ]
color_scheme: "Dark"
website: https://elvalabs.ai/
description: >
  该风格致力于营造高端、沉浸、极具电影质感的科技氛围。整体以大面积纯黑与深邃的暗调作为画布，通过高饱和度的微光气泡、流体三维球体以及流光线条作为核心视觉锚点，打破暗黑的沉闷。排版上采用极具张力的超大无衬线字体，通过极端的字重对比（超粗标题与极细正文）和紧凑的字距压缩，传递出先锋且专业的科技感。
  触发词：elva-cinematic-dark-style
---

# Elva Cinematic Dark Minimalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：沉浸深邃、电影质感、先锋科技、灵动克制。
- **视觉特征**：大面积高纯度暗黑留白、超大字重与极紧字距的排版张力、拟真质感的三维多维浮球/气泡（用于承载图像素材）、动态流光线条与微光反馈。
- **适用场景**：AI 创作工具、多媒体剪辑工作台、高端科技产品官网、艺术家作品集、沉浸式娱乐影音应用。
- **不适用场景**：传统政企办公系统、高密度数据表格后台、少儿教育或强调明快温馨的社区平台。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：手机框容器及核心展示卡片使用 `rounded-[40px]` 或 `rounded-3xl`；小组件、胶囊按钮或标签采用全圆角 `rounded-full`。
- **阴影与发光策略 (Shadow/Glow)**：不使用传统的灰色物理阴影。采用滤色模式下的荧光或渐变微光，如使用 `shadow-[0_0_50px_rgba(255,255,255,0.08)]` 或利用毛玻璃混合模式实现局部提亮。
- **边框策略 (Border)**：极度克制，常规内容不加边框。在需要分割手机界面或独立卡片时，使用 `border border-white/10` 或 `border border-neutral-800` 的极细发丝线。
- **间距与留白 (Spacing)**：在大屏排版中，块级元素间采用极致的呼吸感留白（如 `space-y-24` 或 `gap-16`），而在手机 mock-up 或内容卡片内部，则保持紧凑的一体化布局。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#FFFFFF` - 用于高亮文本、核心标题及主要行动点，在暗黑背景下形成绝对的高反差。
- **Background/Canvas (画布背景)**：`#000000` - 纯黑。作为大面积的沉浸式底色，确保三维浮球与流光特效能完美显色。
- **Surface (容器/卡片背景)**：`#1A1A1A` 或 `#121212` - 极暗灰。用于手机外框内部、次级功能面板或深色气泡底色。
- **Border/Hairline (线条/描边)**：`#262626` (或 `rgba(255,255,255,0.1)`) - 用于极细的分隔线或容器边缘。
- **Text/Ink (主要文本)**：`#FFFFFF` - 用于大标题、醒目文案，保持高清晰度。
- **Muted (弱化文本)**：`#8C8C8C` (或 `text-neutral-400`) - 用于副标题、说明文字及未激活状态标签。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：用于核心大标题。必须使用无衬线体（如 Inter/SF Pro），配合超粗字重、极紧字距与紧凑行高。典型类名组合：`font-bold tracking-tighter leading-none text-white`。
- **正文字体 (Body)**：用于说明文字与标签。保持中等字重与舒适的行间距，确保在暗色背景下的可读性。典型类名组合：`font-normal text-neutral-400 tracking-normal leading-relaxed`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<button
  class="bg-white/10 text-white text-xs font-semibold px-4 py-2 rounded-full border border-white/20 backdrop-blur-md hover:bg-white hover:text-black hover:scale-105 transition-all duration-300"
>
  Try Yourself
</button>

<div
  class="bg-[#121212] rounded-[32px] p-8 border border-neutral-800 shadow-[0_0_40px_rgba(0,0,0,0.5)] max-w-sm text-center"
>
  <div
    class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-tr from-cyan-500 via-purple-500 to-indigo-500 opacity-80 blur-[2px] animate-pulse shadow-[0_0_30px_rgba(99,102,241,0.5)]"
  ></div>

  <h3 class="text-2xl font-bold text-white tracking-tighter mb-2">
    Pick a music mood
  </h3>
  <p class="text-sm text-neutral-400 font-normal leading-relaxed mb-6">
    It listens and turns your idea into a finished edit.
  </p>

  <div class="flex flex-wrap justify-center gap-2">
    <span
      class="px-4 py-1.5 bg-white text-black text-xs font-medium rounded-full"
      >Pop</span
    >
    <span
      class="px-4 py-1.5 bg-neutral-900 text-neutral-300 text-xs font-medium rounded-full border border-neutral-800"
      >Cinematic</span
    >
    <span
      class="px-4 py-1.5 bg-neutral-900 text-neutral-300 text-xs font-medium rounded-full border border-neutral-800"
      >Ambient</span
    >
  </div>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：采用大开大合的“剧场式”留白排版。四周留出极其宽裕的绝对纯黑空间，将视觉焦点牢牢锁定在屏幕中央的手机 Mock-up 或动态气泡流体上。
- **叙事性层级**：左侧或背景为巨大的文案宣告，右侧或上层为交互实体，形成如同电影谢幕表或海报般的构图。

## 7. Elevation & Depth (层级与深度)

- **多维球体悬浮**：打破传统的平面卡片层级，大量使用三维带有玻璃质感、反光的圆形浮球（Bubble）来承载视频与图片素材。
- **层级穿插**：浮球在 Z 轴上具有动态深度，通过大小透视和模糊滤镜（`blur`）形成前后穿插的景深效果（Depth of Field），营造出信息在三维夜空中漂浮的质感。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：
- 坚持使用纯黑（`#000000`）作为大面积背景，让图像和微光组件自然“浮”出来。
- 标题文字一定要足够大、字距一定要紧（`tracking-tighter`），以产生视觉压迫感与时尚感。
- 材质上多借用毛玻璃（`backdrop-blur`）与流体渐变来体现 AI 的灵动性。

- **Don't**：
- 绝对不要使用明亮的浅灰色卡片背景或大面积的物理灰色阴影。
- 严禁使用过于花哨、衬线或小字重的弱排版作为核心主标题。
- 严禁使用生硬的直角（`rounded-none`），所有的容器和交互按钮都应具备圆润或胶囊状的流线外形。
