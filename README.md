# AITECC 社团规范

> 只有两张表要记：**P 表**管人——踩线就按表处理，不商量；**T 表**管 PR——打回时只引用序号。其余全在 `soft/` 二级目录里，是"怎么做"的说明，**不能当拒绝理由**。

## P · 违反社团规范（P0–P4，数字越小越严重）

| 编号 | 踩什么线 | 怎么处理 |
| --- | --- | --- |
| **P0** | 外泄内部资产：把仓库内容、赛题、Issue / PR 讨论用链接、截图、复制、转发等任何形式给组织外的人，或挂到公开简历、博客、社交账号 | 立即移出组织，当期考核资格作废；上报人工智能学院指导教师，后果自负 |
| **P1** | 破坏仓库：强推覆盖历史、删主干或他人分支、删别人写的代码、绕过分支保护直改主干、擅改仓库权限或 Webhook | 收回全部写权限 1 个月并还原内容；第二次直接清退 |
| **P2** | 评审造假：自己 approve 自己、找人刷批准、把他人代码或 AI 整篇生成的代码当自己写的且不声明 | 当期 PR 作废，考核顺延一轮；已入社的由技术部通报 |
| **P3** | 占题造假：不占题就开工、抢别人已占的题目、同一题反复刷 PR 占位 | 题目收回，本人重新排队 |
| **P4** | 带病交付：明知跑不通却写「已完成」、夹带无关改动掩盖问题、密钥或令牌硬编码进仓库 | PR 打回并本人书面说明；密钥立即轮换，造成实际损失的按 P1 处理 |

- 执行：技术部部长提出、组织管理员复核，结论直接写在对应 Issue / PR 里，不另开讨论串。
- P 表只管人，不管代码写法；写法问题一律走 T 表。

## T · 打回 PR 引用的序号（T0–T12，数字越小越严重）

| 序号 | 一句话 | 细则在哪 |
| --- | --- | --- |
| **T0** | 不许绕过 PR 改主干：`main` / `develop` 只接受合并 | [soft/repo.md](./soft/repo.md) A3 |
| **T1** | PR 目标分支是 `develop`，提向 `main` 的直接拒 | [soft/pr.md](./soft/pr.md) C1 |
| **T2** | Reviewers 里 assign ≥2 人、≥1 人批准、项目负责人合并；只在正文打 @ 不算 | [soft/pr.md](./soft/pr.md) C5 |
| **T3** | 仓库长期分支只有 `main` 和 `develop` | [soft/repo.md](./soft/repo.md) A2 |
| **T4** | 分支名只能 `feature/...` 或 `bugfix/...` | [soft/develop.md](./soft/develop.md) B2 |
| **T5** | 开工前 rebase 最新 `develop`，带冲突的 PR 不收 | [soft/develop.md](./soft/develop.md) B1 |
| **T6** | 标题 `feat:` 或 `fix:` 开头 | [soft/pr.md](./soft/pr.md) C2 |
| **T7** | 描述写全三段：目的 / 改动 / 测试 | [soft/pr.md](./soft/pr.md) C3 |
| **T8** | 自查清单逐条勾选，没勾等于没自查 | [soft/pr.md](./soft/pr.md) C4 |
| **T9** | 开工前在 Issue 占题：姓名 + fork 链接 + 计划分支名 | [soft/develop.md](./soft/develop.md) B1 |
| **T10** | 一个 PR 只做一件事：不顺手重构、不碰无关文件 | [soft/pr.md](./soft/pr.md) C5 |
| **T11** | 项目仓 README 必含五段：项目简介 / 设备依赖 / 环境配置 / 使用方法 / 维护人员 | [soft/documents.md](./soft/documents.md) E1 |
| **T12** | 必有 LICENSE：默认 MIT；派生 GPL / Apache 代码沿用上游 | [soft/documents.md](./soft/documents.md) E2 |

**用法**：打回只写序号，不写理由——`违反 T6`、`T7、T8`、`见 T2`。成员自己查表，不服在 PR 里追问。
表外的问题只能算建议（`soft/` 里的东西），不得作为拒绝依据：**规范了就行，不挑刺**。

## 二级目录：怎么做，不是检查项

| 文件 | 内容 |
| --- | --- |
| [soft/repo.md](./soft/repo.md) | A · 仓库命名、分支模型、分支保护怎么配 |
| [soft/develop.md](./soft/develop.md) | B · 开发流程、分支命名、占题与防撞车、注释与可运行 |
| [soft/pr.md](./soft/pr.md) | C · PR 目标分支、标题、描述、自查、评审与合并 |
| [soft/permissions.md](./soft/permissions.md) | D · 角色与权限、权限申请、保密（P0 出处） |
| [soft/documents.md](./soft/documents.md) | E · README 模板、LICENSE、依赖文件 |
| [soft/device.md](./soft/device.md) | F · 硬件设备项目：设备信息标注、资料归档 |
| [soft/academic.md](./soft/academic.md) | G · 学术成果与代码关联 |

## 要改规范

照 C 章提 PR 进 `develop`，大版本打 tag、发 milestone。这里不放更新日志，也不写维护说明。