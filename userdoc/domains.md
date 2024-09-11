---
title: Domains
parent: "User Documentation"
layout: default
nav_order: 4
---
# Domains
Domains are the 'rows' in the SAF Grid. They implement the Stakeholder Perspective Concept from ISO 42010
{% for element in site.data.domains %}
## {{ element.Name }} Domain
{{ element.Documentation }}
{% endfor %}
