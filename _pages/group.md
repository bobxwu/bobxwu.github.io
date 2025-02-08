---
layout: page
title: Group
permalink:
description: 
nav: false
nav_order: 6
---

{% assign people = site.data.people%}

<h2>Principle Investigator</h2>
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% for user in people.PI %}
    {% include person.liquid user=user %}
{% endfor %}
</div>

---
<br>
<br>

<h2>Ph.D.</h2>
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% for user in people.PhD %}
    {% include person.liquid user=user %}
{% endfor %}
</div>

---
<br>
<br>

<h2>Master</h2>
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% for user in people.Master %}
    {% include person.liquid user=user %}
{% endfor %}
</div>

---
<br>
<br>

{% include clustrmaps.liquid %}
