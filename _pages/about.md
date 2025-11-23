---
layout: about
title: About
permalink: /
subtitle: 

profile:
  align: right
  image: profile7.jpg
  image_caption: Photo credit -- Hangrui Zhou @ Berlin
  second_image: cat.jpg
  second_image_caption: My cute cat -- Peppa
  image_circular: false # crops the image to make it circular
  address: >


news: false  # includes a list of news items
# latest_posts: false  # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

<style>
* {
  font-family: sans-serif;
}

/* Keep content on the left side, never wrap under the right-aligned profile */
.post article .clearfix {
  max-width: calc(100% - 380px); /* Adjust based on your profile width */
  clear: none !important;
}

@media (max-width: 768px) {
  .post article .clearfix {
    max-width: 100%;
  }
}

/* Paper link styling */
.paper-link {
  display: inline-block;
  padding: 0.2rem 0.6rem;
  margin-left: 0.3rem;
  background: rgba(138, 43, 226, 0.08);
  color: var(--global-theme-color) !important;
  text-decoration: none !important;
  border: 1px solid rgba(138, 43, 226, 0.25);
  border-radius: 4px;
  font-size: 0.85rem;
  font-weight: 500;
  transition: all 0.3s ease;
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
  margin-bottom: 0.8rem;
}
</style>

Hi, I'm Qiuyang Mang, a first year CS PhD student at advised by [Prof. Alvin Cheung](https://people.eecs.berkeley.edu/~akcheung/) at UC Berkeley at [SkyLab](https://sky.cs.berkeley.edu/). Prior to this, I received B.E. at *The Chinese University of Hong Kong, Shenzhen,* advised [Prof. Pinjia He](https://pinjiahe.github.io/). I also spent an unforgettable year as a research assistant at *National University of Singapore* with [Prof. Manuel Rigger](https://www.manuelrigger.at/).


My research interests lie in *Data Management*, *Software Engineering*, and *Algorithms*, with a focus on:

- **Database Testing and Verification**: I aim to develop the next generation of *automated database validation techniques*, combining *LLMs* with *post-verification*, toward generating effective, fully automated test cases for database systems.<a href="https://arxiv.org/abs/2510.06663" target="_blank" class="paper-link">📄 Argus</a>
- **Large Language Model for Database**: I'm exploring how to *train LLMs/LRMs using database execution feedback*, enabling them to understand the internal behavior of database engines and ultimately support *complex query optimizations* and *rule discovery*.
- **From Competitive Programming to Research**: I'm always interested in how techniques from *competitive programming* can translate into solving practical problems, especially in data-centric systems. I'm also interested in *integrating competitive programming expertise into LLMs/LRMs*. 

<details>
<summary class="mentees-toggle"><strong>Mentees</strong></summary>

<div class="mentees-list">
  <p><strong><a href="https://www.linkedin.com/in/wesley-zheng-cal/" target="_blank">Wesley Zheng</a></strong> (Berkeley UG'26), co-advised by <a href="https://huanzhimao.com/" target="_blank">Huanzhi Mao</a></p>
  
  <p><strong><a href="https://github.com/zengzirong" target="_blank">Zirong Zeng</a></strong> (CUHK-Shenzhen UG'26, ICPC World Finalist, NOI Silver)</p>
  
  <p><strong><a href="https://github.com/momoway" target="_blank">Runyuan He</a></strong> (CUHK-Shenzhen UG'27, ICPC World Finalist, NOI Silver), co-advised by <a href="https://hanchenli.github.io/" target="_blank">Hanchen Li</a></p>
  
  <p><strong><a href="https://github.com/DMoRanSky" target="_blank">Frank (Yufan) Xiang</a></strong> (UW-Madison UG'27, NOI Silver, USACO Platinum)</p>
  
  <p><strong><a href="https://www.linkedin.com/in/alexander-du-0268642a4/" target="_blank">Alexander Du</a></strong> (Berkeley UG'28, USACO Platinum)</p>
</div>

</details>

<style>
details {
  margin: 1rem 0;
}

.mentees-toggle {
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
  content: '▶';
  display: inline-block;
  margin-right: 0.5rem;
  transition: transform 0.2s ease;
  font-size: 0.7em;
  color: var(--global-theme-color);
}

details[open] .mentees-toggle::before {
  transform: rotate(90deg);
}

.mentees-list {
  margin-top: 0.5rem;
}

.mentees-list p {
  margin: 0.5rem 0;
  line-height: 1.6;
}

.mentees-list strong a {
  color: var(--global-text-color);
  text-decoration: none;
}

.mentees-list strong a:hover {
  color: var(--global-theme-color);
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
}

.teaching-service ul {
  padding-left: 1.2rem;
}

.teaching-service li {
  margin-bottom: 0.5rem;
  line-height: 1.6;
}
</style>


<details>
<summary class="mentees-toggle"><strong>Teaching & Service</strong></summary>

<div class="teaching-service" markdown="1">

#### CUHK-Shenzhen

- **AY2024/2025 Semester 2:** CSC4001 Software Engineering - Undergraduate Student Teaching Fellow
- **AY2023/2024 Semester 2:** CSC4001 Software Engineering - Undergraduate Student Teaching Fellow  
  🏆 *2023-2024 Excellent USTF Award First Class*
- **AY2021/2022, AY2022/2023, and AY2023/2024:** Co-coach of Competitive Programming

#### Service

- **Artifact Evaluation Committee:** PLDI' 2024, SIGMOD' 25
- **Reviewer:** KDD' 2024, KDD' 2025
- **External Reviewer:** OSDI' 2023 Artifact Evaluation

</div>

</details>



### Miscellaneous

- 忙秋阳 is my name in Chinese, which is pronounced like "Chew-yahng Mahng".
- I participated in the 46th ICPC World Finals and served as a problem setter for several ICPC regionals.
- Besides my research, I enjoy basketball, cooking, and video games. I also have a beautiful ragdoll cat.

I understand how deeply research success depends on access and opportunity, and I feel incredibly fortunate for the support and opportunities provided by Pinjia, Manuel, Alvin, and many others along the way. Many talented students never receive the opportunities they need to fully realize their potential. If you're from an underrepresented group and think it might help to talk or want to collaborate with me, feel free to reach out by [email](mailto:qmang@berkeley.edu).
