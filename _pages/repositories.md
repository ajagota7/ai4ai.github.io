---
layout: page
permalink: /repositories/
title: repositories
description: Research code and open-source projects from the AI4AI Lab at Imperial College London.
nav: true
nav_order: 4
---

## AI4AI Lab Organization

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center" style="margin-bottom: 2rem;">
  <div style="display: flex; align-items: center; padding: 1.5rem; border: 1px solid var(--global-divider-color); border-radius: 6px; width: 100%; max-width: 600px;">
    <a href="https://github.com/ai4ai-lab" target="_blank" style="display: flex; align-items: center; text-decoration: none; width: 100;">
      <img src="{{ '/assets/img/logo.png' | relative_url }}" alt="AI4AI Lab" style="width: 64px; height: 64px; border-radius: 6px; margin-right: 1rem;">
      <div>
        <h3 style="margin: 0; font-size: 1.25rem; color: var(--global-text-color);">ai4ai-lab</h3>
        <p style="margin: 0.25rem 0 0 0; color: var(--global-text-color-light);">AI for Actionable Impact Lab at Imperial College London</p>
      </div>
    </a>
  </div>
</div>

---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
