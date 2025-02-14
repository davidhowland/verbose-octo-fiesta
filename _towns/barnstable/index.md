---
title: Trail Running in Barnstable, MA
layout: collection
permalink: /barnstable/
nav_order: 1
has_toc: false
lat: -70.3716
lng: 41.6725
zoom: 11
---

{% assign trailheads = site.towns | where: "layout","trailhead" | where: "town", page.permalink %}
{% for trailhead in trailheads %}
{{ trailhead.title }}
{% endfor %}