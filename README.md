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
| **Windows** | x64 | [toapis-for-openclaw-win-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-win-x64-offline.zip) |
| **macOS** | Apple Silicon (M1/M2/M3/M4) | [toapis-for-openclaw-macos-arm64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-arm64-offline.zip) |
| **macOS** | Intel | [toapis-for-openclaw-macos-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-x64-offline.zip) |
| **Linux** | x64 | [toapis-for-openclaw-linux-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64-offline.zip) |
| **Linux** | ARM64 | [toapis-for-openclaw-linux-arm64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-arm64-offline.zip) |

### 快速开始

#### Windows

1. 下载并解压 `toapis-for-openclaw-win-x64-offline.zip`
2. 运行 `toapis-for-openclaw-win-x64.exe`（建议右键 → **以管理员身份运行**），浏览器会自动打开管理页面
3. 按照向导填入 [toapis.com](https://toapis.com) API Key，创建第一个实例

#### macOS

1. 下载对应架构的 `*-offline.zip` 并解压
2. 双击 `start-macos.command` 即可启动（会自动处理系统安全限制）
3. 浏览器自动打开管理页面

#### Linux

```bash
# 下载并解压（以 x64 为例）
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64-offline.zip
unzip toapis-for-openclaw-linux-x64-offline.zip
cd toapis-for-openclaw-linux-x64

# 启动
./toapis-for-openclaw-linux-x64
```

管理页面地址：`http://<服务器IP>:51888`

> 再次运行同一命令不会启动第二个进程，而是直接打开已运行实例的浏览器页面。

### 功能特性

- **多平台支持** — Telegram、Discord、飞书一键对接
- **多模型切换** — 通过 toapis.com 接入多家主流模型，每个实例可独立切换模型
- **可视化管理** — Web UI 管理所有实例，启停、配置一目了然
- **离线安装** — Release 包已内置 Node.js、openclaw CLI 及 MinGit (Windows)，无需联网即可完成首次部署
- **自动更新** — 内置 OTA 更新，一键升级到最新版本
- **开机自启** — 支持设置系统启动时自动运行（macOS / Windows / Linux systemd）
- **用户审批** — 白名单机制，通过对接码审批授权用户
- **一键卸载** — Web UI 或命令行 `--uninstall` 即可彻底清理所有组件
- **国内加速** — 自动使用国内镜像下载 Node.js 和 npm 包

### 前置条件

Release 包已内置所有运行时依赖（Node.js 22、openclaw CLI），开箱即用，**无需额外安装**。

需要提前准备：

- [toapis.com](https://toapis.com) 账号及 API Key

### 卸载

```bash
# 命令行卸载
./toapis-for-openclaw-linux-x64 --uninstall
```

也可在 Web 管理界面中点击卸载按钮。Windows 下还可通过"添加或删除程序"卸载。

---

## English

ToAPIs for OpenClaw is a visual management tool for the OpenClaw AI gateway, powered by [toapis.com](https://toapis.com). Deploy, configure, and manage multiple AI chatbot instances with one click. Supports Telegram, Discord, Feishu (Lark), and more.

### Download

Get the latest version from [Releases](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest):

| Platform | Arch | Download |
|----------|------|----------|
| **Windows** | x64 | [toapis-for-openclaw-win-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-win-x64-offline.zip) |
| **macOS** | Apple Silicon (M1/M2/M3/M4) | [toapis-for-openclaw-macos-arm64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-arm64-offline.zip) |
| **macOS** | Intel | [toapis-for-openclaw-macos-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-macos-x64-offline.zip) |
| **Linux** | x64 | [toapis-for-openclaw-linux-x64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64-offline.zip) |
| **Linux** | ARM64 | [toapis-for-openclaw-linux-arm64-offline.zip](https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-arm64-offline.zip) |

### Quick Start

#### Windows

1. Download and extract `toapis-for-openclaw-win-x64-offline.zip`
2. Run `toapis-for-openclaw-win-x64.exe` (recommended: Right-click → **Run as Administrator**), the browser will open automatically
3. Follow the wizard to enter your [toapis.com](https://toapis.com) API Key and create your first instance

#### macOS

1. Download the `*-offline.zip` for your architecture and extract it
2. Double-click `start-macos.command` to launch (handles macOS security restrictions automatically)
3. The browser will open the dashboard automatically

#### Linux

```bash
# Download and extract (x64 example)
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64-offline.zip
unzip toapis-for-openclaw-linux-x64-offline.zip
cd toapis-for-openclaw-linux-x64

# Run
./toapis-for-openclaw-linux-x64
```

Dashboard URL: `http://<server-ip>:51888`

> Running the command again won't start a second process — it simply opens the browser to the existing instance.

### Features

- **Multi-platform** — One-click integration with Telegram, Discord, and Feishu (Lark)
- **Model switching** — Access multiple AI models via toapis.com; switch models on existing instances at any time
- **Visual management** — Web UI for all instances: start/stop, configure
- **Offline install** — Release packages bundle Node.js, openclaw CLI, and MinGit (Windows) for fully offline deployment
- **Auto-update** — Built-in OTA updates, one-click upgrade
- **Autostart** — Optionally launch on system boot (macOS / Windows / Linux systemd)
- **User approval** — Whitelist with pairing code authorization
- **One-click uninstall** — Web UI or `--uninstall` flag to cleanly remove all components
- **China mirror acceleration** — Automatically uses domestic mirrors for Node.js and npm downloads

### Prerequisites

Release packages include all runtime dependencies (Node.js 22, openclaw CLI) — **no additional installation required**.

You will need:

- A [toapis.com](https://toapis.com) account and API Key

### Uninstall

```bash
# Command-line uninstall
./toapis-for-openclaw-linux-x64 --uninstall
```

You can also uninstall from the Web dashboard. On Windows, use "Add or Remove Programs".

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

### クイックスタート

#### Windows

1. `toapis-for-openclaw-win-x64.exe` をダウンロード
2. 右クリック → **管理者として実行**、ブラウザが自動で開きます
3. ウィザードに従い [toapis.com](https://toapis.com) の API Key を入力して最初のインスタンスを作成

#### macOS

1. アーキテクチャに対応する `.zip` をダウンロードして解凍
2. `start-macos.command` をダブルクリックして起動（macOS のセキュリティ制限を自動処理）
3. ブラウザが自動で管理画面を開きます

#### Linux

```bash
# ダウンロード（x64 の例）
wget https://github.com/blackai2025/ToAPIs4openClaw-Releases/releases/latest/download/toapis-for-openclaw-linux-x64
chmod +x toapis-for-openclaw-linux-x64

# 起動
./toapis-for-openclaw-linux-x64
```

管理画面：`http://<サーバーIP>:51888`

> 同じコマンドを再実行しても二重起動せず、既存インスタンスのブラウザページを開きます。

### 機能

- **マルチプラットフォーム** — Telegram、Discord、Feishu（Lark）にワンクリックで連携
- **モデル切り替え** — toapis.com 経由で複数の AI モデルに対応、既存インスタンスでもモデルを随時変更可能
- **ビジュアル管理** — Web UI で全インスタンスを管理：起動/停止、設定
- **オフラインインストール** — リリースパッケージに Node.js、openclaw CLI、MinGit（Windows）を同梱、ネットワーク不要で初回デプロイ可能
- **自動アップデート** — 内蔵 OTA アップデート、ワンクリックで最新版に
- **自動起動** — システム起動時の自動実行を設定可能（macOS / Windows / Linux systemd）
- **ユーザー承認** — ペアリングコードによるホワイトリスト管理
- **ワンクリックアンインストール** — Web UI またはコマンドライン `--uninstall` で全コンポーネントをクリーンに削除
- **中国国内ミラー加速** — Node.js および npm パッケージのダウンロードに国内ミラーを自動使用

### 前提条件

リリースパッケージにはすべてのランタイム依存（Node.js 22、openclaw CLI）が同梱されており、**追加インストール不要**です。

事前に必要なもの：

- [toapis.com](https://toapis.com) アカウントと API Key

### アンインストール

```bash
# コマンドラインでアンインストール
./toapis-for-openclaw-linux-x64 --uninstall
```

Web 管理画面からもアンインストール可能です。Windows では「アプリと機能」からも削除できます。

---

## 问题反馈 / Issues / フィードバック

[提交 Issue](https://github.com/blackai2025/toapis-for-openclaw/issues)

## License

MIT
