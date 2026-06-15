# 出海学习

<!-- SIUSER-REPO-GUIDE:START -->
## Repository Guide

### What This Repository Does

出海学习库：镜像金山文档团队空间并生成互动学习页、飞书同步和资料索引。

English summary: Overseas expansion learning hub mirroring KDocs materials into interactive pages, Feishu sync, and indexed resources.

### Online Entry Points

- GitHub repository: https://github.com/siuserxiaowei/chuhai-xuexi
- Live / GitHub Pages: https://siuserxiaowei.github.io/chuhai-xuexi/
- Default branch: `main`
- Primary language: `HTML`

### How To Read / Learn This Repository

1. 先读本 README，确认项目目标、在线入口和本地运行方式。
2. 打开上方 Live / GitHub Pages 链接，先从最终效果理解项目。
3. 按仓库目录从入口文件、数据文件、脚本和文档依次阅读。
4. 如果要修改内容，先小范围改动，再运行本 README 中的验证命令。

### Clone This Repository

```bash
git clone https://github.com/siuserxiaowei/chuhai-xuexi.git
cd chuhai-xuexi
```

### Run Or View Locally

```bash
python3 -m http.server 8000
```

然后打开 `http://127.0.0.1:8000/`。

### Repository Map

| Path | Purpose |
| --- | --- |
| `README.md` | 项目入口说明，先读这里。 |
| `index.html` | 静态站首页或页面入口。 |
| `data/` | 数据、索引或结构化内容。 |
| `assets/` | 图片、样式、字体或页面资源。 |
| `scripts/` | 构建、同步、生成或维护脚本。 |
| `content/` | 项目目录。 |
| `feishu_pages/` | 项目目录。 |
| `learn/` | 项目目录。 |
| `reports/` | 项目目录。 |
| `unsupported.md` | 项目文件。 |

### Maintenance Notes

- Keep this README in sync when the project purpose, live link, or run commands change.
- Prefer small, focused commits when changing code, data, or generated pages.
- Run the relevant build or validation command before publishing changes.
- If this is a generated/static archive, update the source data first, then regenerate the public files.

### Privacy And Safety

- Do not commit API keys, tokens, passwords, cookies, private URLs, or internal account data.
- Keep private source material out of public GitHub Pages output unless it has been explicitly cleared for publication.
- When in doubt, run a quick secret scan such as `rg -n "token|secret|password|access_key|authorization"` before pushing.
<!-- SIUSER-REPO-GUIDE:END -->

金山文档团队空间镜像归档、互动学习页与飞书知识库同步项目。

## 在线结构

- `index.html`：总入口、搜索与文档索引。
- `learn/<slug>/index.html`：每篇文档的翻页式互动学习页。
- `content/<slug>.md`：从金山文档读取后的 Markdown/结构化正文。
- `archive/`：可下载且低于 GitHub 单文件限制的原始文件。
- `data/manifest.json`：金山、飞书、GitHub Pages 链接映射。
- `reports/dao-fa-shu-qi-shi.md`：全局「道、法、术、器、势」分析。

## 本地生成

```bash
export PATH="$HOME/.local/bin:$PATH"
python3 scripts/kdocs_crawl.py --drive 2524825563 --drive 2581401869
python3 scripts/generate_site.py --base-url "https://siuserxiaowei.github.io/chuhai-xuexi"
python3 scripts/feishu_sync.py --base-url "https://siuserxiaowei.github.io/chuhai-xuexi"
```

## 注意

仓库是公开仓库。执行迁移前请确认金山文档内容允许公开发布。
