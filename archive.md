---
layout: default
title: 归档
permalink: /archive/
description: 按时间查看 zfensi 个人博客的全部文章归档。
---

# 文章归档

<p class="page-intro">这里按时间倒序展示全部已发布文章，方便搜索引擎抓取和读者快速回看。</p>

{% if site.posts.size > 0 %}
<section class="archive-list">
{% for post in site.posts %}
  <article>
    <p class="archive-list__meta">{{ post.date | date: "%Y-%m-%d" }}</p>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
    {% if post.description %}
    <p>{{ post.description }}</p>
    {% elsif post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
    {% endif %}
  </article>
{% endfor %}
</section>
{% else %}
<p>当前还没有已发布文章。</p>
{% endif %}
