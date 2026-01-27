# Orchids Account Manager

<div align="center">

[![Release](https://img.shields.io/github/v/release/hj01857655/orchids-account-manager?style=flat-square)](https://github.com/hj01857655/orchids-account-manager/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/hj01857655/orchids-account-manager/total?style=flat-square)](https://github.com/hj01857655/orchids-account-manager/releases)
[![License](https://img.shields.io/badge/license-学习交流-blue?style=flat-square)](LICENSE)
[![QQ群](https://img.shields.io/badge/QQ群-1025779377-blue?style=flat-square)](https://qm.qq.com/q/LtgykFYlqM)

Orchids 账号管理工具，基于 Tauri 2 + React 19 + TypeScript 开发。

</div>

---

## 下载安装

前往 [Releases](https://github.com/hj01857655/orchids-account-manager/releases/latest) 下载最新版本：

- **Windows**: `orchids-account-manager_x.x.x_x64-setup.msi`
- **macOS**: `orchids-account-manager_x.x.x_aarch64.dmg`
- **Linux**: 
  - `.deb` - Debian/Ubuntu
  - `.rpm` - RedHat/Fedora/CentOS
  - `.AppImage` - 通用 Linux

## 功能特性

### 📊 仪表盘
- 查看当前账号信息（邮箱、用户 ID）
- 查看套餐信息（套餐名、额度）
- 查看设备信息（机器码）
- 一键刷新最新数据
- 保存当前账号到数据库

### 👥 账号管理
- **添加账号**：支持密码登录和 Cookie 登录
- **批量操作**：导入/导出账号（JSON 格式）
- **账号切换**：快速切换不同账号
- **账号删除**：单个或批量删除

### 🔧 客户端维护
- **重置机器码**：删除 leveldb 目录重置设备标识
- **初始化客户端**：清理 Orchids 全部数据（缓存、Cookie、本地存储）
- **操作日志**：实时显示维护操作日志

### ⚙️ 设置
- **主题切换**：浅色/深色主题
- **窗口记忆**：自动记住窗口大小和位置

## 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | React 19 + TypeScript + Vite 7 |
| 后端 | Rust + Tauri 2 |
| 数据库 | SQLite (tauri-plugin-sql) |
| 样式 | CSS + Framer Motion |
| 图标 | Lucide React |

## 开发

### 环境要求

- Node.js 20+
- Rust 1.70+
- Tauri CLI

### 开发流程

```bash
# 安装依赖
npm install

# 开发模式（热重载）
npm run tauri dev

# 构建生产版本
npm run tauri build

# 代码检查
cargo clippy  # Rust 代码检查
npm run build # TypeScript 类型检查
```

## 项目结构

```
src/                    # 前端代码
├── components/         # 组件
├── pages/              # 页面（懒加载）
├── hooks/              # 自定义 Hooks
├── types/              # 类型定义
└── services/           # 服务层

src-tauri/              # Rust 后端
├── src/commands/       # Tauri 命令
└── capabilities/       # 权限配置
```

## 双仓库原则

本项目遵循双仓库原则：

- **私有仓库 dev 分支**（`orchids-account-manager_dev/dev`）：用于源码开发
- **公开仓库**（`orchids-account-manager`）：仅用于发布 Release

详见：[发布流程](docs/PRIVATE_REPO_RELEASE.md)

## 社区交流

- **QQ 群**: [Orchids 交流群 - 1025779377](https://qm.qq.com/q/LtgykFYlqM)
- **GitHub**: [@hj01857655](https://github.com/hj01857655)

## 许可证

本项目仅供学习交流使用，请勿用于商业用途。

## 文档

- [开发规范](docs/DEVELOPMENT_SPEC.md)
- [发布流程](docs/PRIVATE_REPO_RELEASE.md)
- [Tauri 2 发布工作流](docs/TAURI2_RELEASE_WORKFLOW.md)
