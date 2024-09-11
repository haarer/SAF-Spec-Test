{% assign vp_tmp = site.data.viewpoints | where: "Name",page.title %}
{% assign vp = vp_tmp.first %}

**{{ vp.VP_ID }}** {{ vp.Name }}

|**Domain**|**Aspect**|**Maturity**|
| --- | --- | --- |
|[{{ vp.Domain }}](/userdoc/domains.html#{{ vp.Domain | downcase }}-domain)|[{{ vp.Aspect }}](../aspects.html#{{ vp.Aspect | downcase | replace: " ","-" | replace: "&",""}}-aspect)|![{{ vp.Maturity }}](/diagrams/Symbol_confirmed.png )[released](../maturity.html#released)|

## Example
![{{ vp.Example }}](../../diagrams/vp-examples/{{ vp.Example }})
## Purpose
{{vp.Purpose}}
## Applicability
{{vp.Applicability}}
## Presentation
{% for pres in vp.Presentations %}
{{ pres }}
{% endfor %}
## Stakeholder
## Concern
{% for concern in vp.Concerns %}
* [{{ concern.Body }}](../concerns.md#{{ concern.ID }})
{% endfor %}
## Profile Model Reference
The following Stereotypes / Model Elements are used in the Viewpoint:
{% for st in vp.UsedStereotypes %}
* [{{ st.Name }}](../stereotypes.md#{{ st.ID }})
{% endfor %}
## Input from other Viewpoints
### Required Viewpoints
### Recommended Viewpoints
