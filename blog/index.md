---
layout: default

main: true
title: "Blog"
subtitle : "SunWoo Blog"
description: "관심 분야의 글을 올려요."

basic-header: true
header-img: img/about.jpg
---
<div class="catalogue">
<ul class="catalogue">
{% assign sorted = site.pages | sort: 'order' | reverse %}
{% for page in sorted %}
    {% if page.blog == true %}
        {% include body-post-list.html %}
    {% endif %}
{% endfor %}
</ul>
</div>
