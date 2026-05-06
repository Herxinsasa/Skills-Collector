# Code Simplifier

[English](./README.md) | 简体中文

Use when changed code should be reviewed for reuse, code quality, and efficiency, then cleaned up before finalizing.

## 这个技能是做什么的

Code Simplifier 把 Claude Code 中可复用的一类工作流提取成独立 skill 仓库，方便在不同智能体环境里直接安装、复用和持续维护。

## 核心特点

- 聚焦单一能力边界，适合公开分发
- 仓库根目录就是 skill 根目录
- 内置 `agents/openai.yaml` 元数据
- 保留来源说明，便于追踪提取依据
- 提供中英文双语 README

## 擅长场景

- Review and simplify changed code
- 执行 `SKILL.md` 中定义的标准工作流
- 为智能体或操作者提供稳定、可复用的输出

## 示例请求

- Review my diff for duplicate logic and unnecessary complexity.
- Clean up this changed code before I ship it.

## 工作流程

1. Inspect the relevant diff or latest modified files.
2. Review for existing utilities that should be reused.
3. Review for code smell: parameter sprawl, copy-paste, leaky abstractions, or unnecessary comments.
4. Review for efficiency problems: repeated work, unnecessary reads, event churn, and hot-path bloat.
5. Fix confirmed issues and summarize what changed.

## 输入

- Relevant diff or changed files
- Optional focus area

## 输出

- Concrete cleanup changes
- Short summary of improvements

## 成功标准

- Duplication or awkward abstractions were reduced.
- Performance regressions were checked.
- No unnecessary churn was introduced.

## 不适用场景

- Massive style-only rewrites
- Review of untouched code with no link to the change

## 安装方式

### 作为独立 skill 使用

克隆本仓库，并将仓库根目录放入兼容的 skill 目录即可。

### 从合集仓库使用

该 skill 也收录在总仓库中：

- [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)

## 仓库结构

- `SKILL.md`：技能主定义
- `README.md`：英文说明
- `README.zh-CN.md`：中文说明
- `agents/openai.yaml`：面向智能体 UI 的元数据
- `references/`：来源与补充说明
- `LICENSE`：开源许可证

## 来源说明

Derived from `src/skills/bundled/simplify.ts`.

## 相关项目

- 总仓库：[claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)
- 当前仓库：[code-simplifier-skill](https://github.com/wimi321/code-simplifier-skill)
