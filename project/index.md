---
layout: default

main: true
title: "Projects"
subtitle: "Sunwoo Projects"
description: "지금까지 작업한 프로젝트"

basic-header: true
header-img: "img/about.jpg"
---

<div class="catalogue">
{% assign sorted = site.pages | sort: 'order' | reverse %}

{% for page in sorted %}
    {% if page.projects == true %}
        {% include body-post-list.html %}
    {% endif %}
{% endfor %}
</div>
