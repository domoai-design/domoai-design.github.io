# DomoAI Design Tokens

> 唯一事实来源：`packages/tokens/src/*.ts`。改 Token 只改那里，然后运行 `pnpm tokens`。

## 使用规则（必读）

1. 颜色只用下表的语义类名（`bg-surface`、`text-foreground-secondary`、`border-border`…）。Tailwind 默认色板（`bg-blue-500` 等）已被移除，写了也不会生效。
2. 禁止写死颜色值（`#fff`、`rgb()`、`bg-[#...]`）和 `--primitive-*` 变量。
3. 文字样式只用 `typo-*` 组合类，不要单独拼 `text-sm font-medium`。
4. 圆角用 `rounded-*`（xs / sm / sm-plus / md / lg / xl / 2xl / 3xl / full），间距用 Tailwind 4px 刻度（space/12 → `p-3`）。
5. 响应式只用 `md:`（≥768 tablet）和 `xl:`（≥1280 desktop）。

## 语义颜色

| Tailwind 名（bg-/text-/border-） | CSS 变量 | Figma 变量 | 引用 | 实际值 | 说明 |
|---|---|---|---|---|---|
| `background` | `--background` | `background/default` | `color/black` | `#000000` | 页面根背景 |
| `background-secondary` | `--background-secondary` | `background/secondary` | `color/neutral/900` | `#111111` | 次级页面背景 |
| `surface` | `--surface` | `surface/default` | `color/neutral/800` | `#282828` | 默认容器面 |
| `surface-secondary` | `--surface-secondary` | `surface/secondary` | `color/alpha/white/20` | `rgb(255 255 255 / 20%)` | 半透明容器面 |
| `surface-tertiary` | `--surface-tertiary` | `surface/tertiary` | `color/alpha/white/10` | `rgb(255 255 255 / 10%)` | 半透明容器面弱 |
| `surface-muted` | `--surface-muted` | `surface/muted` | `color/alpha/white/5` | `rgb(255 255 255 / 5%)` | 极弱半透明容器面 |
| `surface-inverse` | `--surface-inverse` | `surface/inverse` | `color/alpha/black/40` | `rgb(0 0 0 / 40%)` | 反色（黑色半透明）容器面 |
| `backdrop` | `--backdrop` | `surface/backdrop` | `color/alpha/black/70` | `rgb(0 0 0 / 70%)` | 弹窗、抽屉的背景遮罩 |
| `foreground` | `--foreground` | `foreground/default` | `color/white` | `#ffffff` | 主文本 / 主图标色 |
| `foreground-secondary` | `--foreground-secondary` | `foreground/secondary` | `color/alpha/white/80` | `rgb(255 255 255 / 80%)` | 弱文本 / 次级内容 |
| `foreground-tertiary` | `--foreground-tertiary` | `foreground/tertiary` | `color/alpha/white/60` | `rgb(255 255 255 / 60%)` | 极弱文本 / 不显眼内容 |
| `foreground-muted` | `--foreground-muted` | `foreground/muted` | `color/alpha/white/40` | `rgb(255 255 255 / 40%)` | 禁用文本 / 禁用图标（对比度 3.6:1，不要用于正常文字；正常的弱文字用 foreground-tertiary） |
| `foreground-inverse` | `--foreground-inverse` | `foreground/inverse` | `color/black` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `border` | `--border` | `border/default` | `color/alpha/white/20` | `rgb(255 255 255 / 20%)` | 通用描边 |
| `border-secondary` | `--border-secondary` | `border/secondary` | `color/alpha/white/10` | `rgb(255 255 255 / 10%)` | 弱描边 / 分割线 |
| `border-tertiary` | `--border-tertiary` | `border/tertiary` | `color/alpha/white/5` | `rgb(255 255 255 / 5%)` | 极弱描边 / 轻分割线 |
| `focus` | `--focus` | `border/focus` | `color/white` | `#ffffff` | 聚焦描边 |
| `default` | `--default` | `default/default` | `color/alpha/white/10` | `rgb(255 255 255 / 10%)` | 默认中性背景 |
| `default-hover` | `--default-hover` | `default/hover` | `color/alpha/white/15` | `rgb(255 255 255 / 15%)` | 中性 hover 背景 |
| `default-foreground` | `--default-foreground` | `default/foreground` | `foreground/default` | `#ffffff` | 中性背景上的文字 / 图标 |
| `accent` | `--accent` | `accent/default` | `color/brand/500` | `#32ec9e` | 品牌强调色背景 |
| `accent-hover` | `--accent-hover` | `accent/hover` | `color/brand/400` | `#39faaa` |  |
| `accent-foreground` | `--accent-foreground` | `accent/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `accent-border` | `--accent-border` | `accent/border` | `color/brand/500` | `#32ec9e` |  |
| `accent-soft` | `--accent-soft` | `accent/soft` | `color/alpha/brand/15` | `rgb(50 236 158 / 15%)` |  |
| `accent-soft-hover` | `--accent-soft-hover` | `accent/soft-hover` | `color/alpha/brand/20` | `rgb(50 236 158 / 20%)` |  |
| `accent-soft-foreground` | `--accent-soft-foreground` | `accent/soft-foreground` | `color/brand/500` | `#32ec9e` | soft 背景上的文字 / 图标 |
| `accent-soft-border` | `--accent-soft-border` | `accent/soft-border` | `color/alpha/brand/30` | `rgb(50 236 158 / 30%)` |  |
| `success` | `--success` | `success/default` | `color/brand/500` | `#32ec9e` | 成功状态背景 |
| `success-hover` | `--success-hover` | `success/hover` | `color/brand/300` | `#5ffeb3` |  |
| `success-foreground` | `--success-foreground` | `success/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `success-soft` | `--success-soft` | `success/soft` | `color/alpha/brand/15` | `rgb(50 236 158 / 15%)` |  |
| `success-soft-hover` | `--success-soft-hover` | `success/soft-hover` | `color/alpha/brand/20` | `rgb(50 236 158 / 20%)` |  |
| `success-soft-foreground` | `--success-soft-foreground` | `success/soft-foreground` | `color/brand/500` | `#32ec9e` | soft 背景上的文字 / 图标 |
| `warning` | `--warning` | `warning/default` | `color/yellow/500` | `#ffc800` | 警告 / 提醒 / 注意 背景色 |
| `warning-hover` | `--warning-hover` | `warning/hover` | `color/yellow/400` | `#ffd47b` |  |
| `warning-foreground` | `--warning-foreground` | `warning/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `warning-border` | `--warning-border` | `warning/border` | `color/yellow/500` | `#ffc800` |  |
| `warning-soft` | `--warning-soft` | `warning/soft` | `color/alpha/yellow/15` | `rgb(255 200 0 / 15%)` |  |
| `warning-soft-hover` | `--warning-soft-hover` | `warning/soft-hover` | `color/alpha/yellow/20` | `rgb(255 200 0 / 20%)` |  |
| `warning-soft-foreground` | `--warning-soft-foreground` | `warning/soft-foreground` | `color/yellow/500` | `#ffc800` | soft 背景上的文字 / 图标 |
| `warning-soft-border` | `--warning-soft-border` | `warning/soft-border` | `color/alpha/yellow/30` | `rgb(255 200 0 / 30%)` |  |
| `danger` | `--danger` | `danger/default` | `color/red/500` | `#fc5659` | 错误 / 危险 / 删除 背景色 |
| `danger-hover` | `--danger-hover` | `danger/hover` | `color/red/400` | `#fc6869` |  |
| `danger-foreground` | `--danger-foreground` | `danger/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `danger-border` | `--danger-border` | `danger/border` | `color/red/500` | `#fc5659` |  |
| `danger-soft` | `--danger-soft` | `danger/soft` | `color/alpha/red/15` | `rgb(255 81 84 / 15%)` |  |
| `danger-soft-hover` | `--danger-soft-hover` | `danger/soft-hover` | `color/alpha/red/20` | `rgb(255 81 84 / 20%)` |  |
| `danger-soft-foreground` | `--danger-soft-foreground` | `danger/soft-foreground` | `color/red/500` | `#fc5659` | soft 背景上的文字 / 图标 |
| `danger-soft-border` | `--danger-soft-border` | `danger/soft-border` | `color/alpha/red/50` | `rgb(255 81 84 / 50%)` |  |
| `link` | `--link` | `link/default` | `color/blue/500` | `#368eee` | 链接文字 |
| `link-hover` | `--link-hover` | `link/hover` | `color/blue/400` | `#6ea4f6` | 链接文字 hover |
| `extended-white` | `--extended-white` | `extended/white/default` | `color/white` | `#ffffff` | 白色功能背景 / 白色按钮背景 |
| `extended-white-hover` | `--extended-white-hover` | `extended/white/hover` | `color/alpha/white/90` | `rgb(255 255 255 / 90%)` | 白色功能背景 hover |
| `extended-white-foreground` | `--extended-white-foreground` | `extended/white/foreground` | `foreground/inverse` | `#000000` |  |
| `extended-black` | `--extended-black` | `extended/black/default` | `color/alpha/black/30` | `rgb(0 0 0 / 30%)` | 黑色半透明功能背景 / 黑色遮罩按钮背景 |
| `extended-black-hover` | `--extended-black-hover` | `extended/black/hover` | `color/alpha/black/40` | `rgb(0 0 0 / 40%)` | 黑色半透明功能背景 hover |
| `extended-black-foreground` | `--extended-black-foreground` | `extended/black/foreground` | `foreground/default` | `#ffffff` |  |
| `extended-red-soft-foreground` | `--extended-red-soft-foreground` | `extended/red/foreground` | `color/red/500` | `#fc5659` | soft 背景上的文字 / 图标 |
| `extended-blue` | `--extended-blue` | `extended/blue/default` | `color/blue/500` | `#368eee` |  |
| `extended-blue-hover` | `--extended-blue-hover` | `extended/blue/hover` | `color/blue/400` | `#6ea4f6` |  |
| `extended-blue-foreground` | `--extended-blue-foreground` | `extended/blue/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-blue-soft` | `--extended-blue-soft` | `extended/blue/soft` | `color/alpha/blue/15` | `rgb(54 142 238 / 15%)` |  |
| `extended-blue-soft-hover` | `--extended-blue-soft-hover` | `extended/blue/soft-hover` | `color/alpha/blue/20` | `rgb(54 142 238 / 20%)` |  |
| `extended-blue-soft-foreground` | `--extended-blue-soft-foreground` | `extended/blue/soft-foreground` | `color/blue/500` | `#368eee` | soft 背景上的文字 / 图标 |
| `extended-yellow` | `--extended-yellow` | `extended/yellow/default` | `color/yellow/500` | `#ffc800` |  |
| `extended-yellow-hover` | `--extended-yellow-hover` | `extended/yellow/hover` | `color/yellow/400` | `#ffd47b` |  |
| `extended-yellow-foreground` | `--extended-yellow-foreground` | `extended/yellow/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-yellow-soft` | `--extended-yellow-soft` | `extended/yellow/soft` | `color/alpha/yellow/15` | `rgb(255 200 0 / 15%)` |  |
| `extended-yellow-soft-hover` | `--extended-yellow-soft-hover` | `extended/yellow/soft-hover` | `color/alpha/yellow/20` | `rgb(255 200 0 / 20%)` |  |
| `extended-yellow-soft-foreground` | `--extended-yellow-soft-foreground` | `extended/yellow/soft-foreground` | `color/yellow/500` | `#ffc800` | soft 背景上的文字 / 图标 |
| `extended-orange` | `--extended-orange` | `extended/orange/default` | `color/orange/500` | `#ff7f14` |  |
| `extended-orange-hover` | `--extended-orange-hover` | `extended/orange/hover` | `color/orange/400` | `#ff9d71` |  |
| `extended-orange-foreground` | `--extended-orange-foreground` | `extended/orange/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-orange-soft` | `--extended-orange-soft` | `extended/orange/soft` | `color/alpha/orange/15` | `rgb(255 127 20 / 15%)` |  |
| `extended-orange-soft-hover` | `--extended-orange-soft-hover` | `extended/orange/soft-hover` | `color/alpha/orange/20` | `rgb(255 127 20 / 20%)` |  |
| `extended-orange-soft-foreground` | `--extended-orange-soft-foreground` | `extended/orange/soft-foreground` | `color/orange/500` | `#ff7f14` | soft 背景上的文字 / 图标 |
| `extended-purple` | `--extended-purple` | `extended/purple/default` | `color/purple/500` | `#894ff6` |  |
| `extended-purple-hover` | `--extended-purple-hover` | `extended/purple/hover` | `color/purple/400` | `#9d76f8` |  |
| `extended-purple-foreground` | `--extended-purple-foreground` | `extended/purple/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-purple-soft` | `--extended-purple-soft` | `extended/purple/soft` | `color/alpha/purple/15` | `rgb(137 79 246 / 15%)` |  |
| `extended-purple-soft-hover` | `--extended-purple-soft-hover` | `extended/purple/soft-hover` | `color/alpha/purple/20` | `rgb(137 79 246 / 20%)` |  |
| `extended-purple-soft-foreground` | `--extended-purple-soft-foreground` | `extended/purple/soft-foreground` | `color/purple/500` | `#894ff6` | soft 背景上的文字 / 图标 |
| `extended-pink` | `--extended-pink` | `extended/pink/default` | `color/pink/500` | `#ea348f` |  |
| `extended-pink-hover` | `--extended-pink-hover` | `extended/pink/hover` | `color/pink/400` | `#f368a4` |  |
| `extended-pink-foreground` | `--extended-pink-foreground` | `extended/pink/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-pink-soft` | `--extended-pink-soft` | `extended/pink/soft` | `color/alpha/pink/15` | `rgb(234 52 143 / 15%)` |  |
| `extended-pink-soft-hover` | `--extended-pink-soft-hover` | `extended/pink/soft-hover` | `color/alpha/pink/20` | `rgb(234 52 143 / 20%)` |  |
| `extended-pink-soft-foreground` | `--extended-pink-soft-foreground` | `extended/pink/soft-foreground` | `color/pink/500` | `#ea348f` | soft 背景上的文字 / 图标 |
| `extended-teal` | `--extended-teal` | `extended/teal/default` | `color/teal/500` | `#13aeb9` |  |
| `extended-teal-hover` | `--extended-teal-hover` | `extended/teal/hover` | `color/teal/400` | `#17c3cf` |  |
| `extended-teal-foreground` | `--extended-teal-foreground` | `extended/teal/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-teal-soft` | `--extended-teal-soft` | `extended/teal/soft` | `color/alpha/teal/15` | `rgb(19 174 185 / 15%)` |  |
| `extended-teal-soft-hover` | `--extended-teal-soft-hover` | `extended/teal/soft-hover` | `color/alpha/teal/20` | `rgb(19 174 185 / 20%)` |  |
| `extended-teal-soft-foreground` | `--extended-teal-soft-foreground` | `extended/teal/soft-foreground` | `color/teal/500` | `#13aeb9` | soft 背景上的文字 / 图标 |
| `extended-lime` | `--extended-lime` | `extended/lime/default` | `color/lime/500` | `#bcdd3a` |  |
| `extended-lime-hover` | `--extended-lime-hover` | `extended/lime/hover` | `color/lime/400` | `#c5e83d` |  |
| `extended-lime-foreground` | `--extended-lime-foreground` | `extended/lime/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-lime-soft` | `--extended-lime-soft` | `extended/lime/soft` | `color/alpha/lime/15` | `rgb(188 221 58 / 15%)` |  |
| `extended-lime-soft-hover` | `--extended-lime-soft-hover` | `extended/lime/soft-hover` | `color/alpha/lime/20` | `rgb(188 221 58 / 20%)` |  |
| `extended-lime-soft-foreground` | `--extended-lime-soft-foreground` | `extended/lime/soft-foreground` | `color/lime/500` | `#bcdd3a` | soft 背景上的文字 / 图标 |
| `extended-orchid` | `--extended-orchid` | `extended/orchid/default` | `color/orchid/500` | `#c044e4` |  |
| `extended-orchid-hover` | `--extended-orchid-hover` | `extended/orchid/hover` | `color/orchid/400` | `#cb70eb` |  |
| `extended-orchid-foreground` | `--extended-orchid-foreground` | `extended/orchid/foreground` | `foreground/inverse` | `#000000` | 反色文本 / 图标，用于浅色背景、强调色背景、功能色实色背景 |
| `extended-orchid-soft` | `--extended-orchid-soft` | `extended/orchid/soft` | `color/alpha/orchid/15` | `rgb(192 68 228 / 15%)` |  |
| `extended-orchid-soft-hover` | `--extended-orchid-soft-hover` | `extended/orchid/soft-hover` | `color/alpha/orchid/20` | `rgb(192 68 228 / 20%)` |  |
| `extended-orchid-soft-foreground` | `--extended-orchid-soft-foreground` | `extended/orchid/soft-foreground` | `color/orchid/500` | `#c044e4` | soft 背景上的文字 / 图标 |
| `extended-yellow-soft-border` | `--extended-yellow-soft-border` | `extended/yellow/soft-border` | `color/alpha/yellow/30` | `rgb(255 200 0 / 30%)` |  |

