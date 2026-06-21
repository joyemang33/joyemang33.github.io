---
layout: about
title: About
permalink: /
subtitle: 

profile:
  align: right
  image: profile7.jpg
  image_caption: Photo credit &mdash; Hangrui Zhou @ Berlin
  second_image: cat.jpg
  second_image_caption: My cute cat &mdash; Peppa
  image_circular: false # crops the image to make it circular
  address: >
    <span class="profile-email">email: qmang AT berkeley.edu</span>
  more_info: >
    <details class="teaching-service-sidebar">
      <summary class="mentees-toggle"><strong>Teaching & Service</strong></summary>
      <div class="teaching-service">
        <h4>CUHK-Shenzhen</h4>
        <p><strong>2025 Spring:</strong> Teaching Assitant of CSC4001 Software Engineering</p>
        <p><strong>2024 Spring:</strong> Teaching Assitant of CSC4001 Software Engineering<br>
        🏆 <em>2023-2024 Excellent USTF Award</em></p>
        <p><strong>2021&ndash;2025:</strong> Competitive Programming Coach</p>
        <h4>Service</h4>
        <p><strong>Artifact Evaluation Committee:</strong> PLDI' 2024, SIGMOD' 25</p>
        <p><strong>Reviewer:</strong> KDD' 2024 -- 2026, NeurIPS 2026</p>
        <p><strong>External Reviewer:</strong> OSDI' 2023 Artifact Evaluation</p>
      </div>
    </details>


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

#miscellaneous-section h3 {
  font-size: 1.3rem;
}

.about-featured-publications {
  clear: both;
  margin-top: 2.5rem;
  scroll-margin-top: 4.5rem;
}

