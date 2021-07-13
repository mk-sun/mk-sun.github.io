---
layout: default

main: true
title: "Self Projects"
subtitle: "Sunwoo Self Projects"
description: "Self 프로젝트"

basic-header: true
header-img: "img/about.jpg"
---

<div class="catalogue">
{% assign sorted = site.pages | sort: 'order' | reverse %}

{% for page in sorted %}
    {% if page.self_project == true %}
        {% include body-post-list.html %}
    {% endif %}
{% endfor %}
</div>
