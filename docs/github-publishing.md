# 发布到 GitHub

推荐仓库名称：**awesome-ai-tools-navtool**。

默认首页为中文 `README.md`，英文版为 `README.en.md`，两页顶部互相切换。目录名已同步为 `awesome-ai-tools-navtool/`。

名称前半部分保留 `awesome-ai-tools`，直接表达 AI 工具精选；后半部分加入品牌 `navtool`，便于与同类清单区分，并对应 navtool.cn。GitHub 可按名称、简介和 Topics 检索仓库，发布时应一起完善这些字段。[GitHub 搜索说明](https://docs.github.com/en/search-github/searching-on-github/searching-for-repositories)

不同 GitHub 账号或组织下可以存在同名仓库，名称只需在所属账号或组织下唯一。这里加入品牌是为了辨识项目；是否能在你的账号下创建，以 GitHub 创建页面为准。[GitHub 创建仓库说明](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)

中文简介可以直接使用：

> Awesome AI Tools · 探兔AI导航，中文 AI 工具精选。收录 120 个工具、16 个分类，覆盖 AI 对话、编程、Agent、绘画、视频、办公与学习，配中文介绍和在线导航。navtool.cn

英文简介可用于 GitHub 的 About 字段，兼顾英文关键词检索：

> Curated AI tools for coding, agents, RAG, local LLMs, image generation, video and productivity. 120 tools, 16 categories, Chinese & English. Explore more at navtool.cn.

Website 填写：`https://www.navtool.cn/`

建议 Topics：`ai`、`ai-tools`、`awesome`、`awesome-list`、`ai-directory`、`ai-agents`、`rag`、`llm`、`developer-tools`、`generative-ai`、`ai-coding`、`productivity`、`chinese`、`navtool`。[GitHub Topics 说明](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)

## 网页上传

1. 登录 GitHub，创建名为 `awesome-ai-tools-navtool` 的 Public 仓库。
2. 这里已准备好 README、LICENSE 和 .gitignore，创建时无需再自动生成这些文件。
3. 进入新仓库的文件上传页面，上传本目录里的内容，保留 `images/`、`data/`、`docs/` 和 `.github/` 的目录结构。
4. 根目录应直接看到 `README.md`，不要再套一层 `awesome-ai-tools-navtool/`。
5. 提交后填写简介、Website 和 Topics。若网页上传遗漏隐藏的 `.github/` 或 `.gitignore`，可以用下面的命令行方式完整上传。

## 使用 GitHub CLI

在**本目录**打开终端。首次使用需要先安装 Git、GitHub CLI，并通过 `gh auth login` 登录自己的账号。

```bash
git init -b main
git add .
git commit -m "Add awesome-ai-tools-navtool curated directory"
gh repo create awesome-ai-tools-navtool --public --source=. --remote=origin --push
```

以上命令会实际创建公开仓库并推送内容；仓库名称已存在时，请先确认现有仓库归属，不要覆盖不相关的项目。

## 发布后检查

- 仓库首页能显示 README、封面、分类概览、访问横幅及折叠区内的开发者地图。
- 默认显示中文，English 链接能切换到包含相同 120 个工具的英文版。
- `TOOLS.md` 与 `data/tools.json` 均可打开。
- `images/` 下的图片位于仓库内，README 没有依赖本机路径。
- Issues 页面能选择推荐工具、修正信息两个模板。
- 简介准确表述为工具清单与展示仓库。

当前目录只准备了公开文档、工具数据与品牌展示素材。网站的部署源码、数据库、后台配置及账号信息不属于本次发布内容。
