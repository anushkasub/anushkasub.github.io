---
layout: default
title: CV
permalink: /cv/
published: false
---

{% assign cv_file = site.static_files | where: "path", site.cv_pdf | first %}
{% if cv_file %}
<p><a class="btn btn-primary" href="{{ site.cv_pdf | relative_url }}"><i class="fa-solid fa-file-pdf" aria-hidden="true"></i> Download CV (PDF)</a></p>
{% endif %}
