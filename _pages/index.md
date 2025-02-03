---
layout: page
title: Home
id: home
permalink: /
---

## about

hey. my name is joe, and I'm currently a software engineer in boston. ([linkedin](https://www.linkedin.com/in/joe-konno/) [github](https://github.com/MechaJoe))

my other interests include electronic music, [reading](https://www.goodreads.com/user/show/110022557-joe-konno), skiing, and amateur
distance running

## writing

<ul>
  {% for note in site.notes | sort: "last_modified_at_timestamp" | reverse %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<strong>recently updated posts</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 2 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
