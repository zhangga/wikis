# 资料来源与事实摘记

## 用户给定推文

- 原链接：https://x.com/AYi_AInotes/status/2055954675526934642
- Tweet ID 解码时间：2026-05-17T10:12:47.093Z。
- 镜像检索摘记：AYi 将 GBrain v0.31.1 解读为 MCP thin client 架构升级；核心表达包括“一个家庭服务器跑中央大脑，所有电脑、手机、所有 AI Agent，全部通过 MCP 协议远程连接”“一个大脑，养所有设备和所有 Agent”“个人 AI 正在走和企业软件一模一样的路，从单机版到客户端-服务器架构”。

## Garry Tan 原始动态

- 镜像页：https://di.gg/ai/in2p92l2
- 原动态摘记：GBrain v0.31.1 shipped real MCP thin client support；可以运行一台 home GBrain server，其他入口通过 MCP 连接；GBrain went client-server。
- 原动态 ID `2053306243704410460` 解码时间：2026-05-10T02:48:51.741Z。

## GBrain 官方仓库

- README：https://github.com/garrytan/gbrain
- Raw README：https://raw.githubusercontent.com/garrytan/gbrain/master/README.md
- 关键信息：
  - GBrain 是 Garry Tan 用来运行实际 OpenClaw 和 Hermes 部署的 agent brain。
  - README 当前写到生产 brain 包含 17,888 pages、4,383 people、723 companies、21 cron jobs。
  - GBrain exposes 30+ MCP tools via stdio。
  - `gbrain serve --http` 支持 OAuth 2.1、admin dashboard、scoped operations、request logs 等远程 MCP 能力。

## GBrain 架构文档

- Topologies：https://github.com/garrytan/gbrain/blob/master/docs/architecture/topologies.md
- 关键信息：
  - Thin client 拓扑中，agent 机器通过 HTTP MCP with OAuth 消费远端 brain。
  - Thin client 机器没有本地 engine，查询、搜索、embedding、indexing 都发生在 host。
  - 适用场景包括 heavy brain 在较强机器上运行，其他 agents 消费它；需要 many machines 共享 one source of truth；避免重复索引和 source-ID contention。

## GBrain CHANGELOG

- Raw CHANGELOG：https://raw.githubusercontent.com/garrytan/gbrain/master/CHANGELOG.md
- 查询时间：2026-05-17。
- 当前最新记录：`0.35.1.1`，日期 2026-05-16。
- 文章因此不把 v0.31.1 写成“截至发稿最新版本”，而写成一个被中文社区热议、具有架构信号意义的节点。

## 第三方评测

- Vectorize review：https://vectorize.io/articles/gbrain-review
- 关键信息：
  - GBrain 是 Garry Tan 于 2026-04-05 released 的开源 AI agent memory system。
  - 评价其架构扎实，但仍年轻、更新频繁、自托管、偏单操作者和技术用户。
  - 文章中的谨慎段落参考了这一判断，但没有沿用其结论措辞。
