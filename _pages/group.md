---
layout: page
title: Group
permalink: /group/
description: 
nav: false
nav_order: 6
---

{% assign people = site.data.people%}

<h3>Principle Investigator</h3>
<div class="d-flex flex-wrap justify-content-start align-items-start">
{% for user in people.PI %}
    {% include person.liquid user=user %}
{% endfor %}
</div>



---
<h3>Ph.D. students</h3>
<div class="d-flex flex-wrap justify-content-start align-items-start">
{% for user in people.PhD %}
    {% include person.liquid user=user %}
{% endfor %}
</div>

---
<h3>Master students</h3>
<div class="d-flex flex-wrap justify-content-start align-items-start">
{% for user in people.Master %}
    {% include person.liquid user=user %}
{% endfor %}
</div>

---
<h3>Alumni</h3>
<ul>
{% for user in people.Alumni %}
    <li>{{ user.name }}. {{user.role}}, {{user.employment}}</li>
{% endfor %}
</ul>
