# DeepSeek V4 发布资料整理

检索时间：2026-04-24  
主题目录：`wechat-deepseek-v4-release/`

## 已确认信息

1. DeepSeek API 文档已经列出 `deepseek-v4-flash` 和 `deepseek-v4-pro`。
   - 来源：https://api-docs.deepseek.com/zh-cn/
   - 要点：`deepseek-chat` 与 `deepseek-reasoner` 将于 2026/07/24 弃用，并映射到 V4 Flash 的非思考 / 思考模式。

2. DeepSeek V4 两个 API 模型均支持 1M 上下文，最大输出 384K。
   - 来源：https://api-docs.deepseek.com/zh-cn/quick_start/pricing
   - 功能：JSON Output、Tool Calls、对话前缀续写、FIM 补全。

3. 官方人民币价格：
   - Flash：缓存命中输入 0.2 元 / 百万 tokens，缓存未命中输入 1 元 / 百万 tokens，输出 2 元 / 百万 tokens。
   - Pro：缓存命中输入 1 元 / 百万 tokens，缓存未命中输入 12 元 / 百万 tokens，输出 24 元 / 百万 tokens。
   - 来源：https://api-docs.deepseek.com/zh-cn/quick_start/pricing

4. Hugging Face 已上线 DeepSeek-V4 Collection。
   - 来源：https://huggingface.co/collections/deepseek-ai/deepseek-v4
   - 包含：DeepSeek-V4-Flash-Base、DeepSeek-V4-Flash、DeepSeek-V4-Pro-Base、DeepSeek-V4-Pro。

5. 模型卡确认：
   - DeepSeek-V4-Pro：1.6T 总参数，49B 激活参数，1M 上下文。
   - DeepSeek-V4-Flash：284B 总参数，13B 激活参数，1M 上下文。
   - 许可：MIT License。
   - 来源：https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro
   - 来源：https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash

6. 技术要点：
   - Hybrid Attention Architecture：CSA + HCA。
   - mHC：Manifold-Constrained Hyper-Connections。
   - Muon Optimizer。
   - 训练数据：超过 32T tokens。
   - 来源：https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro

7. 媒体确认：
   - Reuters / Investing.com 报道 DeepSeek 于 2026/04/24 发布 V4 预览版，包含 Pro 与 Flash。
   - 来源：https://www.investing.com/news/stock-market-news/deepseek-releases-new-flagship-open-source-ai-model-v4-4634548
   - The Straits Times / Bloomberg 报道 DeepSeek 于 2026/04/24 推出 V4 Flash 和 V4 Pro。
   - 来源：https://www.straitstimes.com/business/companies-markets/chinas-deepseek-unveils-new-flagship-ai-model-a-year-after-breakthrough

8. 第三方分发信息：
   - OpenRouter V4 Pro 页面显示 Released Apr 24, 2026，1,048,576 context，$1.74/M input tokens，$3.48/M output tokens。
   - 来源：https://openrouter.ai/deepseek/deepseek-v4-pro/uptime

## 写作判断

本篇不写成参数新闻，而写成“开源模型争夺主工作流”的快评。

核心判断：

DeepSeek V4 的冲击不只来自 1.6T 参数，而来自 1M 上下文、低价 API、Flash/Pro 分层、MIT 开源和工具生态兼容的组合拳。

风险提示：

- 官方称本次是 preview version，真实稳定性需要社区在长上下文、编码 Agent、工具调用和高频 API 使用中验证。
- 所有 benchmark 均应标注为 DeepSeek 自测或模型卡数据，不写成第三方独立结论。

## 正文数据图

1. `imgs/01-model-specs.png`
   - 对应源文件：`imgs/01-model-specs.svg`
   - 数据来源：DeepSeek API 文档、Hugging Face DeepSeek-V4 模型卡。
   - 使用数据：Flash / Pro 的总参数、激活参数、1M 上下文、384K 最大输出、工具能力、MIT License。

2. `imgs/02-api-pricing.png`
   - 对应源文件：`imgs/02-api-pricing.svg`
   - 数据来源：DeepSeek API 模型与价格页。
   - 使用数据：Flash / Pro 的缓存命中输入、缓存未命中输入、输出价格，单位为人民币 / 百万 tokens。

3. `imgs/03-benchmark-snapshot.png`
   - 对应源文件：`imgs/03-benchmark-snapshot.svg`
   - 数据来源：Hugging Face DeepSeek-V4 模型卡。
   - 使用数据：V4-Flash Max 与 V4-Pro Max 在 LiveCodeBench、SWE Verified、MRCR 1M、Terminal Bench 2.0 上的官方自测节选。
