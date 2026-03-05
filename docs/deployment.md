# ToAPIs for OpenClaw 部署总览

## 1. 简介

ToAPIs for OpenClaw 是 OpenClaw 网关的可视化管理工具。  
通过 Web 界面可以完成实例创建、启动/停止、模型配置、日志查看和用户配对码审批。

## 2. 功能特性

- 单文件部署，开箱即用
- 首次运行自动检测依赖（Node.js / openclaw CLI）
- 支持 Telegram / Discord / Feishu 渠道
- 支持按实例选择模型
- 支持 pairing code 审批授权
- 支持系统自启动开关

## 3. 前置条件

请提前准备：

1. [toapis.com](https://toapis.com) API Key
2. 对应渠道 Bot 凭证（Telegram Token、Feishu App ID/Secret 等）

## 4. 下载与启动

请从 Releases 下载对应平台可执行文件：

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
2. 若被系统拦截，按提示在安全设置中放行
3. 运行程序并访问管理界面

### 4.3 Linux

```bash
chmod +x ./toapis-for-openclaw-linux-x64
./toapis-for-openclaw-linux-x64
```

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

## 8. 常见问题

### Q1: 页面无法访问

- 检查进程是否已启动
- 检查 `51888` 端口是否被占用
- 检查本机/服务器防火墙策略

### Q2: openclaw 安装失败

- 先确认 Node.js 安装成功
- Windows 下确认 Git 可用
- 检查网络可访问 npm 和 Node 下载源

### Q3: 实例启动后无响应

- 确认实例状态为 Running
- 重新验证渠道凭证（Verify）
- 检查日志输出定位具体报错

## 9. 下一步

根据你的渠道选择继续阅读：

- Telegram：[`channels/telegram.md`](channels/telegram.md)
- 飞书（Feishu）：[`channels/feishu.md`](channels/feishu.md)
