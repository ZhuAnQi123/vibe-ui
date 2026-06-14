---
name: ui-style-library
description: 按触发词加载预设 UI 审美风格并输出可落地的设计 token 与组件规范。当用户提到 Tiimo、有机极简、治愈系、低饱和、粉彩、ADHD 友好、纸质便利贴风、或要求按某套 UI 风格实现页面时使用。
---

# UI 风格库

## 快速开始

1. 从下方「风格索引」匹配用户提到的风格或触发词
2. 读取对应 `references/<style>.md` 全文
3. 按该风格输出设计 token + 组件建议 + 实现约束，**全文使用中文**

若用户未指定风格，先列出可用风格让用户选择，不要猜测。

## 风格索引

| 风格 ID | 触发词 | 参考文件 | 适用场景 |
|---|---|---|---|
| copula-neo-brutalism | Copula、高饱和撞色、新粗野主义、先锋创意 | [references/copula-neo-brutalism.md](references/copula-neo-brutalism.md) | 创意机构 / 数字化工作室 / 潮流品牌 |
| tiimo-organic-minimalism | Tiimo、有机极简、治愈系、低饱和、ADHD 友好 | [references/tiimo-organic-minimalism.md](references/tiimo-organic-minimalism.md) | 日程/专注/心理健康类 App |
| units-playful-brutalism | Units、像素网格、大色块拼接、青春玩味、新粗野 | [references/units-playful-brutalism.md](references/units-playful-brutalism.md) | 青年社区 / 创意住宿 / 互动生活平台 |

新增风格时：复制 [references/_template.md](references/_template.md)，填完后在本表加一行，并更新本 Skill 的 `description` 触发词。

## 输出模板

匹配到风格后，严格按以下结构输出：

```markdown
## 风格概览
- 风格名称：
- 情绪基调：
- 不适用场景：

## Design Tokens
| 类别 | 值 | 说明 |
|---|---|---|
| 主色 | | |
| 中性色 | | |
| 圆角 | | |
| 阴影 | | |
| 字体 | | |
| 动效时长 | | |

## 组件模式
- 按钮：
- 卡片：
- 列表/时间轴：
- 空态/错误态：

## 实现约束
- 技术栈建议：
- 禁止项：
- 可访问性：

## 代码骨架（可选）
[给出 Tailwind/CSS 变量示例]
```

## 决策规则

- 风格是约束，不是装饰堆砌；核心任务效率优先
- 每个 token 必须可映射到 CSS/Tailwind 变量
- 动效需包含 `prefers-reduced-motion` 降级
- 若风格与项目现有 design system 冲突，说明冲突点并给出折中方案

## 检查清单

- [ ] 已加载正确的 references 文件
- [ ] Token 完整且可执行
- [ ] 组件模式覆盖当前页面关键元素
- [ ] 未牺牲可访问性与核心效率
