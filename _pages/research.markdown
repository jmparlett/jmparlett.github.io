---
layout: default
permalink: /research
id: research
---

# Publications
<ul>
{% for pub in site.data.publications%}
    <li class="pub">{{pub.authors}} - <b>{{ pub.name }}</b> - <a href="{{ pub.link}}">{{ pub.link }}</a> </li>
{% endfor %}
</ul>

# Presentations
<ul>
{% for pres in site.data.presentations%}
    <li class="pub"> {{ pres.name }} - <a href="{{ pres.link}}">{{ pres.link }}</a> </li>
{% endfor %}
</ul>



