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
