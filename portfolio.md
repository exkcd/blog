---
layout: page
---

{% for image in site.static_files %}
{% if image.path contains 'gallery' %}
<img src="{{ site.baseurl }}{{ image.path }}" alt="image">
{% endif %}
{% endfor %}