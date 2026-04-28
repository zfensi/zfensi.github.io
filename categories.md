---
layout: default
title: 分类
permalink: /categories/
description: 按分类浏览 zfensi 博客文章。
---

<nav class="breadcrumbs" aria-label="面包屑">
  <a href="{{ '/' | relative_url }}">首页</a>
  <span>/</span>
  <span>分类</span>
</nav>

# 分类页

<p class="page-intro">按主题聚合文章，方便做内链、做专题，也更利于搜索引擎理解站点结构。</p>

{% if site.categories.size > 0 %}
<section class="taxonomy-links">
  {% for category in site.categories %}
    <a class="tag-chip" href="#{{ category[0] | slugify }}">{{ category[0] }} ({{ category[1].size }})</a>
  {% endfor %}
</section>

{% for category in site.categories %}
<section class="page-block" id="{{ category[0] | slugify }}">
  <h2>{{ category[0] }}</h2>
  <div class="post-listing">
    {% for post in category[1] %}
      {% include post-card.html post=post %}
    {% endfor %}
  </div>
</section>
{% endfor %}
{% else %}
<p>当前还没有分类内容。</p>
{% endif %}
