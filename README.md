# 出海学习

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
