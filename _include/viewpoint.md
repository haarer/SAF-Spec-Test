**{{vp.VP_ID}}** {{vp.Name}}

|**Domain**|**Aspect**|**Maturity**|
| --- | --- | --- |
|[{{vp.Domain}}](../domains.md#common-domain)|[{{vp.Aspect}}](../aspects.md#taxonomy--structure-aspect)|![{{vp.Maturity}}](/diagrams/Symbol_confirmed.png )[released](../maturity.md#released)|

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
