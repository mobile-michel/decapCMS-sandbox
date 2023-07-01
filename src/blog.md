---
title: Blog
layout: base
tags: primary
pagination:
    data: collections.blog
    size: 3
    alias: items
---
{%- for post in items reversed %}
- [{{ post.data.title }}]({{ post.url }})
{%- endfor %}