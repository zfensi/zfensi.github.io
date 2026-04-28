# zfensi.github.io

最小 GitHub Pages 多文章个人博客，已包含中文博客首页、分页、404、归档页、分类页、标签页、关于页、RSS、sitemap、robots 和基础 SEO 配置。

## 结构

1. `index.html`：中文博客首页，支持分页。
2. `404.html`：自定义 404 页面。
3. `archive.md`：文章归档页。
4. `categories.md`：分类页。
5. `tags.md`：标签页。
6. `about.md`：关于页。
7. `_layouts/post.html`：文章布局，包含面包屑、相关文章和内链。
8. `_posts/`：文章目录和模板文章。
9. `_config.yml`：GitHub Pages / Jekyll / SEO 配置。
10. `robots.txt`：搜索引擎抓取规则。
11. `_includes/head-custom.html`：图标、自定义样式和补充 meta。
12. `_includes/structured-data.html`：结构化数据。
13. `.github/workflows/pages.yml`：推送到 `main` 后自动部署。

## 使用方式

1. 在 `_posts` 新建文章，文件名格式：`YYYY-MM-DD-文章名.md`
2. 参考 `_posts/2026-04-29-post-template.md` 写文章头信息和正文
3. 提交并推送到 `main`
4. 等待 GitHub Actions 部署完成

## 文章格式

1. 支持 `title`、`date`、`slug`、`tags`、`target_repo`、`category`、`description`、`cover`
2. 为了兼容 Jekyll 分类聚合，建议同时保留 `categories: [你的分类]`
3. `cover` 建议使用站内路径，例如：`/images/blog/Instagram/your-post.jpg`

## SEO 基础

1. 已启用 RSS：`/feed.xml`
2. 已启用站点地图：`/sitemap.xml`
3. 已添加 `robots.txt`
4. 已接入 Google 验证文件
5. 已补充基础描述、封面图、favicon、robots meta 和结构化数据
6. 已加入面包屑、分类页、标签页和相关文章内链
7. 当文章数量超过 6 篇时，首页会自动出现分页
8. 导航栏支持直接显示分类入口

## 封面图

1. 文章封面优先使用站内本地图片，避免外链失效
2. 当前已下载两张可免费使用的真实照片封面到 `images/blog/...`
3. 旧的 `.svg` 封面仍保留，后续可自行删除

## 图标

站点 favicon 已同步自 `www.zfensi.com`。

## 注意

如果你要使用根域名 `https://zfensi.github.io`，GitHub 仓库名必须叫 `zfensi.github.io`。
