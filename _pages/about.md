---
layout: about
title: About
display_name: Qiuyang Mang
native_name: 忙秋阳
permalink: /
subtitle: 

profile:
  align: right
  image: profile7.jpg
  second_image: cat.jpg
  second_image_caption: My cute cat &mdash; Peppa
  image_circular: false # crops the image to make it circular
  address: >
    <span class="profile-email">email: qmang AT berkeley.edu</span>


news: false  # includes a list of news items
# latest_posts: false  # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

<style>
/* Ensure body text uses Merriweather */
.post article p,
.post article li,
.post article div {
  font-family: 'Merriweather', Georgia, serif !important;
}

/* Keep content on the left side, never wrap under the right-aligned profile */
.post article .clearfix {
  max-width: calc(100% - 340px); /* Adjust based on your profile width */
  clear: none !important;
}

.post-title .native-name {
  font-family: "Songti SC", "STSong", SimSun, serif;
  font-weight: 450;
}

.profile .social {
  display: flex;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: center;
  gap: 0.45rem;
  font-size: 2.8rem;
}

.profile-flip-front .address {
  margin-top: 0.9rem;
}

.profile-flip-card {
  perspective: 1000px;
  cursor: pointer;
  outline: none;
}

.profile-flip-card:focus-visible {
  outline: 2px solid var(--global-theme-color);
  outline-offset: 4px;
  border-radius: 4px;
}

.profile-flip-card-inner {
  display: grid;
  transform-style: preserve-3d;
  transition: transform 0.55s cubic-bezier(0.22, 1, 0.36, 1);
}

.profile-flip-face {
  grid-area: 1 / 1;
  min-width: 0;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
}

.profile-flip-face figure {
  margin: 0;
}

.profile-flip-back {
  display: flex;
  flex-direction: column;
  justify-content: center;
  transform: rotateY(180deg);
}

.profile-flip-back .caption {
  margin-bottom: 0;
}

.profile-flip-card.is-flipped .profile-flip-card-inner {
  transform: rotateY(180deg);
}

@media (hover: hover) and (pointer: fine) {
  .profile-flip-card:hover .profile-flip-card-inner {
    transform: rotateY(180deg);
  }
}

@media (prefers-reduced-motion: reduce) {
  .profile-flip-card-inner {
    transition: none;
  }
}

.mentee-section {
  margin: 0.85rem 0 1.35rem;
  text-align: left;
  line-height: 1.5;
}

.mentee-entry {
  white-space: nowrap;
}

@media (max-width: 768px) {
  .post article .clearfix {
    max-width: 100%;
    clear: both !important;
  }
  
  /* Force profile images to stack above content on mobile */
  .profile {
    float: none !important;
    margin: 0 auto 2rem auto !important;
    text-align: center !important;
  }
  
  .profile img {
    margin: 0 auto !important;
  }
  
  /* Ensure content starts below images on mobile */
  .post article {
    clear: both;
  }
}

/* Paper link styling */
.paper-link {
  display: inline-block;
  padding: 0.15rem 0.5rem;
  margin-left: 0.3rem;
  background: rgba(138, 43, 226, 0.08);
  color: var(--global-theme-color) !important;
  text-decoration: none !important;
  border: 1px solid rgba(138, 43, 226, 0.25);
  border-radius: 3px;
  font-size: 0.75rem;
  font-weight: 500;
  transition: all 0.3s ease;
  vertical-align: middle;
}

.paper-link:hover {
  background: rgba(138, 43, 226, 0.15);
  border-color: rgba(138, 43, 226, 0.4);
  transform: translateY(-1px);
}

/* Reduce list indentation */
.post article ul {
  padding-left: 1.2rem;
}

.post article li {
  margin-bottom: 0.5rem;
}

/* Ensure bold text works in lists */
.post article li strong,
.post article li b {
  font-weight: 600 !important;
}

.about-featured-publications {
  clear: both;
  margin-top: 2.5rem;
  scroll-margin-top: 4.5rem;
}

.featured-publications-heading {
  display: flex;
  flex-wrap: wrap;
  align-items: baseline;
  gap: 0.25rem 1.2rem;
  margin-bottom: 1.05rem;
}

.about-featured-publications .featured-publications-heading h3 {
  font-size: 1.3rem;
  margin: 0;
}

.featured-paper-legend {
  display: flex;
  flex-wrap: wrap;
  gap: 0.25rem 1.1rem;
  color: var(--global-text-color-light);
  margin: 0;
}

.mentee-first-author {
  border-bottom: 1px dashed currentColor;
  padding-bottom: 1px;
}

.featured-paper-list {
  display: grid;
  gap: 1.35rem;
}

