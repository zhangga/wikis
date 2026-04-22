# 微信公众号 API 发布说明

这套配置用于通过 `baoyu-post-to-wechat` 的 API 链路，把文章提交到公众号后台草稿箱。

## 当前仓库配置

- 账号别名：`youxiquan`
- `app_id` 来源：`C:\work\github\wikis\.baoyu-skills\baoyu-post-to-wechat\EXTEND.md`
- `app_secret` 填写位置：`C:\work\github\wikis\.baoyu-skills\.env`

## 一次性配置

1. 打开 `C:\work\github\wikis\.baoyu-skills\.env`
2. 填入真实的 `WECHAT_YOUXIQUAN_APP_SECRET`

示例：

```env
WECHAT_YOUXIQUAN_APP_ID=wx69a798ce04241325
WECHAT_YOUXIQUAN_APP_SECRET=你的真实AppSecret
```

## 发布命令

在仓库根目录执行：

```powershell
npx -y bun C:\Users\Admin\.agents\skills\baoyu-post-to-wechat\scripts\wechat-api.ts `
  .\wechat-ai-first-engineering\article.md `
  --theme default `
  --cover .\wechat-ai-first-engineering\imgs\00-cover.png `
  --account youxiquan
```

## 常用可选参数

```powershell
--color blue
--title "自定义标题"
--summary "自定义摘要"
--author "张嘎"
--no-cite
--dry-run
```

## 发布前检查

- 文章路径形如 `wechat-<topic>/article.md`
- 封面图存在，优先显式传入当前稿件实际封面，例如 `imgs/00-cover.png`
- 正文图片使用相对路径，例如 `imgs/01-cover.png`
- 先执行一次 `--dry-run` 检查标题、摘要、封面解析是否正常

## 干跑示例

```powershell
npx -y bun C:\Users\Admin\.agents\skills\baoyu-post-to-wechat\scripts\wechat-api.ts `
  .\wechat-ai-first-engineering\article.md `
  --theme default `
  --cover .\wechat-ai-first-engineering\imgs\00-cover.png `
  --account youxiquan `
  --dry-run
```

## 返回结果

成功后脚本会输出 JSON，包含：

- `success: true`
- `media_id`
- `title`
- `articleType`

这表示文章已经进入公众号后台草稿箱，后续在微信公众平台里继续预览和群发。
