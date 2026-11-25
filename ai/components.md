# DomoAI Components

所有组件从 `@domoai/ui` 引入：`import { Button, Input } from "@domoai/ui";`；图标从 `@domoai/icons` 引入。

| 组件 | 用途 | Figma |
|---|---|---|
| [Button](#button) | 触发一个操作。10 种样式 × 4 个尺寸，可带左右图标或纯图标。 | [Button](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=384-13681) |
| [Input](#input) | 单行文本输入。3 种外观，支持左右图标、右侧文字操作（如获取验证码）、辅助说明与错误提示。 | [Input](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=663-13773) |
| [Dropdown](#dropdown) | 点击触发器后弹出的选项菜单。菜单项支持图标 / 缩略图、标题、标签、描述和右侧内容，可单选 / 多选。 | [Dropdown](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1347-3225) |
| [Tag](#tag) | 状态、分类或标记的小标签。filled / soft 两种填充 × 13 种颜色 × 3 个尺寸。 | [Tag](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=444-3189) |
| [Switch](#switch) | 两种状态之间立即切换的开关（如月付 / 年付）。sm / md / lg 三个尺寸；开为 accent 轨道，关为白 10% 轨道，禁用 50%。 | [Switch](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1347-6258) |
| [Slider](#slider) | 滑块。`Slider` 支持分档（marks，如 Pricing 的 8,000 / 16,000 / 24,000 Credits）和连续数值；`TickSlider` 是带刻度的速度滑块（Speed 1.0x）；`SliderHandle` 是拖拽手柄条。 | [Slider](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=7464-116676) |
| [Stepper](#stepper) | 用减号 / 加号调整一个整数（如团队席位数）。 | [（待补）Pricing / Team 卡片 UploadPlan](https://www.figma.com/design/pOmJayvXkysQFVncy6xOfp/DomoAI-Web-UI-V3.0?node-id=14208-80834) |
| [PricingButton](#pricingbutton) | 价格卡里的购买按钮（Get Pro / Current）。44px 高、12px 圆角。 | [Pricing](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=3508-32930) |
| [SelectionGroup](#selectiongroup) | 一组选项，四种形态对应 Figma `type`：segmentedOption 分段胶囊（Monthly / Yearly）、selectableCard 平分宽度的卡片（Agent 面板的 Ratio / Resolution / Audio）、radio 单选、checkbox 多选。 | [Radio](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=683-1175) |
| [Accordion](#accordion) | 卡片式折叠问答列表（FAQ）。点击问题展开答案，默认一次只展开一项。 | [FAQ](https://www.figma.com/design/pOmJayvXkysQFVncy6xOfp/DomoAI-Web-UI-V3.0?node-id=13570-37090) |
| [Modal](#modal) | 居中弹出的对话框：遮罩 + surface 面板。4 种类型（default 确认 / secondary 欢迎插画 / tertiary 带分割线的业务面板 / tutorial 教程），内容用 ModalHeader、ModalBody、ModalFooter、ModalImage、ModalChecklist 组合。 | [Modal](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=692-2182) |
| [AnnouncementBanner](#announcementbanner) | 页面顶部的全宽公告条：一句文案 + 一个行动按钮 + 关闭按钮。用于产品公告、营销活动。 | [AnnouncementBanner](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=14127-7953) |
| [TextArea](#textarea) | 多行文本输入（如生成提示词）。带标题、必填星号、帮助图标、头部操作、底部插槽、字数统计与拖动缩放；speech 变体用于配音段落。 | [TextArea](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=664-1274) |
| [InputTag](#inputtag) | 标签输入框：输入文字后回车生成标签，空输入时 Backspace 删除最后一个，点击 × 删除。支持数量上限计数、右侧图标、辅助说明与错误提示。 | [InputTag](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1509-1654) |
| [Toast](#toast) | 操作结果的即时反馈，自动消失。在应用根部渲染一次 `<ToastProvider />`，之后在任意位置调用 `toast.success / failed / tips(...)`。基于 HeroUI Toast 队列：最多同时显示 3 条，悬停暂停计时。 | [Toast](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=664-4866) |
| [Alert](#alert) | 页面内的静态提示条：图标 + 一段说明文字。`warning` 用于限制 / 风险提醒，`tip` 用于中性补充说明。 | [Alert](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1954-8179) |
| [Skeleton](#skeleton) | 内容加载占位。基础 `Skeleton` 色块 + 4 个预设组合：SkeletonCard、SkeletonTextContent、SkeletonUserProfile、SkeletonListItems。默认带扫光动画。 | [Skeleton](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=11063-228333) |
| [Checkbox](#checkbox) | 多选勾选框（圆形）。default / assets 两种外观 × sm / md 两个尺寸，支持未选、半选、选中；可带右侧文字，多个用 CheckboxGroup 组合。 | [Radio](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=683-1046) |
| [Radio](#radio) | 单选圆点。sm / md 两个尺寸，可带右侧文字；必须放在 RadioGroup 中使用（方向键切换）。 | [Radio](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=6023-128004) |
| [Tabs](#tabs) | 标签页：在同一区域切换几组平级内容。primary（品牌色下划线）/ secondary（胶囊分段）/ modal（弹窗内白色下划线）× web / mobile 两种密度，标签可带计数徽标。 | [Tabs](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1202-3129) |
| [Badge](#badge) | 数字徽标与红点。accent / neutral / dot 三种样式 × sm / md 两个尺寸；可单独跟在文字后，也可用 BadgeAnchor 挂在图标按钮右上角。 | [Badge](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=726-8033) |
| [Link](#link) | 文字链接，用于页面跳转。default / blue 两种颜色 × 4 个尺寸，可带左右图标或纯图标；支持 Next.js 客户端路由。 | [Button](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=6474-51455) |
| [Breadcrumbs](#breadcrumbs) | 面包屑导航：显示当前页面在层级中的位置，前面的层级可点击返回。 | [Breadcrumbs](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=9721-142865) |
| [Separator](#separator) | 分割线：横向或竖向的 1px 线，可在中间放一段文字（如登录方式之间的 OR）。三种强度。 | [Separator](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=9608-136704) |
| [Indicator](#indicator) | 轮播图 / 横滑卡片底部的分页指示器。primary 为圆点，secondary 的当前项为自动播放进度条；鼠标移入时外扩为深色胶囊。 | [Indicator](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=949-6458) |
| [Drawer](#drawer) | 移动端底部抽屉：遮罩 + 顶部圆角 surface 面板，带拖拽条，可下拉关闭。内容用 DrawerHeader、DrawerBody、DrawerFooter 组合。 | [Drawer](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1782-3130) |
| [Popover](#popover) | 新手引导气泡：带箭头指向触发元素，可含标题、正文、配图、步骤进度和上一步 / 下一步按钮。12 个方向。 | [Popover](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=745-9897) |
| [Tooltip](#tooltip) | 悬停或键盘聚焦时显示的简短文字提示，可在文字右侧带一个 16px 图标。无箭头。 | [Tooltip](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=744-4723) |
| [Upload](#upload) | 素材上传区：拖拽 / 点击 / 粘贴选择图片、视频、音频，显示上传中与已上传预览，可删除、替换。r2v 模式支持多素材网格（最多 50 个）。只负责选文件与预览，不做网络上传。 | [Upload](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1545-2447) |
| [UploadMedia](#uploadmedia) | 已上传图片 / 视频的缩略图：左上角名称角标，右上角删除、右下角编辑。web 悬停显示按钮，mobile 常显。 | [Upload](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=12906-88969) |
| [AudioPlayer](#audioplayer) | 胶囊形音频播放条：播放 / 暂停、时间、可拖动进度条（悬停预览），可选音量与全屏按钮。基于原生 audio + React Aria Slider。 | [AudioPlayer](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=726-8112) |
| [Form](#form) | 表单项 FormField：标签 + 控件 + 说明 / 错误的布局，控件复用 Input / TextArea / RadioGroup / SelectionGroup / CheckboxGroup（对应 Figma `type`）；vertical 标签在上、horizontal 标签在左。标签自动关联控件（aria-labelledby / htmlFor），必填、出错状态自动传给控件。外层用 Form（原生 form + React Aria 校验）。 | [Form](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=7663-49934) |
| [Navigation](#navigation) | 导航基础件：Web 侧栏 SidebarNavigation（NavigationItem、SidebarNavigationIcon、SidebarLogo、SidebarAvatar）、移动端顶栏 TopBarMobile、移动端底部标签栏 Tabber / TabberItem，以及头像 Avatar。 | [Navigation](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=954-8526) |

## Button

触发一个操作。10 种样式 × 4 个尺寸，可带左右图标或纯图标。

Figma：[Button / 384:13681](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=384-13681)

**何时使用**

- 页面主操作用 `primary`，一个区域最多一个 primary。
- 次要操作用 `secondary` / `outline` / `ghost`。
- 破坏性操作（删除等）用 `primary-danger`、`outline-danger` 或 `ghost-danger`。
- 深色图片 / 视频上方的按钮用 `primary-white` 或 `secondary-black`。
- 纯图标按钮必须加 `aria-label`。

**不要**

- 不要用 className 改按钮颜色、圆角、高度；需要新样式先在设计系统中新增变体。
- 不要把链接写成 Button；跳转用 Link 组件。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"primary" \| "secondary" \| "outline" \| "ghost" \| "primary-white" \| "primary-danger" \| "secondary-black" \| "outline-accent" \| "outline-danger" \| "ghost-danger"` | `"primary"` | 视觉样式 | variant |
| `size` | `"xs" \| "sm" \| "md" \| "lg"` | `"md"` | 高度 28 / 32 / 36 / 44px | size |
| `isIconOnly` | `boolean` | `false` | 纯图标正方形按钮，children 传图标 | isIconOnly |
| `startIcon` | `ReactNode` | — | 左侧图标 | showStartIcon |
| `endIcon` | `ReactNode` | — | 右侧图标 | showEndIcon |
| `isDisabled` | `boolean` | `false` | 禁用（整体 50% 透明度） | state=disabled |
| `isPending` | `boolean` | `false` | 加载中，禁止交互 | — |
| `fullWidth` | `boolean` | `false` | 撑满父容器宽度 | — |
| `onPress` | `(e: PressEvent) => void` | — | 点击回调（React Aria，兼容键盘与触屏） | — |

**主按钮**

```tsx
<Button variant="primary" startIcon={<CubeLineIcon />}>Generate</Button>
```

**纯图标**

```tsx
<Button variant="ghost" size="sm" isIconOnly aria-label="More"><CubeLineIcon /></Button>
```

**危险操作**

```tsx
<Button variant="outline-danger">Delete</Button>
```

## Input

单行文本输入。3 种外观，支持左右图标、右侧文字操作（如获取验证码）、辅助说明与错误提示。

Figma：[Input / 663:13773](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=663-13773)

**何时使用**

- 默认用 `filled`；放在半透明 / 图片背景上用 `subtle`；需要强调边界时用 `outline`。
- 没有可见 label 时必须传 `aria-label`。
- 验证码等文字操作用 `suffix={<InputAction>…</InputAction>}`。

**不要**

- 不要用 className 改输入框高度、底色或描边。
- 多行输入用 TextArea，不要用 Input。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"filled" \| "subtle" \| "outline"` | `"filled"` | 外观 | variant |
| `placeholder` | `string` | — | 占位文字 | — |
| `startIcon` | `ReactNode` | — | 左侧 16px 图标 | showStartIcon |
| `endIcon` | `ReactNode` | — | 右侧 16px 图标 / 图标按钮 | showEndIcon |
| `suffix` | `ReactNode` | — | 右侧文字操作 | showSuffix |
| `helpText` | `ReactNode` | — | 辅助说明 | showHelpText |
| `isInvalid / errorMessage` | `boolean / ReactNode` | — | 错误态：红色描边、红色文字与提示 | state=error |
| `isDisabled` | `boolean` | — | 禁用（整体 50% 透明度） | state=disabled |
| `value / defaultValue / onChange` | `string / (value: string) => void` | — | 受控 / 非受控值（React Aria TextField） | — |

**基础**

```tsx
<Input aria-label="Name" placeholder="Enter your content" />
```

**验证码**

```tsx
<Input aria-label="Code" placeholder="Code" suffix={<InputAction>Get code</InputAction>} />
```

**错误**

```tsx
<Input aria-label="Email" isInvalid errorMessage="Something went wrong, please try again." />
```

## Dropdown

点击触发器后弹出的选项菜单。菜单项支持图标 / 缩略图、标题、标签、描述和右侧内容，可单选 / 多选。

Figma：[Dropdown / 1347:3225](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1347-3225)

**何时使用**

- 触发器用 <Button>，菜单用 <DropdownMenu>，选项用 <DropdownItem>。
- 需要选择状态时设置 `selectionMode` 与 `selectedKeys`，选中项自动显示对勾。
- 标题后的「NEW」等标记用 Tag（size xs、variant soft）。

**不要**

- 不要手写浮层和列表样式；需要新的菜单样式先在设计系统中新增。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `DropdownMenu.selectionMode` | `"none" \| "single" \| "multiple"` | `"none"` | 选择模式 | — |
| `DropdownMenu.onAction` | `(key: Key) => void` | — | 点击菜单项 | — |
| `DropdownMenu.placement` | `Placement` | `"bottom start"` | 浮层位置 | — |
| `DropdownItem.title` | `ReactNode` | — | 标题 | — |
| `DropdownItem.description` | `ReactNode` | — | 描述 | showDescription |
| `DropdownItem.startContent` | `ReactNode` | — | 28px 图标 | media=icon |
| `DropdownItem.thumbnail` | `string` | — | 38px 缩略图 | media=thumbnail |
| `DropdownItem.tag` | `ReactNode` | — | 标题后的标签 | showTag |
| `DropdownItem.titleIcon / descriptionIcon` | `ReactNode` | — | 14px / 12px 小图标 | showTitleIcon / showDescriptionIcon |
| `DropdownItem.endContent` | `ReactNode` | — | 右侧 20px 内容 | endSlot |
| `DropdownItem.isDisabled` | `boolean` | — | 禁用（50% 透明度） | state=disabled |

**模型选择**

```tsx
<Dropdown>
  <Button variant="secondary">Model</Button>
  <DropdownMenu aria-label="Model" selectionMode="single" defaultSelectedKeys={["auto"]}>
    <DropdownItem id="auto" title="Auto" description="Agent chooses the model that best fits your task." startContent={<CubeLineIcon />} />
    <DropdownItem id="pro" title="Model Pro" description="Ultimate performance" startContent={<CubeLineIcon />} endContent={<RightSmallLineIcon />} />
  </DropdownMenu>
</Dropdown>
```

## Tag

状态、分类或标记的小标签。filled / soft 两种填充 × 13 种颜色 × 3 个尺寸。

Figma：[Tag / 444:3189](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=444-3189)

**何时使用**

- 「NEW」等新功能标记：`<Tag size="xs" color="accent">NEW</Tag>`。
- 会员等级、分类用 extended 颜色（yellow / blue / purple …）。
- 强调程度低用 soft，高用 filled。

**不要**

- 不要把 Tag 当按钮用；可点击的选项用 SelectionGroup（分段 / 选择卡片）。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"soft" \| "filled"` | `"soft"` | 填充方式 | variant |
| `color` | `"default" \| "accent" \| "black" \| "white" \| "danger" \| "yellow" \| "blue" \| "purple" \| "pink" \| "orange" \| "teal" \| "lime" \| "orchid"` | `"default"` | 颜色（filled 无 default/black，soft 无 white） | color |
| `size` | `"xs" \| "sm" \| "md"` | `"sm"` | 高度 18 / 26 / 32px | size |
| `shape` | `"rounded" \| "pill"` | `"rounded"` | rounded：按尺寸 4 / 6px 圆角；pill：全圆角胶囊（营销场景，Figma 待补变体） | — |
| `startIcon` | `ReactNode` | — | 左侧图标 | showStartIcon |
| `onClose / closeIcon` | `() => void / ReactNode` | — | 关闭按钮 | showCloseIcon |

**新功能标记**

```tsx
<Tag size="xs" color="accent">NEW</Tag>
```

**实心**

```tsx
<Tag variant="filled" color="purple">Pro</Tag>
```

## Switch

两种状态之间立即切换的开关（如月付 / 年付）。sm / md / lg 三个尺寸；开为 accent 轨道，关为白 10% 轨道，禁用 50%。

Figma：[Switch / 1347:6258](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1347-6258)

**何时使用**

- 切换后立即生效的设置用 Switch。
- 开关旁边有文字说明时，给 Switch 传 `aria-label`。

**不要**

- 需要“确认 / 提交”才生效的选项不要用 Switch，用 Checkbox。
- 三个以上的互斥选项用 SelectionGroup。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `size` | `"sm" \| "md" \| "lg"` | `"sm"` | 轨道 40×24 / 48×28 / 56×32px，滑块 16 / 20 / 24px | size |
| `isSelected` | `boolean` | — | 受控：是否打开 | isSelected |
| `defaultSelected` | `boolean` | — | 非受控初始值 | — |
| `onChange` | `(isSelected: boolean) => void` | — | 切换回调 | — |
| `isDisabled` | `boolean` | `false` | 禁用（50% 透明度） | state=disabled |

**月付 / 年付**

```tsx
<Switch aria-label="Yearly billing" isSelected={yearly} onChange={setYearly} />
```

**尺寸**

```tsx
<Switch aria-label="Auto upscale" size="lg" defaultSelected />
```

## Slider

滑块。`Slider` 支持分档（marks，如 Pricing 的 8,000 / 16,000 / 24,000 Credits）和连续数值；`TickSlider` 是带刻度的速度滑块（Speed 1.0x）；`SliderHandle` 是拖拽手柄条。

Figma：[Slider / 7464:116676](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=7464-116676)

**何时使用**

- 档位不多（2–6 个）、需要直观对比大小时，用 `Slider` 的 `marks`；选中档位的标签可以带图标（`activeIcon`）。
- 音量、进度等连续数值用不传 `marks` 的 `Slider`（`minValue` / `maxValue` / `step`）。
- 速度、强度这类有固定步长的小范围数值用 `TickSlider`，右侧实时显示数值（`formatValue`）。
- 可拖拽调整尺寸的分隔条、抽屉抓手用 `SliderHandle`（只有外观，拖动逻辑自己处理）。

**不要**

- 不要用 className 改轨道 / 手柄颜色和尺寸。
- `TickSlider` 的刻度数 = (max - min) / step + 1，超过 20 根会显得拥挤，此时改用连续 `Slider`。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `marks` | `{ label: ReactNode; activeIcon?: ReactNode }[]` | — | Slider：分档模式的档位与标签；不传为连续滑块 | — |
| `value / defaultValue` | `number` | — | Slider：当前值（分档模式为档位序号，从 0 开始） | — |
| `onChange / onChangeEnd` | `(value: number) => void` | — | Slider / TickSlider：值变化 / 拖动结束 | — |
| `minValue / maxValue / step` | `number` | `0 / 100 / 1` | Slider 连续模式的范围与步长（TickSlider 默认 0.5 / 2 / 0.1） | — |
| `orientation` | `"horizontal" \| "vertical"` | `"horizontal"` | Slider 连续模式方向 | arrow |
| `aria-label` | `string` | — | 无障碍名称（Slider 必填） | — |
| `label` | `ReactNode` | — | TickSlider：左侧标题（如 Speed） | — |
| `infoIcon` | `ReactNode \| false` | — | TickSlider：标题后的信息图标，默认 InfoCircleLine，false 隐藏 | — |
| `formatValue` | `(value: number) => string` | `v => `${v.toFixed(1)}x`` | TickSlider：右侧数值格式 | — |
| `arrow` | `"horizontal" \| "vertical"` | `"horizontal"` | SliderHandle：方向（120×4 / 4×120），hover 态自动处理 | arrow |
| `isDisabled` | `boolean` | `false` | 禁用 | — |

**Credits 档位**

```tsx
<Slider aria-label="Monthly credits" marks={[{ label: "8,000" }, { label: "16,000" }, { label: "24,000" }]} value={tier} onChange={setTier} />
```

**连续数值**

```tsx
<Slider aria-label="Volume" defaultValue={50} />
```

**速度（带刻度）**

```tsx
<TickSlider label="Speed" value={speed} onChange={setSpeed} />
```

**拖拽手柄**

```tsx
<SliderHandle arrow="vertical" />
```

## Stepper

用减号 / 加号调整一个整数（如团队席位数）。

Figma：[（待补）Pricing / Team 卡片 UploadPlan / 14208:80834](https://www.figma.com/design/pOmJayvXkysQFVncy6xOfp/DomoAI-Web-UI-V3.0?node-id=14208-80834)

**何时使用**

- 数值范围小、通常只加减几步时使用。
- 用 `formatValue` 带上单位（3 Seats）。

**不要**

- 需要直接输入大数字时用 NumberField。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `value` | `number` | — | 当前值（受控） | — |
| `onChange` | `(value: number) => void` | — | 变化回调 | — |
| `min / max / step` | `number` | `0 / ∞ / 1` | 范围与步长；到边界时对应按钮禁用（50% 透明度） | — |
| `formatValue` | `(value: number) => ReactNode` | — | 中间显示的文字 | — |
| `aria-label` | `string` | — | 无障碍名称（必填） | — |

**团队席位**

```tsx
<Stepper aria-label="Seats" value={seats} min={3} onChange={setSeats} formatValue={(v) => `${v} Seats`} />
```

## PricingButton

价格卡里的购买按钮（Get Pro / Current）。44px 高、12px 圆角。

Figma：[Pricing / 3508:32930](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=3508-32930)

**何时使用**

- 只在价格卡（Pricing）里使用，撑满卡片宽度。
- 用户已订阅的套餐用 `isCurrent`，显示 Current 且不可点。

**不要**

- 其他页面的主按钮用通用 Button，不要用 PricingButton。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `isCurrent` | `boolean` | `false` | 当前套餐：中性底、50% 白字、不可点 | state=current |
| `isDisabled` | `boolean` | `false` | 禁用（50% 透明度） | state=disabled |
| `onPress` | `(e: PressEvent) => void` | — | 点击购买 | — |

**购买**

```tsx
<PricingButton onPress={checkout}>Get Pro</PricingButton>
```

**当前套餐**

```tsx
<PricingButton isCurrent>Current</PricingButton>
```

## SelectionGroup

一组选项，四种形态对应 Figma `type`：segmentedOption 分段胶囊（Monthly / Yearly）、selectableCard 平分宽度的卡片（Agent 面板的 Ratio / Resolution / Audio）、radio 单选、checkbox 多选。

Figma：[Radio / 683:1175](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=683-1175)

**何时使用**

- 2–5 个互斥选项、切换后立即生效时用 segmentedOption（宽度随内容）。
- 选项需要撑满面板宽度、或带 24px 图标（比例、分辨率、开关项）时用 selectableCard。
- 需要读清楚每个选项的文字、表单里的单选 / 多选用 radio / checkbox。
- 必须传 `aria-label`，或用 `aria-labelledby` 关联可见标题（如面板里的「Ratio」）。
- 移动端底部平分宽度的套餐切换用 `variant="plain"`。

**不要**

- 只有开 / 关两种状态时用 Switch。
- 选项超过 5 个或文字很长时用 Dropdown。
- 不要用它做页面导航，导航用 Tabs。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `type` | `"segmentedOption" \| "selectableCard" \| "radio" \| "checkbox"` | `"segmentedOption"` | 选项形态 | type |
| `options` | `{ id; label; icon?; labelIcon?; isDisabled? }[]` | — | 选项列表。icon：分段 14px 在文字左侧 / 卡片 24px 在文字上方；labelIcon：卡片文字左侧 12px（Figma showLabelIcon） | showIcon / showLabelIcon |
| `value / defaultValue / onChange` | `K / K[]（checkbox）` | — | 选中项（受控 / 非受控）；checkbox 为数组 | state=selected |
| `size` | `"sm" \| "md" \| "lg"` | `"md"` | 仅 segmentedOption：选项高度 24 / 28 / 32px（lg 为 Body/16） | .SegmentedOption size |
| `variant` | `"filled" \| "plain"` | `"filled"` | 仅 segmentedOption：filled 有 surface/tertiary 底；plain 无底、选项平分宽度、固定 36px | — |
| `isDisabled` | `boolean` | `false` | 整组禁用；单个选项用 option.isDisabled | state=disabled |
| `aria-label / aria-labelledby` | `string` | — | 读屏用的组名（二选一，必填） | — |

**月付 / 年付**

```tsx
<SelectionGroup aria-label="Billing" size="sm" value={billing} onChange={setBilling} options={[{ id: "monthly", label: "Monthly" }, { id: "yearly", label: "Yearly" }]} />
```

**Agent 面板：Ratio**

```tsx
<SelectionGroup type="selectableCard" aria-label="Ratio" value={ratio} onChange={setRatio} options={[{ id: "auto", label: "Auto", icon: <RadioAutoLineIcon /> }, { id: "3:4", label: "3:4", icon: <Ratio3x4LineIcon /> }]} />
```

**Agent 面板：Resolution / Audio**

```tsx
<SelectionGroup type="selectableCard" aria-label="Audio" value={audio} onChange={setAudio} options={[{ id: "on", label: "On" }, { id: "off", label: "Off" }]} />
```

## Accordion

卡片式折叠问答列表（FAQ）。点击问题展开答案，默认一次只展开一项。

Figma：[FAQ / 13570:37090](https://www.figma.com/design/pOmJayvXkysQFVncy6xOfp/DomoAI-Web-UI-V3.0?node-id=13570-37090)

**何时使用**

- FAQ、帮助说明等“问题 + 答案”列表。
- 问题文字写成完整问句，答案保持简短。

**不要**

- 不要把重要信息只放在折叠内容里。
- 表单分组、设置面板不要用 Accordion。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `children` | `AccordionItem[]` | — | 问答项 | — |
| `allowsMultipleExpanded` | `boolean` | `false` | 允许同时展开多项 | — |
| `defaultExpandedKeys` | `string[]` | — | 默认展开的项 id | — |
| `AccordionItem.id / title / children` | `string / ReactNode / ReactNode` | — | 项 id、问题、答案 | — |

**FAQ**

```tsx
<Accordion>
  <AccordionItem id="modes" title="What are Fast Mode and Relax Mode?">Fast Mode uses credits…</AccordionItem>
  <AccordionItem id="promo" title="How to use your promo code?">Enter the code at checkout…</AccordionItem>
</Accordion>
```

## Modal

居中弹出的对话框：遮罩 + surface 面板。4 种类型（default 确认 / secondary 欢迎插画 / tertiary 带分割线的业务面板 / tutorial 教程），内容用 ModalHeader、ModalBody、ModalFooter、ModalImage、ModalChecklist 组合。

Figma：[Modal / 692:2182](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=692-2182)

**何时使用**

- 需要用户立刻注意、或完成一个短任务时使用。
- 二次确认（如停止生成）用 `type="default"`，底部两个 lg 按钮：左 outline 取消，右 primary / primary-danger 确认。
- 欢迎、奖励类弹窗用 `secondary`（插画 + 居中文案）；带工具栏的业务面板用 `tertiary`；纯说明用 `tutorial`。
- 必须提供关闭方式（关闭按钮 / Esc / 点遮罩）。有 `ModalHeader` 时标题自动作为对话框名称，否则传 `aria-label`。

**不要**

- 不要弹窗套弹窗。
- 长表单、复杂流程用 Drawer 或独立页面。
- 不要用 className 改面板颜色、圆角、宽度；需要新宽度先在设计系统中新增类型。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `isOpen / onOpenChange` | `boolean / (open: boolean) => void` | — | 受控打开状态 | — |
| `type` | `"default" \| "secondary" \| "tertiary" \| "tutorial"` | — | 弹窗类型：宽度 480 / 480 / 620 / 420px、关闭按钮位置与插槽内边距。不传 = 自定义内容 | type |
| `appearance` | `"solid" \| "glass"` | `"solid"` | 面板外观：实色（Figma 组件集）或毛玻璃（活动 / 公告类弹窗） | — |
| `isClosable` | `boolean` | `tutorial 以外为 true` | 右上角关闭按钮（ghost md CloseLine） | — |
| `isDismissable` | `boolean` | `true` | 点遮罩关闭 | — |
| `isKeyboardDismissDisabled` | `boolean` | `false` | 禁止 Esc 关闭 | — |
| `size` | `"sm" \| "md" \| "lg"` | `"md"` | 仅自定义内容：面板最大宽度 400 / 480 / 640px | — |
| `portalContainer` | `HTMLElement` | — | 浮层渲染容器，默认 document.body | — |
| `ModalHeader.title / startContent / endContent` | `ReactNode` | — | 头部标题、标题后内容（信息按钮）、右侧内容 | header |
| `ModalBody.children` | `ReactNode` | — | 内容区，过长时内部滚动 | content |
| `ModalFooter.children` | `ReactNode` | — | 底部按钮（自动平分宽度） | footer |
| `ModalImage.src / alt` | `string` | — | tutorial 配图（16:9、radius/md） | image |
| `ModalChecklist.items` | `ReactNode[]` | — | tutorial 要点列表（CheckCircleFill + Body/14-400） | textArea |

**二次确认（default）**

```tsx
<Modal type="default" isOpen={open} onOpenChange={setOpen}>
  <ModalHeader title="Stop Generation" />
  <ModalBody>This task is already in progress…</ModalBody>
  <ModalFooter>
    <Button variant="outline" size="lg" slot="close">Cancel</Button>
    <Button variant="primary-danger" size="lg" onPress={stop}>Stop Generation</Button>
  </ModalFooter>
</Modal>
```

**教程（tutorial）**

```tsx
<Modal type="tutorial" isOpen={open} onOpenChange={setOpen}>
  <ModalHeader title="Video Upload Guide" />
  <ModalBody>
    <ModalImage src={cover} alt="" />
    <ModalChecklist items={["Your video should have a clear subject."]} />
  </ModalBody>
</Modal>
```

**自定义内容 + 毛玻璃面板（活动公告）**

```tsx
<Modal appearance="glass" size="lg" isOpen={open} onOpenChange={setOpen} aria-label="Notice">
  <div className="p-6">…</div>
</Modal>
```

## AnnouncementBanner

页面顶部的全宽公告条：一句文案 + 一个行动按钮 + 关闭按钮。用于产品公告、营销活动。

Figma：[AnnouncementBanner / 14127:7953](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=14127-7953)

**何时使用**

- 文案控制在一句话，只放一个行动按钮。
- 关闭后的再展示规则按活动单独定义（如同一阶段不再出现）。
- 深色主视觉的活动用 `tone="dark"`。

**不要**

- 不要同时显示两条 Banner。
- 不要用它显示错误或系统状态，那类信息用 Alert / Toast。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `children` | `ReactNode` | — | 公告文案（横幅宽度 ≥768px 时 Body/16-500，更窄时 Body/14-500；按横幅自身宽度响应） | message |
| `actionLabel` | `string` | — | 行动按钮文字；不传则不显示按钮 | showAction |
| `actionIcon` | `ReactNode` | — | 按钮文字后的图标（如 `<ArrowRightSmallLineIcon size={16} />`），hover 时右移（Figma 待补） | — |
| `href / onAction` | `string / () => void` | — | 按钮跳转地址或回调 | — |
| `onDismiss` | `() => void` | — | 关闭回调；不传则不显示关闭按钮 | dismissible |
| `accessory` | `ReactNode` | — | 文案与按钮之间的附加信息（如倒计时），仅横幅宽度 ≥768px 时显示 | — |
| `tone` | `"accent" \| "dark"` | `"accent"` | accent = Figma 品牌绿；dark = 深色底（Figma 待补） | — |

**产品公告**

```tsx
<AnnouncementBanner actionLabel="Learn more" href="/lip-sync" onDismiss={hide}>
  Video lip sync is coming soon
</AnnouncementBanner>
```

**活动公告**

```tsx
<AnnouncementBanner actionLabel="Claim Deal" actionIcon={<ArrowRightSmallLineIcon size={16} />} href="/pricing?promotion_code=BLACKFRIDAY26" onDismiss={hide}>
  Black Friday Sale: Save up to 37% on DomoAI!
</AnnouncementBanner>
```

**仅文案（不可关闭）**

```tsx
<AnnouncementBanner>Scheduled maintenance on Nov 30, 02:00–04:00 UTC.</AnnouncementBanner>
```

## TextArea

多行文本输入（如生成提示词）。带标题、必填星号、帮助图标、头部操作、底部插槽、字数统计与拖动缩放；speech 变体用于配音段落。

Figma：[TextArea / 664:1274](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=664-1274)

**何时使用**

- 提示词输入用 `default`：`title` + `headerEnd={<TextAreaAction>Tutorial</TextAreaAction>}` + `footer`（AI optimize 等）+ `maxLength`。
- 配音分段用 `speech`：`headerStart` 放说话人选择按钮，`headerEnd` 放关闭按钮。
- 没有 `title` 时必须传 `aria-label`。

**不要**

- 单行输入用 Input。
- 不要用 className 改底色、圆角或高度；初始高度用 `height`。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"default" \| "speech"` | `"default"` | 外观；speech 没有底部栏 | variant |
| `isFilled` | `boolean` | `false` | 底色改为 default/default（与 Input filled 一致），放进 FormField 时使用 | — |
| `title` | `ReactNode` | — | 标题（可见 label），Body/14-700 | showTitle |
| `isRequired` | `boolean` | — | 标题后显示红色 *，并设置 required | showRequired |
| `tip` | `string` | — | 标题后的 HelpFill 帮助图标说明 | showTip |
| `headerStart` | `ReactNode` | — | 替换标题区（speech 的说话人选择） | — |
| `headerEnd` | `ReactNode` | — | 头部右侧操作（Tutorial / 关闭） | showTutorial |
| `footer` | `ReactNode` | — | 底部左侧插槽（AI optimize 等），仅 default | footerSlot / showFooter |
| `maxLength` | `number` | — | 最大字数；传入后显示「当前/最大」统计 | — |
| `counterFormatter` | `(length, maxLength) => ReactNode` | — | 自定义字数统计文案 | — |
| `isResizable` | `boolean` | — | 右下角缩放手柄，拖动调整高度 | — |
| `height` | `number` | `160` | 初始高度（px） | — |
| `placeholder` | `string` | — | 占位文字 | — |
| `isInvalid / errorMessage` | `boolean / ReactNode` | — | 错误态（Figma 未设计，沿用 Input：红色描边 + 提示） | — |
| `isDisabled` | `boolean` | — | 禁用（整体 50% 透明度） | — |
| `value / defaultValue / onChange` | `string / (value: string) => void` | — | 受控 / 非受控值 | hasValue |

**提示词**

```tsx
<TextArea title="Prompt" isRequired tip="Describe your video" headerEnd={<TextAreaAction icon={<HelpFillIcon />}>Tutorial</TextAreaAction>} footer={<Button variant="outline" size="xs" startIcon={<OptimizeLineIcon />}>AI optimize</Button>} maxLength={1000} isResizable placeholder="Describe your video…" />
```

**配音段落**

```tsx
<TextArea variant="speech" aria-label="Speech" headerStart={<Button variant="outline" size="xs" startIcon={<ProfileLineIcon />} endIcon={<DownSmallLineIcon />}>Speaker A</Button>} headerEnd={<Button variant="ghost" size="xs" isIconOnly aria-label="Remove"><CloseLineIcon /></Button>} />
```

## InputTag

标签输入框：输入文字后回车生成标签，空输入时 Backspace 删除最后一个，点击 × 删除。支持数量上限计数、右侧图标、辅助说明与错误提示。

Figma：[InputTag / 1509:1654](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1509-1654)

**何时使用**

- 关键词、风格标签等「多个短文本」输入时使用。
- 需要限制数量时传 `maxTags`，右侧会显示计数，到达上限后不能再添加。
- 没有可见 label 时必须传 `aria-label`。

**不要**

- 从固定选项里多选用 SelectionGroup / Dropdown，不要用 InputTag。
- 不要用 className 改输入框底色、圆角或高度。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"filled" \| "subtle"` | `"filled"` | 外观 | variant |
| `value / defaultValue / onChange` | `string[] / (value: string[]) => void` | — | 受控 / 非受控标签列表 | tagSlot |
| `placeholder` | `string` | — | 没有标签时的占位文字 | — |
| `maxTags` | `number` | — | 最多标签数；传入后显示「当前/最大」计数 | showCounter |
| `allowsDuplicates` | `boolean` | `false` | 是否允许重复标签 | — |
| `endIcon` | `ReactNode` | — | 右侧 18px 图标 | showEndIcon |
| `helpText` | `ReactNode` | — | 辅助说明 | showHelpText |
| `isInvalid / errorMessage` | `boolean / ReactNode` | — | 错误态：红色描边与提示 | state=error |
| `isDisabled` | `boolean` | — | 禁用（整体 50% 透明度） | state=disabled |

**基础**

```tsx
<InputTag aria-label="Tags" placeholder="Enter your tag" maxTags={3} helpText="Press Enter to add a tag" />
```

**初始标签**

```tsx
<InputTag aria-label="Tags" defaultValue={["cat", "neon"]} endIcon={<DownSmallLineIcon />} />
```

**错误**

```tsx
<InputTag aria-label="Tags" isInvalid errorMessage="Something went wrong, please try again." />
```

## Toast

操作结果的即时反馈，自动消失。在应用根部渲染一次 `<ToastProvider />`，之后在任意位置调用 `toast.success / failed / tips(...)`。基于 HeroUI Toast 队列：最多同时显示 3 条，悬停暂停计时。

Figma：[Toast / 664:4866](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=664-4866)

**何时使用**

- 在根 layout 的 `<body>` 末尾放一次 `<ToastProvider />`（client 组件），不要在每个页面重复放。
- 操作成功用 `toast.success`，失败用 `toast.failed`，一般信息用 `toast.tips`。
- 标题一句话说明结果，需要补充时用 `description`；最多一个 `action` 按钮（如 Retry、View）。
- 需要用户处理的 Toast 设 `timeout: 0` 并保留关闭按钮；长任务可先 `tips` 再用 `toast.update(id, "success", …)` 原位更新。

**不要**

- 不要用 Toast 承载需要用户确认的关键信息，用 Modal。
- 不要用 Toast 显示页面内常驻提示，用 Alert。
- Figma 的 `credits` 类型属于业务类型，设计系统不提供（决策 D4）。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `toast(title, options)` | `(title: ReactNode, options?: ToastOptions) => string` | — | 弹出 tips 类型，返回 key；另有 `toast.success` / `toast.failed` / `toast.tips` / `toast.show(type, …)` | type |
| `options.description` | `ReactNode` | — | 第二行描述（Body/14-400 foreground/tertiary） | showDescription |
| `options.action` | `{ label: ReactNode; onPress: () => void \| boolean }` | — | 右侧 outline xs 按钮；点击后默认关闭，onPress 返回 false 保持打开 | showButton |
| `options.isClosable` | `boolean` | `true` | 显示关闭按钮 | showClose |
| `options.timeout` | `number` | `4000` | 自动消失时间（ms），0 = 不自动消失 | — |
| `options.onClose` | `() => void` | — | 关闭后回调 | — |
| `toast.update(key, type, title, options)` | `function` | — | 原位更新一条 Toast | — |
| `toast.close(key) / toast.clear()` | `function` | — | 关闭一条 / 全部 | — |
| `ToastProvider.placement` | `"top" \| "top start" \| "top end" \| "bottom" \| "bottom start" \| "bottom end"` | `"top"` | 出现位置 | — |
| `ToastProvider.maxVisibleToasts` | `number` | `3` | 同时可见条数 | — |
| `ToastProvider.toaster` | `Toaster` | `toast` | 使用的队列；`createToaster()` 可创建独立队列 | — |
| `ToastProvider.container` | `HTMLElement \| null` | — | 渲染到指定容器内（局部展示用），默认固定在视口 | — |

**在根 layout 放置 Provider**

```tsx
// app/layout.tsx
import { ToastProvider } from "@domoai/ui";

<body>
  {children}
  <ToastProvider />
</body>
```

**成功 / 失败 / 提示**

```tsx
toast.success("Action Succeed", { description: "Your video is ready." });
toast.failed("Action Failed", { action: { label: "Retry", onPress: retry } });
toast.tips("This is an information");
```

**原位更新**

```tsx
const id = toast.tips("Uploading…", { timeout: 0, isClosable: false });
await upload();
toast.update(id, "success", "Upload complete", { timeout: 4000 });
```

## Alert

页面内的静态提示条：图标 + 一段说明文字。`warning` 用于限制 / 风险提醒，`tip` 用于中性补充说明。

Figma：[Alert / 1954:8179](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1954-8179)

**何时使用**

- 放在相关内容附近（表单、套餐卡、支付方式下方），说明限制条件或注意事项。
- 需要用户注意但不阻断操作时用 `warning`；一般性补充说明用 `tip`。
- 文字控制在 1–2 行，长说明放到帮助文档链接里。

**不要**

- 不要用 Alert 反馈操作结果（成功 / 失败），那类即时反馈用 Toast。
- 不要用 Alert 做全站公告，用 AnnouncementBanner。
- 不要用 className 改底色或文字颜色。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `type` | `"tip" \| "warning"` | `"warning"` | warning：warning/soft 底 + 黄色图标与文字；tip：default 灰底 + 白色图标与文字 | type |
| `children` | `ReactNode` | — | 提示文字（Body/12-400，可换行） | — |
| `icon` | `ReactNode \| null` | `<TipsFillIcon />` | 替换左侧 14px 图标；传 null 隐藏 | — |
| `className` | `string` | — | 仅用于布局，默认撑满父容器宽度 | — |

**警示**

```tsx
<Alert type="warning">Due to Alipay restrictions, you can only upgrade plans after the current subscription ends and is canceled.</Alert>
```

**提示**

```tsx
<Alert type="tip">Relax Mode doesn't use credits — it just takes longer.</Alert>
```

## Skeleton

内容加载占位。基础 `Skeleton` 色块 + 4 个预设组合：SkeletonCard、SkeletonTextContent、SkeletonUserProfile、SkeletonListItems。默认带扫光动画。

Figma：[Skeleton / 11063:228333](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=11063-228333)

**何时使用**

- 优先用预设组合；预设不合适时用基础 `Skeleton` 按真实布局拼，尺寸用 className 设置。
- 骨架的尺寸和排布尽量贴近加载完成后的内容，避免加载完成时跳动。
- 文本行用 `radius="xs"`，图片 / 图标用 `md`，头像用 `full`。
- 同一区域内的骨架用同一种 `animationType`。

**不要**

- 不要用 className 改骨架颜色。
- 加载时间很短（< 300ms）时不要闪一下骨架，直接展示内容。
- 不要用骨架代替按钮的 loading 状态（Button 用 `isPending`）。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `Skeleton.animationType` | `"shimmer" \| "pulse" \| "none"` | `"shimmer"` | 扫光（Figma type=start → end 两帧之间的动画）/ 呼吸 / 静止 | type |
| `Skeleton.radius` | `"xs" \| "md" \| "full"` | `"md"` | 圆角 2px / 8px / 全圆 | — |
| `Skeleton.className` | `string` | — | 宽高与布局，如 `h-[66px] w-full` | — |
| `SkeletonCard` | `{ animationType?, className? }` | — | 卡片：66px 图片 + 3 行胶囊文本，内边距 8，宽度跟随父容器（Figma 130px） | — |
| `SkeletonTextContent.lines` | `number` | `5` | 段落行数（6px 高、行距 6、圆角 2） | — |
| `SkeletonUserProfile` | `{ animationType?, className? }` | — | 24px 圆形头像 + 两行文本 | — |
| `SkeletonListItems.rows` | `number` | `3` | 列表行数（24px 图标 + 两行文本，行距 8） | — |
| `aria-label` | `string` | `"Loading"` | 预设组合根节点为 role=status，读屏文字 | — |

**预设组合**

```tsx
<SkeletonCard className="w-[130px]" />
<SkeletonTextContent />
<SkeletonUserProfile />
<SkeletonListItems rows={3} />
```

**自定义拼装**

```tsx
<div className="flex flex-col gap-2">
  <Skeleton className="aspect-video w-full" />
  <Skeleton radius="xs" className="h-1.5 w-2/3" />
</div>
```

**关闭动画**

```tsx
<SkeletonListItems animationType="none" />
```

## Checkbox

多选勾选框（圆形）。default / assets 两种外观 × sm / md 两个尺寸，支持未选、半选、选中；可带右侧文字，多个用 CheckboxGroup 组合。

Figma：[Radio / 683:1046](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=683-1046)

**何时使用**

- 可以同时选多个、或单个开关需要提交后才生效（如同意条款）时用 Checkbox。
- 叠在图片 / 视频缩略图上做批量选择时用 `variant="assets"`。
- “全选”且只选中了一部分时用 `isIndeterminate`。
- 没有文字时必须传 `aria-label`；一组选项用 <CheckboxGroup> 包起来并给组 `aria-label`。

**不要**

- 互斥的单选不要用 Checkbox，用 Radio 或 SelectionGroup。
- 切换后立即生效的设置不要用 Checkbox，用 Switch。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"default" \| "assets"` | `"default"` | default 透明底 + 20% 白描边；assets 黑 40% 底 + 白描边（叠在素材上） | variant |
| `size` | `"sm" \| "md"` | `"sm"` | default 16 / 20px；assets 18 / 26px | size |
| `isSelected / defaultSelected` | `boolean` | — | 选中（受控 / 非受控） | selection=checked |
| `isIndeterminate` | `boolean` | `false` | 半选（显示横线），优先于选中 | selection=indeterminate |
| `onChange` | `(isSelected: boolean) => void` | — | 切换回调 | — |
| `isDisabled` | `boolean` | `false` | 禁用（整体 50% 透明度） | state=disabled |
| `children` | `ReactNode` | — | 右侧文字（Body/14-400，间距 8px），对应 Figma Checkbox 组件 | — |
| `value` | `string` | — | 在 CheckboxGroup 中的取值 | — |
| `CheckboxGroup.orientation` | `"horizontal" \| "vertical"` | `"horizontal"` | 组排列方向：横向间距 24px，纵向 12px | — |

**带文字**

```tsx
<Checkbox isSelected={agree} onChange={setAgree}>I agree to the Terms</Checkbox>
```

**素材多选**

```tsx
<Checkbox variant="assets" size="md" aria-label="Select image" />
```

**多选组**

```tsx
<CheckboxGroup aria-label="Format" value={formats} onChange={setFormats}>
  <Checkbox value="mp4">MP4</Checkbox>
  <Checkbox value="gif">GIF</Checkbox>
</CheckboxGroup>
```

## Radio

单选圆点。sm / md 两个尺寸，可带右侧文字；必须放在 RadioGroup 中使用（方向键切换）。

Figma：[Radio / 6023:128004](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=6023-128004)

**何时使用**

- 2 个以上互斥选项、并且需要看到全部选项文字时用 RadioGroup + Radio。
- 给 RadioGroup 传 `aria-label`（或用 aria-labelledby 关联可见标题）。
- 只有圆点没有文字时，给 Radio 传 `aria-label`。

**不要**

- 可以多选的场景用 Checkbox。
- 紧凑的分段切换（Monthly / Yearly、比例、分辨率）用 SelectionGroup。
- 不要单独使用 Radio（必须在 RadioGroup 内）。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `value` | `string` | — | 选项取值（必填） | — |
| `size` | `"sm" \| "md"` | `"sm"` | 圆点 16 / 20px；选中描边 1.5 / 2px，内圆 8 / 10px | size |
| `isDisabled` | `boolean` | `false` | 禁用（整体 50% 透明度） | state=disabled |
| `children` | `ReactNode` | — | 右侧文字（Body/14-400，间距 8px），对应 Figma Radio 组件 | — |
| `RadioGroup.value / onChange` | `string / (value: string) => void` | — | 受控选中值（也可用 defaultValue） | isSelected |
| `RadioGroup.orientation` | `"horizontal" \| "vertical"` | `"horizontal"` | 横向间距 24px，纵向 12px | — |
| `RadioGroup.isDisabled` | `boolean` | — | 整组禁用 | — |

**单选组**

```tsx
<RadioGroup aria-label="Quality" value={quality} onChange={setQuality}>
  <Radio value="standard">Standard</Radio>
  <Radio value="high">High</Radio>
</RadioGroup>
```

**纵向排列**

```tsx
<RadioGroup aria-label="Plan" orientation="vertical" defaultValue="pro">…</RadioGroup>
```

## Tabs

标签页：在同一区域切换几组平级内容。primary（品牌色下划线）/ secondary（胶囊分段）/ modal（弹窗内白色下划线）× web / mobile 两种密度，标签可带计数徽标。

Figma：[Tabs / 1202:3129](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1202-3129)

**何时使用**

- 页面级内容分组用 primary；桌面端 `density="web"`（20px 字号），移动端 `density="mobile"`（16px）。
- 弹窗 / 抽屉内的分组用 `variant="modal"`。
- 工具栏内的小范围筛选用 secondary（胶囊）。
- 数量提示用 Tab 的 `badge`（neutral Badge）。
- TabList 必须有 `aria-label`；每个 Tab 的 `id` 与 TabPanel 的 `id` 对应。只做导航（每个 Tab 跳不同路由）时给 Tab 传 `href`，不渲染 TabPanel。

**不要**

- 不要只放标签栏不放 TabPanel：每个 Tab 都要有同 id 的 TabPanel（读屏软件靠它跳到对应内容）。只是切换选项、没有对应内容区时，用 SelectionGroup（分段）。
- 不要用 Tabs 做单选表单项，表单里的单选用 SelectionGroup / Radio。
- 不要用 className 改标签的颜色、字号、下划线。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `Tabs.variant` | `"primary" \| "secondary" \| "modal"` | `"primary"` | 容器样式 | variant |
| `Tabs.density` | `"web" \| "mobile"` | `"web"` | web 用 md 标签，mobile 用 sm 标签（modal 固定 sm） | density |
| `Tabs.selectedKey / defaultSelectedKey` | `Key` | — | 当前选中的标签（受控 / 非受控） | — |
| `Tabs.onSelectionChange` | `(key: Key) => void` | — | 切换回调 | — |
| `Tabs.disabledKeys` | `Iterable<Key>` | — | 禁用的标签 | .TabsElement state=disabled |
| `TabList.aria-label` | `string` | — | 标签栏的无障碍名称（必填） | TabItem（slot） |
| `Tab.id` | `Key` | — | 与 TabPanel.id 对应 | — |
| `Tab.badge` | `ReactNode` | — | 文字后的计数徽标（primary / modal） | .TabsElement showBadge |
| `Tab.startIcon / endIcon` | `ReactNode` | — | 胶囊样式的左右图标（14 / 16px） | — |
| `Tab.href` | `string` | — | 导航型标签：点击跳转（配合 RouterProvider 走客户端路由） | — |
| `Tab.isDisabled` | `boolean` | `false` | 禁用 | .TabsElement state=disabled |
| `Tab.variant / size` | `"primary" \| "secondary" \| "tertiary" / "sm" \| "md"` | — | 单个标签样式与尺寸，默认由 Tabs 推导（一般不传） | .TabsElement variant / size |

**基础**

```tsx
<Tabs defaultSelectedKey="images">
  <TabList aria-label="Assets">
    <Tab id="images" badge={9}>Images</Tab>
    <Tab id="videos">Videos</Tab>
  </TabList>
  <TabPanel id="images">…</TabPanel>
  <TabPanel id="videos">…</TabPanel>
</Tabs>
```

**胶囊（secondary）**

```tsx
<Tabs variant="secondary" density="mobile" selectedKey={tab} onSelectionChange={setTab}>
  <TabList aria-label="Filter">
    <Tab id="all">All</Tab>
    <Tab id="liked">Liked</Tab>
  </TabList>
</Tabs>
```

## Badge

数字徽标与红点。accent / neutral / dot 三种样式 × sm / md 两个尺寸；可单独跟在文字后，也可用 BadgeAnchor 挂在图标按钮右上角。

Figma：[Badge / 726:8033](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=726-8033)

**何时使用**

- 未读数、数量提示用 accent；Tab 标题后的计数等弱提示用 neutral。
- 只需提示「有新内容」不需要数量时用 `variant="dot"`，并提供 `aria-label`。
- 挂在图标按钮右上角时用 `<BadgeAnchor>` 包住按钮与 Badge（对应 Figma BadgeType）。
- 数量过大时自行截断，例如 `{count > 99 ? "99+" : count}`。

**不要**

- 不要用 Badge 表示状态或分类文字（如 NEW、Pro），那是 Tag。
- 不要用 className 改颜色和尺寸。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"accent" \| "neutral" \| "dot"` | `"accent"` | 样式：品牌色底 / 半透明白底 / 红色圆点 | variant |
| `size` | `"xs" \| "sm" \| "md"` | `"md"` | 高度 15 / 20 / 24px（dot 为 8 / 8 / 12px）。xs 来自 BadgeType 的计数角标 | size |
| `children` | `ReactNode` | — | 数字或短文本。单字符为正圆，多字符左右各 4px 内边距（Figma digits 自动决定） | digits |
| `BadgeAnchor` | `component` | — | 角标定位容器：count 角标外扩 5px、dot 外扩 2px 到右上角 | BadgeType.badge |

**数字**

```tsx
<Badge>9</Badge>
<Badge variant="neutral" size="sm">99</Badge>
```

**红点**

```tsx
<Badge variant="dot" aria-label="有新消息" />
```

**挂在图标按钮上**

```tsx
<BadgeAnchor>
  <Button variant="primary-white" size="sm" isIconOnly aria-label="Cube"><CubeLineIcon /></Button>
  <Badge size="xs">9</Badge>
</BadgeAnchor>
```

## Link

文字链接，用于页面跳转。default / blue 两种颜色 × 4 个尺寸，可带左右图标或纯图标；支持 Next.js 客户端路由。

Figma：[Button / 6474:51455](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=6474-51455)

**何时使用**

- 跳转（站内页面、外链、协议条款）用 Link；触发操作（提交、打开弹窗）用 Button。
- 正文中需要突出的链接用 `color="blue"`；工具栏、页脚等弱链接用默认 `default`。
- Next.js 项目在根布局包一层 RouterProvider（见下方示例），之后所有 `href` 都走客户端路由，无需再包 next/link。
- 需要 next/link 的 prefetch 时，用 `render` 渲染 NextLink：`render={(props) => ("href" in props ? <NextLink {...props} /> : <span {...props} />)}`。
- 外链传 `target="_blank"`（React Aria 会自动补 rel="noopener noreferrer"），纯图标链接必须加 `aria-label`。

**不要**

- 不要把 Link 写成 `<a className=…>` 或用 Button 包 next/link。
- 不要用 className 改颜色、字号、下划线。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `href` | `string` | — | 链接地址（站内地址配合 RouterProvider 走客户端路由） | — |
| `color` | `"default" \| "blue"` | `"default"` | 颜色：60% 白（hover 变白）/ 链接蓝 | color |
| `size` | `"xs" \| "sm" \| "md" \| "lg"` | `"md"` | 字号 10 / 12 / 14 / 16px，图标 10 / 14 / 16 / 20px | size |
| `isIconOnly` | `boolean` | `false` | 纯图标链接（图标 10 / 14 / 18 / 22px），children 传图标 | isIconOnly |
| `startIcon` | `ReactNode` | — | 左侧图标 | showStartIcon |
| `endIcon` | `ReactNode` | — | 右侧图标 | showEndIcon |
| `isDisabled` | `boolean` | `false` | 禁用（50% 透明度） | state=disabled |
| `target / rel / download` | `string` | — | 原生 <a> 属性 | — |
| `render` | `(props, renderProps) => ReactElement` | — | 替换渲染的元素（如 next/link 的 NextLink），需透传 props | — |
| `onPress` | `(e: PressEvent) => void` | — | 点击回调（React Aria） | — |

**基础**

```tsx
<Link href="/pricing">Pricing</Link>
<Link color="blue" href="/terms">Terms of Service</Link>
```

**带图标**

```tsx
<Link color="blue" size="sm" href="/docs" endIcon={<RightSmallLineIcon />}>Learn more</Link>
```

**Next.js 路由（app/providers.tsx）**

```tsx
"use client";
import { RouterProvider } from "@domoai/ui";
import { useRouter } from "next/navigation";

export function Providers({ children }: { children: React.ReactNode }) {
  const router = useRouter();
  return <RouterProvider navigate={router.push}>{children}</RouterProvider>;
}
```

**使用 next/link（需要 prefetch 时）**

```tsx
import NextLink from "next/link";

<Link href="/pricing" render={(props) => ("href" in props ? <NextLink {...props} /> : <span {...props} />)}>Pricing</Link>
```

## Breadcrumbs

面包屑导航：显示当前页面在层级中的位置，前面的层级可点击返回。

Figma：[Breadcrumbs / 9721:142865](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=9721-142865)

**何时使用**

- 层级 ≥ 2 的页面（如 项目 → 文件夹 → 文件）在标题上方放面包屑。
- 最后一项是当前页，不传 href；它会自动设为 aria-current="page"，显示为白色、不可点击。
- 站内跳转配合 RouterProvider 走 Next.js 客户端路由（同 Link）。

**不要**

- 不要手写「文字 + 箭头图标」拼面包屑。
- 层级只有一层时不要显示面包屑。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `Breadcrumbs.children` | `ReactNode` | — | 一组 BreadcrumbsItem | Item（slot） |
| `Breadcrumbs.onAction` | `(key: Key) => void` | — | 点击某一项（不使用 href 时） | — |
| `Breadcrumbs.isDisabled` | `boolean` | `false` | 整体禁用 | — |
| `BreadcrumbsItem.href` | `string` | — | 跳转地址，当前页省略 | — |
| `BreadcrumbsItem.children` | `ReactNode` | — | 显示文字 | — |

**基础**

```tsx
<Breadcrumbs>
  <BreadcrumbsItem href="/">Home</BreadcrumbsItem>
  <BreadcrumbsItem href="/projects">Projects</BreadcrumbsItem>
  <BreadcrumbsItem>Untitled</BreadcrumbsItem>
</Breadcrumbs>
```

## Separator

分割线：横向或竖向的 1px 线，可在中间放一段文字（如登录方式之间的 OR）。三种强度。

Figma：[Separator / 9608:136704](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=9608-136704)

**何时使用**

- 区块之间的分隔用 primary；列表项、卡片内的轻分隔用 secondary / tertiary。
- 两组可选方式之间（如邮箱登录 / 第三方登录）用带文字的分割线：`<Separator>OR</Separator>`。
- 竖向分割线放在 flex 行里，高度跟随父容器（需要时用 className 限制高度，如 `h-4`）。

**不要**

- 不要用 border-b / <hr> 自己画分割线。
- 不要用 className 改线条颜色或粗细。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"primary" \| "secondary" \| "tertiary"` | `"primary"` | 线条强度：border / border-secondary / border-tertiary | variant |
| `orientation` | `"horizontal" \| "vertical"` | `"horizontal"` | 方向 | orientation |
| `children` | `ReactNode` | — | 中间文字（Body/12-500、foreground-tertiary；Figma 为 muted，按无障碍对比度调整） | showText / text |
| `isDecorative` | `boolean` | `false` | 纯装饰，对读屏隐藏（仅无文字时） | — |

**横向**

```tsx
<Separator />
<Separator variant="secondary" />
<Separator variant="tertiary" />
```

**带文字**

```tsx
<Separator>OR</Separator>
```

**竖向**

```tsx
<div className="flex h-6 items-center gap-3">
  <span>Images</span>
  <Separator orientation="vertical" />
  <span>Videos</span>
</div>
```

## Indicator

轮播图 / 横滑卡片底部的分页指示器。primary 为圆点，secondary 的当前项为自动播放进度条；鼠标移入时外扩为深色胶囊。

Figma：[Indicator / 949:6458](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=949-6458)

**何时使用**

- 轮播、引导页、横滑卡片的页码提示，放在内容底部居中（绝对定位由业务布局决定）。
- 可手动切换时传 `onChange`，每个点是可聚焦的按钮（aria-label 默认 `Go to slide N`）。
- 自动播放的轮播用 `variant="secondary"`，把当前页已播放比例传给 `progress`（0–1）。
- 触屏设备上需要常显深色底时传 `isHovered`。

**不要**

- 不要用于超过 8 页的分页，长列表用页码分页。
- 不要用 className 改点的颜色和尺寸。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `variant` | `"primary" \| "secondary"` | `"primary"` | 圆点 / 当前项为 32px 进度条 | variant |
| `total` | `number` | — | 总页数 | — |
| `selectedIndex` | `number` | — | 当前页（从 0 开始） | — |
| `onChange` | `(index: number) => void` | — | 点击某个点；不传则仅展示 | — |
| `progress` | `number` | `1` | secondary 当前项进度 0–1 | — |
| `isHovered` | `boolean` | — | 强制 hover 外观（padding 8 + surface 底色）；默认跟随鼠标 | hover |
| `getItemLabel` | `(index: number) => string` | — | 每个点的无障碍名称 | — |

**圆点**

```tsx
<Indicator total={4} selectedIndex={index} onChange={setIndex} />
```

**自动播放进度**

```tsx
<Indicator variant="secondary" total={4} selectedIndex={index} progress={elapsed / duration} onChange={setIndex} />
```

## Drawer

移动端底部抽屉：遮罩 + 顶部圆角 surface 面板，带拖拽条，可下拉关闭。内容用 DrawerHeader、DrawerBody、DrawerFooter 组合。

Figma：[Drawer / 1782:3130](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1782-3130)

**何时使用**

- 移动端的选择、确认、补充说明等短流程，从底部滑出。
- 底部操作按钮放在 `DrawerFooter`，主操作用 primary，按钮自动撑满宽度。
- 有 `DrawerHeader` 时标题自动作为抽屉名称，否则传 `aria-label`。

**不要**

- 桌面端的确认对话框用 Modal。
- 不要在抽屉里再打开抽屉。
- 不要用 className 改面板颜色和圆角。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `isOpen / onOpenChange` | `boolean / (open: boolean) => void` | — | 受控打开状态 | — |
| `placement` | `"bottom" \| "top" \| "left" \| "right"` | `"bottom"` | 滑出方向（Figma 只有 bottom） | — |
| `isDismissable` | `boolean` | `true` | 点遮罩、下拉关闭 | — |
| `isKeyboardDismissDisabled` | `boolean` | `false` | 禁止 Esc 关闭 | — |
| `portalContainer` | `HTMLElement` | — | 浮层渲染容器，默认 document.body | — |
| `DrawerHeader.title / endContent` | `ReactNode` | — | 标题（Body/16-700）与右侧内容 | Drawer › Header |
| `DrawerBody.children` | `ReactNode` | — | 内容区（Body/14-400 secondary），过长时内部滚动 | Drawer › Content |
| `DrawerFooter.children` | `ReactNode` | — | 底部按钮（自动平分宽度） | Drawer › Footer |

**底部抽屉**

```tsx
<Drawer isOpen={open} onOpenChange={setOpen}>
  <DrawerHeader title="Header Title" />
  <DrawerBody>This is the body text.</DrawerBody>
  <DrawerFooter>
    <Button slot="close">OK</Button>
  </DrawerFooter>
</Drawer>
```

## Popover

新手引导气泡：带箭头指向触发元素，可含标题、正文、配图、步骤进度和上一步 / 下一步按钮。12 个方向。

Figma：[Popover / 745:9897](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=745-9897)

**何时使用**

- 功能引导、分步教程：每一步用一个 Popover 指向对应的界面元素，底部显示「1 of 5」进度和 Prev / Next。
- placement 用 HeroUI 写法："right top" / "bottom start" / "left bottom" 等；空间不够时会自动翻转。
- 没有 title 时传 `aria-label`。

**不要**

- 简短的文字提示用 Tooltip，不要用 Popover。
- 菜单、选项列表用 Dropdown。
- 不要用 className 改气泡宽度、颜色、圆角。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `Popover.isOpen / onOpenChange` | `boolean / (open: boolean) => void` | — | 受控打开状态（不传则点击触发器切换） | — |
| `placement` | `"right top" \| "right" \| "right bottom" \| "bottom start" \| "bottom" \| "bottom end" \| "top start" \| "top" \| "top end" \| "left top" \| "left" \| "left bottom"` | `"right top"` | 浮层位置（Figma right-start / buttom / left start 等已统一为 HeroUI 写法） | placement |
| `title` | `ReactNode` | — | 标题 Body/16-700 | showHeader |
| `children` | `ReactNode` | — | 正文 Body/14-400 secondary | contentSlot |
| `image / imageAlt` | `string` | — | 配图（328×184，radius/md） | showImage |
| `progress` | `ReactNode` | — | 步骤进度，如 "1 of 5" | showProgress |
| `onPrev / prevLabel` | `() => void / ReactNode` | `"Prev"` | 传了 onPrev 才显示 outline 上一步按钮 | showPrevButton |
| `onNext / nextLabel` | `() => void / ReactNode` | `"Next"` | 传了 onNext 才显示 primary 下一步按钮 | showNextButton |
| `isClosable` | `boolean` | `true` | 右上角关闭按钮 | — |
| `offset` | `number` | `8` | 气泡与触发元素的距离（px） | — |

**分步引导**

```tsx
<Popover isOpen={open} onOpenChange={setOpen}>
  <Button variant="secondary">Upload</Button>
  <PopoverContent placement="bottom start" title="Header Title" image={cover} progress="1 of 5" onPrev={prev} onNext={next}>
    This is the body text.
  </PopoverContent>
</Popover>
```

**只有文字**

```tsx
<Popover>
  <Button variant="ghost" isIconOnly aria-label="Help"><HelpFillIcon /></Button>
  <PopoverContent placement="top" title="Tips">You can drag to reorder.</PopoverContent>
</Popover>
```

## Tooltip

悬停或键盘聚焦时显示的简短文字提示，可在文字右侧带一个 16px 图标。无箭头。

Figma：[Tooltip / 744:4723](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=744-4723)

**何时使用**

- 给纯图标按钮补充名称或快捷说明（按钮本身仍要有 aria-label）。
- 触发元素用可聚焦的组件（Button 等）；图标、文字这类普通元素包一层 `TooltipTrigger`。
- 文字保持一行、简短。

**不要**

- 不要在 Tooltip 里放按钮、链接等可交互内容（用 Popover）。
- 不要用 Tooltip 承载完成任务必需的信息（触屏设备看不到）。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `content` | `ReactNode` | — | 提示文字（Body/14-400） | — |
| `icon` | `ReactNode` | — | 文字右侧 16px 图标 | showIcon |
| `placement` | `"top" \| "bottom" \| "left" \| "right" \| "top start" \| …` | `"top"` | 浮层位置（HeroUI 写法） | — |
| `offset` | `number` | `3` | 与触发元素的距离（px） | — |
| `delay / closeDelay` | `number` | — | 显示 / 隐藏延时（ms），默认取 HeroUI 设置 | — |
| `isOpen / defaultOpen / onOpenChange` | `boolean / boolean / (open: boolean) => void` | — | 受控 / 非受控打开状态 | — |
| `isDisabled` | `boolean` | `false` | 禁用提示 | — |
| `children` | `ReactNode` | — | 触发元素（可聚焦组件，或包在 TooltipTrigger 里） | — |

**图标按钮提示**

```tsx
<Tooltip content="Upscale">
  <Button variant="ghost" isIconOnly aria-label="Upscale"><OptimizeLineIcon /></Button>
</Tooltip>
```

**带图标**

```tsx
<Tooltip content="Tooltip" icon={<CubeLineIcon />}>
  <Button variant="secondary">Hover me</Button>
</Tooltip>
```

**普通元素触发**

```tsx
<Tooltip content="Credits never expire">
  <TooltipTrigger><InfoCircleLineIcon size={16} /></TooltipTrigger>
</Tooltip>
```

## Upload

素材上传区：拖拽 / 点击 / 粘贴选择图片、视频、音频，显示上传中与已上传预览，可删除、替换。r2v 模式支持多素材网格（最多 50 个）。只负责选文件与预览，不做网络上传。

Figma：[Upload / 1545:2447](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=1545-2447)

**何时使用**

- 用受控的 `files` + `onFilesChange` 管理文件；新选的文件带 `file`（原始 File）和 `url`（blob 预览地址）。
- 自己上传时，把对应文件的 `status` 设为 "uploading" 并更新 `progress`（0–100），完成后改回 "done" 并可把 `url` 换成远程地址。
- 生成页侧栏用 `size="desktop"`（撑满父容器宽度）；移动端紧凑布局用 `size="mobile"`（136×136）。
- 参考生视频（多图 / 视频 / 音频混合）用 `media="r2v"`。
- Assets、Tutorial 按钮传了 `onAssetsPress` / `onTutorialPress` 才显示；额外按钮放 `actionSlot`。

**不要**

- 不要用 className 改背景、圆角、高度。
- state（default / hover / uploading / filled）不是 prop：由文件列表与鼠标交互决定。
- 不要在组件外再包一层 input[type=file]，点击、拖入、粘贴都已处理。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `media` | `"image" \| "video" \| "audio" \| "r2v"` | `"image"` | 素材类型（Figma 的 Video 统一为小写 video） | media |
| `size` | `"desktop" \| "mobile"` | `"desktop"` | desktop 撑满宽度，高 212（video 272 / r2v 220）；mobile 136×136 | size |
| `files / defaultFiles` | `UploadFile[]` | — | 已选文件（受控 / 非受控） | — |
| `onFilesChange` | `(files: UploadFile[]) => void` | — | 选择、拖入、粘贴、替换、删除时触发 | — |
| `accept` | `string[]` | — | 允许的 MIME / 扩展名，默认按 media 推断（image/* 等） | — |
| `maxFiles` | `number` | `r2v 50，其余 1` | 最多文件数；单文件时新文件替换旧文件 | — |
| `showTutorial / onTutorialPress` | `boolean / () => void` | — | 右上角 Tutorial 按钮 | showTutorial |
| `showAssets / onAssetsPress` | `boolean / () => void` | — | Assets（素材库）按钮 | showAssets |
| `actionSlot` | `ReactNode` | — | 空状态按钮区的额外内容 | actionSlot |
| `showIndex / index` | `boolean / number` | `true / 1` | 角标序号（Image 1）与音频左上角序号 | showIndex |
| `title / icon` | `ReactNode` | — | 覆盖空状态的默认文字与图标 | — |
| `onEdit` | `(file) => void` | — | 图片 / 视频编辑按钮（传入才显示） | — |
| `onAddToAssets` | `(file) => void` | — | 音频「加入素材库」按钮（传入才显示） | — |
| `isDisabled` | `boolean` | `false` | 禁用 | — |

**图片上传**

```tsx
<Upload media="image" files={files} onFilesChange={setFiles} onAssetsPress={openAssets} onTutorialPress={openTutorial} />
```

**移动端**

```tsx
<Upload media="image" size="mobile" files={files} onFilesChange={setFiles} />
```

**参考生视频（多素材）**

```tsx
<Upload media="r2v" files={files} onFilesChange={setFiles} onAssetsPress={openAssets} />
```

## UploadMedia

已上传图片 / 视频的缩略图：左上角名称角标，右上角删除、右下角编辑。web 悬停显示按钮，mobile 常显。

Figma：[Upload / 12906:88969](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=12906-88969)

**何时使用**

- 在素材列表、参考图网格中展示已上传的素材。
- 需要删除 / 编辑时传 `onRemove` / `onEdit`，按钮才会出现。

**不要**

- 不要用它做上传入口；上传入口用 Upload。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `type` | `"image" \| "video"` | `"image"` | 素材类型 | type |
| `src / poster / alt` | `string` | — | 素材地址 / 视频封面 / 替代文本 | — |
| `label` | `ReactNode` | — | 左上角角标，如 Image 1 | — |
| `platform` | `"web" \| "mobile"` | `"web"` | web 144px 悬停显示按钮；mobile 113px 按钮常显 | platform |
| `onRemove / onEdit` | `() => void` | — | 删除 / 编辑（传入才显示按钮） | State=hover |

**图片**

```tsx
<UploadMedia src={url} label="Image 1" onRemove={remove} onEdit={edit} />
```

## AudioPlayer

胶囊形音频播放条：播放 / 暂停、时间、可拖动进度条（悬停预览），可选音量与全屏按钮。基于原生 audio + React Aria Slider。

Figma：[AudioPlayer / 726:8112](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=726-8112)

**何时使用**

- 试听生成的语音、配乐时使用；传 `src` 即可，播放状态默认由组件自己管理。
- 需要和外部同步（例如同一时间只播一个）时用受控的 `isPlaying` + `onPlayingChange`。
- 音频有音量差异、需要用户调节时加 `showVolume`（悬停音量按钮展开音量条，点击切换静音）。
- 悬停、拖动进度条、展开音量条这些交互状态由组件内部处理，不需要也不能通过 props 指定。

**不要**

- 不要用它播放视频；视频用 <video> 自带控件或视频播放组件。
- 不要用 className 改背景色、高度。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `src` | `string` | — | 音频地址；不传时只做展示（配合 duration / currentTime） | — |
| `isPlaying / defaultPlaying` | `boolean` | `false` | 是否播放（受控 / 非受控） | 播放中 |
| `onPlayingChange` | `(isPlaying: boolean) => void` | — | 播放 / 暂停切换（含播放结束） | — |
| `isMuted / defaultMuted` | `boolean` | `false` | 是否静音 | 静音 |
| `volume / defaultVolume` | `number (0–1)` | `1` | 音量 | — |
| `currentTime / defaultCurrentTime` | `number（秒）` | `0` | 播放位置 | — |
| `onTimeChange` | `(seconds: number) => void` | — | 播放推进或拖动进度条 | — |
| `duration` | `number（秒）` | — | 总时长；不传时读取音频元数据 | — |
| `showVolume` | `boolean` | `false` | 显示音量按钮与音量条 | 带音频 |
| `isFullscreen / onFullscreenChange` | `boolean / (v: boolean) => void` | — | 全屏按钮状态与回调；传了回调才显示按钮 | — |
| `aria-label` | `string` | `"Audio player"` | 无障碍名称 | — |

**基础**

```tsx
<AudioPlayer src="/voice.mp3" />
```

**带音量**

```tsx
<AudioPlayer src="/voice.mp3" showVolume />
```

**受控播放**

```tsx
<AudioPlayer src={url} isPlaying={playing} onPlayingChange={setPlaying} />
```

## Form

表单项 FormField：标签 + 控件 + 说明 / 错误的布局，控件复用 Input / TextArea / RadioGroup / SelectionGroup / CheckboxGroup（对应 Figma `type`）；vertical 标签在上、horizontal 标签在左。标签自动关联控件（aria-labelledby / htmlFor），必填、出错状态自动传给控件。外层用 Form（原生 form + React Aria 校验）。

Figma：[Form / 7663:49934](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=7663-49934)

**何时使用**

- 带可见标签的输入框、多行输入、单选 / 多选组都放进 FormField，标签写在 `label`，不要再给控件传 aria-label。
- 说明文字和错误提示写在 FormField 的 `description` / `errorMessage`，不要再用 Input 的 helpText / errorMessage（避免两套说明）。
- 标签较短、页面较宽时可用 `orientation="horizontal"`；多个横排表单项传同一个 `labelWidth` 让控件左对齐。
- 必填项传 `isRequired`：显示红色「*」，控件得到原生 required / aria-required，外层 Form 提交时自动校验。
- 需要额外解释、又不想常驻显示的说明放 `tip`（帮助图标 + Tooltip）。

**不要**

- TextArea 放进 FormField 时不要再传 `title`，标签由 FormField 提供。
- 不要用 FormField 包按钮、开关等自带文字的控件；开关用 Switch 自身的文字。
- 不要用 className 改标签颜色、字号或间距。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `label` | `ReactNode` | — | 标签文字（Body/14-400），作为控件的可访问名称 | — |
| `orientation` | `"vertical" \| "horizontal"` | `"vertical"` | vertical 标签在上（间距 8px）/ horizontal 标签在左（间距 16px，与 Input / TextArea 首行垂直居中） | orientation |
| `isRequired` | `boolean` | `false` | 标签后红色「*」，并把 isRequired 传给控件 | showRequired |
| `tip` | `ReactNode` | — | 标签后 16px 帮助图标，悬停 / 聚焦显示 Tooltip | showTip |
| `showColon` | `boolean` | `false` | 标签后显示冒号「:」 | showColon |
| `labelWidth` | `number \| string` | — | 横排时标签列宽度（px 或 CSS 长度），默认随文字宽度 | — |
| `description` | `ReactNode` | — | 控件下方说明（Body/12-400，foreground-tertiary），出错时被 errorMessage 替换 | — |
| `isInvalid` | `boolean` | `false` | 出错：传给控件（红色描边、aria-invalid）并显示 errorMessage | — |
| `errorMessage` | `ReactNode` | — | 错误提示（Body/12-400，danger）。原生 / validate 校验的错误由控件自身显示 | — |
| `children` | `ReactNode` | — | 控件：Input / TextArea / RadioGroup / SelectionGroup / CheckboxGroup | type |
| `Form` | `HeroUI Form props` | — | 外层表单：onSubmit、validationBehavior（默认 native）、validationErrors（按 name 显示服务端错误） | — |

**输入框（纵向）**

```tsx
<FormField label="Email" isRequired description="We'll never share it.">
  <Input type="email" name="email" placeholder="Enter your email" />
</FormField>
```

**单选（横向 + 冒号 + 提示）**

```tsx
<FormField label="Quality" orientation="horizontal" showColon tip="Higher quality costs more credits">
  <RadioGroup name="quality" defaultValue="standard">
    <Radio value="standard">Standard</Radio>
    <Radio value="high">High</Radio>
  </RadioGroup>
</FormField>
```

**表单提交**

```tsx
<Form onSubmit={onSubmit} className="flex flex-col gap-6">
  <FormField label="Name" isRequired><Input name="name" placeholder="Enter your name" /></FormField>
  <FormField label="Message"><TextArea name="message" height={120} placeholder="Say something" /></FormField>
  <Button type="submit">Submit</Button>
</Form>
```

## Navigation

导航基础件：Web 侧栏 SidebarNavigation（NavigationItem、SidebarNavigationIcon、SidebarLogo、SidebarAvatar）、移动端顶栏 TopBarMobile、移动端底部标签栏 Tabber / TabberItem，以及头像 Avatar。

Figma：[Navigation / 954:8526](https://www.figma.com/design/72yiL7SnlbcIzmFnkSQw2v/DomoAI-Design-System-V3.0?node-id=954-8526)

**何时使用**

- SidebarNavigation：Web 端（xl）页面的左侧导航都用它；`primaryArea` 放一级入口，`secondaryArea` 放 MCP / API / Help 等次级入口，`footer` 放升级入口与 SidebarAvatar。
- SidebarNavigation：展开状态需要记忆时用受控的 `isExpanded` + `onExpandedChange`；内部的 NavigationItem / SidebarAvatar / Logo 会自动切换形态，不用逐个传。
- NavigationItem：页面入口传 `href`（配合 RouterProvider 走客户端路由），当前页传 `isSelected`（输出 aria-current="page"）。
- NavigationItem：一级入口图标用 `<SidebarNavigationIcon variant="…" />`，选中时自动换成 Fill 图标；其他入口传 Line 图标，需要时用 `selectedIcon` 指定 Fill 图标。
- SidebarAvatar：已登录时配合 Dropdown 打开账户菜单（不传 href 即渲染为按钮）；未登录时 `isSignedIn={false}` 并传 `onSignIn`。
- TopBarMobile：已登录（Figma variant=LoggedIn）的 actions 放积分入口、`<TopBarMobileAction>`（通知）和 `<Avatar size="sm">`。
- TopBarMobile：未登录（variant=NotLoggedIn）的 actions 放语言切换 `<TopBarMobileAction>` 和 primary「Get Started」按钮。
- TopBarMobileAction：顶栏里的纯图标操作都用它（图标自动为 foreground/secondary），必须写 aria-label。
- Tabber：只在 mobile 布局使用，固定在页面底部；Web 端用 SidebarNavigation。
- TabberItem：页面入口传 `href` + `isActive`（输出 aria-current），图标传 Line，`activeIcon` 传对应的 Fill。
- TabberItem：中间的创作入口用 `isIconOnly` 并传 `onPress`；文字仍要写，作为读屏名称。
- Avatar：移动端顶栏右上角用 `size="sm"`（32px）。
- Avatar：侧栏底部的账户入口不要自己拼，用 `SidebarAvatar`（已处理登录 / 未登录、展开 / 收起）。
- Avatar：头像旁边已经显示用户名时传 `alt=""`，避免读屏重复朗读。

**不要**

- NavigationItem：不要用 className 改导航项颜色、高度或圆角。
- SidebarNavigation：不要把侧栏写死路由或在组件里判断当前路径；选中态由页面根据路由传 `isSelected`。
- 不要在 Web 端（xl）使用 TopBarMobile；Web 端用 SidebarNavigation。
- 不要在 Tabber 里放超过 5 个标签项。
- 不要用 className 改标签项颜色或高度。
- Avatar：不要用 className 改头像尺寸或圆角；需要新尺寸先在设计系统中新增。

| Prop | 类型 | 默认 | 说明 | Figma 属性 |
|---|---|---|---|---|
| `SidebarNavigation.isExpanded / defaultExpanded` | `boolean` | `true` | 展开 240px / 收起 68px（受控 / 非受控） | expand |
| `SidebarNavigation.onExpandedChange` | `(isExpanded: boolean) => void` | — | 点击 Logo 区收起 / 展开按钮时触发 | — |
| `SidebarNavigation.primaryArea` | `ReactNode` | — | 主导航，占满剩余高度、过多时滚动，项间距 2px | primary area（slot） |
| `SidebarNavigation.secondaryArea` | `ReactNode` | — | 次级导航，项间距 2px | secondary area（slot） |
| `SidebarNavigation.footer` | `ReactNode` | — | 底部：升级 / 积分入口与 SidebarAvatar（展开间距 8px，收起 16px） | — |
| `SidebarNavigation.logoHref / logo` | `string / ReactNode` | — | 默认 Logo 的跳转地址 / 替换整个 Logo 区 | — |
| `SidebarNavigation.aria-label` | `string` | `"Main"` | 导航地标的读屏名称 | — |
| `NavigationItem.children` | `ReactNode` | — | 导航文字（circle 时作为读屏名称） | — |
| `NavigationItem.icon / selectedIcon` | `ReactNode` | — | 18px 图标 / 选中时换用的图标 | — |
| `NavigationItem.isSelected` | `boolean` | `false` | 当前页：品牌色 soft 底，输出 aria-current="page" | state=selected |
| `NavigationItem.size` | `"rounded" \| "circle"` | `跟随侧栏` | 216×36 图标 + 文字 / 36×36 仅图标 | size |
| `NavigationItem.href / onPress` | `string / (e: PressEvent) => void` | — | 传 href 渲染为链接，否则渲染为按钮 | — |
| `NavigationItem.endContent` | `ReactNode` | — | 文字右侧 16px 内容（如展开箭头） | DownSmallLine / UpSmallLine（隐藏图层） |
| `SidebarNavigationIcon.variant` | `"home" \| "agent" \| "video" \| "image" \| "quickapps" \| "assets"` | — | 一级入口图标（Icons 库 Line / Fill 对） | variant |
| `SidebarNavigationIcon.isFull` | `boolean` | `跟随 NavigationItem 选中态` | Fill 图标 + accent/soft-foreground | isFull |
| `SidebarLogo.isExpanded / onToggle / href` | `boolean / () => void / string` | `跟随侧栏` | Logo 区（侧栏自动渲染）：展开 = 完整 Logo + 收起按钮；收起 = 圆形 Logo，悬停显示展开按钮 | .Logo state expand / fold / fold-hover |
| `SidebarAvatar.isSignedIn` | `boolean` | `true` | 已登录显示头像（+ 用户名），未登录显示 Sign In 按钮 | .Avatar state（Figma 名称与画面相反） |
| `SidebarAvatar.isExpanded` | `boolean` | `跟随侧栏` | 展开：头像 + 用户名整行 / 宽按钮；收起：40px 头像 / 40px 图标按钮 | .Avatar #1666:2874 / #1666:3104 |
| `SidebarAvatar.src / name` | `string` | — | 头像地址 / 用户名（同时作为读屏名称） | — |
| `SidebarAvatar.href / onPress` | `string / (e: PressEvent) => void` | — | 已登录入口的跳转或点击（也可作为 Dropdown 的触发器） | — |
| `SidebarAvatar.onSignIn / signInLabel` | `(e: PressEvent) => void / string` | `"Sign In"` | 未登录时的登录按钮 | — |
| `TopBarMobile.actions` | `ReactNode` | — | 右侧操作组（间距 8px） | variant（LoggedIn / NotLoggedIn 由内容体现） |
| `TopBarMobile.logo` | `ReactNode` | — | 替换左侧 Logo（默认 DomoAILogo full） | — |
| `TopBarMobile.logoHref` | `string` | — | 默认 Logo 的跳转地址 | — |
| `TopBarMobile.children` | `ReactNode` | — | 完全自定义内容（忽略 logo / actions） | Content（slot） |
| `TopBarMobileAction` | `ButtonProps（无 variant / size）` | — | ghost 36px 纯图标按钮，图标 foreground/secondary；需 aria-label | — |
| `Tabber.children` | `ReactNode` | — | 若干 TabberItem，自动等分宽度 | content（slot） |
| `Tabber.aria-label` | `string` | `"Main"` | 导航地标的读屏名称 | — |
| `TabberItem.children` | `ReactNode` | — | 标签文字（Body/10），isIconOnly 时作为读屏名称 | — |
| `TabberItem.icon / activeIcon` | `ReactNode` | — | 图标 18px（纯图标 38px）/ 选中时换用的图标 | — |
| `TabberItem.isActive` | `boolean` | `false` | 当前页：品牌色 + Body/10-700，输出 aria-current | active（default 取反） |
| `TabberItem.isIconOnly` | `boolean` | `false` | 38px 纯图标大按钮，无选中样式 | only icon |
| `TabberItem.showBadge / badgeLabel` | `boolean / string` | `false` | 图标右上角 6px 品牌色圆点 / 圆点的读屏文字 | showBadge |
| `TabberItem.href` | `string` | — | 链接地址（不传则渲染为按钮，用 onPress） | — |
| `TabberItem.onPress` | `(e: PressEvent) => void` | — | 点击回调（React Aria） | — |
| `Avatar.src` | `string` | — | 头像图片地址，不传或加载失败时显示首字母 | — |
| `Avatar.name` | `string` | — | 用户名：图片替代文本 + 无图时的首字母 | — |
| `Avatar.alt` | `string` | — | 图片替代文本，默认取 name | — |
| `Avatar.fallback` | `ReactNode` | — | 自定义无图时的内容 | — |
| `Avatar.size` | `"sm" \| "md" \| "lg"` | `"md"` | 32 / 36 / 40px | — |

**侧栏**

```tsx
<SidebarNavigation
  logoHref="/"
  primaryArea={
    <>
      <NavigationItem href="/" isSelected icon={<SidebarNavigationIcon variant="home" />}>Home</NavigationItem>
      <NavigationItem href="/assets" icon={<SidebarNavigationIcon variant="assets" />}>Assets</NavigationItem>
    </>
  }
  secondaryArea={<NavigationItem href="/help" icon={<HelpLineIcon />}>Help</NavigationItem>}
  footer={<SidebarAvatar src={user.avatar} name={user.name} onPress={openAccountMenu} />}
/>
```

**移动端顶栏（已登录）**

```tsx
<TopBarMobile
  logoHref="/"
  actions={
    <>
      <TopBarMobileAction aria-label="Inbox" onPress={openInbox}><InboxLineIcon /></TopBarMobileAction>
      <Avatar src={user.avatar} name={user.name} size="sm" />
    </>
  }
/>
```

**底部标签栏**

```tsx
<Tabber>
  <TabberItem href="/" isActive icon={<HomeLineIcon />} activeIcon={<HomeFillIcon />}>Home</TabberItem>
  <TabberItem isIconOnly icon={<PlusLineIcon />} onPress={create}>Create</TabberItem>
  <TabberItem href="/inbox" showBadge badgeLabel="New messages" icon={<InboxLineIcon />}>Inbox</TabberItem>
</Tabber>
```

**基础**

```tsx
<Avatar src={user.avatarUrl} name={user.name} />
```

**顶栏**

```tsx
<Avatar src={user.avatarUrl} name={user.name} size="sm" />
```