.featured-paper {
  display: grid;
  grid-template-columns: minmax(150px, 240px) minmax(0, 1fr);
  gap: 1rem;
  align-items: start;
  padding: 0.35rem 0;
}

.featured-paper-visual {
  display: block;
  line-height: 0;
}

.featured-paper-visual img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 4px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.11);
}

.featured-paper h4 {
  font-size: 1.2rem;
  line-height: 1.3;
  margin: 0 0 0.25rem;
  font-weight: 600;
}

.featured-paper h4 a {
  color: var(--global-text-color);
  text-decoration: none;
}

.featured-paper h4 a:hover {
  text-decoration: underline;
}

.featured-paper-meta {
  color: #003262;
  font-weight: 600;
  margin: 0 0 0.35rem;
}

.featured-paper-authors {
  color: var(--global-text-color);
  line-height: 1.45;
  margin: 0 0 0.25rem;
}

.featured-paper-authors strong {
  font-weight: 600;
}

.featured-paper-authors .more-authors {
  color: var(--global-theme-color);
  cursor: pointer;
  white-space: normal;
  overflow-wrap: anywhere;
}

.featured-paper-authors .more-authors:hover {
  color: var(--global-hover-color);
  text-decoration: underline;
}

.featured-paper-desc {
  line-height: 1.55;
  margin: 0.25rem 0 0.45rem;
}

.featured-paper-links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.35rem 0.65rem;
  font-weight: 600;
}

.featured-paper-links a {
  color: var(--global-text-color-light);
  text-decoration: underline;
}

.featured-paper-links a:hover {
  color: var(--global-text-color);
}

@media (min-width: 769px) {
  .about-featured-publications {
    width: calc(100% + 340px);
    max-width: none;
  }

  .featured-paper-visual {
    transform: translateX(-0.35rem);
  }

  .featured-paper {
    grid-template-columns: minmax(260px, 340px) minmax(0, 1fr);
    gap: 1.25rem;
    padding: 1rem 0;
  }
}

@media (max-width: 768px) {
  .featured-paper {
    grid-template-columns: 1fr;
    gap: 0.75rem;
  }
}

.post article a {
  text-decoration: underline;
  text-decoration-color: #722F37;
}
</style>


