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

.post article a {
  text-decoration: underline;
  text-decoration-color: #722F37;
}
</style>


Hi, I’m Qiuyang Mang, a first-year CS PhD student in the [Sky Computing Lab](https://sky.cs.berkeley.edu/) at UC Berkeley, advised by [Prof. Alvin Cheung](https://people.eecs.berkeley.edu/~akcheung/).
I lead [FrontierCS](https://arxiv.org/abs/2512.15699) and [FrontierSmith](https://arxiv.org/abs/2605.14445), a benchmark and data synthesis system for LLM-driven algorithm evolution on open-ended coding tasks. My research interests center on two themes:

- **LLM Long-Horizon Optimization**: Leveraging LLMs for complex, multi-step optimization, powering long-horizon code-agent from data curation to post-training. [FrontierCS](https://arxiv.org/abs/2512.15699), [FrontierSmith](https://arxiv.org/abs/2605.14445), [Argus](https://arxiv.org/abs/2510.06663), [SkyDiscover](https://github.com/skydiscover-ai/skydiscover)

- **Machine Learning Systems**: Efficient algorithms for ML workloads, from data-processing to inference scheduling. [PLOP](https://arxiv.org/abs/2604.09944), [SVG-EAR](https://arxiv.org/abs/2603.08982), [Continuum](https://arxiv.org/abs/2511.02230)

Prior to joining Berkeley, I received my B.E. from [The Chinese University of Hong Kong, Shenzhen](https://www.cuhk.edu.cn/), where I was advised by [Prof. Pinjia He](https://pinjiahe.github.io/). I also spent an unforgettable year as a research assistant at the [National University of Singapore](https://nus-test.github.io/) with [Prof. Manuel Rigger](https://www.manuelrigger.at/). During my undergraduate years, I worked on robustifying NLP systems and Database Management Systems.


<details>
<summary class="mentees-toggle"><strong>Mentees & Opportunities for undergraduate collaborations</strong></summary>

I'm very fortunate to work with amazing undergraduate students learn from their passion and talent: 

<div class="mentees-list">
  <p><strong><a href="https://runyuanhe.github.io/" target="_blank">Runyuan He</a></strong> (2025 &ndash; Present)</p>

  <p><strong>Past Mentees:</strong>
  <strong><a href="https://www.linkedin.com/in/wesley-zheng-cal/" target="_blank">Wesley Zheng</a></strong> (2025 &ndash; 2026) → 5th-year Master @ Berkeley,
  <strong><a href="https://github.com/zengzirong" target="_blank">Zirong Zeng</a></strong> (2025 &ndash; 2026),
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
