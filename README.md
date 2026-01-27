# Orchids Account Manager

Orchids 账号管理工具，基于 Tauri 2 + React 19 + TypeScript 开发。

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

## 社区交流

- **QQ 群**: 1025779377
- **GitHub**: [@hj01857655](https://github.com/hj01857655)

## 许可证

本项目仅供学习交流使用，请勿用于商业用途。
