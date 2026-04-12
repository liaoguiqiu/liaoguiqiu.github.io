---
layout: page
permalink: /repositories/
title: Repositories
description: Selected GitHub repositories.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub user

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

{% endif %}

{% if site.data.repositories.github_repos %}

---

## Pinned repositories

<ul>
  {% for repo in site.data.repositories.github_repos %}
    <li><a href="https://github.com/{{ repo }}">{{ repo }}</a></li>
  {% endfor %}
</ul>
{% endif %}
