---
layout: country
title: Brasil
group: navigation-06
header-img: BILD_BRASILIEN-10.jpg
bodyclass: brasilien
order: 7
surface: 8'515'770
population: 207'652'865
gdp: 8'650
altitude: 1172
lang: pt
ref: brasilien
---
{% assign brasilien = site.brasilien | where: 'lang', page.lang | sort: "order" %}
{% for ch in brasilien %}
<section class="box chapter-{{ ch.subject }}" id="{{ ch.subject }}">
    {% if ch.chapter_image %}
        <div class="image grid" style="background-image: url({{ ch.chapter_image | prepend: '/media/img/chapter/' | prepend: site.baseurl }});">
        </div>
    {% endif %}
    <div class="content">
        <span class="chapter-subject">{{ ch.subject }}</span>
        <h1 class="chapter-title">{{ ch.title }}</h1>
    </div>
    {{ ch.content }}
</section>
{% endfor %}
