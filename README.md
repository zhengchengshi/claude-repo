# Claude Repo

AI 生成代码的统一管理仓库。通过分类目录组织不同类型的项目，保持结构清晰、易于检索。

## 目录结构

```
claude-repo/
├── apps/            # 完整的应用项目（Web 应用、CLI 工具、移动端等）
├── packages/        # 可复用的库和模块（跨项目共享的通用代码）
├── experiments/     # 实验性代码和原型（快速验证想法，允许粗糙）
├── scripts/         # 通用脚本和工具（自动化、数据处理等）
├── docs/            # 项目文档
└── landing/         # 产品落地页（GitHub Pages 部署）
```

### apps/

完整的、可独立运行的应用项目。每个项目拥有自己的依赖管理和构建配置。

### packages/

可被多个项目复用的库或模块。适合提取出来的通用逻辑、UI 组件库等。

### experiments/

实验性质的代码、快速原型、概念验证。不要求生产质量，重在快速迭代。

### scripts/

独立的脚本和小工具，如数据处理、批量操作、自动化任务等。

### docs/

跨项目的文档、架构设计、技术决策记录等。

## 新增项目

在对应分类目录下创建子目录，使用 kebab-case 命名：

```bash
# 新建一个 Web 应用
mkdir apps/my-web-app

# 新建一个实验项目
mkdir experiments/chatbot-prototype

# 新建一个工具库
mkdir packages/shared-utils
```

每个项目目录内应包含自己的 `README.md`，说明项目用途、技术栈和运行方式。

## 分支策略

| 分支 | 用途 |
|------|------|
| `master` | 主分支（受保护，需 PR 审查合并） |
| `dev` | 日常开发分支 |
| `feat/*` | 功能开发分支 |
