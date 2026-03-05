# 飞书（Feishu）渠道接入指南

## 1. 前置条件

开始前请确认：

- 已完成基础部署（见 [`../deployment.md`](../deployment.md)）
- 管理界面可访问：`http://127.0.0.1:51888`
- 已准备 ToAPIs API Key
- 已有飞书企业管理员权限（用于应用发布）

## 2. 创建飞书应用

1. 进入飞书开放平台并创建企业自建应用
2. 填写应用基础信息
3. 获取并保存 App ID 与 App Secret

> App Secret 为敏感信息，请避免在聊天或截图中泄露。

## 3. 配置权限与事件

1. 在应用后台开启消息相关权限
2. 在事件订阅中将订阅方式设为 **Long Connection**
3. 添加事件 `im.message.receive_v1`
4. 每次权限或事件修改后，创建新版本并发布

## 4. 在 Manager 创建 Feishu 实例

1. 打开管理界面，点击新建实例
2. 输入实例名称
3. 选择模型并填写 ToAPIs API Key
4. 渠道选择 Feishu
5. 填写 App ID / App Secret（可选 Encrypt Key）
6. 创建并启动实例

## 5. 完成 pairing code 绑定

1. 用户在飞书内给 Bot 发送任意消息
2. Bot 返回 8 位 pairing code
3. 管理员在实例中输入 code 并点击 Approve
4. 审批通过后用户可正常使用

## 6. 排障建议

### 6.1 Bot 不回消息

- 确认实例状态为 Running
- 确认订阅方式是 Long Connection
- 确认已添加 `im.message.receive_v1`
- 确认最新版本已发布生效

### 6.2 pairing code 审批失败

- 检查 code 是否输入正确（区分大小写）
- 检查实例是否运行
- 重新让用户获取新 code 并再次审批
