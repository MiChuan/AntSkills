# AntSkills

我的 AI Agent 技能集合（My AI Agent skills），共 43 个技能，按来源与用途分类。

## README 与文档

- **formalize-readme** — 将项目 README 改写为正式开源项目表述：徽章、锚点目录、标准章节，写作前核查仓库事实，交付前校验锚点与文件一致性

## 工程实践

- **adversarial-test** — 对已完成代码做对抗性测试，攻击异常输入、边界值、并发与网络失败，发现问题后补永久回归测试
- **commit-review** — 审查最后一次提交，只关注安全、性能与逻辑问题，每条给出文件、行号与触发条件
- **html-report** — 将结果输出为单文件 HTML（标签页、流程图、颜色），而非 Markdown
- **lock-behavior** — 重构前先用测试固定现有行为（含奇怪边界），再动手
- **minimal-change** — 以最小改动实现需求，不增加未来抽象，匹配项目现有风格
- **reproduce-first** — 遇到 Bug 先写最小复现测试，确认问题真实存在后再修复
- **understand-first** — 修改前先阅读相关代码、测试、配置与依赖，复述需求并列出方案

## Superpowers 工作流

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

## Cursor 官方技能

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
