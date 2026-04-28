# zfensi.github.io

最小 GitHub Pages 多文章个人博客，已包含中文博客首页、归档页、关于页、RSS、sitemap、robots 和基础 SEO 配置。

## 结构

1. `index.md`：中文博客首页。
2. `archive.md`：文章归档页。
3. `about.md`：关于页。
4. `_posts/`：文章目录和模板文章。
5. `_config.yml`：GitHub Pages / Jekyll / SEO 配置。
6. `robots.txt`：搜索引擎抓取规则。
7. `_includes/head-custom.html`：图标、自定义样式和补充 meta。
8. `.github/workflows/pages.yml`：推送到 `main` 后自动部署。

## 使用方式

1. 在 `_posts` 新建文章，文件名格式：`YYYY-MM-DD-文章名.md`
2. 参考 `_posts/2026-04-29-post-template.md` 写文章头信息和正文
3. 提交并推送到 `main`
4. 等待 GitHub Actions 部署完成

## SEO 基础

1. 已启用 RSS：`/feed.xml`
2. 已启用站点地图：`/sitemap.xml`
3. 已添加 `robots.txt`
4. 已接入 Google 验证文件
5. 已补充基础描述、封面图、favicon 和 robots meta

## 图标

站点 favicon 已同步自 `www.zfensi.com`。

## 注意

如果你要使用根域名 `https://zfensi.github.io`，GitHub 仓库名必须叫 `zfensi.github.io`。
