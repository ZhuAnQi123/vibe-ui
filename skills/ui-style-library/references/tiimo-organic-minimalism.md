---
id: tiimo-organic-minimalism
name: Tiimo Organic Minimalism
name_zh: "Tiimo 有机治愈极简风"
cover_image: "../assets/tiimoapp.webp"
domain: ["Healthcare", "Productivity", "移动应用"]
aesthetic: ["Organic", "Soft Minimalism", "Pastel"]
color_scheme: "Light"
website: https://www.tiimoapp.com/
description: >
  这是一种温和、安抚、无压迫感的有机极简主义风格。大量使用低饱和水彩/粉彩渐变、柔和的手绘感边缘和纸质便利贴般的立体感，营造出治愈、减压的氛围。特别适合 ADHD 友好、日程管理、专注计时、心理健康辅助等需要降低用户认知负荷的产品。
  触发词：Tiimo、有机极简、治愈系、低饱和、粉彩、ADHD 友好、纸质便利贴
---

# Tiimo Organic Minimalism UI 规范说明书

## 1. Overview (概览)

- **核心基调**：温和、安抚、无压迫感、治愈系。
- **视觉特征**：低饱和水彩/粉彩渐变、柔和手绘感边缘、纸质便利贴立体感、极细阴影与分层、大量留白。
- **适用场景**：日程管理、专注计时、习惯追踪、心理健康辅助。
- **不适用场景**：高频交易、硬核工具、需要强警示的合规场景。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：
  - 核心卡片：使用 `rounded-2xl` 或 `rounded-3xl`
  - 按钮/标签：使用 `rounded-xl` 或 `rounded-full`
- **阴影策略 (Shadow)**：使用极柔和、弥散的阴影，如 `shadow-[0_2px_12px_rgba(0,0,0,0.06)]` 或 `shadow-sm`，避免生硬的黑影。
- **边框策略 (Border)**：尽量不使用边框，或使用极淡的边框 `border border-gray-100`。
- **间距与留白 (Spacing)**：大量留白，使用 `p-6` 或 `p-8` 增加呼吸感，Section 之间使用 `gap-8` 或 `gap-12`。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (工作/专注)**：`#5BA8A0` (蓝绿) - 用于专注类任务、积极反馈。
- **Secondary (休息/放松)**：`#E8A87C` (暖橙) - 用于休息、放松类提示。
- **Tertiary (过渡/中性)**：`#C5B4E3` (浅紫) - 用于状态过渡。
- **Background/Canvas (画布背景)**：`#F8F9FA` - 极其柔和的浅灰白，避免纯白的刺眼。
- **Surface (容器背景)**：`#FFFFFF` - 卡片底色。
- **Text/Ink (主要文本)**：`#2D3436` - 深灰，避免纯黑的压迫感。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：使用圆润或现代的无衬线字体，字重适中，如 `font-bold tracking-tight text-[#2D3436]`。
- **正文字体 (Body)**：清晰易读，避免过细字重，如 `font-medium leading-relaxed text-gray-600`。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<!-- 示例：一个标准的 Tiimo 风格按钮 -->
<button class="bg-[#5BA8A0] text-white px-6 py-3 rounded-2xl font-medium shadow-[0_2px_12px_rgba(91,168,160,0.3)] hover:opacity-90 transition-opacity">
  Start Focus
</button>

<!-- 示例：一个标准的 Tiimo 风格卡片 (类似纸质便利贴) -->
<div class="bg-white rounded-3xl p-6 shadow-[0_2px_12px_rgba(0,0,0,0.06)] border border-gray-50/50">
  <div class="flex items-center gap-3 mb-3">
    <div class="w-3 h-3 rounded-full bg-[#E8A87C]"></div>
    <h3 class="text-lg font-bold text-[#2D3436]">Break Time</h3>
  </div>
  <p class="text-gray-500 font-medium leading-relaxed">Take a deep breath and relax.</p>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：极大的留白，元素之间保持松散的距离，避免信息过载。

## 7. Elevation & Depth (层级与深度)

通过极细的弥散阴影（如 `0 2px 12px rgba(0, 0, 0, 0.06)`）和微小的层级叠加，营造出类似真实纸质便利贴的轻盈立体感。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：使用低饱和水彩/粉彩渐变。统一明度，避免高刺激纯色。使用柔和手绘感边缘。
- **Don't**：禁止使用纯红（#FF0000）作为错误提示。禁止使用倒计时压迫感（优先使用环状时间轴）。禁止使用惩罚性未完成文案（如“未完成 ❌”）。
