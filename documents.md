# E · Repo 必含文档要求

每个 Repo 必须包含 E1、E2（强制）；E3 为软建议。新手按模板填写即可：

## E1 README.md（强制）

### 新手模板

```markdown
# 项目名称

## 项目简介

一句话说明：如「基于宇树 G1 机器人的强化学习算法实现」

## 设备依赖

参考 device-rules.md 填写

## 环境配置

参考 requirements.txt/environment.yml 说明部署步骤

## 使用方法

简单示例：如「python train.py --device unitree-g1」

## 维护人员

姓名 + 邮箱
```

## E2 LICENSE（强制）

优先选择 MIT 许可证（宽松，便于学术交流）。

## E3 环境依赖文件（软建议）

- Python 项目：必含 requirements.txt（列出所有依赖包 + 版本，如 torch==2.1.0）；
- Conda 项目：可选补充 environment.yml（便于一键创建环境）；
- 新手指令：`pip freeze > requirements.txt` 可自动生成依赖文件。