其他：`--disabled-opacity: 0.5`（Figma `disabled-opacity` = 50）。

## 文字样式（typo-*）

| 工具类 | Figma 样式 | 字体 | 字号 / 行高 | 字重 | 字距 |
|---|---|---|---|---|---|
| `typo-display-72` | Display/72 | Instrument Serif | 72 / 78 | 400 | -1px |
| `typo-display-64` | Display/64 | Instrument Serif | 64 / 70 | 400 | -1px |
| `typo-display-56` | Display/56 | Instrument Serif | 56 / 64 | 400 | -1px |
| `typo-display-48` | Display/48 | Instrument Serif | 48 / 56 | 400 | -1px |
| `typo-display-40` | Display/40 | Instrument Serif | 40 / 46 | 400 | -1px |
| `typo-display-36` | Display/36 | Instrument Serif | 36 / 42 | 400 | -1px |
| `typo-heading-40-700` | Heading/40-700 | Host Grotesk | 40 / 46 | 700 | 0px |
| `typo-heading-40-500` | Heading/40-500 | Host Grotesk | 40 / 46 | 500 | 0px |
| `typo-heading-40-400` | Heading/40-400 | Host Grotesk | 40 / 46 | 400 | 0px |
| `typo-heading-36-700` | Heading/36-700 | Host Grotesk | 36 / 42 | 700 | 0px |
| `typo-heading-36-500` | Heading/36-500 | Host Grotesk | 36 / 42 | 500 | 0px |
| `typo-heading-36-400` | Heading/36-400 | Host Grotesk | 36 / 42 | 400 | 0px |
| `typo-heading-32-700` | Heading/32-700 | Host Grotesk | 32 / 38 | 700 | 0px |
| `typo-heading-32-500` | Heading/32-500 | Host Grotesk | 32 / 38 | 500 | 0px |
| `typo-heading-32-400` | Heading/32-400 | Host Grotesk | 32 / 38 | 400 | 0px |
| `typo-heading-24-700` | Heading/24-700 | Host Grotesk | 24 / 32 | 700 | 0px |
| `typo-heading-24-500` | Heading/24-500 | Host Grotesk | 24 / 32 | 500 | 0px |
| `typo-heading-24-400` | Heading/24-400 | Host Grotesk | 24 / 32 | 400 | 0px |
| `typo-heading-20-700` | Heading/20-700 | Host Grotesk | 20 / 26 | 700 | 0px |
| `typo-heading-20-500` | Heading/20-500 | Host Grotesk | 20 / 26 | 500 | 0px |
| `typo-heading-20-400` | Heading/20-400 | Host Grotesk | 20 / 26 | 400 | 0px |
| `typo-heading-18-700` | Heading/18-700 | Host Grotesk | 18 / 24 | 700 | 0px |
| `typo-heading-18-500` | Heading/18-500 | Host Grotesk | 18 / 24 | 500 | 0px |
| `typo-heading-18-400` | Heading/18-400 | Host Grotesk | 18 / 24 | 400 | 0px |
| `typo-body-16-700` | Body/16-700 | Host Grotesk | 16 / 24 | 700 | 0px |
| `typo-body-16-500` | Body/16-500 | Host Grotesk | 16 / 24 | 500 | 0px |
| `typo-body-16-400` | Body/16-400 | Host Grotesk | 16 / 24 | 400 | 0px |
| `typo-body-14-700` | Body/14-700 | Host Grotesk | 14 / 20 | 700 | 0px |
| `typo-body-14-500` | Body/14-500 | Host Grotesk | 14 / 20 | 500 | 0px |
| `typo-body-14-400` | Body/14-400 | Host Grotesk | 14 / 20 | 400 | 0px |
| `typo-body-12-700` | Body/12-700 | Host Grotesk | 12 / 18 | 700 | 0px |
| `typo-body-12-500` | Body/12-500 | Host Grotesk | 12 / 18 | 500 | 0px |
| `typo-body-12-400` | Body/12-400 | Host Grotesk | 12 / 18 | 400 | 0px |
| `typo-body-10-700` | Body/10-700 | Host Grotesk | 10 / 14 | 700 | 0px |
| `typo-body-10-500` | Body/10-500 | Host Grotesk | 10 / 14 | 500 | 0px |
| `typo-body-10-400` | Body/10-400 | Host Grotesk | 10 / 14 | 400 | 0px |
| `typo-code-16-700` | Code/16-700 | Roboto Mono | 16 / 24 | 700 | 0px |
| `typo-code-16-500` | Code/16-500 | Roboto Mono | 16 / 24 | 500 | 0px |
| `typo-code-16-400` | Code/16-400 | Roboto Mono | 16 / 24 | 400 | 0px |
| `typo-code-14-700` | Code/14-700 | Roboto Mono | 14 / 20 | 700 | 0px |
| `typo-code-14-500` | Code/14-500 | Roboto Mono | 14 / 20 | 500 | 0px |
| `typo-code-14-400` | Code/14-400 | Roboto Mono | 14 / 20 | 400 | 0px |
| `typo-code-12-700` | Code/12-700 | Roboto Mono | 12 / 18 | 700 | 0px |
| `typo-code-12-500` | Code/12-500 | Roboto Mono | 12 / 18 | 500 | 0px |
| `typo-code-12-400` | Code/12-400 | Roboto Mono | 12 / 18 | 400 | 0px |
| `typo-code-10-700` | Code/10-700 | Roboto Mono | 10 / 14 | 700 | 0px |
| `typo-code-10-500` | Code/10-500 | Roboto Mono | 10 / 14 | 500 | 0px |
| `typo-code-10-400` | Code/10-400 | Roboto Mono | 10 / 14 | 400 | 0px |

