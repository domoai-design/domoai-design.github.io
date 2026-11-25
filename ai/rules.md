# DomoAI Design System 规则

这个仓库是 DomoAI Design System V3.0 的代码实现，**也是唯一事实来源**。规范变更先改代码，设计师再同步 Figma。

## 写页面前先读

1. `/ai/components.md`：有哪些组件，props 怎么传，什么时候用。
2. `/ai/tokens.md`：颜色、文字样式、圆角、间距、断点对应的类名。
3. `/ai/icons.md`：可用图标。

## 硬性规则（`pnpm lint` 会检查 apps/ 下的代码）

| 要做 | 不要做 |
|---|---|
| 组件从 `@domoai/ui` 引入 | 直接 `import … from "@heroui/react"` |
| 颜色用语义类：`bg-surface`、`text-foreground-secondary`、`border-border` | `bg-blue-500`、`#fff`、`rgb()`、`bg-[#…]`（Tailwind 默认色板已经移除） |
| 文字用 `typo-*`：`typo-body-14-500`、`typo-heading-24-700` | `text-sm font-medium` 这类拆开的写法 |
| 圆角用 `rounded-xs/sm/sm-plus/md/lg/xl/2xl/3xl/full` | `rounded-[10px]` |
| 间距用 Tailwind 4px 刻度（Figma space/12 → `p-3`） | 不在 Figma 间距表里的数值 |
| 响应式只用 `md:`（≥768 tablet）和 `xl:`（≥1280 desktop），默认写 mobile | `sm:`、`lg:`、`2xl:` |
| 图标用 `@domoai/icons`，颜色跟随 `text-*` | 内联 SVG、第三方图标库 |
| 组件的 `className` 只用来调布局（margin、flex、宽度） | 用 `className` 改组件的颜色、圆角、高度 |

确实需要豁免的单行，在行尾加 `// design-lint-ignore <原因>`。

## 设计系统里没有你要的东西时

不要在页面里自己拼一个。按下面的顺序处理：

1. 先看能不能用现有组件组合出来（Agent 模型选择面板就是 Dropdown、Tag、SelectionGroup 组合出来的）。
2. 组合不出来的话，在 `packages/ui` 新增组件或变体（流程见下一节），新增的同时通知设计师在 Figma 补齐。
