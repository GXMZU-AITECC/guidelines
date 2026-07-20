# Repo 规范

## Repo 命名规范

- 不要使用过于宽泛的名称
  - 错误示范：`calculator`
  - 正确示范：`calculator-py-windows`
- 不要大小写混用，全部使用小写
  - 错误示范：`Calculator-Py-windows`
  - 正确示范：`calculator-py-windows`
- 不要使用除了 `-` 以外的分割符
- 名称优先级为 `方向`->`项目名称`->`标签`
  - 都是可选的

## 仓库PR规则

确保添加了 **branch ruleset**（规则配置见下方 [分支规则](#分支规则branch-ruleset)）

PR 提交规范详见 [pr-rule.md](./pr-rule.md)

### 分支管理

仓库里应该只有 `main` 和 `develop` 两个分支

### 分支规则（branch ruleset）

- 目标分支：`develop`
- [x] 阻止强制推送（Block force pushes）
- [x] 合并前要求提交 PR（Require a pull request before merging）
  - 需要批准数：**1**
  - [x] 新提交推送时撤销过时的 PR 批准
  - [x] 要求解决所有对话后才能合并
     
### README 规范
参考 [documents.md](./documents.md)