## 圆角

| 工具类 | 值 | Figma |
|---|---|---|
| `rounded-none` | 0px | `radius/none` |
| `rounded-xs` | 2px | `radius/xs` |
| `rounded-sm` | 4px | `radius/sm` |
| `rounded-sm-plus` | 6px | `radius/6` |
| `rounded-md` | 8px | `radius/md` |
| `rounded-lg` | 12px | `radius/lg` |
| `rounded-xl` | 16px | `radius/xl` |
| `rounded-2xl` | 24px | `radius/2xl` |
| `rounded-3xl` | 32px | `radius/3xl` |
| `rounded-full` | 999px | `radius/full` |

## 间距

Figma `space/N`（px）→ Tailwind 刻度 N/4：

| Figma | px | Tailwind 刻度 | 示例 |
|---|---|---|---|
| `space/0` | 0 | 0 | `p-0` |
| `space/1` | 1 | px | `p-px` |
| `space/2` | 2 | 0.5 | `p-0.5` |
| `space/4` | 4 | 1 | `p-1` |
| `space/6` | 6 | 1.5 | `p-1.5` |
| `space/8` | 8 | 2 | `p-2` |
| `space/12` | 12 | 3 | `p-3` |
| `space/16` | 16 | 4 | `p-4` |
| `space/20` | 20 | 5 | `p-5` |
| `space/24` | 24 | 6 | `p-6` |
| `space/28` | 28 | 7 | `p-7` |
| `space/32` | 32 | 8 | `p-8` |
| `space/40` | 40 | 10 | `p-10` |
| `space/48` | 48 | 12 | `p-12` |
| `space/64` | 64 | 16 | `p-16` |
| `space/80` | 80 | 20 | `p-20` |
| `space/96` | 96 | 24 | `p-24` |
| `space/128` | 128 | 32 | `p-32` |
| `space/160` | 160 | 40 | `p-40` |

