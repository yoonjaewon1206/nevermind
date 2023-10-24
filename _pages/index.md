---
layout: page
title: Home
id: home
permalink: /
---

# Hi !!

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  <span style="font-weight: bold">[[마인드맵 구경하기]]</span> 
</p>

 [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<strong>최근 업데이트</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
