---
layout: page
permalink: /introduction/
title: Introduction
description:
nav: true
nav_order: 1
---

{% include sc-custom.liquid %}

<style>
  /* 줄간격 약 10% 넓힘 */
  .intro { line-height: 1.78; }
  .intro ul { line-height: 1.78; }
  .intro li { margin-bottom: 4px; }
  .intro h2 {
    margin: 36px 0 12px;
    font-size: 15px;
    font-weight: 700;
    letter-spacing: 0.08em;
    opacity: 0.6;
    border-bottom: 1px solid rgba(128, 128, 128, 0.28);
    padding-bottom: 6px;
  }

  /* 상단: 사진 + 소속 */
  .intro__top {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    align-items: flex-start;
    margin-bottom: 6px;
  }
  .intro__photo {
    flex: 0 0 190px;
    width: 190px;
    border-radius: 6px;
    display: block;
  }
  .intro__who {
    flex: 999 1 320px;
    min-width: 0;
  }
  .intro__name {
    font-size: 23px;
    font-weight: 700;
    letter-spacing: -0.015em;
    margin: 0 0 10px;
  }
  .intro__who p { margin: 0 0 4px; }
  .intro__badges { margin-top: 16px; }
  .intro__badges span {
    display: block;
    font-weight: 600;
  }
  @media (max-width: 560px) {
    .intro__photo { flex: 0 0 150px; width: 150px; }
  }
</style>

<div class="intro" markdown="0">

<div class="intro__top">
  <img class="intro__photo" src="{{ '/assets/img/prof_pic.jpg' | relative_url }}" alt="Shinhyeong Choe">
  <div class="intro__who">
    <div class="intro__name">Shinhyeong Choe</div>
    <p>Postdoctoral Researcher</p>
    <p>Department of Environmental Chemistry</p>
    <p>Eawag, Swiss Federal Institute of Aquatic Science and Technology</p>
    <div class="intro__badges">
      <span>Hyundai CMK Science &amp; Technology Fellow</span>
      <span>2026 ACS CAS Future Leader</span>
    </div>
  </div>
</div>

<h2>Research Interest</h2>
<ul>
  <li>Biodegradability and environmental fate of polymers across natural and engineered systems</li>
  <li>Polymer–microbiome interactions and data-driven prediction of material persistence</li>
  <li>Sustainable, bio-based, and environmentally safe polymer materials</li>
</ul>

<h2>Education</h2>
<ul>
  <li><strong>(Ph.D.)</strong> Civil and Environmental Engineering, KAIST, 2026 (Advisor: Prof. Jaewook Myung)</li>
  <li><strong>(M.S.)</strong> Civil and Environmental Engineering, KAIST, 2022 (Advisor: Prof. Jaewook Myung)</li>
  <li><strong>(B.S.)</strong> Environmental Engineering, Chungnam National University, 2017 (Advisor: Prof. Yongchul Jang)</li>
</ul>

<h2>Professional Experience</h2>
<ul>
  <li><strong>Postdoctoral Researcher</strong>, Eawag, Swiss Federal Institute of Aquatic Science and Technology, Aug. 2026–Present<br>(Advisors: Prof. Thomas Hofstetter, Prof. Kathrin Fenner, Prof. Michael Sander)</li>
  <li><strong>Postdoctoral Researcher</strong>, KAIST, Mar–Jul 2026 (Advisor: Prof. Jaewook Myung)</li>
  <li><strong>Visiting Ph.D. Researcher</strong>, University of Vienna, Austria, Nov–Dec 2025 (Advisor: Prof. Michael Zumstein)</li>
  <li><strong>Visiting Ph.D. Researcher</strong>, Woods Hole Oceanographic Institution, USA, Jan–Feb 2024 (Advisor: Dr. Collin Ward)</li>
  <li><strong>Visiting Ph.D. Researcher</strong>, Polytechnique Montréal, Canada, Sep–Dec 2022 (Advisor: Prof. Clara Santato)</li>
  <li><strong>Process Engineer</strong>, BKT Co., Ltd., Republic of Korea, Feb. 2018–May 2019</li>
  <li><strong>Intern</strong>, Secretariat of the BRS conventions, United Nations Environment, Geneva, Switzerland, Jan–Jul 2017</li>
</ul>

<h2>Honors &amp; Awards</h2>
<ul>
  <li>Hyundai Motor CMK Science &amp; Technology Fellow, 2026–2028</li>
  <li>CAS Future Leaders, American Chemical Society (ACS), 2026</li>
  <li>Graduate Student Award in Environmental Chemistry, American Chemical Society (ACS), 2025</li>
  <li>Best Poster Award, MEWE-11, International Water Association (IWA), 2025</li>
  <li>Global Leadership Award (Challenge), KAIST, 2025</li>
  <li>Outstanding Paper Award, KAIST, 2025</li>
  <li>Hyundai Motor Chung Mong-Koo Global Scholar, 2022–2025</li>
  <li>Talent Award of Korea, Ministry of Education, Republic of Korea, 2024</li>
  <li>Daejeon City Environment Award, Mayor of Daejeon, 2024</li>
  <li>Q-Day Special Award (Creative Talent), KAIST, 2024</li>
  <li>First Prize, KAIST Brain Korea 21 Overseas Visit Essay Contest, 2024</li>
  <li>Global Excellence Award, Hyundai Motor Chung Mong-Koo Foundation, 2024</li>
  <li>Global Leadership Award (Challenge), KAIST, 2023</li>
  <li>Excellent Presentation Award, Korean Society for Microbiology and Biotechnology, 2023</li>
  <li>S.M.A.R.T Leader Award, Dept. of Civil and Environmental Engineering, KAIST, 2022</li>
  <li>Globalink Research Award, Mitacs Canada, 2022</li>
  <li>Certificate of Merit, Division of Environmental Chemistry, American Chemical Society (ACS), 2021</li>
  <li>Best Paper Award, Korea Society for Waste Management, 2021</li>
</ul>

</div>
