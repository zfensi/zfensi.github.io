---
layout: default
title: 标签
permalink: /tags/
description: 按标签浏览 zfensi 博客文章。
---

<nav class="breadcrumbs" aria-label="面包屑">
  <a href="{{ '/' | relative_url }}">首页</a>
  <span>/</span>
  <span>标签</span>
</nav>

# 标签页

<p class="page-intro">标签用于连接跨分类的主题词，比如 SEO、社交营销、Instagram 和内容增长。</p>

{% if site.tags.size > 0 %}
<section class="taxonomy-links">
  {% for tag in site.tags %}
    <a class="tag-chip" href="#{{ tag[0] | slugify }}">{{ tag[0] }} ({{ tag[1].size }})</a>
  {% endfor %}
</section>

{% for tag in site.tags %}
<section class="page-block" id="{{ tag[0] | slugify }}">
  <h2>{{ tag[0] }}</h2>
  <div class="post-listing">
    {% for post in tag[1] %}
      {% include post-card.html post=post %}
    {% endfor %}
  </div>
</section>
{% endfor %}
{% else %}
<p>当前还没有标签内容。</p>
{% endif %}
