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
Kayla Traxler - <b>Long Paths in Polynomial Divisor Graphs</b> - Presented at <a href="https://ymc.osu.edu/about">YMC 2024</a> - <a href="https://ymc.osu.edu/sites/default/files/2024-08/YMC_2024-2.pdf">Abstract of Talk</a>, <a href="{{ "/_data/documents/long_paths_YMC2024_presentation.pdf" | relative_url }}">Slides</a> </li>

<li class="pub"> Jonathan Parlett, Abhishek Jeyapratap - <b>Subnet Communicability: Diffusive Communication Across the Brain Through a Backbone Subnetwork</b> - Poster presented at Drexel's <a href="https://drexel.edu/pennoni/news-events/events/week-undergraduate-excellence/">week of undergraduate exellence</a> - <a href="https://youtu.be/yaOKOUFLI0o
" >Video</a> </li>

<li class="pub"> Jonathan Parlett, Abhishek Jeyapratap - <b>Subnet Communicability: Diffusive Communication Across the Brain Through a Backbone Subnetwork</b> - Presented at <a href="http://cmic.cs.ucl.ac.uk/cdmri23/">CDMRI 2023</a> - <a href="{{ "/_data/documents/subnetCommunicability_CDMRI2023.pdf" | relative_url }}" >Slides</a> </li>

</ul>



