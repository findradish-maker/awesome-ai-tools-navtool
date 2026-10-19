# Data guide

[简体中文](data-guide.md) · **English**

[`data/tools.json`](../data/tools.json) contains the same curated tools as both READMEs. Use it for a directory, search index, resource page, or team tool-selection table.

## Structure

`updated_at` is the editorial snapshot date. `categories` defines bilingual categories; `sources` records public source pages.

| Entry field | Meaning |
| --- | --- |
| `id` | Unique ID, such as `navtool-2204` |
| `name` / `name_en` | Original display name and English label |
| `category` | ID from `categories` |
| `description` / `description_en` | Chinese and English use cases |
| `url` | Direct product or project link |
| `navtool_url` | Chinese overview on NavTool |
| `tags` | English filter tags |
| `source_url` | Public page used to prepare the entry |

Existing Chinese fields are preserved. Read `name_en` and `description_en` to display English. Categories use the same convention.

## Example

Run this Python code from the repository root. No additional dependencies are required:

```python
import json
from pathlib import Path

catalog = json.loads(Path("data/tools.json").read_text(encoding="utf-8"))

for tool in catalog["tools"]:
    if "rag" in tool["tags"]:
        print(f"{tool['name_en']}: {tool['url']}")
```

Filter by IDs such as `coding`, `agents`, `local-ai`, or `documents`. The JSON file contains the complete list.

This is a curated snapshot, not a live API or full website export. URLs omit `utm_` parameters. WPS AI and Generative AI for Beginners use corrected direct resource links.

Check providers for current features, pricing, licensing, and availability. Follow [CC BY 4.0](../LICENSE) and the [brand notice](../NOTICE.en.md) when reusing the content.

[Back to the English README](../README.en.md)
