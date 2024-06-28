---
layout: page
title: About
---

```
{% for trait in site.data.about %}
  Name: {{ trait.name }}

  Age: {{ trait.age }}
  
  Height: {{ trait.height }}
  
  Weight: {{ trait.weight }}

  Gender: {{ trait.gender }}
  
  Sex: {{ trait.sex }}
{% endfor %}
```