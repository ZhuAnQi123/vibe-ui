---
id: terminal-ai-first-aesthetic
name: Terminal AI-First Aesthetic
cover_image: "../assets/supabase.webp"
domain: ["AI 工具", "开发者工具", "自动化平台", "代码产品"]
aesthetic: ["极客终端风", "Dark mode first", "Monospace", "霓虹强调"]
color_scheme: "Dark"
website: "https://supabase.com/"
description: >
  Terminal AI-First Aesthetic 是面向 AI 工具和开发者产品的深色界面风格。它借鉴代码编辑器、命令行和现代 DevTools 的视觉语言，用纯黑或深灰背景、等宽字体、高对比文本和少量霓虹强调色营造专业、精确、技术可信的氛围。触发词：developer-tools aesthetic, dark mode first, monospace typography, terminal inspired, neon glowing accents, high contrast
---

# Terminal AI-First Aesthetic UI 规范说明书

## 1. Overview (概览)

- **核心基调**：极客、精准、冷静、高效、AI-native。
- **视觉特征**：深色背景、等宽字体、命令行式标签、细线分割、荧光强调色、编辑器面板结构。
- **适用场景**：AI Agent 控制台、脚本工具、开发者 SaaS、日志分析、自动化工作流。
- **不适用场景**：儿童产品、柔和生活方式应用、高级奢侈品视觉、需要大量图片情绪表达的页面。

## 2. 具象化的 Tailwind 字典 (Tailwind Dictionary)

> ⚠️ **AI 约束**：不要只使用模糊的形容词，必须明确指定 Tailwind 类名。

- **圆角策略 (Rounded)**：使用 `rounded-lg` 或 `rounded-xl`，整体偏工具感；避免 `rounded-3xl` 大圆角滥用。
- **阴影策略 (Shadow)**：少用传统阴影，可使用霓虹光晕 `shadow-[0_0_40px_rgba(34,197,94,0.18)]`。
- **边框策略 (Border)**：高频使用 `border border-white/10`、`divide-y divide-white/10` 和 `ring-1 ring-inset ring-white/5`。
- **间距与留白 (Spacing)**：面板使用 `p-4 md:p-6`，组件之间使用 `gap-3 md:gap-4`，保持开发工具的紧凑效率。

## 3. 色彩变量映射 (Color Variables)

> ⚠️ **AI 约束**：明确告诉 AI 主色、背景色、边框色的具体 Hex 值，避免 AI 自由发挥。

- **Primary (主色)**：`#22C55E` - 荧光绿色，用于运行状态、CTA 和高亮代码。
- **Background/Canvas (画布背景)**：`#020617` - 近黑蓝色主背景。
- **Surface (容器背景)**：`#0F172A` - 编辑器面板和卡片背景。
- **Border/Hairline (线条/描边)**：`#1E293B` - 面板边框和分割线。
- **Text/Ink (主要文本)**：`#E2E8F0` - 主文本和命令输出。
- **Muted (弱化文本)**：`#64748B` - 注释、时间戳、次级说明。

## 4. Typography (排版系统原则)

- **展示字体 (Display)**：标题可混用无衬线和等宽字体，示例：`font-semibold tracking-tight text-slate-100`。
- **功能字体 (Code/Mono)**：按钮、标签、日志和状态使用 `font-mono text-sm tracking-tight`。
- **正文字体 (Body)**：正文使用 `text-sm leading-6 text-slate-400`，避免过大字号破坏工具密度。

## 5. 基准组件示例 (Anchor Component)

> ⚠️ **AI 约束**：请 AI 在生成其他组件时，严格参考以下基准组件的 HTML/Tailwind 结构。

```html
<div class="rounded-xl border border-[#1E293B] bg-[#0F172A] shadow-[0_0_40px_rgba(34,197,94,0.12)]">
  <div class="flex items-center justify-between border-b border-white/10 px-4 py-3 font-mono text-xs text-[#64748B]">
    <span>~/agent/run.sh</span>
    <span class="text-[#22C55E]">● ONLINE</span>
  </div>
  <div class="space-y-4 p-6">
    <h3 class="text-2xl font-semibold tracking-tight text-[#E2E8F0]">Deploy autonomous workflow</h3>
    <p class="font-mono text-sm leading-6 text-[#94A3B8]">$ vibe agent start --mode production --watch</p>
    <button class="rounded-lg border border-[#22C55E]/40 bg-[#22C55E]/10 px-4 py-2 font-mono text-sm font-semibold text-[#22C55E] transition hover:bg-[#22C55E]/20">RUN COMMAND</button>
  </div>
</div>
```

## 6. Layout & Spacing (布局与空间)

- **留白哲学**：保持面板化和信息密度，留白服务于扫描效率，而不是营造生活方式品牌的空灵感。

## 7. Elevation & Depth (层级与深度)

- 使用深浅面板、细边框、状态色光晕和代码块层级表达深度，避免传统卡片阴影。

## 8. Do's and Don'ts (设计禁忌)

- **Do**：坚持深色优先、等宽字体、状态指示和命令行语汇。
- **Don't**：不要使用粉彩治愈渐变、大量插画、厚重圆角或浅色 Apple-like 小组件风。
