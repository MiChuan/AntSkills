# AntSkills — AI Agent 技能集合

[![Skills](https://img.shields.io/badge/Skills-43-4a90d9.svg)](https://github.com/MiChuan/AntSkills)
[![Format](https://img.shields.io/badge/Format-SKILL.md-181717.svg)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/MiChuan/AntSkills?style=social)](https://github.com/MiChuan/AntSkills/stargazers)

本项目基于 MIT License 开源发布，欢迎在遵守许可证条款的前提下自由使用、修改与再发布。

## 目录导航

- [项目简介](#introduction)
- [项目亮点](#highlights)
- [技能分类](#features)
- [目录结构](#structure)
- [安装与使用](#quick-start)
- [常见问题](#faq)
- [开源声明与版权归属](#open-source-statement--copyright)
- [其他说明](#notes)

<a id="introduction"></a>
## 项目简介

AntSkills 是一个 AI Agent 技能（Skill）集合仓库，收录 **43 个技能**，覆盖文档优化、工程实践、软件工程工作流与 Cursor 平台自动化等场景。每个技能均为独立目录，遵循 SKILL.md 标准组织，可复制到 Cursor（`.cursor/skills`）、Codex（`~/.codex/skills`）等支持 Agent Skills 的环境中直接使用。

技能按来源分为四类：自研文档技能（formalize-readme）、工程实践技能（7）、Superpowers 开源工作流（15）与 Cursor 官方技能（20）。

<a id="highlights"></a>
## 项目亮点

- **标准格式**：全部技能遵循 SKILL.md（YAML frontmatter + Markdown 指令），跨工具可移植
- **覆盖完整工作流**：从需求探索、计划编写、测试驱动开发、代码评审到文档交付，形成闭环
- **官方技能内置**：收录 Cursor 官方 20 个技能与 Superpowers 15 个工作流技能，开箱即用
- **文档友好**：内置 README 正式化改写技能，可直接用于项目文档优化
- **轻量可裁剪**：每个技能独立目录，按需复制即可，无全局依赖

<a id="features"></a>
## 技能分类

### README 与文档

- **formalize-readme** — 将项目 README 改写为正式开源项目表述：徽章、锚点目录、标准章节，写作前核查仓库事实，交付前校验锚点与文件一致性

### 工程实践

- **adversarial-test** — 对已完成代码做对抗性测试，攻击异常输入、边界值、并发与网络失败，发现问题后补永久回归测试
- **commit-review** — 审查最后一次提交，只关注安全、性能与逻辑问题，每条给出文件、行号与触发条件
- **html-report** — 将结果输出为单文件 HTML（标签页、流程图、颜色），而非 Markdown
- **lock-behavior** — 重构前先用测试固定现有行为（含奇怪边界），再动手
- **minimal-change** — 以最小改动实现需求，不增加未来抽象，匹配项目现有风格
- **reproduce-first** — 遇到 Bug 先写最小复现测试，确认问题真实存在后再修复
- **understand-first** — 修改前先阅读相关代码、测试、配置与依赖，复述需求并列出方案

### Superpowers 工作流

- **brainstorming** — 创意工作（创建功能、组件、修改行为）前的需求与设计探索
- **dispatching-parallel-agents** — 面向多个独立任务的并行子代理分发
- **executing-plans** — 按书面实施计划分步执行并设置评审检查点
- **finishing-a-development-branch** — 开发完成后合并 / PR / 清理的集成决策
- **i-have-adhd** — 面向 ADHD 读者的输出风格：先给下一步行动、编号多步任务、抑制离题
- **receiving-code-review** — 接收代码评审反馈时的技术核实与验证
- **requesting-code-review** — 完成任务、实现大功能或合并前请求代码评审
- **subagent-driven-development** — 以子代理执行独立任务的计划实施
- **systematic-debugging** — 遇到 Bug、测试失败或异常行为时先定位根因再修复
- **test-driven-development** — 实现功能或修复 Bug 前先写测试
- **using-git-worktrees** — 用 git worktree 隔离特性工作区
- **using-superpowers** — 会话启动时的技能发现与使用
- **verification-before-completion** — 声称完成前先运行验证命令并确认输出
- **writing-plans** — 有规格或需求后、动手前编写多步实施计划
- **writing-skills** — 以 TDD 方式创建、编辑并验证技能

### Cursor 官方技能

- **automate** — 创建 Cursor Automations
- **autopilot** — 循环处理评论、解决冲突并修复 CI，保持 PR 可合并
- **canvas** — 使用 Cursor Canvas（实时 React 应用），含 SDK 类型定义
- **create-hook** — 创建 Cursor hooks 并配置 hooks.json
- **create-rule** — 创建 Cursor rules，提供持久化 AI 指导
- **create-skill** — 创建 Cursor Agent Skills
- **create-subagent** — 创建自定义子代理
- **loop** — 以固定或可变间隔循环运行提示或技能
- **migrate-to-skills** — 将 Cursor rules 与斜杠命令迁移为 Agent Skills
- **onboard** — Cursor 上手流程，学习偏好并引导下一步
- **rename-chat** — 重命名当前会话
- **review** — 使用 Bugbot 或 Security Review 子代理评审代码
- **review-bugbot** — 使用 Bugbot 子代理评审代码
- **review-security** — 使用 Security Review 子代理评审代码
- **sdk** — 基于 Cursor SDK（TypeScript / Python）构建应用与自动化
- **shell** — 将 /shell 请求的剩余内容作为字面 shell 命令执行
- **split-to-prs** — 将当前工作拆分为多个可评审的小 PR
- **statusline** — 配置 CLI 自定义状态栏
- **update-cli-config** — 查看与修改 Cursor CLI 配置
- **update-cursor-settings** — 修改 Cursor / VSCode 用户设置

<a id="structure"></a>
## 目录结构

```text
AntSkills/
├── <skill-name>/          # 43 个技能目录，每个包含 SKILL.md 及可选的
│                          #   agents/（界面元数据）、references/、scripts/ 等
├── LICENSE                # MIT 许可证
└── README.md              # 项目说明（本文件）
```

技能目录采用扁平布局，完整技能清单见[技能分类](#features)。

<a id="quick-start"></a>
## 安装与使用

Agent Skills 为目录约定，将所需技能目录复制到目标工具的 skills 目录即可：

```bash
# 获取技能集合
git clone git@github.com:MiChuan/AntSkills.git

# Cursor
cp -r AntSkills/<skill-name> ~/.cursor/skills/

# Codex
cp -r AntSkills/<skill-name> ~/.codex/skills/
```

Windows PowerShell 等价命令：

```powershell
Copy-Item -Recurse .\<skill-name> $env:USERPROFILE\.cursor\skills\
Copy-Item -Recurse .\<skill-name> $env:USERPROFILE\.codex\skills\
```

安装后，技能通过名称或描述自动触发；部分 Cursor 官方技能支持斜杠命令显式调用（如 `/loop`、`/shell`、`/rename-chat`、`/onboard`）。

<a id="faq"></a>
## 常见问题

### 1. 技能无法被工具识别

请确认技能目录已复制到目标工具的 skills 目录（如 `~/.cursor/skills` 或 `~/.codex/skills`），且 `SKILL.md` 位于技能目录根部。

### 2. 校验提示 Unexpected key in frontmatter

部分 Cursor 官方技能使用 Cursor 平台扩展字段（`environments`、`disable-model-invocation`、`disabled-environments` 等）。在 Codex 等更严格的环境中校验会提示多余键，不影响在 Cursor 中使用，仓库按原样保留。

### 3. 技能需要哪些前置依赖

Superpowers 工作流技能可能需要对应的工具链（如 git、gh 等）；Cursor 官方技能面向 Cursor 平台设计。具体前置条件以各技能 SKILL.md 为准。

### 4. 如何保持技能更新

定期 `git pull` 获取最新内容，或按需仅复制更新的单个技能目录。

<a id="open-source-statement--copyright"></a>
## 开源声明与版权归属

本仓库基于 MIT License 开源发布（详见 [LICENSE](LICENSE)）。在保留原始署名与许可证声明的前提下，使用者可以自由复制、修改、分发、再发布，或用于个人学习与二次开发。

仓库内技能版权归其各自作者所有：Superpowers 技能来自开源项目，Cursor 官方技能来自 Cursor 官方发布，使用或再分发时请遵守对应来源的许可与署名要求。

<a id="notes"></a>
## 其他说明

- 技能来源：自研文档技能（1）、工程实践技能（7）、Superpowers 开源工作流（15）、Cursor 官方技能（20）。
- 部分技能保留 Cursor 平台专用 frontmatter 字段，未做改动，以保证在 Cursor 中的原始行为。
- 各技能目录内附带的 `agents/`、`references/`、`scripts/` 等文件为技能运行所需资源，请随目录一并复制。
