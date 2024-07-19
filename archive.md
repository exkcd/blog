---
layout: page
---

{% for post in site.posts %}
{% capture currentyear %}{{ post.date | date: "%Y" }}{% endcapture %}
{% if currentyear != year %}
{% unless forloop.first %}

{% endunless %}

<h2>{{ currentyear }}</h2>
{% capture year %}{{ currentyear }}{% endcapture %}
{% endif %}
<ul class="archive">
    <div class="archive-item"><a href="{{ post.url }}">{{ post.title }}</a> 
        <div class="archive-spacer"></div>
        <time class="archive-date">{{ post.date | date: "%B %-d, %Y" }}</time>
    </div>
</ul>
{% endfor %}
