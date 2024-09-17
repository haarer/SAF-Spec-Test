---
title: Stereotypes
parent: "User Documentation"
layout: default
nav_order: 60
---
# SAF User Documentation : Stereotypes
{% assign stereotypes = site.data.stereotypes | sort: "Name" %}
{% for element in stereotypes %}
<A id={{ element.ID }}></A>
## {{ element.Name }} 
{{ element.Documentation }}
{% endfor %}
