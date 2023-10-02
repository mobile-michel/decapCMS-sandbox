---
title: Agenda
layout: base
tags: primary
---
{% for item in agenda2.items %}
    - {{ item.titre }}
{% endfor %}
