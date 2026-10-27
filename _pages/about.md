---
layout: about
title: Home
permalink: /
subtitle:

selected_papers: false
social: true # 하단 소셜 아이콘

announcements:
  enabled: false # 홈의 News는 아래 블록에서 직접 고릅니다
  scrollable: false
  limit:

latest_posts:
  enabled: false
  scrollable: false
  limit:
---

<style>
  /* al-folio 가 about 페이지 맨 위에 자동으로 넣는 이름/부제를 숨깁니다.
     (히어로에 이미 이름이 있어서 중복됨) */
  .post-header, .post-title, h1.post-title, .post .post-header, p.desc { display: none !important; }

  /* ---- 홈 전용 스타일 ---------------------------------------------- */
  .sc-full { width: 100vw; margin-left: calc(50% - 50vw); }
  .sc-wrap { max-width: 1180px; margin: 0 auto; padding: 0 40px; }
  .sc-home img { display: block; }
  .sc-home a { text-decoration: none; }

  /* 히어로 */
  .sc-hero { position: relative; min-height: 440px; display: flex; align-items: center; overflow: hidden; background: #0b222c; }
  .sc-hero__img { position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover; }
  .sc-hero__veil { position: absolute; inset: 0; background: linear-gradient(100deg, rgba(8,34,44,.88) 0%, rgba(8,34,44,.64) 46%, rgba(8,34,44,.24) 100%); }
  .sc-hero__in { position: relative; width: 100%; max-width: 1180px; margin: 0 auto; padding: 68px 40px; }
  .sc-eyebrow { margin: 0 0 16px; font-size: 12px; letter-spacing: .18em; text-transform: uppercase; color: #8ED6EA; font-weight: 700; }
  .sc-hero h1 { margin: 0; font-size: 52px; line-height: 1.06; letter-spacing: -.03em; font-weight: 800; color: #fff; max-width: 15ch; }
  .sc-hero p { margin: 20px 0 0; font-size: 18px; line-height: 1.65; color: #DCE7EB; max-width: 48ch; }
  .sc-cta { display: inline-flex; align-items: center; gap: 9px; margin-top: 26px; font-size: 16px; font-weight: 650; color: #fff; border-bottom: 2px solid #8ED6EA; padding-bottom: 4px; }
  .sc-cta svg { width: 15px; height: 15px; }

  /* 뉴스 */
  .sc-news { background: #17191A; padding: 54px 0 62px; }
  .sc-news__head { display: flex; flex-wrap: wrap; gap: 14px; align-items: baseline; margin-bottom: 24px; }
  .sc-news__head h2 { margin: 0; font-size: 28px; letter-spacing: -.02em; font-weight: 750; color: #F2F4F5; }
  .sc-more { margin-left: auto; display: inline-flex; align-items: center; gap: 7px; font-size: 15px; font-weight: 650; color: #7FD0E8; }
  .sc-more svg { width: 13px; height: 13px; }
  .sc-grid { display: grid; grid-template-columns: minmax(0,1.08fr) minmax(0,1fr); gap: 20px; }
  .sc-feat { background: #202325; display: flex; flex-direction: column; }
  .sc-feat img { width: 100%; aspect-ratio: 16/10; object-fit: cover; }
  .sc-feat__b { padding: 22px 24px 26px; }
  .sc-kicker { font-size: 12px; font-weight: 700; letter-spacing: .1em; text-transform: uppercase; color: #7FD0E8; }
  .sc-feat h3 { margin: 10px 0 0; font-size: 24px; line-height: 1.26; letter-spacing: -.016em; font-weight: 700; color: #F2F4F5; }
  .sc-meta { margin: 9px 0 0; font-size: 13px; color: #A9B2B7; }
  .sc-ex { margin: 12px 0 0; font-size: 15px; line-height: 1.66; color: #C6CED2; }
  .sc-side { display: grid; grid-template-rows: repeat(3, minmax(0,1fr)); gap: 20px; }
  .sc-card { background: #202325; display: grid; grid-template-columns: 160px minmax(0,1fr); }
  .sc-card img { width: 100%; height: 100%; object-fit: cover; }
  .sc-card__b { padding: 15px 18px; display: flex; flex-direction: column; justify-content: center; }
  .sc-card h3 { margin: 6px 0 0; font-size: 16px; line-height: 1.38; font-weight: 650; color: #F2F4F5; }

  @media (max-width: 860px) {
    .sc-hero h1 { font-size: 36px; }
    .sc-grid { grid-template-columns: minmax(0,1fr); }
    .sc-side { grid-template-rows: none; }
    .sc-card { grid-template-columns: 116px minmax(0,1fr); }
    .sc-hero__in, .sc-wrap { padding-left: 16px; padding-right: 16px; }
  }
</style>

<div class="sc-home">

<!-- ================= 히어로 =================
     사진 바꾸기 : 아래 img 의 파일명만 교체 (assets/img/news/ 안에 있어야 함)
     문구 바꾸기 : h1 과 바로 아래 p
============================================== -->
<section class="sc-full sc-hero">
  <img class="sc-hero__img" src="{{ '/assets/img/news/banner-wave.jpg' | relative_url }}" alt="">
  <span class="sc-hero__veil"></span>
  <div class="sc-hero__in">
    <p class="sc-eyebrow">Eawag · Environmental Chemistry</p>
    <h1>Shinhyeong Choe</h1>
    <p>I study how polymers biodegrade in the environment — and I want that to be a quantitative question, not a pass/fail one.</p>
    <a class="sc-cta" href="{{ '/introduction/' | relative_url }}">More about my work
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.6" aria-hidden="true"><path d="M5 12h13M13 6l6 6-6 6"/></svg></a>
  </div>
</section>

<!-- ================= 뉴스 =================
     큰 기사 1개 (.sc-feat) + 작은 카드 3개 (.sc-card)
     새 소식이 생기면 : 큰 기사를 새것으로 바꾸고, 기존 큰 기사를 작은 카드 맨 위로 내리고,
                      맨 아래 작은 카드 하나를 지우면 됩니다.
     전체 목록은 _news/ 폴더에 그대로 쌓이고 /news/ 페이지에 자동으로 나옵니다.
========================================== -->
<section class="sc-full sc-news">
  <div class="sc-wrap">
    <div class="sc-news__head">
      <h2>News</h2>
      <a class="sc-more" href="{{ '/news/' | relative_url }}">All news
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.8" aria-hidden="true"><path d="M9 5l7 7-7 7"/></svg></a>
    </div>

    <div class="sc-grid">

      <!-- ===== 큰 기사 ===== -->
      <article class="sc-feat">
        <img src="{{ '/assets/img/news/2026-10-nature-communications.jpg' | relative_url }}" alt="Same biodegradable label, different fates">
        <div class="sc-feat__b">
          <span class="sc-kicker">Publication</span>
          <h3>Divergent anaerobic fates of biodegradable plastics in landfill leachate</h3>
          <p class="sc-meta">20 October 2026 · Nature Communications</p>
          <p class="sc-ex">PHB mineralised almost completely in 17 days; PBAT barely moved in 320. Same label, three very different fates — with Prof. Changsoo Lee's group at UNIST.</p>
        </div>
      </article>

      <!-- ===== 작은 카드 3개 ===== -->
      <div class="sc-side">

        <article class="sc-card">
          <img src="{{ '/assets/img/news/2026-10-setac-brussels.jpg' | relative_url }}" alt="ICCS and SETAC Europe expert workshop in Brussels">
          <div class="sc-card__b">
            <span class="sc-kicker">Workshop</span>
            <h3>ICCS and SETAC Europe expert workshop, Brussels</h3>
            <p class="sc-meta">October 2026</p>
          </div>
        </article>

        <article class="sc-card">
          <img src="{{ '/assets/img/news/2026-09-chem-circularity.jpg' | relative_url }}" alt="Hierarchical endpoints for biodegradability claims">
          <div class="sc-card__b">
            <span class="sc-kicker">Commentary</span>
            <h3>Making biodegradability a defensible claim for circularity</h3>
            <p class="sc-meta">September 2026 · Chem Circularity</p>
          </div>
        </article>

        <article class="sc-card">
          <img src="{{ '/assets/img/news/2026-08-eawag.jpg' | relative_url }}" alt="Eawag in Dübendorf">
          <div class="sc-card__b">
            <span class="sc-kicker">Moving</span>
            <h3>Started as a postdoctoral scientist at Eawag</h3>
            <p class="sc-meta">August 2026 · Dübendorf, Switzerland</p>
          </div>
        </article>

      </div>
    </div>

  </div>
</section>

</div>

I am a postdoctoral scientist in the Department of Environmental Chemistry at Eawag, the Swiss Federal Institute of Aquatic Science and Technology. My work is on the biodegradation of water-soluble polymers and biodegradable plastics — how fast they break down, under what conditions, and which organisms are doing the work.

I am a Hyundai CMK Science &amp; Technology Fellow and a 2026 ACS CAS Future Leader.
