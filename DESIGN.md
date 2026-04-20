# Modern Tech & Glassmorphism Design System (Linear / Raycast Inspired)

## Visual Theme & Atmosphere
- **Mood**: 未来感、沉浸式、极客专业、优雅且轻盈。
- **Philosophy**: 模糊物理与数字的边界，通过光影、磨砂玻璃质感和微妙的层级关系打造高级感。
- **Signature Details**: 动态网格/径向渐变背景、半透明磨砂玻璃卡片（Backdrop Blur）、1px 极细发光边框、平滑入场动画。

## Color Palette & Roles (Dark Mode First)
- **Background**: `#09090b` (深邃黑) 搭配微弱的紫色/蓝色径向渐变光源（如 `radial-gradient(circle at 50% 0%, rgba(120,119,198,0.15), transparent)`）。
- **Card Background**: `rgba(255, 255, 255, 0.03)` (极低透明度白)。
- **Primary Text**: `#ffffff` (纯白，用于标题和输入内容)。
- **Muted Text**: `#a1a1aa` (高级灰，用于分类、提示文本)。
- **Accents**: `#8b5cf6` (霓虹紫) 到 `#3b82f6` (科技蓝) 的渐变，用于按钮和聚焦状态。
- **Borders**: `rgba(255, 255, 255, 0.1)` (半透明细边框，模拟玻璃边缘的反光)。

## Typography Rules
- **Primary Font**: `Inter`, `system-ui`, `-apple-system`。
- **Headings**: 追踪字距收紧 (`letter-spacing: -0.03em`)，呈现锐利的专业感。
- **Data Table**: 表格字体略小（14px），分类标签使用大写字母（Uppercase）增加结构感。

## Layout Principles
- **Container**: 居中对齐，最大宽度 900px，周围留有充足的呼吸空间。
- **Spacing**: 采用 8px 基础网格系统（16px, 24px, 32px, 48px, 64px）。

## Depth & Elevation
- **Glass Cards**: 采用 `backdrop-filter: blur(24px)` 配合多重微弱阴影（如 `box-shadow: 0 4px 24px -1px rgba(0,0,0,0.2), 0 0 1px rgba(255,255,255,0.1)`）制造悬浮感。
- **Inputs/Rows**: 交互元素在 Hover 时，背景亮度微调 (`rgba(255,255,255,0.06)`)，Focus 时出现柔和的外发光（Glow）。

## Component Stylings
- **Table**: 摒弃传统的全包围网格线，仅保留极其微弱的行底边（或者在深色模式下使用行间距），让数据“悬浮”在玻璃板上。分类单元格（Category）高亮展示。
- **Editable Cells**: 类似 Notion 的无缝编辑体验。平时就像普通文本，悬停时出现微妙底色，点击时出现紫色光环边框。
- **Buttons**: 
  - **Primary**: 带有微妙渐变和发光阴影的实心按钮，点击时有真实的物理下压感（`transform: scale(0.96)`）。
  - **Secondary**: 玻璃质感描边按钮，Hover 时边框变亮。

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
- 内置 5 套完整的预设模板，一键加载：
  - ⌨️ **程序员**：RTOS、Python/Rust/Go、Linux内核、机械臂。
  - 🎨 **设计师**：Figma、极简/莫兰迪配色、矢量插画。
  - 📚 **学生**：STM32、神经网络、B站教程、游戏/二次元。
  - 📋 **产品经理**：Agent开发、商业分析、结构化表格。
  - ✨ **创作者**：Prompt工程、赛博朋克/毛玻璃、3D渲染。
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
