# Code Simplifier

[![Repo](https://img.shields.io/badge/github-code-simplifier-skill-181717?logo=github)](https://github.com/wimi321/code-simplifier-skill)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Collection](https://img.shields.io/badge/collection-claude--code--skills--extract-blue)](https://github.com/wimi321/claude-code-skills-extract)

Use when changed code should be reviewed for reuse, code quality, and efficiency, then cleaned up before finalizing.

English | [简体中文](./README.zh-CN.md)

## Why This Skill Exists

Code Simplifier packages a reusable Claude Code workflow as a standalone public skill repository. It is designed for agent teams that want a well-documented, installable, and maintainable capability rather than an internal prompt fragment.

## Highlights

- Focused, reusable workflow with a clear trigger boundary
- Standalone skill root that works well in agent workspaces
- Agent metadata in `agents/openai.yaml`
- Public provenance back to the extracted Claude Code source
- Bilingual documentation for English and Chinese readers

## What It Is Good At

- Review and simplify changed code
- Running the workflow described in `SKILL.md` with explicit boundaries
- Producing repeatable outputs for operators and agent runtimes

## Example Requests

- Review my diff for duplicate logic and unnecessary complexity.
- Clean up this changed code before I ship it.

## Workflow

1. Inspect the relevant diff or latest modified files.
2. Review for existing utilities that should be reused.
3. Review for code smell: parameter sprawl, copy-paste, leaky abstractions, or unnecessary comments.
4. Review for efficiency problems: repeated work, unnecessary reads, event churn, and hot-path bloat.
5. Fix confirmed issues and summarize what changed.

## Inputs

- Relevant diff or changed files
- Optional focus area

## Outputs

- Concrete cleanup changes
- Short summary of improvements

## Success Criteria

- Duplication or awkward abstractions were reduced.
- Performance regressions were checked.
- No unnecessary churn was introduced.

## Non-Goals

- Massive style-only rewrites
- Review of untouched code with no link to the change

## Installation

### Use as a standalone skill

Clone this repository and place the repository root in a compatible skill directory.

### Use from a larger collection

This skill is also included in the parent collection:

- [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)

## Repository Layout

- `SKILL.md`: canonical skill instructions
- `README.md`: English project overview
- `README.zh-CN.md`: Simplified Chinese project overview
- `agents/openai.yaml`: UI-facing metadata for agent runtimes
- `references/`: provenance and support notes
- `LICENSE`: repository license

## Provenance

Derived from `src/skills/bundled/simplify.ts`.

## Related Projects

- Parent collection: [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)
- GitHub repository: [code-simplifier-skill](https://github.com/wimi321/code-simplifier-skill)
