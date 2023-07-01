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
<nav aria-label="breadcrumb">
{% if page.url != pagination.href.first %}<a href="{{ pagination.href.first }}">First page</a>{% else %}First page{% endif %} - {% if pagination.href.previous %}<a href="{{ pagination.href.previous }}">Previous</a>{% else %}Previous{% endif %} - This is page {{ pagination.pageNumber | plus: 1 }} - {% if pagination.href.next %}<a href="{{ pagination.href.next }}">Next</a>{% else %}Next{% endif %} - {% if page.url != pagination.href.last %}<a href="{{ pagination.href.last }}">Last page</a>{% else %}Last page{% endif %}
</nav>
