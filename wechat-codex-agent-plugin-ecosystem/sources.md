# 资料来源与写作笔记

## 核心资料

1. OpenAI - Codex for (almost) everything  
   https://openai.com/index/codex-for-almost-everything/  
   关键点：2026 年 4 月 16 日更新强调 Codex App 覆盖软件开发生命周期；新增 GitHub review comments、多终端标签、SSH 远程 devbox、文件 rich preview、summary pane 等工作区能力。

2. OpenAI Academy - Plugins and skills  
   https://openai.com/academy/codex-plugins-and-skills/  
   关键点：OpenAI 将 plugin 定义为连接外部工具和信息源；skill 定义为 Codex 可遵循的 playbook，用于沉淀团队流程。

3. Anthropic - Introducing the Model Context Protocol  
   https://www.anthropic.com/news/model-context-protocol  
   关键点：MCP 是连接 AI assistant 与数据源、业务工具、开发环境的开放标准，包含 specification / SDK、Claude Desktop local server support、开源 server repository。

4. Anthropic - Redesigning Claude Code on desktop for parallel agents  
   https://claude.com/blog/claude-code-desktop-redesign  
   关键点：2026 年 4 月 14 日 Claude Code Desktop 重做，加入多会话侧边栏、可拖拽工作区、内置终端、文件编辑器、Diff viewer、HTML/PDF 预览。

5. Claude Docs - Agent Skills  
   https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview  
   关键点：Agent Skills 采用 filesystem-based architecture 和 progressive disclosure；Claude 只在需要时读取 SKILL.md、资源和脚本。

6. Cursor 3.0 Changelog  
   https://cursor.com/changelog/3-0  
   关键点：Cursor 3.0 强化 Agent Tabs、agent panel、team/enterprise controls 等 Agent-first 工作区能力。

7. TRAE SOLO official page  
   https://www.trae.ai/ja/solo  
   关键点：TRAE 将 SOLO 定位为 all-in-one visual workspace，强调工具变成 AI 可编排的组件。

8. MCP Blog - MCP Apps  
   https://blog.modelcontextprotocol.io/posts/2026-01-26-mcp-apps/  
   关键点：MCP Apps 是 MCP 第一个官方扩展，允许 tools 返回可交互 UI，覆盖 dashboard、form、visualization、document review 等场景，并通过 sandboxed iframe 和 JSON-RPC 通信。

9. OpenAI Help Center - Build with the Apps SDK  
   https://help.openai.com/en/articles/12515353-build-with-the-apps-sdk  
   关键点：Apps SDK 让开发者同时定义 app 的 chat logic 和 UI，基于 MCP，支持在 ChatGPT 内运行；未来 monetization 会和 Agentic Commerce Protocol 相关。

10. arXiv - Agent Skills for Large Language Models  
    https://arxiv.org/abs/2602.12430  
    关键点：把 skills 视为 Agent 模块化能力层，强调 progressive disclosure、portable skill definitions、MCP integration；也指出社区技能存在安全风险。

11. arXiv - Bridging Protocol and Production  
    https://arxiv.org/abs/2603.13417  
    关键点：MCP 是协议基础，但生产级 Agent 工具集成仍缺 identity propagation、adaptive tool budgeting、structured error semantics 等基础设施。

## 本文核心判断

- 三栏工作台不是 UI 趋同，而是 Agent 工作分工变化：任务管理、意图沟通、结果操作。
- MCP 和 Skill 分别解决“连接”和“流程”，但用户二次编辑需要可交互 UI。
- MCP Apps / Apps SDK 代表 Agent 从纯语言交互走向操作交互。
- 插件生态的商业价值不在 prompt，而在服务、数据、UI、权限、审计和结果闭环。
- 中小团队更适合做垂直插件，而不是重做通用 Agent。
