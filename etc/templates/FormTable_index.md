{% import 'util.md' as util %}
{% set forms = [] %}
{% for f in ctx %}
{% if f.parameter.id == parameterReference %}
{% set form_string = f.language.name %}
{% set form_string =form_string+" _"+f.cldf.form+"_" %}
{% set forms = forms.append(form_string)%}
{% endif %}
{% endfor %}
{{ ", ".join(forms) }}.
