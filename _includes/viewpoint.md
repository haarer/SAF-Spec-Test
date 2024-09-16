{% assign vp_tmp = site.data.viewpoints | where: "Name", page.title %}
{% assign vp = vp_tmp.first %}
{% assign examples = site.data.mdexamples | where: "ExampleForVPID", vp.VP_ID %}
{% capture maturityimage -%}
<img src="{% link /assets/images/maturity-{{ vp.Maturity | replace: " ", "-"  }}.svg %}" height="20" width="20" >
{%- endcapture %}
{% capture domainlink -%}
[{{ vp.Domain }}](../domains.html#{{ vp.Domain | downcase }}-domain)
{%- endcapture %}
{% capture aspectlink -%}
[{{ vp.Aspect }}](../aspects.html#{{ vp.Aspect | downcase | replace: " ","-" | replace: "&",""}}-aspect)
{%- endcapture %}
{% capture maturitylink -%}
[{{ vp.Maturity }}](../maturity.html#{{ vp.Maturity }})
{%- endcapture %}
**{{ vp.VP_ID }}** {{ vp.Name }}

|**Domain**|**Aspect**|**Maturity**|
| --- | --- | --- |
|{{ domainlink }}|{{ aspectlink }}|{{ maturityimage }}{{ maturitylink }}|



## Example
{% for ex in examples %}
<img src="../../diagrams/examples_md/exa{{ ex.ID }}.svg" />
{% endfor %}

## Purpose
{{ vp.Purpose }}
## Applicability
{{ vp.Applicability }}
## Presentation
{% for pres in vp.Presentation %}
{{ pres }}
{% endfor %}
## Stakeholder
{% for stk_id in vp.Stakeholders %}
{% assign stk = site.data.stakeholders | where: "ID", stk_id %}
* [{{ stk.first.Name }}](../stakeholders.html#{{ stk_id }} )
{% endfor %}
## Concern
{% for concern_id in vp.Concern %}
{% assign concern = site.data.concerns | where: "ID", concern_id %}
* [{{ concern.first.Name }}](../concerns.html#{{ concern_id }} )
{% endfor %}
## Profile Model Reference
The following Stereotypes / Model Elements are used in the Viewpoint:
{% for st in vp.UsedStereotypes %}
* [{{ st.Name }}](../stereotypes.md#{{ st.ID }})
{% endfor %}
## Input from other Viewpoints
### Required Viewpoints
### Recommended Viewpoints
