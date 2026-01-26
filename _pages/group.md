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


<br/>
<br/>
<hr class="segmentation-line">

<!-- Members Section -->
<div class="mb-4">
  <h3 class="fw-bold mb-3">Members</h3>
  <div class="row g-4">
    {% for user in people.members %}
      <div class="col-md-3 col-sm-6">
            {% include person.liquid user=user %}
      </div>
    {% endfor %}
  </div>
</div>


<br/>
<br/>
<hr class="segmentation-line">

<!-- Alumni Section -->
<div class="mb-4">
  <h3 class="fw-bold mb-3">Alumni</h3>
  <ul class="list-unstyled">
    {% for user in people.alumni %}
      <li class="mb-1">
        <b>{{ user.name }}</b>, {{ user.role }}. First Employment: {{ user.employment }}.
      </li>
    {% endfor %}
  </ul>
</div>
