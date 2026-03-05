# Telegram 渠道接入指南

## 1. 前置条件

开始前请确认：

- 已完成基础部署（见 [`../deployment.md`](../deployment.md)）
- 管理界面可访问：`http://127.0.0.1:51888`
- 已准备 ToAPIs API Key

## 2. 在 Telegram 创建 Bot

1. 打开 Telegram，搜索 `@BotFather`
2. 发送 `/newbot`
3. 按提示设置 Bot 名称与用户名
4. 保存 BotFather 返回的 Bot Token

> Bot Token 属于敏感凭证，请勿泄露。如已泄露请立即在 BotFather 中重置。

## 3. 在 Manager 创建 Telegram 实例

1. 打开管理界面，点击新建实例
2. 输入实例名称（建议仅使用字母、数字、`-`、`_`）
3. 选择模型并填写 ToAPIs API Key
4. 渠道选择 Telegram
5. 粘贴 Bot Token
6. 点击创建并启动实例

## 4. 完成 pairing code 绑定

1. 用户在 Telegram 给 Bot 发送任意消息
2. Bot 返回 8 位 pairing code
3. 管理员在实例中输入该 code 并点击 Approve
4. 审批成功后用户可正常对话

## 5. 排障建议

### 5.1 Bot 无响应

- 确认实例状态为 Running
- 确认 Bot Token 填写正确
- 在管理端重新执行 Verify 检查凭证

### 5.2 pairing code 审批失败

- 确认 code 未过期且大小写正确
- 确认实例处于运行状态
- 让用户重新发消息获取新 code 后再审批
