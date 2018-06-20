---
layout: archive
title: "Fiction"
permalink: /fiction/
author_profile: true
---

{% include base_path %}

{% for post in site.fiction reversed %}
  {% include archive-single.html %}
{% endfor %}
