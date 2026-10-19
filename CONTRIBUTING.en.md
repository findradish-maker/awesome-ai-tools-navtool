# Contributing

[简体中文](CONTRIBUTING.md) · **English**

Suggest a useful tool, improve a description, or report a broken link through an Issue or Pull Request.

## Suggest a tool

Include the tool name, a direct product or project URL, a one-sentence use case, a category, 2–5 English tags, and public documentation that supports the description. Disclose your relationship to the product.

Search existing names and domains first. Describe registration, payment, and access conditions accurately. A trial does not imply a permanently free service. Suggestions are reviewed before inclusion.

## Edit the data

Entries are in the `tools` array of `data/tools.json`; categories are in `categories`.

| Field | What to provide |
| --- | --- |
| `id` | A unique ID. Preserve `navtool-ID` for existing entries; use `community-slug` for new suggestions. |
| `name` / `name_en` | Original display name and a useful English label. Do not present an informal translation as an official brand. |
| `category` | An existing category ID. Explain proposals for new categories. |
| `description` / `description_en` | Short Chinese and English use cases, without unsupported claims. |
| `url` | Direct product or project link without referral parameters. |
| `navtool_url` | Existing NavTool overview page, or `null` if not listed. |
| `tags` | Lowercase English tags such as `local-ai`, `rag`, and `workflow`. |
| `source_url` | Public source supporting the entry. |

Keep both READMEs and both `TOOLS` files consistent. Chinese is the default. Both editions must include the same tools, categories, and destinations. If no overview exists, keep the direct product link and use `—` for the overview link.

Update counts, Chinese and English images, and the top-level `updated_at` date when needed. Check JSON syntax from the repository root:

```bash
python3 -m json.tool data/tools.json > /dev/null
```

Explain what changed, why, and which sources you checked. Do not submit credentials, administrative configuration, caches, or complete website backups.

## Corrections and website submissions

For corrections, provide the entry name, link, observation date, and what happened. A temporary connection failure is not proof of permanent closure.

GitHub contributions and [website submissions](https://www.navtool.cn/contribute) follow separate workflows. Merging a PR does not automatically update the website.

By contributing, you confirm that you may share the material and agree to publish your original editorial text and data under [CC BY 4.0](LICENSE). Do not upload material you are not entitled to distribute.
