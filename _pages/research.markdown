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
    <li class="pub"> Jay Calkins, Nicole Froitzheim, Jonathan Parlett,
Kayla Traxler - <b>Long Paths in Polynomial Divisor Graphs</b> - <a href="https://ymc.osu.edu/sites/default/files/2024-08/YMC_2024-2.pdf">Abstract of Talk</a>, <a href="{{ "/_data/documents/long_paths_YMC2024_presentation.pdf" | relative_url }}">Slides</a> </li>

{% for pres in site.data.presentations%}
    <li class="pub"> Jonathan Parlett - <b>{{ pres.name }}</b> - <a href="{{ pres.link}}">{{ pres.link }}</a> </li>
{% endfor %}
</ul>