.about-featured-publications h3 {
  font-size: 1.3rem;
  margin-bottom: 1.05rem;
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
  color: var(--global-text-color-light);
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


Hi, I’m Qiuyang Mang, a first-year CS PhD student in the [Sky Computing Lab](https://sky.cs.berkeley.edu/) at UC Berkeley, advised by [Prof. Alvin Cheung](https://people.eecs.berkeley.edu/~akcheung/).
I lead [FrontierCS](https://frontier-cs.org) and [FrontierSmith](https://arxiv.org/abs/2605.14445), a benchmark and data synthesis system for LLM-driven algorithm evolution on open-ended coding tasks. My research interests center on two themes:

- **LLM Long-Horizon Optimization**: Leveraging LLMs for complex, multi-step optimization, powering long-horizon code-agent from data curation to post-training. [FrontierCS](https://frontier-cs.org), [FrontierSmith](https://arxiv.org/abs/2605.14445), [Argus](https://arxiv.org/abs/2510.06663), [SkyDiscover](https://github.com/skydiscover-ai/skydiscover)

- **Machine Learning Systems**: Efficient algorithms for ML workloads, from data-processing to inference scheduling. [PLOP](https://arxiv.org/abs/2604.09944), [SVG-EAR](https://arxiv.org/abs/2603.08982), [Continuum](https://arxiv.org/abs/2511.02230)

Prior to joining Berkeley, I received my B.E. from [The Chinese University of Hong Kong, Shenzhen](https://www.cuhk.edu.cn/), where I was advised by [Prof. Pinjia He](https://pinjiahe.github.io/). I also spent an unforgettable year as a research assistant at the [National University of Singapore](https://nus-test.github.io/) with [Prof. Manuel Rigger](https://www.manuelrigger.at/). During my undergraduate years, I worked on robustifying NLP systems and Database Management Systems.


<details>
<summary class="mentees-toggle"><strong>Mentees & Opportunities for undergraduate collaborations</strong></summary>

I'm very fortunate to work with amazing undergraduate students learn from their passion and talent: 

<div class="mentees-list">
  <p><strong><a href="https://runyuanhe.github.io/" target="_blank">Runyuan He</a></strong> (2025 &ndash; Present)</p>

  <p><strong>Past Mentees:</strong>
  <strong><a href="https://www.linkedin.com/in/wesley-zheng-cal/" target="_blank">Wesley Zheng</a></strong> (2025 &ndash; 2026) → 5th-year Master @ Berkeley,
  <strong><a href="https://github.com/zengzirong" target="_blank">Zirong Zeng</a></strong> (2025 &ndash; 2026) → PhD @ CUHK-Shenzhen,
  <strong><a href="https://github.com/DMoRanSky" target="_blank">Frank (Yufan) Xiang</a></strong> (2025 &ndash; 2026) → Citadel Securities Summer 2026,
  <strong><a href="https://www.linkedin.com/in/alexander-du-0268642a4/" target="_blank">Alexander Du</a></strong> (2025 &ndash; 2026) → Optiver Summer 2026</p>
</div>

If you're an undergraduate student interested in research collaboration, please feel free to shoot me an <a href="mailto:qmang@berkeley.edu">email</a> with your background and your interest, e.g., <span class="requirement-item">resume</span>, <span class="requirement-item">transcript</span>, optional related exprience like previous research or competitive programming (ICPC, NOI, USACO, etc.) achievements.
</details>

<style>
details {
  margin: 1rem 0;
}

.mentees-toggle {
  display: flex;
  align-items: baseline;
  gap: 0.55rem;
  cursor: pointer;
  user-select: none;
  color: var(--global-text-color);
  font-size: 1.25rem;
  font-weight: 700;
  padding: 0.5rem 0;
  list-style: none;
  transition: color 0.2s ease;
  font-family: 'Merriweather', Georgia, serif;
  line-height: 1.3;
}

.mentees-toggle:hover {
  color: var(--global-hover-color);
}

.mentees-toggle::-webkit-details-marker {
  display: none;
}

.mentees-toggle::before {
  content: '';
  display: inline-block;
  flex: 0 0 auto;
  width: 0.72em;
  height: 0.72em;
  color: var(--global-theme-color);
  background:
    linear-gradient(currentColor, currentColor) center / 100% 2px no-repeat,
    linear-gradient(currentColor, currentColor) center / 2px 100% no-repeat;
  transform: translateY(0.02em);
  transition: background-size 0.2s ease, transform 0.2s ease;
}

details[open] .mentees-toggle::before {
  background-size: 100% 2px, 0 0;
  transform: translateY(0.02em);
}

.mentees-list {
  margin-top: 0.5rem;
}

.mentees-list ul {
  list-style-type: disc;
  padding-left: 1.5rem;
  margin: 0.5rem 0;
}

.mentees-list li {
  margin: 0.5rem 0;
  line-height: 1.6;
}

.mentees-list p {
  margin: 0.5rem 0;
  line-height: 1.6;
}

.mentees-list strong a {
  color: var(--global-theme-color);
  text-decoration: none;
  font-weight: 600;
}

.mentees-list strong a:hover {
  text-decoration: underline;
}

.requirement-item {
  text-decoration: underline;
  text-decoration-color: var(--global-theme-color);
  text-decoration-thickness: 1.5px;
  text-underline-offset: 2px;
  font-weight: 500;
}

.collaboration-info {
  margin-top: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid var(--global-divider-color);
}

.collaboration-info p {
  margin: 0.8rem 0;
  line-height: 1.6;
}

.teaching-service {
  margin-top: 1rem;
}

.teaching-service h4 {
  font-size: 1.1rem;
  font-weight: 600;
  margin-top: 1rem;
  margin-bottom: 0.5rem;
  color: var(--global-text-color);
  padding-left: 0;
}

.teaching-service p {
  margin-bottom: 0.8rem;
  line-height: 1.6;
  padding-left: 1.5rem;
}

.teaching-service ul {
  padding-left: 1.2rem;
}

.teaching-service li {
  margin-bottom: 0.5rem;
  line-height: 1.6;
}

/* Teaching & Service in sidebar */
.teaching-service-sidebar {
  margin-top: 0.5rem;
  font-size: 0.9rem;
}

.teaching-service-sidebar .mentees-toggle {
  font-size: 1.1rem;
}

.teaching-service-sidebar .teaching-service h4 {
  font-size: 1rem;
  margin-top: 1rem;
  margin-bottom: 0.5rem;
}

.teaching-service-sidebar .teaching-service p {
  margin-bottom: 0.6rem;
  padding-left: 0;
  font-size: 0.85rem;
}

/* Hide on mobile, show inline */
@media (max-width: 768px) {
  .teaching-service-sidebar {
    display: none;
  }
  
  #teaching-service-mobile {
    display: block;
  }
}

@media (min-width: 769px) {
  #teaching-service-mobile {
    display: none;
  }
}
</style>


<details markdown="1" id="teaching-service-mobile">
<summary class="mentees-toggle"><strong>Teaching & Service</strong></summary>

<div class="teaching-service" markdown="1">

#### CUHK-Shenzhen

**2025 Spring:** Teaching Assitant of CSC4001 Software Engineering

**2024 Spring:** Teaching Assitant of CSC4001 Software Engineering  
🏆 *2023-2024 Excellent USTF Award*

**2021 &ndash; 2025:** Competitive Programming Coach

#### Service

**Artifact Evaluation Committee:** PLDI' 2024, SIGMOD' 25

**Reviewer:** KDD' 2024 -- 2026, NeurIPS 2026

**External Reviewer:** OSDI' 2023 Artifact Evaluation

</div>

</details>


<div id="miscellaneous-section" markdown="1">

### Miscellaneous

- 忙秋阳 is my name in Chinese, which is pronounced like "Chew-yahng Mahng".
- I was in the 46th ICPC World Finalist 🎈 and served as [problem setters](https://qoj.ac/user/profile/Joyemang) for regionals.
- I enjoy basketball, cooking, and video games. I also have a beautiful ragdoll cat.

I understand how deeply research success depends on access and opportunity, and I feel incredibly fortunate for the support and opportunities provided by Pinjia, Manuel, Alvin, and many others along the way. Many talented students never receive the opportunities they need to fully realize their potential. If you're from an underrepresented group and think it might help to talk or want to collaborate with me, feel free to reach out by [email](mailto:qmang@berkeley.edu).

</div>

<div class="about-featured-publications" markdown="1">

### Selected Publications

<div class="featured-paper-list">
  <article class="featured-paper">
    <a class="featured-paper-visual" href="https://arxiv.org/abs/2605.14445" aria-label="FrontierSmith paper">
      <img src="/assets/img/featured-publications/frontiersmith-pipeline.png" alt="FrontierSmith pipeline overview">
    </a>
    <div>
      <h4><a href="https://arxiv.org/abs/2605.14445">FrontierSmith: Synthesizing Open-Ended Coding Problems at Scale</a></h4>
      <p class="featured-paper-authors"><strong>Runyuan He*</strong>, <strong>Qiuyang Mang*</strong>, Shang Zhou, Kaiyuan Liu, Hanchen Li, Huanzhi Mao, Qizheng Zhang, Zerui Li, Bo Peng, Lufeng Cheng, Tianfu Fu, Yichuan Wang, Wenhao Chai, Jingbo Shang, Alex Dimakis, Joseph E. Gonzalez, Alvin Cheung</p>
      <p class="featured-paper-meta">Preprint, 2026</p>
      <p class="featured-paper-desc">A system for synthesizing open-ended coding problems at scale, connecting data generation, validation, and agent evaluation.</p>
      <div class="featured-paper-links">
        <a href="https://arxiv.org/abs/2605.14445">paper</a>
        <a href="https://github.com/FrontierCS/FrontierSmith">code</a>
        <a href="/assets/pdf/frontiersmith.pdf">slides</a>
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
        <a href="https://frontier-cs.org">website</a>
        <a href="https://arxiv.org/abs/2512.15699">paper</a>
        <a href="https://github.com/FrontierCS/Frontier-CS">code</a>
        <a href="/assets/pdf/frontiercs-presentation.pdf">slides</a>
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
</div>

</div>
