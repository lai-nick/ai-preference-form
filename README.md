# 🧠 AI Preference Form | 个人偏好与技能设定系统

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-yellow.svg)
![Design](https://img.shields.io/badge/Design-Glassmorphism-purple.svg)

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

## 🚀 快速开始 (Quick Start)

因为本项目是一个纯静态页面，您无需安装任何依赖（如 Node.js 或 npm）。

### 本地预览

1. 克隆或下载本仓库到本地。
   ```bash
   git clone https://github.com/您的用户名/ai-preference-form.git
   ```
2. 直接双击打开 `index.html`，或者使用 VS Code 的 Live Server 插件、Python 简易服务器等启动：
   ```bash
   # Python 3
   python3 -m http.server 8000
   ```
3. 在浏览器中访问 `http://localhost:8000` 即可体验。

## 🌐 部署指南 (Deployment)

由于没有后端，本项目非常适合部署在 **Vercel**、**GitHub Pages** 或 **Netlify** 等免费静态托管平台上。

### 使用 Vercel 部署 (推荐)

1. 确保您的代码已经推送到 GitHub 仓库。
2. 访问 [Vercel](https://vercel.com/) 并使用 GitHub 账号登录。
3. 点击 **"Add New Project"**，选择导入（Import）您刚才推送的 `ai-preference-form` 仓库。
4. 框架预设（Framework Preset）保持默认的 **Other**。
5. 点击 **Deploy**。
6. 几秒钟后，您的表单就成功上线并拥有了一个免费的 HTTPS 域名！

### 使用 GitHub Pages 部署

1. 在您的 GitHub 仓库页面，点击顶部的 **Settings**。
2. 在左侧菜单找到 **Pages**。
3. 在 **Source** 下的下拉菜单中，选择 `main` 分支，并点击 Save。
4. 几分钟后，您的页面就会发布在 `https://您的用户名.github.io/ai-preference-form/`。

## 📖 如何使用导出的数据？

1. 在网页上完成所有偏好的填写。
2. 点击页面右下角的 **“复制为 Markdown”**。
3. 打开您常用的 AI 对话窗口（如 Trae / ChatGPT / Claude）。
4. 将剪贴板的内容直接粘贴并发送。
5. 享受 AI 为您生成的深度解析与 4 周专属成长计划！

## 📄 许可证 (License)

本项目基于 [MIT License](LICENSE) 协议开源，您可以自由地使用、修改和分发。
