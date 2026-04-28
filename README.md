# zfensi.github.io

最小 GitHub Pages 多文章个人博客。

## 结构

1. `index.md`：博客首页，自动展示文章列表。
2. `_posts/`：文章目录，每篇文章一个 Markdown 文件。
3. `_config.yml`：GitHub Pages / Jekyll 基础配置。
4. `_includes/head-custom.html`：站点图标配置。
5. `.github/workflows/pages.yml`：推送到 `main` 后自动部署。

## 使用方式

1. 在 `_posts` 新建文章，文件名格式：`YYYY-MM-DD-文章名.md`
2. 按 Jekyll front matter 写文章头信息。
3. 提交并推送到 `main`。
4. 等待 GitHub Actions 部署完成。

## 图标

站点 favicon 已同步自 `www.zfensi.com`。

## 注意

如果你要使用根域名 `https://zfensi.github.io`，GitHub 仓库名必须叫 `zfensi.github.io`。
