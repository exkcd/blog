---
layout: default
---

This following code snippet is a guide on how to properly enjoy this website

{% highlight python %}

have_high_expectations = False

if have_high_expectations:
    be_disappointed()
else:
    tolerate_this_human_being()

{% endhighlight %}

<br/>

{% for post in site.posts limit: 3%}
{% capture currentmonth %}{{ post.date | date: "%M" }}{% endcapture %}
{% if currentmonth != month %}
{% unless forloop.first %}

{% endunless %}

#### Recent posts

{% capture month %}{{ currentmonth }}{% endcapture %}
{% endif %}
<article class="page">
<ul>
    <li>
        <time>({{ post.date | date: "%B %-d, %Y" }})</time>
        <a href="{{ post.url }}"> {{ post.title }}</a>
    </li>
</ul>
</article>
{% endfor %}