## 阴影 / 模糊

| 工具类 | Figma | 值 | 说明 |
|---|---|---|---|
| `shadow-100` | `shadow/100` | `0 2px 16px 0 rgb(0 0 0 / 20%)` | 小组件微阴影 |
| `shadow-200` | `shadow/200` | `0 16px 32px 0 rgb(0 0 0 / 25%), 0 4px 8px 0 rgb(0 0 0 / 35%)` | 弹窗 / 抽屉 / 浮层阴影 |
| `backdrop-blur-xs` | `blur/xs` | 5px（Figma 10） | |
| `backdrop-blur-sm` | `blur/sm` | 10px（Figma 20） | |
| `backdrop-blur-md` | `blur/md` | 20px（Figma 40） | |
| `backdrop-blur-lg` | `blur/lg` | 30px（Figma 60） | |
| `backdrop-blur-xl` | `blur/xl` | 40px（Figma 80） | |
| `backdrop-blur-2xl` | `blur/2xl` | 50px（Figma 100） | |
| `backdrop-blur-3xl` | `blur/3xl` | 75px（Figma 150） | |
| `backdrop-blur-4xl` | `blur/4xl` | 100px（Figma 200） | |

## 断点与栅格

| 前缀 | 宽度 | 设备 |
|---|---|---|
| （无） | < 768 | mobile |
| `md:` | ≥ 768 | tablet |
| `xl:` | ≥ 1280 | desktop |

