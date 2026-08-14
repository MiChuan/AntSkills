---
name: formalize-readme
description: Use when a user asks to optimize, rewrite, beautify, or formalize a project README (typically Chinese GitHub/Gitee project README.md) into a more formal open-source project presentation, optionally referencing another README's structure. Triggers include "同样处理", "优化 README", "改为正式开源表述", "参考 X 的 README 改写", or applying the same treatment to multiple READMEs.
---

# Formalize Readme

## Overview

Rewrite a project's README into a formal open-source presentation: badges, license statement, anchored table of contents, and consistent sections (简介 / 亮点 / 功能 / 结构 / 环境 / 快速开始 / FAQ / 开源声明 / 其他说明). Preserve all factual content and links; verify every claim against the actual repository before writing.

## Workflow

1. Read the target README and the reference README (if any) fully with UTF-8 encoding.
2. Explore the repository and verify facts: `git remote -v` for the clone URL, LICENSE header for license type and copyright holder, directory tree, key source/config files, sub-READMEs, and CI workflows.
3. Draft the new README in a scratch location following the canonical structure in [references/structure.md](references/structure.md).
4. Fix inaccuracies found during verification (stale clone URLs, wrong counts, missing modules, duplicate numbering, stale historical notes) and keep the user informed of every correction.
5. Back up the original README to the scratch directory before overwriting (the repo's git also protects it).
6. Write the final file to the target path; if the target is outside the sandbox, request escalation for the copy. Verify the target file is identical to the draft.
7. When the session has a user-facing outputs folder convention, also copy the final README there and link it in the reply.

## Rules

- Preserve all existing factual content, tables, and links; formalize tone only.
- Never invent features, numbers, versions, commands, or links — verify against the repository.
- When the user provides a reference README, mirror its structure (badges, anchors, section style); otherwise use the canonical structure.
- Every TOC entry must have a matching `<a id="..."></a>` anchor; verify with a regex pass before delivery.
- The license badge and statement must match the repository's actual LICENSE (MIT, CC BY-SA, etc.).
- Ground FAQ items in real repo content: documented pitfalls, config fields, known failure modes.
- Keep the language consistent with the original README (usually Chinese).
- Mark example credentials, IPs, and absolute paths as "示例值，按实际环境修改"; never ship real secrets.

## References

- [references/structure.md](references/structure.md) — canonical section layout, badge patterns, verification checklist, and common mistakes. Load it before drafting.

## Verification Before Completion

After writing: confirm all anchors match TOC entries, confirm the target file is byte-identical to the draft, and report what was preserved versus corrected.
