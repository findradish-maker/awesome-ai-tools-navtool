# 数据使用说明

**简体中文** · [English](data-guide.en.md)

[`data/tools.json`](../data/tools.json) 是 README 中精选条目的结构化版本，可用于个人导航、搜索索引、资源页与团队选型表。

## 字段

顶层 `updated_at` 是整理日期，`categories` 定义中英文分类，`sources` 记录公开来源。中文字段保持原名，英文使用 `name_en` 和 `description_en`。

| 条目字段 | 含义 |
| --- | --- |
| `id` | 唯一标识，例如 `navtool-2204` |
| `name` | 工具名称 |
| `name_en` | 英文展示名称 |
| `category` | 对应 `categories` 的分类 ID |
| `description` | 简短用途说明 |
| `description_en` | 英文用途说明 |
| `url` | 工具或项目的直接入口 |
| `navtool_url` | 探兔中文介绍页 |
| `tags` | 用于筛选的英文标签 |
| `source_url` | 整理时使用的探兔公开页面 |

## 读取示例

在仓库根目录运行以下 Python 代码，无需额外安装依赖：

```python
import json
from pathlib import Path

catalog = json.loads(Path("data/tools.json").read_text(encoding="utf-8"))

for tool in catalog["tools"]:
    if "rag" in tool["tags"]:
        print(f"{tool['name']}: {tool['url']}")
```

也可以按分类筛选，例如 `coding`、`agents`、`local-ai`、`documents`。完整分类 ID 以 JSON 文件为准。

这是随仓库保存的精选快照，不是实时 API，也不是网站的完整数据导出。工具入口去掉了 `utm_` 推广参数；WPS AI 和生成式 AI 入门课程的链接整理为对应资源的直接入口。

功能、价格、第三方许可和可用性请在使用前核对。复用文字与分类数据时请遵循 [CC BY 4.0](../LICENSE) 与 [品牌说明](../NOTICE.md)。

[返回 README](../README.md)
