# Orchids Account Manager

<div align="center">

![Logo](https://img.shields.io/badge/Orchids-Account%20Manager-blue?style=for-the-badge)
[![Release](https://img.shields.io/github/v/release/hj01857655/orchids-account-manager?style=for-the-badge)](https://github.com/hj01857655/orchids-account-manager/releases)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)

**Orchids 桌面客户端的账号管理工具**

[下载](#-下载) • [功能](#-功能特性) • [使用](#-使用说明) • [反馈](#-问题反馈)

</div>

---

## ✨ 功能特性

### 账号管理
- 🔐 **多账号支持** - 管理多个 Orchids 账号
- 🔄 **快速切换** - 一键切换不同账号
- 📝 **账号信息** - 查看账号详细信息
- 🏷️ **自定义备注** - 为账号添加备注名称

### 实用工具
- 🛠️ **工具集成** - 内置常用工具
- 📊 **数据统计** - 账号使用统计
- ⚙️ **设置管理** - 个性化配置

### 安全性
- 🔒 **本地存储** - 数据存储在本地，不上传云端
- 🔑 **加密保护** - 敏感信息加密存储
- 🛡️ **隐私优先** - 不收集用户隐私数据

## 📥 下载

前往 [Releases](https://github.com/hj01857655/orchids-account-manager/releases) 页面下载最新版本。

### 支持平台

| 平台 | 文件格式 | 说明 |
|------|---------|------|
| Windows | `.msi` | Windows 10/11 (64-bit) |
| macOS | `.dmg` | macOS 11+ (Apple Silicon & Intel) |
| Linux | `.deb` | Ubuntu/Debian 系列 |

### 系统要求

- **Windows**: Windows 10 或更高版本
- **macOS**: macOS 11 (Big Sur) 或更高版本
- **Linux**: Ubuntu 20.04+ / Debian 11+

## 📖 使用说明

### 安装

#### Windows
1. 下载 `.msi` 安装包
2. 双击运行安装程序
3. 按照向导完成安装

#### macOS
1. 下载 `.dmg` 文件
2. 打开 DMG 文件
3. 将应用拖入 Applications 文件夹

#### Linux
```bash
# 下载 .deb 文件后
sudo dpkg -i orchids-account-manager_*.deb
```

### 快速开始

1. **启动应用** - 双击桌面图标或从应用列表启动
2. **添加账号** - 点击"添加账号"按钮
3. **填写信息** - 输入账号信息
4. **开始使用** - 选择账号并使用相关功能

### 常见问题

<details>
<summary>如何导入现有账号？</summary>

在"账号管理"页面点击"导入"按钮，选择账号数据文件。
</details>

<details>
<summary>数据存储在哪里？</summary>

- Windows: `%APPDATA%\orchids-account-manager\`
- macOS: `~/Library/Application Support/orchids-account-manager/`
- Linux: `~/.config/orchids-account-manager/`
</details>

<details>
<summary>如何卸载？</summary>

- Windows: 控制面板 → 程序和功能 → 卸载
- macOS: 从 Applications 文件夹删除
- Linux: `sudo apt remove orchids-account-manager`
</details>

## 🛠️ 技术栈

- **前端**: React 18 + TypeScript + Vite
- **后端**: Rust + Tauri 2.0
- **数据库**: SQLite
- **UI**: CSS Modules

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

## 💬 问题反馈

- 🐛 **Bug 报告**: [提交 Issue](https://github.com/hj01857655/orchids-account-manager/issues/new?labels=bug)
- 💡 **功能建议**: [提交 Issue](https://github.com/hj01857655/orchids-account-manager/issues/new?labels=enhancement)
- 📧 **联系方式**: 1292548381@qq.com

---

<div align="center">

**⭐ 如果这个项目对你有帮助，请给个 Star！**

Made with ❤️ by [hj01857655](https://github.com/hj01857655)

</div>
