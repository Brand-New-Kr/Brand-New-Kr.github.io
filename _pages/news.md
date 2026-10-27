---
layout: page
permalink: /news/
title: News
description: Talks, awards, papers and moves, newest first.
nav: false # 상단 메뉴에는 넣지 않고, 홈의 "All news" 에서만 들어갑니다
nav_order: 5
---

<style>
  .sc-newslist article { padding: 22px 0; border-bottom: 1px solid rgba(128,128,128,0.22); }
  .sc-newslist article:first-of-type { border-top: 1px solid rgba(128,128,128,0.22); }
  .sc-newslist time { display: block; margin-bottom: 7px; font-size: 13px; font-weight: 600; letter-spacing: 0.05em; text-transform: uppercase; opacity: 0.65; }
  .sc-newslist img { max-width: 440px; }
</style>

<div class="sc-newslist">
{% assign items = site.news | sort: "date" | reverse %}
{% for item in items %}
  <article>
    <time datetime="{{ item.date | date_to_xmlschema }}">{{ item.date | date: "%d %B %Y" }}</time>
    {{ item.content }}
  </article>
{% endfor %}
</div>
