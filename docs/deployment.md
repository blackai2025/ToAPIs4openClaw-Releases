# ToAPIs for OpenClaw 部署总览

## 1. 简介

ToAPIs for OpenClaw 是 OpenClaw 网关的可视化管理工具。  
通过 Web 界面可以完成实例创建、启动/停止、模型配置（含在线切换模型）、日志查看和用户配对码审批。

## 2. 功能特性

- 单文件部署，开箱即用
- 离线安装 — Release 包已内置 Node.js 22、openclaw CLI 和 MinGit (Windows)，无需联网
- 支持 Telegram / Discord / Feishu 渠道
- 支持按实例选择和切换模型
- 支持 pairing code 审批授权
- 支持开机自启（macOS / Windows / Linux systemd）
- 支持一键卸载（Web UI 或 `--uninstall`）
- 国内镜像加速（自动使用国内源下载 Node.js 和 npm 包）

## 3. 前置条件

Release 包已内置所有运行时依赖，**无需额外安装 Node.js 或 openclaw**。

请提前准备：

1. [toapis.com](https://toapis.com) API Key
2. 对应渠道 Bot 凭证（Telegram Token、Feishu App ID/Secret 等）

## 4. 下载与启动

请从 [Releases](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest) 下载对应平台可执行文件：

- Windows x64: `toapis-for-openclaw-win-x64.exe`
- macOS ARM: `toapis-for-openclaw-macos-arm64.zip`
- macOS Intel: `toapis-for-openclaw-macos-x64.zip`
- Linux x64: `toapis-for-openclaw-linux-x64`
- Linux ARM64: `toapis-for-openclaw-linux-arm64`

### 4.1 Windows

1. 下载 `toapis-for-openclaw-win-x64.exe`
2. 右键以管理员身份运行（推荐）
3. 启动后自动打开管理界面

### 4.2 macOS

1. 下载并解压 zip
2. 双击 `start-macos.command` 即可启动（自动处理 macOS 安全限制，无需手动 `xattr`）
3. 浏览器自动打开管理界面

### 4.3 Linux

```bash
chmod +x ./toapis-for-openclaw-linux-x64
./toapis-for-openclaw-linux-x64
```

> 如果程序已在运行，再次执行同一命令不会启动第二个进程，而是直接打开浏览器。

## 5. 管理界面地址

- 本机访问：`http://127.0.0.1:51888`
- 远程访问：`http://<server-ip>:51888`

> 默认监听端口为 `51888`，请确认防火墙已放行。

## 6. 创建实例（通用流程）

1. 打开管理界面，点击新建实例
2. 输入实例名称
3. 选择模型
4. 填写 ToAPIs API Key
5. 选择渠道并填写对应凭证
6. 创建并启动实例

常见实例操作：

- Start
- Stop
- Restart
- Delete
- Verify（校验渠道凭证）
- Approve（审批 pairing code）

## 7. 数据与配置目录

- 管理器配置：`~/.toapis-for-openclaw/config.json`
- OpenClaw 配置：`~/.openclaw/openclaw.json`
- 托管依赖目录：`~/.toapis-for-openclaw/`

## 8. 开机自启

在 Web 管理界面中可开启/关闭"开机自启"开关，启用后系统重启时自动运行 ToAPIs for OpenClaw。

支持平台：

- **macOS** — Launch Agent
- **Windows** — 注册表 Run Key
- **Linux** — systemd user service

## 9. 卸载

### 9.1 Web UI 卸载

在管理界面中点击卸载按钮，将清理所有托管依赖（Node.js、openclaw CLI、MinGit）。

### 9.2 命令行卸载

```bash
./toapis-for-openclaw-linux-x64 --uninstall
```

### 9.3 Windows

除命令行外，也可通过系统"添加或删除程序"卸载。

卸载操作会清理：

- 托管 Node.js 和 npm 全局目录
- openclaw CLI
- MinGit (Windows)
- 自启动配置
- Windows 注册表卸载条目

> 默认**不删除**用户数据（`~/.toapis-for-openclaw/config.json` 和实例配置）。

## 10. 常见问题

### Q1: 页面无法访问

- 检查进程是否已启动
- 检查 `51888` 端口是否被占用
- 检查本机/服务器防火墙策略

### Q2: 已手动安装过 openclaw CLI，如何清理？

推荐使用内置卸载功能（见第 9 节），会自动清理所有托管组件。

如需手动清理，在 Windows 下执行：

```powershell
npm uninstall -g openclaw
Remove-Item -Recurse -Force "$env:USERPROFILE\.openclaw" -ErrorAction SilentlyContinue
```

清理后重新运行 `toapis-for-openclaw-win-x64.exe`，程序会自动安装并管理所需版本。

### Q3: openclaw 安装失败

使用 Release 包中的离线安装通常不会遇到此问题。如果仍然失败：

- 确认 zip/包完整（未损坏或截断）
- 确认磁盘空间充足
- 查看日志输出定位具体报错

### Q4: 实例启动后无响应

- 确认实例状态为 Running
- 重新验证渠道凭证（Verify）
- 检查日志输出定位具体报错

## 11. 下一步

根据你的渠道选择继续阅读：

- Telegram：[`channels/telegram.md`](channels/telegram.md)
- 飞书（Feishu）：[`channels/feishu.md`](channels/feishu.md)
