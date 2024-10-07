---
title: Aspects
parent: "Framework Structure"
layout: default
nav_order: 5
---
# Aspects
{% for element in site.data.aspects %}
## {{ element.Name }} Aspect
{{ element.Documentation }}
{% endfor %}
