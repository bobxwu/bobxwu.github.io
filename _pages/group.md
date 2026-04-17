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
{% assign members = include.members | default: site.data.people.members %}
{% assign grouped_members = members | group_by: 'role' %}

<div class="mb-5">
  {% for role_group in grouped_members %}
    <div class="mb-4">
      <h3 class="h4 fw-semibold mb-3">{{ role_group.name }}</h3>
      <ul class="mb-3">
        {% for user in role_group.items %}
          <li class="mb-1">
            {% if user.homepage %}
              <a href="{{ user.homepage }}" target="_blank" rel="noopener" class="fw-bold fs-6">{{ user.name }}</a>
            {% elsif user.email %}
              <a href="mailto:{{ user.email }}" class="fw-bold fs-6">{{ user.name }}</a>
            {% else %}
              <span class="fw-bold fs-6">{{ user.name }}</span>
            {% endif %}
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>


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
