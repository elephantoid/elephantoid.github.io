---
layout: posts
pemalink: /learning/
title: "Learning Posts by Tags"
author_profile: true
header:
  image: "/_images/sarah-dokowicz-nAme0YH7hdU-unsplash.jpg"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in groud_names %}
{% assign posts = group_items[forloop.index0] %}

  <h2 id="{{ tag | slugify }} class="archive_subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
