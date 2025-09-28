# StravaSync 使用说明

## 快速开始

### 1. 配置环境变量

编辑 `.env` 文件，填入你的真实账号信息：

```bash
# 佳明中国区账号
GARMIN_USERNAME=你的佳明邮箱
GARMIN_PASSWORD=你的佳明密码

# Strava API 配置
STRAVA_ACCESS_TOKEN=你的Strava访问令牌
STRAVA_CLIENT_ID=你的Strava客户端ID
STRAVA_CLIENT_SECRET=你的Strava客户端密钥
```

### 2. 使用方法

```bash
# 导出最新活动（第1条）
npm run export 0

# 导出倒数第二条活动
npm run export 1

# 导出第5条活动
npm run export 4

# 查看帮助
npm run export
```

### 3. 活动索引说明

| 索引 | 描述 | 实际位置 |
|------|------|----------|
| 0 | 最新活动 | 第1条 |
| 1 | 倒数第二条 | 第2条 |
| 2 | 倒数第三条 | 第3条 |
| 3 | 倒数第四条 | 第4条 |

## 获取 Strava Access Token

1. 访问 [Strava API 设置页面](https://www.strava.com/settings/api)
2. 创建新应用
3. 获取 Client ID 和 Client Secret
4. 使用 OAuth 流程获取 Access Token

## 注意事项

- 确保 `.env` 文件配置正确
- 网络连接要稳定
- Strava 会检测重复活动
- Access Token 会过期，需要定期更新
