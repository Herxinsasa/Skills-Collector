# Agent Skills 收集与开发

收集热门开源 Agent Skills 和个人自研 Skill，覆盖软件开发全流程。按用途分类管理。

---

## 分类索引

### 🧠 思维与决策

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [structured-thinking](./structured-thinking/) | 自研 | 苏格拉底提问 + 第一性原理 + 奥卡姆剃刀，三步法结构化分析 | 产品分析、需求评审、技术选型、日常决策 |
| [planning-with-files](./planning-with-files/) | 社区 | 基于文件的规划方法论，通过结构化文件管理复杂任务 | 复杂任务拆解、多步骤项目规划 |

### 🔧 开发工作流

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [mattpocock-skills](./mattpocock-skills/) | [mattpocock](https://github.com/mattpocock/skills) | 全套工程开发 Skill：grill-me 需求对齐、to-prd 需求文档、to-issues 任务拆分、triage 问题分诊、diagnose 故障诊断、tdd 测试驱动开发、zoom-out 架构审视、improve-codebase-architecture 架构改进 | 日常开发全流程 |
| [andrej-karpathy-skills](./andrej-karpathy-skills/) | [karpathy](https://github.com/andrej-karpathy/skills) | Andrej Karpathy 的个人 Skill 集合 | 代码生成、项目工作流 |
| [anthropics-skills](./anthropics-skills/) | [Anthropic](https://github.com/anthropics/skills) | Anthropic 官方 Skill 示例和规范 | Skill 开发参考、官方最佳实践 |
| [agency-agents](./agency-agents/) | [Agency](https://github.com/agency-agents) | 多 Agent 协作编排框架 | 复杂任务的多 Agent 协同 |
| [gsd-get-shit-done](./gsd-get-shit-done/) | [gsd-build](https://github.com/gsd-build/get-shit-done) | 轻量级 spec 驱动开发系统：6 步流程（需求→讨论→计划→执行→验证→发版），支持并行子 agent | 大型项目规范化开发 |

### 🔍 代码质量

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [code-review-skill](./code-review-skill/) | 社区 | 多维度代码审查：安全、性能、可维护性、逻辑正确性 | PR Review、代码质量门禁 |
| [code-simplifier-skill](./code-simplifier-skill/) | 社区 | 代码简化与重构，消除冗余、提升可读性 | 代码优化、技术债清理 |

### 📊 日志与诊断

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [log-analysis](./log-analysis/) | 社区 | 应用和系统日志分析，识别错误模式和根因 | 故障排查、日志审计 |

### 🎨 UI/UX 设计

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [ui-ux-pro-max-skill](./ui-ux-pro-max-skill/) | 社区 | UI/UX 设计增强，前端界面和交互优化 | 前端开发、界面设计 |

### 🛠 Skill 管理

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [darwin-skill](./darwin-skill/) | [花叔](https://github.com/alchaincyf/darwin-skill) | Skill 进化系统：评估→改进→测试→保留或回滚，8 维度评分 | Skill 迭代优化 |
| [find-skills](./find-skills/) | 社区 | 搜索和发现可安装的 Agent Skill | 查找现成 Skill |

### 📦 其他知名合集

| 合集 | 来源 | 说明 |
|------|------|------|
| [superpowers](./superpowers/) | 社区 | Superpowers Skill 合集，增强 Claude Code 能力边界 |
| [vercel-labs-skills](./vercel-labs-skills/) | [Vercel](https://github.com/vercel-labs/skills) | Vercel Labs 官方 Skill 集 |

### 📝 内容处理

| Skill | 来源 | 说明 | 适用场景 |
|-------|------|------|---------|
| [qiaomu-anything-to-notebooklm](./qiaomu-anything-to-notebooklm/) | [joeseesun](https://github.com/joeseesun/qiaomu-anything-to-notebooklm) | 多源内容转 NotebookLM：微信公众号、网页、YouTube、播客、PDF 等，自动生成播客/PPT/思维导图 | 内容整理、知识转化 |

---

## 使用方式

1. 浏览上方分类索引，找到对应 Skill
2. 打开 Skill 目录查看 `SKILL.md` 了解详细用法
3. 在 Claude Code 中通过 `/skill-name` 调用

## 贡献新 Skill

- 自研 Skill 直接在当前目录创建文件夹
- 热门 Skill 通过 `git clone` 克隆到当前目录
- 添加后更新本 README.md 的分类索引

## 目录结构

```
Agent Skills/
├── README.md                  # 本文件
├── CLAUDE.md                  # AI 自动行为配置
├── structured-thinking/       # 自研：结构化思考
├── mattpocock-skills/         # 知名合集：Matt Pocock
├── andrej-karpathy-skills/    # 知名合集：Andrej Karpathy
├── anthropics-skills/         # 官方：Anthropic
├── agency-agents/             # 框架：多 Agent 协作
├── code-review-skill/         # 工具：代码审查
├── code-simplifier-skill/     # 工具：代码简化
├── log-analysis/              # 工具：日志分析
├── planning-with-files/       # 方法论：文件规划
├── ui-ux-pro-max-skill/       # 工具：UI/UX 设计
├── darwin-skill/              # 工具：Skill 进化
├── find-skills/               # 工具：Skill 发现
├── superpowers/               # 知名合集：Superpowers
└── vercel-labs-skills/        # 知名合集：Vercel Labs
```
