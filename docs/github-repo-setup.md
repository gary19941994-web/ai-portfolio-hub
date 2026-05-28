# GitHub 仓库设置建议

这套设置适合你的目标：把 AI 产品、Power BI、AI 视频流程、Agent/Skill 项目整理成能给面试官看的作品集。

## 推荐仓库策略

当前 `New project` 目录内容比较杂，建议不要直接当成一个公开大仓库全量上传。更适合分成：

1. `ai-portfolio-hub`：作品集首页仓库，放 README、项目索引、截图、演示链接。
2. `tenclass-ai-demo`：Tenclass AI demo 单独仓库，展示前端/产品原型能力。
3. `powerbi-interview-dashboard`：Power BI 面试项目仓库，放说明、截图、数据生成脚本、PBIX。
4. `ai-video-production-workflow`：AI 视频工作流仓库，放分镜、提示词、流程文档、样片链接。
5. `codex-hatch-pet-lab`：Codex pet / skill 实验仓库，可作为 Agent 工具链项目。

如果你想先简单一点，也可以先做一个公开的 `ai-portfolio-hub`，其他项目暂时放子文件夹。

## GitHub 网页设置

进入仓库页面后，点 `Settings`，按下面设置：

## General

- `Repository name`：用英文短名，例如 `ai-portfolio-hub`。
- `Description`：一句话说明价值，例如 `AI portfolio projects: Power BI dashboards, AI video workflow, and agent/skill prototypes.`。
- `Website`：如果有部署页面，填 Vercel/Netlify/GitHub Pages 链接。
- `Features`：开启 `Issues`，开启 `Discussions` 可选；`Wiki` 暂时不用。
- `Pull Requests`：开启 `Allow squash merging`，关闭或少用 merge commit，让历史更干净。

## Branches

- 默认分支建议用 `main`。
- 添加 branch protection rule：`main`。
- 开启 `Require a pull request before merging`。
- 开启 `Require status checks to pass before merging`，选择 `Repo Health`。
- 个人作品集早期可以不开 `Require approvals`，等项目稳定后再开。

## Actions

- 允许 GitHub Actions。
- 当前已加入 `.github/workflows/repo-health.yml`，会检查超大文件并输出仓库摘要。
- 后续如果项目是前端，再加 build/test workflow。

## Security

- 开启 `Dependabot alerts`。
- 开启 `Secret scanning`，避免 API Key 泄漏。
- 如果有 `package.json`，再加 Dependabot version updates。

## About 区域

建议加 topic：

- `ai`
- `portfolio`
- `powerbi`
- `data-analysis`
- `ai-video`
- `agents`
- `codex`
- `prompt-engineering`

## README 推荐结构

```md
# 项目名

一句话说明这个项目解决什么问题。

## Demo

截图、视频链接、在线地址。

## Highlights

- 亮点 1
- 亮点 2
- 亮点 3

## Tech Stack

工具、模型、框架、数据来源。

## Workflow

从输入到输出的流程。

## Results

具体产出、截图、指标或面试展示方式。

## What I Learned

你在产品、数据、AI 工作流、工程化上的思考。
```

## 文件管理建议

- 不上传 `.env`、API Key、账号截图、临时缓存。
- 大视频不要直接放 GitHub，建议放网盘、Bilibili 私密/公开链接、YouTube、飞书文档或 Releases。
- PBIX 可以上传，但最好配截图和说明，否则面试官不一定会下载打开。
- 生成过程中的草稿图太多时，只保留最终图和少量过程图。

## 当前本地已完成

- 已补 `.gitignore`，避免缓存和临时截图进入仓库。
- 已添加 PR 模板。
- 已添加 Issue 模板。
- 已添加 `Repo Health` GitHub Actions workflow。
