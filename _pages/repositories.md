---
layout: page
permalink: /repositories/
title: Repos
description: star了那些项目，列一列
nav: true
nav_order: 2
---

## 本渣的 Github 账户

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>
{% endif %}

---

## 本渣最近在关注的 repos

{% if site.data.repositories.github_repos_blog %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos_blog %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## 本渣在用/将用的 PT 相关 repos

{% if site.data.repositories.github_repos_pt %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos_pt %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

## 奇奇怪怪的 repos

{% if site.data.repositories.github_repos_nazo %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos_nazo %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}