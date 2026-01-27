# Orchids Account Manager

<div align="center">

[![Release](https://img.shields.io/github/v/release/hj01857655/orchids-account-manager?style=flat-square)](https://github.com/hj01857655/orchids-account-manager/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/hj01857655/orchids-account-manager/total?style=flat-square)](https://github.com/hj01857655/orchids-account-manager/releases)
[![License](https://img.shields.io/badge/license-学习交流-blue?style=flat-square)](LICENSE)
[![QQ群](https://img.shields.io/badge/QQ群-1025779377-blue?style=flat-square)](https://qm.qq.com/q/LtgykFYlqM)

Orchids 账号管理工具，基于 Tauri 2 + React 19 + TypeScript 开发。

[下载安装](#下载安装) • [功能特性](#功能特性) • [使用说明](#使用说明) • [常见问题](#常见问题) • [社区交流](#社区交流)

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

### 安装步骤

**Windows**:
1. 下载 `.msi` 安装包
2. 双击运行安装程序
3. 按照向导完成安装

**macOS**:
1. 下载 `.dmg` 文件
2. 打开 dmg 文件，将应用拖入 Applications 文件夹
3. 首次运行可能需要在"系统偏好设置 > 安全性与隐私"中允许

**Linux**:
```bash
# Debian/Ubuntu
sudo dpkg -i orchids-account-manager_x.x.x_amd64.deb

# RedHat/Fedora/CentOS
sudo rpm -i orchids-account-manager_x.x.x_x86_64.rpm

# AppImage（无需安装）
chmod +x orchids-account-manager_x.x.x_amd64.AppImage
./orchids-account-manager_x.x.x_amd64.AppImage
```

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

## 使用说明

### 首次使用

1. **启动应用**：安装完成后启动 Orchids Account Manager
2. **添加账号**：
   - 点击"账号管理"页面
   - 点击"添加账号"按钮
   - 选择登录方式（密码登录或 Cookie 登录）
   - 填写账号信息并保存
3. **切换账号**：在账号列表中点击"切换"按钮

### 账号导入导出

**导出账号**：
1. 进入"账号管理"页面
2. 点击"导出账号"按钮
3. 选择保存位置，文件格式为 JSON

**导入账号**：
1. 进入"账号管理"页面
2. 点击"导入账号"按钮
3. 选择之前导出的 JSON 文件

### 客户端维护

**重置机器码**：
1. 进入"工具"页面
2. 点击"重置机器码"按钮
3. 确认操作后，leveldb 目录将被删除

**初始化客户端**：
1. 进入"工具"页面
2. 点击"初始化客户端"按钮
3. 确认操作后，所有 Orchids 数据将被清理

⚠️ **注意**：初始化操作会清除所有本地数据，请谨慎操作！

## 常见问题

### Q: Windows 提示"无法验证发布者"怎么办？
A: 这是正常现象，因为应用未签名。点击"更多信息" → "仍要运行"即可。

### Q: macOS 提示"无法打开，因为无法验证开发者"？
A: 有两种解决方法：

**方法 1（推荐）**：使用终端移除隔离属性
```bash
# 进入 Applications 目录
cd /Applications

# 移除隔离属性
sudo xattr -rd com.apple.quarantine "Orchids Account Manager.app"
```

**方法 2**：手动允许
1. 右键点击应用 → 选择"打开"
2. 在弹出的对话框中点击"打开"
3. 或在"系统偏好设置 > 安全性与隐私"中允许

### Q: 账号数据存储在哪里？
A: 
- **Windows**: `%APPDATA%\orchids-account-manager\data.db`
- **macOS**: `~/Library/Application Support/orchids-account-manager/data.db`
- **Linux**: `~/.local/share/orchids-account-manager/data.db`

### Q: 如何备份账号数据？
A: 使用"导出账号"功能将账号导出为 JSON 文件，或直接备份上述数据库文件。

### Q: 支持哪些 Orchids 客户端版本？
A: 理论上支持所有版本，但建议使用最新版本的 Orchids 客户端。

### Q: 遇到问题如何反馈？
A: 
1. 加入 QQ 群：[Orchids 交流群 - 1025779377](https://qm.qq.com/q/LtgykFYlqM)
2. 在 GitHub 提交 [Issue](https://github.com/hj01857655/orchids-account-manager/issues)

## 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | React 19 + TypeScript + Vite 7 |
| 后端 | Rust + Tauri 2 |
| 数据库 | SQLite (tauri-plugin-sql) |
| 样式 | CSS + Framer Motion |
| 图标 | Lucide React |

## 更新日志

查看 [Releases](https://github.com/hj01857655/orchids-account-manager/releases) 了解每个版本的更新内容。

## 社区交流

- **QQ 群**: [Orchids 交流群 - 1025779377](https://qm.qq.com/q/LtgykFYlqM)
- **GitHub**: [@hj01857655](https://github.com/hj01857655)
- **Issues**: [反馈问题](https://github.com/hj01857655/orchids-account-manager/issues)

## 许可证

本项目仅供学习交流使用，请勿用于商业用途。

---

<div align="center">

**如果觉得有用，欢迎 Star ⭐**

</div>
