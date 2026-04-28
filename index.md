---
layout: default
title: zfensi 个人博客
description: 中文个人博客首页，展示最新文章、写作方向和常用入口。
---

<section class="hero">
  <p class="hero__eyebrow">ZFENSI BLOG</p>
  <h1>zfensi 个人博客</h1>
  <p class="hero__lead">记录技术、运营、出海观察与个人思考。站点基于 GitHub Pages，内容以 Markdown 持续更新。</p>
  <p class="hero__actions">
    <a class="button-like" href="{{ '/archive/' | relative_url }}">查看归档</a>
    <a class="button-like button-like--ghost" href="{{ '/about/' | relative_url }}">关于本站</a>
    <a class="button-like button-like--ghost" href="{{ '/feed.xml' | relative_url }}">RSS</a>
  </p>
</section>

<section class="home-grid">
  <div class="card">
    <h2>写作方向</h2>
    <p>技术实践、独立站、SEO、内容运营，以及能沉淀长期价值的经验记录。</p>
  </div>
  <div class="card">
    <h2>更新方式</h2>
    <p>本地写 Markdown，提交到 GitHub 后自动构建部署，不依赖复杂后台。</p>
  </div>
  <div class="card">
    <h2>订阅入口</h2>
    <p>可以通过 <a href="{{ '/feed.xml' | relative_url }}">RSS</a> 跟踪更新，也可以从归档页快速回看历史文章。</p>
  </div>
</section>

<section class="section-header">
  <h2>最新文章</h2>
  <p>最近发布的内容会优先展示在这里。</p>
</section>

{% assign latest_posts = site.posts | slice: 0, 6 %}
{% if latest_posts.size > 0 %}
<section class="post-listing">
{% for post in latest_posts %}
  <article class="post-card">
    <p class="post-card__meta">{{ post.date | date: "%Y-%m-%d" }}</p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
    {% if post.description %}
    <p>{{ post.description }}</p>
    {% elsif post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    {% endif %}
  </article>
{% endfor %}
</section>
{% else %}
<p>还没有文章，先去写第 1 篇吧。</p>
{% endif %}

<section class="section-header">
  <h2>快速入口</h2>
  <p>
    <a href="{{ '/archive/' | relative_url }}">归档页</a> /
    <a href="{{ '/about/' | relative_url }}">关于页</a> /
    <a href="{{ '/robots.txt' | relative_url }}">robots.txt</a> /
    <a href="{{ '/sitemap.xml' | relative_url }}">sitemap.xml</a>
  </p>
</section>
