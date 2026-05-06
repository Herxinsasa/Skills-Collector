# CLAUDE.md — Agent Skills 工作区

## 核心行为

### 用户描述需求时自动搜索 Skill

当用户说"有没有一个 skill 可以..."、"帮我找一下...的 skill"、"需要一个...的功能"、或者描述一个开发需求且可能已有现成 Skill 时，执行以下流程：

1. **调用 find-skills 联网搜索**，找到与用户需求匹配的 Skill
2. **比较热度**（GitHub stars、forks、最近更新日期），选择星最多、活跃度最高的
3. **克隆到当前目录并清理 .git**（删除嵌套 .git 便于统一纳入 Skills-Collector 仓库管理）：

```bash
git clone <repo-url> "F:/Dev/Agent Skills/<skill-name>" && rm -rf "F:/Dev/Agent Skills/<skill-name>/.git"
```

4. **阅读其 SKILL.md 或 README**，确认功能与用户需求匹配
5. **更新 README.md**，将新 Skill 加入对应的分类索引表

### 更新 README 规则

- 找到 Skill 所属的分类，在对应表格中追加一行
- 表格格式：`| [skill-name](./skill-name/) | 来源（作者/org） | 一句话说明 | 适用场景 |`
- 知名合集放在"知名合集"分类
- 如果现有分类都不匹配，新增一个分类

### 克隆前确认

- 如果是同名 Skill 已存在，提示用户是否覆盖
- 如果搜索结果不明确（多个同名/同功能 Skill），列出候选让用户选
- 优先选通过 `npx skills` 可安装的官方渠道 Skill

## 目录约定

- 自研 Skill：`F:/Dev/Agent Skills/<skill-name>/`
- 克隆的热门 Skill：同上路径
- 测试数据/workspace：`*-workspace/`，不提交

## 当前已有 Skill 速查

| Skill | 用途 |
|-------|------|
| structured-thinking | 结构化思考分析 |
| mattpocock-skills | 开发全流程（grill/diagnose/tdd/triage 等） |
| darwin-skill | Skill 进化优化 |
| find-skills | 搜索发现 Skill |
| code-review-skill | 多维代码审查 |
| code-simplifier-skill | 代码简化重构 |
| log-analysis | 日志分析诊断 |
| ui-ux-pro-max-skill | UI/UX 设计 |
| planning-with-files | 文件规划方法论 |
| anthropics-skills | 官方示例和规范 |
| andrej-karpathy-skills | Karpathy 个人 Skill |
| agency-agents | 多 Agent 协作 |
| superpowers | 社区合集 |
| vercel-labs-skills | Vercel 官方 Skill |
