---
id: band-5051-pixel-punk
name: 5051 Pixel Punk
name_zh: "5051 像素朋克风"
cover_image: "../assets/band5051.webp"
domain: ["音乐/乐队官网", "独立游戏", "潮流文化", "个人主页"]
aesthetic: ["像素艺术 (Pixel Art)", "赛博朋克/复古朋克", "粗野主义 (Brutalism)"]
color_scheme: "Dark"
website: https://band5051.com/
description: >
  该风格灵感来源于 8-bit/16-bit 像素复古游戏与朋克摇滚文化的结合。
  整体视觉充斥着深夜霓虹、大漠落日、像素楼宇与复古演出的情绪基调，传递出张扬叛逆、自由不羁的独立精神。
  核心策略是使用极具颗粒感的像素艺术图形，搭配硬核的纯黑粗边框、像素风字体、无渐变的纯色块，以及极具舞台感和街头感的高饱和度点缀色。
  触发词：pixel-art, retro-punk, 8-bit-gaming, bold-borders, neon-accents
---

# 5051 Pixel Punk UI 规范说明书

## 1. Overview (概览)

- **核心基调**：张扬叛逆、复古极客、舞台燥热、充满故事性。
- **视觉特征**：像素网格网画、无平滑的硬边缘（`antialiased` 的反向应用）、硬核 3D 错位投影、霓虹色块高亮。
- **适用场景**：独立摇滚/朋克乐队官网、像素风游戏社区、潮流厂牌电商、极具个性的个人前端作品集。
- **不适用场景**：严肃的企业级 SaaS、医疗金融等需要极高信任感与平滑现代感的 B 端系统。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：全面禁止使用任何圆角，保持纯粹的直角以符合像素格子的物理特性。必须使用 `rounded-none`。
- **阴影策略 (Shadow)**：禁止使用现代的弥散阴影、模糊阴影。必须使用纯色块错位实现的硬核阴影（如 `shadow-[4px_4px_0px_0px_#000000]` 或 `shadow-[2px_2px_0px_0px_#FF4500]`）。
- **边框策略 (Border)**：使用极具存在感的大像素描边，基础边框为 `border-2 border-black` 或 `border-[3px] border-[#1A1A1A]`。
- **间距与留白 (Spacing)**：Section 之间使用极其工整的硬性间距 `gap-8` 或 `gap-12`，横向排版多采用卷轴式横向滚动布局（Horizontal Scroll Grid）。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#E63946` / `#FF4500` - 用于强烈的警告、摇滚霓虹点缀、LIVE 演出高亮状态。
- **Secondary (次主色)**：`#FFD166` / `#FFB703` - 用于黄昏/大漠落日感文字、重要标签、像素按钮的高亮悬停。
- **Background/Canvas (画布背景)**：`#120F1D` - 深邃的深夜星空/舞台暗场大面积底色。
- **Surface (容器背景)**：`#1E1B29` 或 `#2A263D` - 像素卡片底色、表单输入框底色。
- **Border/Hairline (线条/描边)**：`#000000` - 所有的元素隔离线、像素边框线。
- **Text/Ink (主要文本)**：`#FFFFFF` - 主要高亮像素文字、标题。
- **Muted (弱化文本)**：`#A0A0B0` - 弱化描述、乐手简介、非核心辅助信息。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：使用像素风等宽大标题，英文推荐使用诸如 `Press Start 2P`、`DotGothic16` 风格的字体。Tailwind 表现形式为 `font-mono uppercase tracking-widest font-black text-2xl md:text-4xl`。
- **正文字体 (Body)**：为保障像素风格下的中文可读性，可使用干净的等宽或无衬线字体，但字号不可过小。使用 `font-mono tracking-wide leading-relaxed text-sm`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<button
  class="bg-[#E63946] text-[#FFFFFF] px-6 py-2 rounded-none font-mono font-black border-4 border-black shadow-[4px_4px_0px_0px_#000000] hover:translate-x-[2px] hover:translate-y-[2px] hover:shadow-[2px_2px_0px_0px_#000000] active:translate-x-[4px] active:translate-y-[4px] active:shadow-none transition-all"
>
  GET TICKETS
</button>

<div
  class="bg-[#1E1B29] rounded-none p-6 border-4 border-black shadow-[6px_6px_0px_0px_#000000] max-w-sm"
>
  <div
    class="border-4 border-black mb-4 relative overflow-hidden bg-[#2A263D] aspect-square"
  >
    <img
      src="../assets/ivan-pixel.png"
      alt="Ivan"
      class="w-full h-full object-cover image-render-pixel"
      style="image-rendering: pixelated;"
    />
  </div>
  <h3 class="text-[#FFD166] font-mono font-black text-xl tracking-wider mb-1">
    IVAN
  </h3>
  <p class="text-[#E63946] font-mono text-xs font-bold mb-3">VOCALS / GUITAR</p>
  <p class="text-[#A0A0B0] font-mono text-sm leading-normal">
    Voice of the band. Turned lovers into Belarusian punk. Started 5051.
  </p>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：严谨的像素对齐与网格化。摒弃现代主义的超大呼吸感留白，采用类似复古横版通关游戏（Side-scroller）的卷轴式分层布局。模块与模块之间通过“像素砖墙”、“铁丝网”或纯黑色加粗分界线进行强行分割。

## 7. Elevation & Depth (层级与深度)

- 绝对不使用 Z 轴物理阴影渲染。层级的提升完全通过**黑色实体块的右下角平移**（即硬投影）来表达。投影越厚（如 `shadow-[8px_8px_0px_0px_#000]`），代表元素越靠近用户。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：
- 必须保持 100% 的直角 (`rounded-none`)。
- 在大面积图像上开启 `image-rendering: pixelated;`，确保像素颗粒不被浏览器模糊化。
- 动效采用帧动画（Step transition）效果，而非平滑的线性渐变。

- **Don't**：
- 绝对不要使用 `shadow-xl` 或 `shadow-inner` 等具有高斯模糊的现代阴影。
- 绝对不要使用 CSS 渐变色（Gradient background），必须使用高饱和度的纯色块拼接。
- 严禁引入任何带有圆润弧度的现代 Icon 库，所有图标必须进行像素网格化处理。
