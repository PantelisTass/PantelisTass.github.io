---
layout: archive
title: "Notes"
permalink: /classes/
author_profile: true
---

{% include base_path %}

<h1>Part III Cambridge maths courses 2023-2024</h1>
<ul>
<li><a href = "/files/Part_III_Functional_Analysis_Michaelmas_2023.pdf">Functional Analysis</a></li>
<li><a href = "/files/Part_III_Advanced_Probability_Michaelmas_2023.pdf">Advanced probability</a></li>
<li><a href = "/files/Elliptic%20PDEs.pdf">Elliptic PDEs</a></li>
<li><a href = "/files/Stochastic%20Calculus%20handrwitten%20notes.pdf">Stochastic Calculus</a></li>
<li><a href = "/files/Analysis of PDE.pdf">Analysis of PDE</a></li>
<li><a href = "/files/Distribution%20Theory.pdf">Distribution Theory</a></li>
<li><a href = "/files/Concentration%20Inequalities.pdf">Concentration Inequalities</a></li>
</ul>

<h1>Imperial maths undergraduate courses 2020-2023</h1>
{% for post in site.classes reversed %}
  {% if post.type == "Imperial" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h1>Miscellaneous</h1>
<ul>
<li><a href = "/files/Random_Matrix_Theory_Lecture_Reading_Group_Cam_2024.pdf">Random matrix theory notes</a></li>
</ul>