Hi, I’m Qiuyang Mang, a second-year CS PhD student in the [Sky Computing Lab](https://sky.cs.berkeley.edu/) at UC Berkeley, advised by [Prof. Alvin Cheung](https://people.eecs.berkeley.edu/~akcheung/).
I lead [FrontierCS](https://frontier-cs.org) and [FrontierSmith](https://arxiv.org/abs/2605.14445), a benchmark and data synthesis system for LLM-driven algorithm evolution on open-ended coding tasks. My research interests center on two themes:

- **Long-Horizon LLM Agents**: Understanding, developing, and improving LLM agents for complex, multi-step optimization across data synthesis, test-time scaling, post-training algorithms, and domain-specific applications. [Elo-per-token](https://agent-tts.github.io/agent-tts/), [FrontierCS](https://frontier-cs.org), [FrontierSmith](https://arxiv.org/abs/2605.14445), [Argus](https://arxiv.org/abs/2510.06663), [Combee](https://arxiv.org/abs/2604.04247), [SkyDiscover](https://github.com/skydiscover-ai/skydiscover)

- **Machine Learning Systems**: Efficient algorithms for ML workloads, from data-processing to inference scheduling. [SVG-EAR](https://arxiv.org/abs/2603.08982), [Continuum](https://arxiv.org/abs/2511.02230), [PLOP](https://arxiv.org/abs/2604.09944)

Prior to joining Berkeley, I received my B.E. from [The Chinese University of Hong Kong, Shenzhen](https://www.cuhk.edu.cn/), where I was advised by [Prof. Pinjia He](https://pinjiahe.github.io/). I also spent an unforgettable year as a research assistant at the [National University of Singapore](https://nus-test.github.io/) with [Prof. Manuel Rigger](https://www.manuelrigger.at/). I was in the 46th ICPC World Finalist 🎈 and served as [problem setters](https://qoj.ac/user/profile/Joyemang) for regionals.

<p class="mentee-section"><strong>Mentees:</strong> <span class="mentee-entry"><a href="https://runyuanhe.github.io/" target="_blank">Runyuan He</a></span>, <span class="mentee-entry"><a href="https://kaiyuanliu04.github.io/" target="_blank">Kaiyuan Liu</a></span>, <span class="mentee-entry">Xuanyi Zhou</span></p>

<div class="about-featured-publications" markdown="1">

<div class="featured-publications-heading">
  <h3>Selected Publications</h3>
  <p class="featured-paper-legend"><span>* Equal contribution</span><span class="mentee-first-author">Mentee first author</span></p>
</div>

<div class="featured-paper-list">
  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://agent-tts.github.io/agent-tts/" aria-label="Elo-per-token project webpage">
      <img src="/assets/img/featured-publications/elo-per-token-teaser.png" alt="Elo-per-token agent and human scaling results">
    </a>
    <div>
      <h4><a href="https://agent-tts.github.io/agent-tts/">When Agents Slow Down: Understanding LLM Agents' Test-Time Strategies via Elo-per-token Analysis</a></h4>
      <p class="featured-paper-authors"><span class="mentee-first-author">Kaiyuan Liu</span>*, <strong>Qiuyang Mang*</strong>, Bo Peng, Wenhao Chai, Hanchen Li, Shreyas Pimpalgaonkar, Luke Zettlemoyer, Alex Dimakis, Alvin Cheung</p>
      <p class="featured-paper-meta">Preprint 2026</p>
      <p class="featured-paper-desc">An analysis of how agents convert test-time tokens into progress, revealing where their gains fall below independent sampling while expert humans continue improving.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2609.15309">paper</a>
        <a href="https://github.com/agent-tts/Agent-TTS-Code">code</a>
        <a href="https://joyemang33.github.io/blog/2026/humans-dont-just-sample/">blog</a>
        <a href="https://agent-tts.github.io/agent-tts/">website</a>
      </div>
    </div>
  </article>

  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://arxiv.org/abs/2605.14445" aria-label="FrontierSmith paper">
      <img src="/assets/img/featured-publications/frontiersmith-pipeline.png" alt="FrontierSmith pipeline overview">
    </a>
    <div>
      <h4><a href="https://arxiv.org/abs/2605.14445">FrontierSmith: Synthesizing Open-Ended Coding Problems at Scale</a></h4>
      <p class="featured-paper-authors"><span class="mentee-first-author">Runyuan He</span>*, <strong>Qiuyang Mang*</strong>, Shang Zhou, Kaiyuan Liu, Hanchen Li, Huanzhi Mao, Qizheng Zhang, Zerui Li, Bo Peng, Lufeng Cheng, Tianfu Fu, Yichuan Wang, Wenhao Chai, Jingbo Shang, Alex Dimakis, Joseph E. Gonzalez, Alvin Cheung</p>
      <p class="featured-paper-meta">NeurIPS 2026<span style="display: inline-block; margin-left: 0.35rem; color: #c0266d; white-space: nowrap;">Spotlight · 3.7%</span></p>
      <p class="featured-paper-desc">A system for synthesizing open-ended coding problems at scale, connecting data generation, validation, and agent evaluation.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2605.14445">paper</a>
        <a href="https://github.com/FrontierCS/FrontierSmith">code</a>
        <a href="/assets/pdf/frontiersmith.pdf">slides</a>
        <a href="https://www.youtube.com/watch?v=NtVIOh5jFSQ">talk</a>
        <a href="https://frontier-cs.org/blog/frontiersmith/">blog</a>
      </div>
    </div>
  </article>

  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://frontier-cs.org" aria-label="FrontierCS website">
      <img src="/assets/img/featured-publications/frontiercs-teaser.png" alt="FrontierCS paper teaser">
    </a>
    <div>
      <h4><a href="https://frontier-cs.org">FrontierCS: Evolving Challenges for Evolving Intelligence</a></h4>
      <p class="featured-paper-authors"><strong>Qiuyang Mang*</strong>, Wenhao Chai*, Zhifei Li*, Huanzhi Mao*, Shang Zhou*, Alexander Du*, Hanchen Li*, Shu Liu*, and
        <span class="more-authors" title="click to view 48 more authors"
            onclick="
              var element = $(this);
              element.attr('title', '');
              var hiddenText = 'Edwin Chen, Yichuan Wang, Xieting Chu, Zerui Cheng, Yuan Xu, Tian Xia, Zirui Wang, Tianneng Shi, Jianzhu Yao, Yilong Zhao, Qizheng Zhang, Charlie F. Ruan, Zeyu Shen, Kaiyuan Liu, Zhaoyang Hong, Alex Gu, Ziyi Zhang, Runyuan He, Dong Xing, Zerui Li, Zirong Zeng, Yige Jiang, Lufeng Cheng, Ziyi Zhao, Youran Sun, Suyang Zhong, Junpeng Wang, Donglin Li, Wenyuan Huang, Jialiang Gu, Wesley Kai Zheng, Wangmeiyu Zhang, Ruyi Ji, Xuechang Tu, Zihan Zheng, Zhaozi Wang, Zexing Chen, Jingbang Chen, Jialu Zhang, Aleksandra Korolova, Peter Henderson, Pramod Viswanath, Vijay Ganesh, Saining Xie, Zhuang Liu, Dawn Song, Sewon Min, Ion Stoica';
              var moreAuthorsText = element.text() == '48 more authors' ? hiddenText : '48 more authors';
              var cursorPosition = 0;
              var textAdder = setInterval(function() {
                element.text(moreAuthorsText.substring(0, cursorPosition + 1));
                if (++cursorPosition == moreAuthorsText.length) {
                  clearInterval(textAdder);
                }
              }, 10);
            "
        >48 more authors</span>, Joseph E. Gonzalez, Jingbo Shang, Alvin Cheung</p>
      <p class="featured-paper-meta">ICML 2026</p>
      <p class="featured-paper-desc">A benchmark of unsolved, open-ended, verifiable computer science challenges that can evolve with increasingly capable agents.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2512.15699">paper</a>
        <a href="https://github.com/FrontierCS/Frontier-CS">code</a>
        <a href="/assets/pdf/frontiercs-presentation.pdf">slides</a>
        <a href="https://frontier-cs.org">website</a>
      </div>
    </div>
  </article>

  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://arxiv.org/abs/2510.06663" aria-label="Argus paper">
      <img src="/assets/img/argus-2.png" alt="Argus pipeline overview">
    </a>
    <div>
      <h4><a href="https://arxiv.org/abs/2510.06663">Argus: Automated Discovery of Test Oracles for Database Management Systems Using LLMs</a></h4>
      <p class="featured-paper-authors"><strong>Qiuyang Mang</strong>, Runyuan He, Suyang Zhong, Xiaoxuan Liu, Huanchen Zhang, Alvin Cheung</p>
      <p class="featured-paper-meta">SIGMOD 2026</p>
      <p class="featured-paper-desc">A framework that discovers and verifies DBMS test oracles with LLMs, finding previously unknown logic bugs in widely used databases.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2510.06663">paper</a>
        <a href="https://github.com/joyemang33/Argus">code</a>
        <a href="/assets/pdf/argus.pdf">slides</a>
        <a href="/blog/2026/argus/">blog</a>
      </div>
    </div>
  </article>

  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://arxiv.org/abs/2603.08982" aria-label="SVG-EAR paper">
      <img src="/assets/img/featured-publications/svgear-fig2.webp" alt="SVG-EAR attention routing and error comparison">
    </a>
    <div>
      <h4><a href="https://arxiv.org/abs/2603.08982">SVG-EAR: Parameter-Free Linear Compensation for Sparse Video Generation via Error-aware Routing</a></h4>
      <p class="featured-paper-authors"><span class="mentee-first-author">Xuanyi Zhou</span>*, <strong>Qiuyang Mang*</strong>, Shuo Yang, Haocheng Xi, Jintao Zhang, Huanzhi Mao, Joseph E. Gonzalez, Kurt Keutzer, Ion Stoica, Alvin Cheung</p>
      <p class="featured-paper-meta">ECCV 2026</p>
      <p class="featured-paper-desc">A parameter-free linear compensation method that mitigates sparse-attention error, accelerating video generation without retraining.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2603.08982">paper</a>
        <a href="https://github.com/svg-project/Sparse-VideoGen">code</a>
      </div>
    </div>
  </article>

  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://arxiv.org/abs/2511.02230" aria-label="Continuum paper">
      <img src="/assets/img/featured-publications/continuum-fig1.webp" alt="Continuum KV-cache eviction and queueing delay failure modes">
    </a>
    <div>
      <h4><a href="https://arxiv.org/abs/2511.02230">Continuum: Efficient and Robust Multi-Turn LLM Agent Scheduling with KV Cache Time-to-Live</a></h4>
      <p class="featured-paper-authors">Hanchen Li*, <span class="mentee-first-author">Runyuan He</span>*, <strong>Qiuyang Mang*</strong>, Qizheng Zhang, Huanzhi Mao, Xiaokun Chen, Hangrui Zhou, Huanchen Zhang, Alvin Cheung, Joseph Gonzalez, Ion Stoica</p>
      <p class="featured-paper-meta">ICLR 2026 LLA Workshop</p>
      <p class="featured-paper-desc">A KV-cache time-to-live and program-level scheduling system for efficient, robust multi-turn LLM agent serving.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2511.02230">paper</a>
        <a href="https://github.com/Hanchenli/vllm-continuum">code</a>
      </div>
    </div>
  </article>
</div>

</div>
