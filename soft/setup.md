# 建仓与交付（谁建仓谁执行）

1. **命名**：全小写连字符，不用人名、不用中文、不用个人账号名；设备类把机型写进去（`unitree-g1-demo`、`unitree-go2-ruicom`、`yundrone-sunray150`）。
2. **长期分支只有两条**：`main` 是发布线，`develop` 是日常开发线；其余分支合并即删。`main` 只由 `develop` 经 PR 合并。纯文档与门面仓（`guidelines`、`.github`、`.github-private`）可以只有 `main`，但研发仓必须先有 `develop` 再收 PR——**T3 要求的目标分支，建仓时就得存在**。
3. **CODEOWNERS 必配**：`.github/CODEOWNERS` 里写 `* @GXMZU-AITECC/<负责这个仓的 team>`，评审由 GitHub 自动派给 team，谁有空谁认领。承担 code owner 的 team 必须是**可见**的（closed 可以，**private 不行**，改私有会静默失去自动派评审）；换届只改 team 成员，**仓库里永远不出现个人账号**。
4. **分支保护**：公开仓必须配 ruleset——禁删、禁强推、PR 须 ≥1 名批准、推新提交撤销旧批准、对话须解决；私有仓受套餐限制开不了 ruleset，靠"进了对应 team 才可见、才可写"收口。
5. **社内不 fork**：进了对应 team 的成员直接在仓里拉分支、向 `develop` 提 PR。fork 只用于对外部候选人开放的仓库。
6. **交付验收**（验收项目时查，不作为打回单个 PR 的依据）：README 五段＝项目简介、设备依赖、环境配置、使用方法、维护团队（写 team 名）；LICENSE 默认 MIT，派生 GPL／Apache 的代码沿用上游许可证；依赖清单（`requirements.txt`、`package.json` 等）随代码一起提交。
7. **学术关联**：代码对应的论文、专利在 README 里列清标题、状态、对应目录；未发表的内容不进公开仓（P0）。