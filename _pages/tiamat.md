---
layout: tiamat
title: tiamat
permalink: /tiamat/
description: Relatos & fragmentos de/mentes de mi autoría.
nav: true
pagination:
  enabled: true
  collection: tiamat
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1 # The number of links before the current page
    after: 3  # The number of links after the current page
---

<div class="post">
    <ul class="post-list">
      {% for tiamat in paginator.tiamat %}
      <li>
        <h3><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ tiamat.title }}</a></h3>
        <p class="post-meta">{{ tiamat.date | date: '%B %-d, %Y' }}</p>
        <p>{{ tiamat.description }}</p>
      </li>
      {% endfor %}
    </ul>

    {% include pagination.html %}
</div>
