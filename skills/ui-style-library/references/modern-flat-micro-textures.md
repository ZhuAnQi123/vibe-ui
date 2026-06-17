---
id: modern-flat-micro-textures
name: Modern Flat With Micro Textures
cover_image: "../assets/monobank.webp"
domain: ["消费产品", "移动应用", "品牌官网", "内容平台"]
aesthetic: ["现代扁平", "微质感", "Grainy overlay", "几何清洁"]
color_scheme: "Light"
website: "https://monobank.ua/"
description: >
  Modern Flat With Micro Textures 是扁平化设计的现代进化版。它保留清晰几何、少阴影和高可用性，同时加入极轻微噪点、纸张质感、微内阴影和细腻色块，让界面不再像生硬纯色块，而是具有温和的触感和高级细节。触发词：modern flat, micro-textures, grainy overlay, subtle inner shadow, clean geometric shapes
---

# Modern Flat With Micro Textures UI 规范说明书

## 1. Overview (概览)

- **核心基调**：清爽、现代、轻质感、友好、不过度装饰。
- **视觉特征**：扁平几何色块、轻微噪点覆盖、细腻内阴影、低强度边框、干净图形。
- **适用场景**：消费级 App、内容平台、品牌官网、轻量 SaaS、移动端首页。
- **不适用场景**：强沉浸玻璃界面、硬核终端工具、极端粗野主义视觉。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：使用 `rounded-2xl` 或 `rounded-3xl`，几何但不生硬。
- **阴影策略 (Shadow)**：使用极轻阴影或内阴影，如 `shadow-[inset_0_1px_0_rgba(255,255,255,0.55)]` 和 `shadow-sm`。
- **边框策略 (Border)**：使用 `border border-black/5` 或 `border-white/50`，保持低存在感。
- **间距与留白 (Spacing)**：卡片使用 `p-6 md:p-8`，Section 使用 `py-20 md:py-28`，整体清爽不拥挤。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#4F46E5` - 用于 CTA、关键图标和品牌强调。
- **Background/Canvas (画布背景)**：`#F4F2EE` - 带纸感的暖灰背景。
- **Surface (容器背景)**：`#FFFFFF` - 主内容卡片。
- **Border/Hairline (线条/描边)**：`#E7E2DA` - 低对比边框。
- **Text/Ink (主要文本)**：`#18181B` - 主文本。
- **Muted (弱化文本)**：`#71717A` - 辅助信息。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：标题使用现代无衬线，示例：`font-bold tracking-tight leading-tight text-[#18181B]`。
- **正文字体 (Body)**：正文使用 `text-base leading-relaxed text-[#71717A]`，保持产品说明的轻松可读。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div class="relative overflow-hidden rounded-3xl border border-[#E7E2DA] bg-white p-8 shadow-sm">
  <div class="pointer-events-none absolute inset-0 opacity-[0.06] [background-image:radial-gradient(#18181B_1px,transparent_1px)] [background-size:6px_6px]"></div>
  <div class="relative">
    <div class="mb-6 flex h-14 w-14 items-center justify-center rounded-2xl bg-[#4F46E5] text-white shadow-[inset_0_1px_0_rgba(255,255,255,0.45)]">✦</div>
    <h3 class="text-3xl font-bold tracking-tight text-[#18181B]">Flat, but not empty.</h3>
    <p class="mt-4 leading-relaxed text-[#71717A]">Add subtle grain and inner highlights to keep clean geometric UI tactile.</p>
    <button class="mt-8 rounded-2xl bg-[#18181B] px-6 py-3 font-semibold text-white transition hover:bg-black">Explore texture</button>
  </div>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：版面保持清洁、轻松和现代，不追求极端留白，也不堆叠复杂质感。

## 7. Elevation & Depth (层级与深度)

- 层级来自色块、细边框、轻微内高光和噪点纹理。阴影要克制，不能回到拟物化重阴影。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：使用微噪点、低对比边框、轻内阴影和干净几何形状。
- **Don't**：不要使用强玻璃模糊、过度渐变、粗黑边框或完全无质感的死板纯色块。
