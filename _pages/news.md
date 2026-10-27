---
layout: page
permalink: /news/
title: News
description:
nav: false # 상단 메뉴에는 넣지 않고, 홈의 "All news" 에서만 들어갑니다
nav_order: 5
---

{% include sc-custom.liquid %}

<style>
  .sc-newslist article { padding: 24px 0; border-bottom: 1px solid rgba(128, 128, 128, 0.22); }
  .sc-newslist article:first-of-type { border-top: 1px solid rgba(128, 128, 128, 0.22); }
  .sc-newslist time {
    display: block;
    margin-bottom: 7px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    opacity: 0.65;
  }
  .sc-newslist img { max-width: 440px; }

  /* ── 사진 여러 장: 좌우로 넘기는 띠 ───────────────────────────── */
  .sc-gal {
    display: flex;
    gap: 10px;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    padding-bottom: 8px;
    margin: 0.7rem 0 0.2rem;
    scrollbar-width: thin;
  }
  .sc-gal img {
    flex: 0 0 auto;
    width: 440px;
    max-width: 86%;
    height: auto;
    border-radius: 6px;
    scroll-snap-align: start;
    margin: 0;
  }
  .sc-gal__hint { font-size: 12px; opacity: 0.55; margin: 2px 0 0; }
</style>

<div class="sc-newslist">
{% assign all = site.news | sort: "date" | reverse %}
{% assign pinned = all | where: "pin", true %}
{% assign rest = all | where_exp: "i", "i.pin != true" %}

{% for item in pinned %}

  <article>
    <time datetime="{{ item.date | date_to_xmlschema }}">{{ item.date | date: "%b %Y" }}</time>
    {{ item.content }}
  </article>
{% endfor %}

{% for item in rest %}

  <article>
    <time datetime="{{ item.date | date_to_xmlschema }}">{{ item.date | date: "%b %Y" }}</time>
    {{ item.content }}
  </article>
{% endfor %}
</div>
