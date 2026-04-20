# 🧠 AI Preference Form | 个人偏好与技能设定系统

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-yellow.svg)
![Design](https://img.shields.io/badge/Design-Glassmorphism-purple.svg)

👉 **在线体验 (Online Demo): [https://ai-preference-form.vercel.app](https://ai-preference-form.vercel.app)**

一个专为 AI（如 ChatGPT、Claude、Trae、Cursor 等大语言模型）设计的**“数字分身记忆注入表单”**。

通过极其优雅的现代科技风（Glassmorphism）界面，引导用户填写个人技术栈、审美偏好、生活习惯与沟通风格。填写完成后，一键生成结构化的 **AI Prompt (提示词) + Markdown 报告**，直接发送给 AI 助手，让它瞬间了解你的所有偏好，化身为最懂你的私人成长教练和代码助理。

## ✨ 核心特性 (Features)

- 🎨 **极简高级的 UI 设计 (Modern Tech & Glassmorphism)**
  - 沉浸式的暗黑科技背景与动态微弱光源映射。
  - 毛玻璃（Backdrop Blur）质感的悬浮卡片。
  - 克制的交互反馈与丝滑的 CSS 动画。
- ⚡ **无后端依赖 (Serverless & Zero-Backend)**
  - 纯前端实现，无需配置任何数据库或服务端。
  - 数据自动实时保存在浏览器的本地存储（LocalStorage）中，刷新不丢失。
- 🏷️ **智能悬浮标签 (Smart Dropdown Tags)**
  - 内置 28 个维度（技术栈、审美、习惯等）的丰富预设标签。
  - 点击单元格自动弹出下拉菜单，支持鼠标点击与手写输入无缝混排。
- 🤖 **AI Prompt 工程级导出 (Prompt Engineering Export)**
  - 一键导出包含特定指令的 Markdown 文本。
  - 引导 AI 建立本地记忆、深度分析用户偏好、定制学习计划及调整回复语气。
- 📱 **响应式布局 (Responsive Design)**
  - 完美适配桌面端和移动端浏览。

## 📖 如何使用？

1. 点击上方链接访问在线表单。
2. 在网页上完成所有偏好的填写（可直接点击下拉标签或手动输入）。
3. 点击页面右下角的 **“复制为 Markdown”**。
4. 打开您常用的 AI 对话窗口（如 Trae / ChatGPT / Claude）。
5. 将剪贴板的内容直接粘贴并发送。
6. 享受 AI 为您生成的深度解析与专属成长计划！

## 💡 AI Prompt 魔法原理解析

当您点击“复制”时，系统并不是单纯地导出一个死板的表格，而是在表格顶部**注入了一段经过精心设计的 AI 角色扮演指令 (System Prompt)**。

这段 Prompt 将直接“调教”大语言模型完成以下三个核心任务：

1. **自动建立数字分身档案 (Memory)**：
   - 如果您使用的是具备本地文件写入能力的 AI 助手（如 Trae、Cursor 或特定的本地化 Agent），Prompt 会要求 AI 主动在您的项目空间内创建一个 `.md` 存档。
   - 它会强制 AI 提取并“记住”您的核心偏好（如“极简主义”、“Apple风”、“专业高冷”），以便未来的对话风格和代码生成都能与您高度同频。
2. **多维度的深度性格与技术分析**：
   - 强迫 AI 跨越单纯的“问答”，去洞察您在“技术栈底层”、“艺术审美”和“生活节奏”之间潜在的联系，为您画出一幅精准的“个人画像”。
3. **自动输出 4 周定制成长计划**：
   - 结合您的“近期目标”，AI 会直接输出一份结构化的学习路线图。
   - 并附带符合您审美的资源（开源库、设计参考等）推荐。

## 📄 许可证 (License)

本项目基于 [MIT License](LICENSE) 协议开源，您可以自由地使用、修改和分发。