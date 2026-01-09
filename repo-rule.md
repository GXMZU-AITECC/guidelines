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
 
 确保添加了 **branch ruleset**

### 分支管理

仓库里应该只有 `main` 和 `develop` 两个分支

### 分支规则（branch ruleset）

- Branch targeting criteria：`develop`
- [x] Block force pushes
- [x] Require a pull request before merging
  - Required approvals：**1**
  - [x] Dismiss stale pull request approvals when new commits are pushed
  - [x] Require conversation resolution before merging
