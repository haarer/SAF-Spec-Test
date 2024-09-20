---
title: Stereotypes
parent: "User Documentation"
layout: default
nav_order: 60
---
# SAF User Documentation : Stereotypes
## Stereotypes of the SAF Profile
{% assign stereotypes = site.data.stereotypes | sort: "Name" %}
{% for element in stereotypes %}
{% assign realizations = site.data.realizeconcept | where: "RealizationOfConcept.ID", element.ID %}
<A id={{ element.ID }}></A>
### {{ element.Name }} 
{{ element.Documentation }}

{: .todo }
just testing, remove later
{% for real in realizations %}
 * realizes [{{ real.RealizedConcept.Name }}](../devdoc/concepts.html#{{ real.ID }})
{% endfor %}
{% endfor %}

## Stereotypes of the SCM Profile
{: .todo }
report dev stereotypes here

{% assign scmstereotypes = site.data.scmstereotypes | sort: "Name" %}
{% for element in scmstereotypes %}
<A id={{ element.ID }}></A>
### {{ element.Name }} 
{{ element.Documentation }}
{% endfor %}

## SCM defined Patterns
{: .todo }
patterns like attribute_of, type_of, contained_in

## Used SysML Stereotypes
{: .todo }
report used SysML and UML objects

