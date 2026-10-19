<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | 微软旧注音 (ㄅ半) 一键免费安装器" height="70" />
</a>

<br /><br />

[繁體中文](../../README.md) · [English](README_en.md) · **简体中文**

# 微软旧注音 (ㄅ半) 一键免费安装器 (Microsoft Legacy Bopomofo 1-Click Installer)

### 专为 Windows 10 / 11 系统打造的原生一键安装、自动修复与还原工具
告别升级 Windows 10/11 后找不到旧注音、新版记事本无选字框的困扰！一键极速找回熟悉顺手的输入体验。

[![Platform](https://img.shields.io/badge/Platform-Windows%207%20%7C%208%20%7C%2010%20%7C%2011%20%7C%20WinPE-blue?style=flat-square&logo=windows)](https://github.com/robert820/winxp-bopomofo-installer)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](../../LICENSE)
[![Type](https://img.shields.io/badge/Type-Freeware%20%7C%20Portable-success?style=flat-square)](#-下载与使用说明)
[![Download](https://img.shields.io/badge/Download-GitHub%20Releases-blue?style=flat-square&logo=github)](https://github.com/robert820/winxp-bopomofo-installer/releases)

[软件简介](#-软件简介) · [核心功能](#-核心功能) · [软件操作画面](#-软件操作画面) · [下载与使用说明](#-下载与使用说明) · [系统需求](#-系统兼容性与需求) · [常见问题](#-常见问题-faq) · [问题反馈](#-问题反馈与支持)

</div>

---

## 📖 软件简介

“微软旧注音（ㄅ半）”陪伴无数传统中文用户数十年，以确定性高、打字迅速、不强制自动联想选字等特性深受众多用户、程序员与行政办公人员喜爱。

然而自从微软推出 **Windows 10** 与 **Windows 11** 以来：
1. 系统默认移除了旧注音选项，仅保留微软新注音。
2. 许多用户手动导入传统注册表后，常遇到系统更新后失效、在新版记事本 (Notepad)、Office 或浏览器中无法出字、候选字框消失等 TSF 框架兼容性问题。
3. 手动修改注册表步骤繁琐，稍有不慎容易影响系统语言设置。

**“微软旧注音 (ㄅ半) 一键免费安装器”** 由得翼科技 (DEI 3C) 基于 Rust 与现代化 Slint GUI 框架打造，专为简化安装流程设计。程序能自动识别系统架构与版本，完整配置系统注册表（包含关键的 Tsf3Override 与 TSF TIP 注册）、自动调用原生 API 并重启输入法服务，**无须重启电脑，一键即可找回微软旧注音！**

---

## ✨ 核心功能

### 1. ⚡ 一键自动化极速安装
- 自动检测当前 Windows 版本 (Win 11 / 10 / 8.1 / 8 / 7) 与架构 (x64 / x86)。
- 自动配置系统注册表项，注入关键 Tsf3Override 与 TSF TIP 注册，完美兼容新版 Windows 现代应用程序。
- 调用 Windows 原生 InstallLayoutOrTip API 并重启 ctfmon.exe，安装完毕立即可用，免重启系统！

### 2. 🔄 一键干净卸载还原
- 若日后不再需要使用，可随时点击“解除安装”，一键还原系统设置，不残留冗余注册表垃圾。

### 3. 📋 实时进度日志与一键复制
- 界面内嵌可视化安装进度日志，清晰呈现每一步系统配置流程。
- 支持“复制日誌”功能，方便排查与技术支持。

### 4. 🔒 纯净绿色、零隐私传输 (100% Offline & Pure Privacy)
- 软件完全在本地离线运行，无任何网络请求与数据传输。
- 绝不收集、记录或上传任何按键记录与个人隐私数据。
- 32 位通用 PE 原生单文件（Portable），无须安装任何外部运行库，亦可放入 WinPE 维护 U 盘即插即用。

---

## 📸 软件操作画面

<div align="center">
  <img src="../../images/應用程式執行畫面.png" alt="微软旧注音 (ㄅ半) 一键免费安装器 软件操作界面" width="720" />
</div>

---

## 📦 下载与使用说明

### 📥 下载方式
1. 前往本项目的 [Releases 页面](https://github.com/robert820/winxp-bopomofo-installer/releases) 下载最新版 微軟舊注音 (ㄅ半) 一鍵免費安裝器.exe。
2. 本程序为**单一免安装绿色执行文件**，下载后即可直接运行。

### 🚀 安装操作指南
1. **以管理员身份运行**：由于本工具需要调用 Windows 系统级输入法 API 并写入注册表，请右键点击程序选择“以管理员身份运行”。
2. **点击“開始安裝”**：程序会自动完成系统检测、注册表配置与服务唤醒，整个过程仅需 1~3 秒。
3. **切换使用**：安装成功后，按快捷键（如 Ctrl + Shift 或 Win + Space）切换至“微软旧注音 (ㄅ半)”即可开始输入！

---

## 🖥️ 系统兼容性与需求

- **操作系统**：Windows 11 / 10 / 8.1 / 8 / 7 (SP1)
- **架构支持**：64 位 (x64) 与 32 位 (x86)
- **运行权限**：需要管理员权限 (Administrator)
- **环境依赖**：单一原生绿色执行文件，免安装任何外部运行时

---

## ❓ 常见问题 (FAQ)

<details>
<summary><b>Q1: 为什么安装完成后在某些新版软件（如新版记事本或 Word）中打不出字？</b></summary>
A: 本工具已默认配置微软 TSF (Text Services Framework) 兼容注册表项与 Tsf3Override。如果在极少数系统环境下仍出现选字框异常，请尝试将该应用程序完全关闭后重新打开，或重启一次电脑使后台服务完全加载。
</details>

<details>
<summary><b>Q2: 这款软件完全免费吗？电脑维修同行可以使用吗？</b></summary>
A: 是的！本软件免费供个人、企业与电脑维修工作室使用，亦可自由放置于工程维护 U 盘中为客户安装修复旧注音。但严禁单独售卖、出租或捆绑收费营利。
</details>

<details>
<summary><b>Q3: 为什么杀毒软件偶尔会提示误报？</b></summary>
A: 本程序为 Rust 编写的纯净原生工具，绝无恶意代码。由于注册系统级输入法必须修改注册表并重启 ctfmon 服务，部分安全软件的启发式扫描判定较严格，请放心允许运行或加入信任白名单。
</details>

---

## 💬 问题反馈与支持

- 🐛 **错误反馈与建议**：欢迎至本项目的 [Issues 页面](https://github.com/robert820/winxp-bopomofo-installer/issues) 提交。
- 🌐 **得翼科技官方网站**：[https://blog.dei3c.com](https://blog.dei3c.com)

---

## 📄 授权条款 (License)

本软件采用专有免费软件授权（Proprietary Freeware），完整授权条款与免责声明请参阅 [LICENSE](../../LICENSE) 文件。
