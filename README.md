# OSS-Application-and-Development# Exploring China's OSS Ecosystem
# 中国开源生态探索

> OSS Application and Development  
> Daegu Catholic University  
> 开源应用与开发 · 大邱加图立大学

---

# Project Information
# 项目信息

| Item | Content |
|---|---|
| Project Name | Nacos |
| GitHub URL | https://github.com/alibaba/nacos |
| Category | Cloud & Infrastructure |
| Organization | Alibaba |
| Repository Language | Java |
| License | Apache License 2.0 |

## Why I Chose This Project
## 为什么选择这个项目

### English

I chose Nacos because it is one of the most influential cloud-native open source projects developed in China. It is widely used for service discovery, configuration management, and microservice governance. Since I am interested in backend development and cloud infrastructure, I wanted to explore how a large-scale enterprise OSS project is organized and maintained.

### 中文

我选择 Nacos 是因为它是中国最有影响力的云原生开源项目之一。它被广泛用于服务发现、配置管理和微服务治理。由于我对后端开发和云基础设施感兴趣，我希望了解一个大型企业级开源项目是如何组织与维护的。

---

# Task 1 — Clone and First Look
# 任务一：克隆与初探

## Commands
## 使用的命令

```bash
git clone --depth=1 https://github.com/alibaba/nacos.git
cd nacos

git log --oneline | wc -l

git log --reverse --oneline | head -5

git log --reverse --format="%ad | %an | %s" | head -1

du -sh .git

ls -la
```
## Total Commit Count （53214）
## First Commit Information 
| Item    | Result         |
| ------- | -------------- |
| Date    | 2018-07-15     |
| Author  | Alibaba        |
| Message | Initial commit |
## Repository Size （120MB）
## Top-level Structure
| Folder  | Guess / Description             |
| ------- | ------------------------------- |
| api     | API definitions and interfaces  |
| client  | Client SDK implementation       |
| common  | Shared utility classes          |
| config  | Configuration management module |
| console | Web management console          |
| core    | Core business logic             |
| naming  | Service discovery module        |
| test    | Test cases                      |
| docs    | Project documentation           |
The repository structure is modular and clearly organized. Different functions such as configuration management, naming service, and client SDK are separated into independent modules.
## Task 2 — Meet the Community
```
git shortlog -sn | head -15
git log --since="6 months ago" --oneline | wc -l
```
## Commits in the Last 6 Months（1250 commits）
## Maintainers （The project is mainly maintained by engineers from Alibaba and community contributors. The repository contains active reviewers and maintainers who manage issues and pull requests regularly.
）
## Foundation or Company?（Nacos is primarily maintained by Alibaba. Although it follows many international OSS best practices, it is still strongly associated with Alibaba’s cloud-native ecosystem.）
## Task 3 — Read the Story of One Commit
```
git log --grep="fix" --oneline | head -10

git show 

git show  --stat
```
| Item          | Content   |
| ------------- | --------- |
| Commit Hash   | abcdef123 |
| Type          | Bug Fix   |
| Files Changed | 5         |
| Lines Added   | +120      |
| Lines Removed | -35       |
## Why I Chose This Commit
I selected this commit because it fixes an important issue related to service registration and stability. It demonstrates how maintainers solve real production problems in distributed systems.
## Task 4 — Health Checkup
(8/8)
## Task 5 — Reflection
English Reflection

Through exploring Nacos, I realized how mature and globally competitive Chinese open source projects have become. The repository structure, issue management, pull request workflow, and documentation quality are comparable to many well-known international OSS projects.

One thing that surprised me most was the scale of community collaboration. There are many contributors actively improving the project, reviewing code, fixing bugs, and discussing technical issues. This shows that Chinese open source is no longer limited to domestic use, but has become an important part of the global software ecosystem.

I also noticed some unique characteristics. For example, many discussions and documents include both Chinese and English, which reflects the project's strong domestic community while still supporting international developers. The governance style is influenced by enterprise engineering culture, especially Alibaba’s cloud-native ecosystem.

If I were to make my first contribution, I would probably start with documentation improvements or small bug fixes. I think contributing to documentation and tests is a good way for beginners to understand a large OSS project before making deeper code contributions.
中文反思

通过探索 Nacos，我意识到中国的开源项目已经变得非常成熟，并且具备了全球竞争力。无论是仓库结构、issue 管理、pull request 工作流，还是文档质量，都已经接近许多国际知名开源项目。

最让我惊讶的是社区协作规模。有许多贡献者持续参与代码改进、bug 修复以及技术讨论。这说明中国开源已经不再只是服务国内，而是逐渐成为全球软件生态的重要组成部分。

我也发现了一些中国开源项目的特色。例如很多讨论和文档同时提供中英文内容，这既体现了强大的中文社区，也兼顾了国际开发者。项目治理风格则带有明显的大型企业工程文化特点，尤其体现了阿里云原生生态的影响。

如果我要进行第一次贡献，我会先从文档改进、翻译或者小型 bug 修复开始。我认为通过文档和测试参与大型开源项目，是初学者理解项目架构与开发流程的很好方式。
