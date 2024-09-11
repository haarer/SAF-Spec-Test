---
title: Logical Domain
parent: "User Documentation"
layout: default
has_children: true
nav_order: 40
---
## Logical Domain
{% assign dom = site.data.domains | where: "Name","Logical" %}
{{ dom.first.Documentation }}
