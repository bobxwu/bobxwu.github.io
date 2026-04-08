---
layout: page
title: Group
permalink: /group/
description: 
nav: false
nav_order: 6
---

{% assign people = site.data.people%}


{% include recruitment.liquid %}


<hr>

<!-- Members Section -->
{% include person.liquid members=people.members %}



<!-- Alumni Section -->
{% if people.alumni and people.alumni.size > 0 %}
<hr>
<div class="mb-5">
  <h3 class="h4 fw-semibold mb-3">Alumni</h3>
  <ul class="mb-3">
    {% for user in people.alumni %}
      <li class="mb-1">
        <span class="fw-bold">{{ user.name }}</span>
        <span>{{ user.role }}</span>
        <span class="text-muted">{{ user.employment }}</span>
      </li>
    {% endfor %}
  </ul>
</div>
{% endif %}
