# Apple HIG Frontend Designer

<div align="center">

![Apple HIG](https://img.shields.io/badge/Apple-HIG-000000?style=for-the-badge&logo=apple&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude-Code_Skill-5A67D8?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A professional-grade Claude Code Skill for creating interfaces following Apple's Human Interface Guidelines (HIG)**

[English](#english) | [中文](#中文)

</div>

---

## English

### 🎯 Overview

This Claude Code Skill enables you to design professional web and mobile interfaces that follow Apple's Human Interface Guidelines. It provides comprehensive knowledge about:

- **Liquid Glass Effects** (iOS 26 / macOS Tahoe style)
- **SF Pro Typography** system
- **Apple System Colors** with light/dark mode support
- **8pt Grid Spacing System**
- **Component Patterns** (buttons, cards, inputs, etc.)
- **Animation Guidelines** with Apple-standard easing curves

### 📦 Installation

#### Method 1: User-level Installation (Recommended)

Copy the skill to your Claude Code skills directory:

```bash
# Windows
xcopy /E /I "apple-hig-designer" "%USERPROFILE%\.claude\skills\apple-hig-designer"

# macOS / Linux
cp -r apple-hig-designer ~/.claude/skills/
```

#### Method 2: Project-level Installation

Copy to your project's `.claude/skills` directory:

```bash
mkdir -p .claude/skills
cp -r apple-hig-designer .claude/skills/
```

### 🚀 Usage

Once installed, Claude Code will automatically activate this skill when you:

- Ask for "Apple-style" or "iOS/macOS-style" interfaces
- Request "HIG-compliant" UI components
- Mention "Liquid Glass" design effects
- Use trigger phrases like:
  - "Design an Apple-style..."
  - "Create a HIG-compliant..."
  - "苹果风格的界面"

### 📁 File Structure

```
apple-hig-designer/
├── Skill.md              # Main skill definition
├── REFERENCE.md          # Detailed HIG reference documentation
├── README.md             # This file
├── LICENSE               # MIT License
└── resources/
    ├── components.jsx    # React component examples
    ├── design-tokens.css # CSS custom properties
    └── ui-patterns.md    # UI pattern documentation
```

### 🎨 Features

| Feature | Description |
|---------|-------------|
| **Typography** | SF Pro font system with proper size thresholds |
| **Colors** | Complete Apple system color palette |
| **Spacing** | 8pt grid system implementation |
| **Components** | Buttons, cards, inputs, glass panels |
| **Animations** | Apple-standard cubic-bezier easing |
| **Accessibility** | WCAG AA compliant, reduced motion support |
| **Dark Mode** | Full light/dark mode support |

### 📚 Resources

- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)
- [Apple Design Resources](https://developer.apple.com/design/resources/)
- [SF Symbols](https://developer.apple.com/sf-symbols/)

---

## 中文

### 🎯 概述

这是一个专业级的 Claude Code Skill，用于创建符合 Apple 人机界面指南的专业界面设计。包含以下知识：

- **Liquid Glass 毛玻璃效果** (iOS 26 / macOS Tahoe 风格)
- **SF Pro 字体系统**
- **Apple 系统色彩** (支持亮色/暗色模式)
- **8pt 网格间距系统**
- **组件模式** (按钮、卡片、输入框等)
- **动画指南** (Apple 标准缓动曲线)

### 📦 安装方法

#### 方法一：用户级安装 (推荐)

将 Skill 复制到 Claude Code 技能目录：

```bash
# Windows
xcopy /E /I "apple-hig-designer" "%USERPROFILE%\.claude\skills\apple-hig-designer"

# macOS / Linux
cp -r apple-hig-designer ~/.claude/skills/
```

#### 方法二：项目级安装

复制到项目的 `.claude/skills` 目录：

```bash
mkdir -p .claude/skills
cp -r apple-hig-designer .claude/skills/
```

### 🚀 使用方法

安装后，当您进行以下操作时，Claude Code 会自动激活此 Skill：

- 请求 "Apple 风格" 或 "iOS/macOS 风格" 的界面
- 请求 "符合 HIG 规范" 的 UI 组件
- 提及 "Liquid Glass" 或 "毛玻璃" 设计效果
- 使用触发短语：
  - "设计一个苹果风格的..."
  - "创建一个符合 HIG 的..."
  - "iOS 风格的组件"

### 🎨 功能特性

| 功能 | 描述 |
|------|------|
| **字体排版** | SF Pro 字体系统，正确的尺寸阈值 |
| **色彩系统** | 完整的 Apple 系统色彩调色板 |
| **间距系统** | 8pt 网格系统实现 |
| **组件库** | 按钮、卡片、输入框、毛玻璃面板 |
| **动画效果** | Apple 标准三次贝塞尔缓动 |
| **无障碍** | WCAG AA 合规，减少动效支持 |
| **深色模式** | 完整的亮色/暗色模式支持 |

### 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

---

<div align="center">

Made with ❤️ for the Claude Code community

</div>
