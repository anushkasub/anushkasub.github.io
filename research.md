---
layout: default
title: Research
permalink: /research/
---

My research interests lie at the intersection of computer architecture and systems, with a focus on hardware-software co-design to support emerging workloads. My experience includes:

- Memory-centric acceleration for graph processing
- Memory management and virtual memory for CPUs and heterogeneous systems
- CPU microarchitecture and hardware security

## Academic Publications

{% assign by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for group in by_year %}
<h3 class="pub-year">{{ group.name }}</h3>
{% for pub in group.items %}{% include publication.html pub=pub %}{% endfor %}
{% endfor %}