| 栅格 | 列 | 间距 | 边距 | Figma |
|---|---|---|---|---|
| 工作台栅格（mobile） | 4 | 12 | 12 | `platform/mobile` |
| 工作台栅格（tablet） | 8 | 16 | 16 | `platform/tablet` |
| 工作台栅格（desktop） | 12 | 16 | 24 | `platform/desktop` |
| 官网栅格（desktop） | 8 | 24 | 64 | `portal/desktop` |

## 原子色板（仅供查阅，代码中禁止直接使用）

| 色板 | 50 | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 | 950 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| neutral | #f1f1f1 | #dfdfdf | #c4c4c4 | #a6a6a6 | #8b8b8b | #6f6f6f | #575757 | #3e3e3e | #282828 | #111111 | #000000 |
| brand | #e8fff1 | #dcffea | #a2fecc | #5ffeb3 | #39faaa | #32ec9e | #25b97b | #188859 | #0c5939 | #04311d | #011c0f |
| yellow | #fff8ef | #fff5e7 | #ffe8c3 | #ffdea3 | #ffd47b | #ffc800 | #c99d00 | #947300 | #614b00 | #362800 | #201600 |
| red | #fff0f0 | #ffe1e1 | #ffc3c3 | #ffa2a3 | #fc6869 | #fc5659 | #e60011 | #ae000a | #790004 | #490002 | #310001 |
| blue | #eff4fe | #dfe8fd | #bacffa | #97baf8 | #6ea4f6 | #368eee | #2971bf | #1c538f | #103863 | #06203c | #031428 |
| orange | #fff4f1 | #ffe6de | #ffd0c1 | #ffb59a | #ff9d71 | #ff7f14 | #cd6300 | #984800 | #693000 | #3b1800 | #280e00 |
| purple | #f2effe | #e5defd | #cdbefc | #b399fa | #9d76f8 | #894ff6 | #751dea | #5814b3 | #3f0c84 | #250453 | #18023a |
| pink | #fdedf2 | #fbdee7 | #f8bbd0 | #f593b8 | #f368a4 | #ea348f | #ba2771 | #8d1b54 | #66113b | #3d0722 | #280314 |
| teal | #d7faff | #b3f7ff | #1eedfc | #1ad8e5 | #17c3cf | #13aeb9 | #0d8992 | #07666d | #03454a | #012629 | #001619 |
| lime | #f2ffd5 | #ebfebb | #d5fa43 | #cdf140 | #c5e83d | #bcdd3a | #93ae2c | #6b7f1d | #465310 | #252d05 | #141a02 |
| orchid | #f7edfc | #f1dffa | #e3bbf5 | #d799f0 | #cb70eb | #c044e4 | #9834b5 | #75268c | #511861 | #320b3d | #1f0527 |

## 命名变更对照（代码名 ≠ Figma 名）

| Figma | 代码 | 原因 |
|---|---|---|
| `radius/6` | `rounded-sm-plus` | 与 xs/sm/md 命名体系统一 |
| `extended/red/foreground` | `extended-red-soft-foreground` | 实际语义是 soft 背景上的文字色 |
| `*/default（如 accent/default）` | `去掉 -default（accent）` | 与 HeroUI v3 主题变量命名一致 |
| `border/focus` | `focus` | 与 HeroUI v3 主题变量命名一致 |
| `surface/backdrop` | `backdrop` | 与 HeroUI v3 主题变量命名一致 |
