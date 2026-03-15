# ToAPIs for OpenClaw

[中文](#中文) | [English](#english) | [日本語](#日本語)

---

## 文档 / Docs

- 中文文档入口：[`docs/README.zh-CN.md`](docs/README.zh-CN.md)
- 部署总览：[`docs/deployment.md`](docs/deployment.md)
- Telegram 接入：[`docs/channels/telegram.md`](docs/channels/telegram.md)
- 飞书接入：[`docs/channels/feishu.md`](docs/channels/feishu.md)

## 中文

ToAPIs for OpenClaw 是基于 [toapis.com](https://toapis.com) 的 OpenClaw AI 网关可视化管理工具。一键部署、配置和管理多个 AI 聊天机器人实例，支持 Telegram、Discord、飞书等平台。

### 下载

从 [Releases](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest) 下载最新版本：

| 平台 | 架构 | 下载 |
|------|------|------|
| **Windows** | x64 | [toapis-for-openclaw-win-x64.exe](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-win-x64.exe) |
| **macOS** | Apple Silicon (M1/M2/M3/M4) | [toapis-for-openclaw-macos-arm64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-arm64.zip) |
| **macOS** | Intel | [toapis-for-openclaw-macos-x64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-x64.zip) |
| **Linux** | x64 | [toapis-for-openclaw-linux-x64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64) |
| **Linux** | ARM64 | [toapis-for-openclaw-linux-arm64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-arm64) |

> **备用下载（百度网盘）**：如果 GitHub 下载较慢，可从 [百度网盘](https://pan.baidu.com/s/1_XVw0R5xE4LUElQPwn81pA?pwd=8kx3)（提取码: `8kx3`）下载。

### 快速开始

#### Windows

1. 下载 `toapis-for-openclaw-win-x64.exe`
2. 右键 → **以管理员身份运行**，浏览器会自动打开管理页面
3. 按照向导填入 [toapis.com](https://toapis.com) API Key，创建第一个实例

#### macOS

1. 下载对应架构的 `.zip` 文件并解压
2. 若提示"无法打开"，在终端执行以下命令移除隔离属性：
   ```bash
   xattr -rd com.apple.quarantine ./toapis-for-openclaw-macos-arm64
   ```
3. 双击运行，浏览器会自动打开管理页面

#### Linux

```bash
# 下载（以 x64 为例）
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64
chmod +x toapis-for-openclaw-linux-x64

# 运行（自动后台运行）
./toapis-for-openclaw-linux-x64

# 查看状态
./toapis-for-openclaw-linux-x64 --status

# 停止
./toapis-for-openclaw-linux-x64 --stop
```

管理页面地址：`http://<服务器IP>:51888`

### 常用命令（Linux / macOS）

```bash
# 前台运行
./toapis-for-openclaw-linux-x64 --foreground

# 后台运行
./toapis-for-openclaw-linux-x64 --daemon

# 查看运行状态
./toapis-for-openclaw-linux-x64 --status

# 停止服务
./toapis-for-openclaw-linux-x64 --stop
```

### 功能特性

- **多平台支持** — Telegram、Discord、飞书一键对接
- **多模型切换** — 通过 toapis.com 接入多家主流模型，每个实例独立配置
- **可视化管理** — Web UI 管理所有实例，启停、配置一目了然
- **自动更新** — 内置 OTA 更新，一键升级到最新版本
- **用户审批** — 白名单机制，通过对接码审批授权用户
- **零依赖部署** — 单文件二进制，自动安装 Node.js 和 openclaw

### 前置条件

首次启动时会**自动检测并安装**以下依赖：

- **Node.js 22+** — 如未安装会自动下载安装
- **openclaw CLI** — 通过 npm 自动安装，每次启动自动检查更新

需要提前准备：

- [toapis.com](https://toapis.com) 账号及 API Key

---

## English

ToAPIs for OpenClaw is a visual management tool for the OpenClaw AI gateway, powered by [toapis.com](https://toapis.com). Deploy, configure, and manage multiple AI chatbot instances with one click. Supports Telegram, Discord, Feishu (Lark), and more.

### Download

Get the latest version from [Releases](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest):

| Platform | Arch | Download |
|----------|------|----------|
| **Windows** | x64 | [toapis-for-openclaw-win-x64.exe](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-win-x64.exe) |
| **macOS** | Apple Silicon (M1/M2/M3/M4) | [toapis-for-openclaw-macos-arm64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-arm64.zip) |
| **macOS** | Intel | [toapis-for-openclaw-macos-x64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-x64.zip) |
| **Linux** | x64 | [toapis-for-openclaw-linux-x64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64) |
| **Linux** | ARM64 | [toapis-for-openclaw-linux-arm64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-arm64) |

> **Alternative download (Baidu Netdisk)**: If GitHub is slow, download from [Baidu Netdisk](https://pan.baidu.com/s/1_XVw0R5xE4LUElQPwn81pA?pwd=8kx3) (code: `8kx3`).

### Quick Start

#### Windows

1. Download `toapis-for-openclaw-win-x64.exe`
2. Right-click → **Run as Administrator**, the browser will open automatically
3. Follow the wizard to enter your [toapis.com](https://toapis.com) API Key and create your first instance

#### macOS

1. Download the `.zip` for your architecture and extract it
2. If blocked by macOS, remove the quarantine flag:
   ```bash
   xattr -rd com.apple.quarantine ./toapis-for-openclaw-macos-arm64
   ```
3. Run the binary, the browser will open automatically

#### Linux

```bash
# Download (x64 example)
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64
chmod +x toapis-for-openclaw-linux-x64

# Run (auto-daemonizes)
./toapis-for-openclaw-linux-x64

# Check status
./toapis-for-openclaw-linux-x64 --status

# Stop
./toapis-for-openclaw-linux-x64 --stop
```

Dashboard URL: `http://<server-ip>:51888`

### Features

- **Multi-platform** — One-click integration with Telegram, Discord, and Feishu (Lark)
- **Model switching** — Access multiple AI models via toapis.com, configured per instance
- **Visual management** — Web UI for all instances: start/stop, configure
- **Auto-update** — Built-in OTA updates, one-click upgrade
- **User approval** — Whitelist with pairing code authorization
- **Zero-dependency** — Single binary, auto-installs Node.js and openclaw

### Prerequisites

Dependencies are **automatically detected and installed** on first launch:

- **Node.js 22+** — Auto-downloaded if not found
- **openclaw CLI** — Auto-installed via npm, updated on every startup

You will need:

- A [toapis.com](https://toapis.com) account and API Key

---

## 日本語

ToAPIs for OpenClaw は [toapis.com](https://toapis.com) を利用した OpenClaw AI ゲートウェイのビジュアル管理ツールです。Telegram、Discord、Feishu（Lark）などのプラットフォームで、AI チャットボットインスタンスをワンクリックでデプロイ・設定・管理できます。

### ダウンロード

[Releases](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest) から最新版をダウンロード：

| プラットフォーム | アーキテクチャ | ダウンロード |
|----------------|--------------|------------|
| **Windows** | x64 | [toapis-for-openclaw-win-x64.exe](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-win-x64.exe) |
| **macOS** | Apple Silicon (M1/M2/M3/M4) | [toapis-for-openclaw-macos-arm64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-arm64.zip) |
| **macOS** | Intel | [toapis-for-openclaw-macos-x64.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-x64.zip) |
| **Linux** | x64 | [toapis-for-openclaw-linux-x64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64) |
| **Linux** | ARM64 | [toapis-for-openclaw-linux-arm64](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-arm64) |

> **代替ダウンロード（百度网盘）**：GitHub が遅い場合は [百度网盘](https://pan.baidu.com/s/1_XVw0R5xE4LUElQPwn81pA?pwd=8kx3)（提取码: `8kx3`）からダウンロードできます。

### クイックスタート

#### Windows

1. `toapis-for-openclaw-win-x64.exe` をダウンロード
2. 右クリック → **管理者として実行**、ブラウザが自動で開きます
3. ウィザードに従い [toapis.com](https://toapis.com) の API Key を入力して最初のインスタンスを作成

#### macOS

1. アーキテクチャに対応する `.zip` をダウンロードして解凍
2. macOS にブロックされた場合、隔離属性を解除：
   ```bash
   xattr -rd com.apple.quarantine ./toapis-for-openclaw-macos-arm64
   ```
3. 実行するとブラウザが自動で開きます

#### Linux

```bash
# ダウンロード（x64 の例）
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64
chmod +x toapis-for-openclaw-linux-x64

# 実行（自動でバックグラウンド化）
./toapis-for-openclaw-linux-x64

# ステータス確認
./toapis-for-openclaw-linux-x64 --status

# 停止
./toapis-for-openclaw-linux-x64 --stop
```

管理画面：`http://<サーバーIP>:51888`

### 機能

- **マルチプラットフォーム** — Telegram、Discord、Feishu（Lark）にワンクリックで連携
- **モデル切り替え** — toapis.com 経由で複数の AI モデルに対応、インスタンスごとに設定可能
- **ビジュアル管理** — Web UI で全インスタンスを管理：起動/停止、設定
- **自動アップデート** — 内蔵 OTA アップデート、ワンクリックで最新版に
- **ユーザー承認** — ペアリングコードによるホワイトリスト管理
- **ゼロ依存デプロイ** — 単一バイナリ、Node.js と openclaw を自動インストール

### 前提条件

初回起動時に以下を**自動検出・インストール**します：

- **Node.js 22+** — 未インストールの場合は自動ダウンロード
- **openclaw CLI** — npm 経由で自動インストール、起動時に毎回更新チェック

事前に必要なもの：

- [toapis.com](https://toapis.com) アカウントと API Key

---

## 问题反馈 / Issues / フィードバック

[提交 Issue](https://github.com/blackai2025/toapis-for-openclaw/issues)

## License

MIT
