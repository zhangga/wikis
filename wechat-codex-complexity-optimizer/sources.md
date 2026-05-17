# Sources

整理时间：2026-05-17（Asia/Shanghai）

## 原帖与社交传播

1. AYi：关于 Greg Brockman 转发 Codex Complexity Optimizer 的中文长帖  
   https://x.com/AYi_AInotes/status/2055717699532013896  
   公开解析备份：https://api.vxtwitter.com/AYi_AInotes/status/2055717699532013896  
   时间：2026-05-17 02:31:07（北京时间）

2. Greg Brockman：转发并评论 “codex for improving computational complexity”  
   https://x.com/gdb/status/2055646916499714488  
   公开解析备份：https://api.vxtwitter.com/gdb/status/2055646916499714488  
   时间：2026-05-16 21:49:51（北京时间）

3. Kappaemme：发布 Codex Complexity Optimizer 的原帖  
   https://x.com/Kappaemme1926/status/2055343704467206506  
   公开解析备份：https://api.vxtwitter.com/Kappaemme1926/status/2055343704467206506  
   时间：2026-05-16 01:45:00（北京时间）

## 项目与包信息

4. GitHub 仓库：Kappaemme-git/codex-complexity-optimizer  
   https://github.com/Kappaemme-git/codex-complexity-optimizer  
   仓库创建：2026-05-15 21:33:28（北京时间）  
   截至整理时：254 Stars，9 Forks，MIT License，主要语言 Python。

5. 项目 README  
   https://raw.githubusercontent.com/Kappaemme-git/codex-complexity-optimizer/main/README.md  
   重点信息：安装到 `${CODEX_HOME:-~/.codex}/skills/complexity-optimizer`；默认报告模式不修改文件；报告包含文件/行号、当前复杂度、建议改法、优化后复杂度、风险等级和测试需求。

6. Skill 文件  
   https://raw.githubusercontent.com/Kappaemme-git/codex-complexity-optimizer/main/complexity-optimizer/SKILL.md  
   重点信息：默认先报告；scanner 输出只是线索，不是证明；真正修改前要确认行为、测试和风险。

7. npm 包：codex-complexity-optimizer  
   https://www.npmjs.com/package/codex-complexity-optimizer  
   registry 信息：https://registry.npmjs.org/codex-complexity-optimizer  
   版本：0.1.0；创建时间：2026-05-15 21:32:07（北京时间）；关键词包含 codex、codex-skill、complexity、performance、optimization、static-analysis。

## OpenAI 官方资料

8. OpenAI Developers：Agent Skills - Codex  
   https://developers.openai.com/codex/skills  
   重点信息：Skills 是 reusable workflows 的 authoring format；目录包含 `SKILL.md`、可选 scripts / references / assets；Codex 使用 progressive disclosure，在需要时读取完整技能说明。

9. OpenAI Developers：Plugins - Codex  
   https://developers.openai.com/codex/plugins  
   重点信息：Plugins 可把 Skills、Apps、MCP servers 打包成 Codex 的可复用工作流和集成。

10. OpenAI：Introducing GPT-5.3-Codex  
    https://openai.com/index/introducing-gpt-5-3-codex/  
    重点信息：GPT-5.3-Codex 被定位为能处理研究、工具使用、复杂执行和更广软件生命周期任务的 agentic coding model。

11. OpenAI Developers：Codex Use Cases  
    https://developers.openai.com/codex/use-cases  
    重点信息：Codex 用例覆盖生产系统、质量、分析、前端、知识工作等，强调可控改动、重复工作流程和生产质量。

