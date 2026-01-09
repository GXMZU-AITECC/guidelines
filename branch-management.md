# 分支管理规范（强制遵守）

## 统一分支模型（新生易记版）

### 核心分支（永久保留）

1. `main`：正式发布分支，仅合并经过评审的稳定代码，禁止直接提交代码；
2. `develop`：日常开发主分支，所有功能开发完成后合并到此分支测试。

### 临时分支（完成后删除）

1. `feature/[功能名]`：新增功能开发（如 `feature/unitreeG1-env`）；
2. `bugfix/[问题描述]`：修复 bug（如 `bugfix/rl-training-crash`）。

## 分支操作流程（新生必看）

1. 开发新功能：从 `develop` 拉取 `feature/*` 分支 → 开发完成 → 提 PR 合并回 `develop` → 删除 `feature/*` 分支；
2. 修复 bug：从 `develop` 拉取 `bugfix/*` 分支 → 修复完成 → 提 PR 合并回 `develop` → 删除 `bugfix/*` 分支；
3. 发布版本：从 `develop` 提 PR 合并到 `main` → 在 `main` 分支打版本标签（如 `v1.0`）。
