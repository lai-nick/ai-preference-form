# Modern Tech & Glassmorphism Design System (Apple / Vercel Inspired)

## Visual Theme & Atmosphere
- **Mood**: 未来感、沉浸式、极客专业、优雅且极其克制。
- **Philosophy**: 模糊物理与数字的边界，通过光影、高级毛玻璃质感和微妙的层级关系打造高奢感。完全摒弃大面积的彩色霓虹渐变，转而追求 Apple 硬件设计般的物理材质感（阳极氧化铝/钛金属光泽）。
- **Signature Details**: 
  - 点阵网格（Dotted Matrix）与多重径向渐变（Radial Gradient）组成的环境光背景。
  - 半透明高级毛玻璃卡片（`backdrop-filter: blur(32px) saturate(150%)`）。
  - 1px 极细高光内边框（模拟玻璃/金属倒角反光）。
  - 极简黑白灰（Monochrome）高对比度文字。

## Color Palette & Roles (Dark Mode First)
- **Background**: `#000000` (纯黑) 搭配多层纯白微弱径向渐变光源（如 `rgba(255,255,255,0.05)`）以及点阵背景。
- **Card Background**: `rgba(24, 24, 27, 0.4)` (极低透明度黑灰)，透过背景光效呈现深空灰色。
- **Primary Text**: `#f4f4f5` (高亮白，用于标题和输入内容)。
- **Muted Text**: `#a1a1aa` (高级灰，用于分类、提示文本)。
- **Accents**: `#e4e4e7` (白银色) 到 `#71717a` (深空灰) 的渐变，完全取代了前期的蓝紫渐变。用于按钮、进度条和聚焦状态。
- **Borders**: 外边框 `rgba(255, 255, 255, 0.06)` 配合内高光 `rgba(255, 255, 255, 0.1)` 制造物理厚度感。

## Typography Rules
- **Primary Font**: `-apple-system`, `BlinkMacSystemFont`, `"SF Pro Display"`, `"PingFang SC"`。全面向 Apple 原生字体栈靠拢。
- **Headings**: 追踪字距收紧 (`letter-spacing: -0.05em`)，采用金属拉丝风格的文字渐变填色，呈现极其锐利的专业感。
- **Data Table**: 表格字体略小（14px），内边距紧凑 (`10px 16px`)，分类标签使用大写字母（Uppercase）增加结构感。

## Depth & Elevation
- **Glass Cards**: 采用强效 `backdrop-filter: blur(32px) saturate(150%)` 配合厚重的底部柔和阴影 (`box-shadow: 0 24px 48px -12px rgba(0,0,0,0.8)`) 和顶部内高光，制造强烈的悬浮与物理质感。
- **Inputs/Rows**: 交互元素在 Hover 时，背景亮度微调 (`rgba(255,255,255,0.04)`)，Focus 时出现柔和的纯白外发光。
- **Active States**: 激活的标签页（Active Tab）采用高反差（白底黑字或黑底白字），配以微弱阴影使其从背景中凸显。

## Component Stylings
- **Table**: 摒弃传统的全包围网格线，仅保留极其微弱的行底边，让数据“悬浮”在玻璃板上。
- **Editable Cells**: 类似 Notion 的无缝编辑体验。平时就像普通文本，悬停时出现微妙底色，点击时出现纯白/银色光环边框。
- **Buttons / Dropdowns**: 
  - 下拉菜单（Dropdowns）与弹窗（Modals）同样继承高级毛玻璃质感，悬浮于页面最顶层。
  - 操作按钮回归极简，使用无彩色的高对比色调，点击时有真实的物理下压感（`transform: scale(0.96)`）。

## Animations & Interactions
- **Reveal**: 页面加载时内容容器从下往上渐现（Fade in up）。
- **Hover Transitions**: 所有颜色、边框和阴影变化使用 `0.3s cubic-bezier(0.4, 0, 0.2, 1)` 曲线，如丝般顺滑。

## Features (Phase 1 Updates)

### 深色 / 浅色模式切换
- 通过顶部右侧的圆形按钮一键切换深色（默认）和浅色模式。
- 使用 CSS `:root.light` 覆盖变量实现完整配色切换。
- 主题偏好保存至 `localStorage`，刷新后自动恢复。

### 填写进度条
- 位于标题与表格之间，实时显示已填写的单元格数量。
- 渐变色进度条（紫色 → 蓝色），平滑动画过渡。

### 多格式导出下拉菜单
- 导出按钮改为下拉菜单，支持一键切换导出格式：
  - **Markdown**：AI 助手指令 + 表格数据（复制给 Trae / ChatGPT / Claude）。
  - **JSON**：结构化数据，含填写数量统计（方便程序读取或导入/备份）。
  - **System Prompt**：直接可粘贴进 AI 系统提示词的角色设定模板。
  - **纯文本**：简单文字，无格式，可复制到任何地方。

### 一键重置
- 左下角新增红色警示风格的重置按钮。
- 点击前需二次确认，防止误操作。操作后进度条同步归零。

## Features (Phase 2 Updates)

### 多档案管理系统 (Multi-Profile)
- 支持创建任意数量的命名档案（如"程序员"、"设计师"、"工作"、"生活"等）。
- 档案以标签页（Profile Tabs）形式显示在标题下方，点击即可一键切换。
- 每个档案的数据完全独立，互不干扰。
- 所有档案数据保存至 `localStorage`，刷新不丢失。
- 新建档案：点击 "+ 新建档案" 按钮，输入名称即可。
- 删除档案：点击档案标签右侧的 × 按钮（默认档案不可删除）。

### 预设模板系统 (Preset Templates)
- 内置 6 套精细化双语职业画像模板，一键加载：
  - ⌨️ **工程师**：RTOS、Python/Rust/Go、Linux内核、机械臂。
  - 🎨 **设计师**：Figma、极简/莫兰迪配色、矢量插画。
  - 📚 **学生**：STM32、神经网络、B站教程、游戏/二次元。
  - 📋 **产品经理**：Agent开发、商业分析、结构化表格。
  - ✨ **创作者**：Prompt工程、赛博朋克/毛玻璃、3D渲染。
  - 🔬 **科研人员**：文献阅读、数据分析、论文写作。
- 模板以卡片网格（Modal + TemplateGrid）形式展示，点击即可填充所有格子。
- 模板加载后仍可自由修改。

### JSON 导入 / 备份恢复
- 支持上传之前导出的 `.json` 备份文件，一键恢复所有配置。
- 导入时自动创建为新档案，保留原始档案名称。
- 每个档案均支持"导出 JSON"实现完整备份。

### 数据结构化重构
- 所有问题配置（分类、ID、选项）与表格 HTML 分离，由 `TABLE_ROWS` JS 常量统一驱动。
- `TEMPLATE_DATA` 数组统一管理所有选项标签（`data-options`）。
- 新增问题或修改选项只需修改 JS 常量，无需改动 HTML 结构。

## Features (Phase 3 Updates)

### 国际化双语支持 (i18n)
- **中英文切换**：右上角增加语言切换按钮（中/EN）
- **全 UI 双语**：涵盖页面标题、分类标签、提示文本、弹窗按钮等全部文字内容
- **双语数据结构**：预设模板和建议选项均支持中英文隔离，切换语言时自动更新当前语言的下拉建议和占位符
- **持久化配置**：语言偏好同样保存在 LocalStorage 中，刷新页面不丢失

## 4. 未来扩展可能性 (Roadmap)
