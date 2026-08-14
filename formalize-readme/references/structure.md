# README 正式化结构参考

## 标准章节与锚点

按项目类型取舍章节,每个 `##` 标题前放置 `<a id="xxx"></a>` 锚点,目录导航使用 `[文字](#xxx)` 链接:

| 章节 | 锚点 id | 适用场景 |
|------|---------|----------|
| 项目简介 | `introduction` | 所有项目 |
| 项目亮点 | `highlights` | 所有项目 |
| 功能模块 / 功能说明 | `features` | 有明确功能清单 |
| 技术架构 | `architecture` | 系统/多模块项目 |
| 目录结构 | `structure` | 有代码目录 |
| 环境要求 | `requirements` | 有依赖/平台要求 |
| 快速开始 / 部署 | `quick-start` / `deploy` | 有使用/部署步骤 |
| 数据维护 / 配置 | `data-maintenance` / `config` | 有数据或配置说明 |
| 常见问题 | `faq` | 有已知问题或排查表 |
| 开源声明与版权归属 | `open-source-statement--copyright` | 所有项目 |
| 其他说明 / 免责声明 | `notes` / `disclaimer` | 收尾说明 |

## 徽章模式

使用 shields.io,徽章必须与仓库实际信息一致:

```markdown
[![Language](https://img.shields.io/badge/<Label>-<Value>-<color>.svg)](<官方链接>)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/<owner>/<repo>?style=social)](https://github.com/<owner>/<repo>/stargazers)
```

- 语言/框架徽章取实际技术栈(如 C++17、Qt 5.10、Java 8+、微信小程序)
- 许可证徽章与仓库 LICENSE 一致(MIT / CC BY-SA 4.0 等)
- stars 徽章使用真实 owner/repo

## 核查清单(写作前)

- `git remote -v` → 确认 clone 地址,更新过时 URL
- LICENSE 头部 → 许可证类型与版权人
- 目录树 → 目录结构章节与实际一致
- 源码/配置/子文档 → 核对数量、版本、命令、端口、CI 配置
- `.gitignore` → 区分"随仓库分发"与"运行时生成/不入库"目录
- 项目为课程/实验仓库时 → 定位、示例凭据与安全提醒要写清楚

## 常见错误

- 徽章仓库地址或许可证类型错误
- 克隆地址过时(旧用户名/旧仓库名)
- 虚构功能、数字或版本
- 锚点与目录导航不匹配
- 忽略被 gitignore 的运行时目录(应标注"运行时生成,不入库")
- 直接暴露示例 IP/账号密码(应注明"示例值,按实际环境修改")
- 保留历史遗留备注(如"××已完成"的旧记录)或重复编号

## 保留 vs 修正

- **保留**:全部事实内容、数据表格、链接、命令与注意事项
- **修正**:过时 URL、错误数量、缺失模块(核查后补充)、重复章节编号、失效的历史备注
