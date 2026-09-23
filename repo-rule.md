# A · Repo 规范

## A1 仓库命名（软建议）

1. 不使用过于宽泛的名称
   - 反例：`calculator`
   - 正例：`calculator-py-windows`
2. 不混用大小写，全部小写
   - 反例：`Calculator-Py-windows`
   - 正例：`calculator-py-windows`
3. 只使用 `-` 作为分隔符
4. 命名优先级：`方向` → `项目名称` → `标签`（均可选）

## A2 分支模型（强制）

仓库只保留 `main`（发版）与 `develop`（开发）两个长期分支。

## A3 分支保护（管理员配置）

> 本条由管理员建仓时配置，不作为成员检查项。

1. 目标分支：`develop`
2. 阻止强制推送（Block force pushes）
3. 合并前必须提交 PR（Require a pull request before merging）
   1. 需要批准数 ≥ **1**
   2. 新提交推送时撤销过时的 PR 批准
   3. 必须解决全部评审对话后才可合并
