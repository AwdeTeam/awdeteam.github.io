# {{ include.name }}

{% assign page.title = include.name %}

{{ include.description }}

{% assign stepslist = include.steps | newline_to_br | split: '<br />' %}
{% for step in stepslist %}
    {% if forloop.first == false and forloop.last == false %}
  1. {{ step }}
    {% endif %}
{% endfor %}
