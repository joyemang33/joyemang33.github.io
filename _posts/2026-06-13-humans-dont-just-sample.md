---
layout: post
title: "Humans Still Beat Agents in the Long Horizon: Revisiting Test-Time Scaling in the Agent Era"
date: 2026-06-16
author: "Qiuyang Mang, Kaiyuan Liu, Bo Peng, Shreyas Pimpalgaonkar, Alex Dimakis, Alvin Cheung"
tags: [test-time-scaling, LLM-agents, scaling-laws]
categories: research
thumbnail: assets/img/repeated-sampling-elo-reference.png
og_image: https://joyemang33.github.io/assets/img/repeated-sampling-elo-reference.png
related_posts: false
published: true
toc:
  sidebar: left
---

<p style="font-size: 1rem; line-height: inherit; margin: 0 0 1.5rem;"><strong style="font-weight: 700;">TL;DR.</strong> Agents can spend test-time compute by trying, observing, and revising, so we ask whether their gains come from a better internal strategy or from something close to repeated sampling. We derive a simple Elo reference line: repeated sampling is linear in log test-time compute. In a 2022 two-week coding marathon, current agents plateau within 24 hours, while top humans keep improving over the official two weeks. The takeaway is that humans still do much better long-horizon test-time adaptation, and agent strategies have a lot of room to improve.</p>

## Agents Bring Intrinsic Test-Time Strategies

OpenAI’s [o1 report](https://openai.com/index/learning-to-reason-with-llms/) showed that more test-time compute can improve model performance. Many papers followed, especially on verifiable tasks like code and math ([Snell et al.](https://arxiv.org/abs/2408.03314), [Large Language Monkeys](https://arxiv.org/abs/2407.21787), [Noam Brown’s recent post](https://x.com/polynoamial/status/2064210146558136827)). The common plot is success rate versus the log number of trials, or log test-time compute. These curves often rise superlinearly before they saturate.

<img src="/assets/img/large-language-monkeys-math-oracle-verifier.png" alt="MATH oracle verifier coverage as the number of samples increases" style="max-width: 60%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Coverage on MATH with an oracle verifier as the number of samples increases, from <a href="https://arxiv.org/abs/2407.21787">Large Language Monkeys</a>.
</p>

These studies measure model performance under an external test-time strategy. The strategy is fixed outside the model: sample many candidate solutions, check them with a verifier, and report pass@k or coverage.

However, agents change this setup. During a run, an agent can try a solution, observe the result, reflect on what failed, and revise its next attempt. This raises the question we study: <strong style="font-weight: 700;">when an agent improves with more test-time compute, is it using a better test-time strategy, or is it mostly reproducing repeated sampling?</strong>

<img src="/assets/img/agent-vs-repeated-sampling-loop.png" alt="External repeated sampling versus an agent internal test-time loop" style="max-width: 70%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Repeated sampling is fixed outside the model, while an agent can use feedback inside the run.
</p>

## A Simple Model for Test-Time Scaling

We first write down the simplest model behind the usual pass@k curves: repeated sampling. The model treats each attempt as an independent draw from the same continuous score distribution. For one task, let $$X$$ be the score of one sample and let $$\tau$$ be the threshold for success. Then one sample succeeds with probability

$$
p = \operatorname{Pr}(X \geq \tau).
$$

With $$k$$ independent samples, pass@k is

$$
\operatorname{Pr}\left(\max_{1 \leq i \leq k} X_i \geq \tau\right)
= 1 - (1 - p)^k.
$$

For a dataset with multiple tasks, the usual test-time scaling curve averages this quantity across tasks. This gives a curve of mean pass@k, or coverage, as a function of the number of samples.

However, this evaluation is awkward for agents. An agent usually stops once it solves the task, so it is not natural to keep asking for more independent samples after success. For open-ended tasks such as [FrontierCS](https://frontier-cs.org/), we could instead compare runs by the task's own score. But raw-score gains are hard to interpret. In circle-packing tasks studied by [AlphaEvolve](https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms/), improving the objective value from 1 to 2 can be trivial, while improving it from 2.35 to 2.36 can require a much harder improvement. The score number does not by itself tell us how much capability changed. We therefore want a comparison that asks a simpler question: <strong style="font-weight: 700;">when one candidate spends more test-time compute than another candidate on the same task, how often does it produce the better answer?</strong>

Following the same repeated-sampling model, this becomes a pairwise question. If one candidate gets $$k_a$$ independent attempts and another gets $$k_b$$ independent attempts, the pairwise win probability is

$$
\operatorname{Pr}\left(\max_{1 \leq i \leq k_a} X_i > \max_{1 \leq j \leq k_b} X'_j\right)
= \frac{k_a}{k_a + k_b},
$$

where $$X_i$$ and $$X'_j$$ are independent attempts on the same task.

Now comes the useful part. A Bradley-Terry model converts pairwise win rates into a one-dimensional strength scale. If candidate $$a$$ has BT log-strength $$\theta_a$$ and candidate $$b$$ has BT log-strength $$\theta_b$$, then

$$
\operatorname{Pr}(a \text{ beats } b)
= \frac{\exp(\theta_a)}{\exp(\theta_a) + \exp(\theta_b)}.
$$

We can see that, for repeated sampling, the pairwise win probability above is exactly matched by

$$
\theta_a = \log k_a + c,
$$

for any constant $$c$$.

<strong style="font-weight: 700;">Thus, repeated sampling is a test-time strategy whose Elo is linear in log test-time compute.</strong> This is super helpful because it gives us a reference line. To judge an agent's intrinsic test-time strategy, we can plot its Elo curve as test-time compute increases and compare it to this line. If the curve is above, below, or close to linear, the agent's strategy is better than, worse than, or equivalent to repeated sampling.

<img src="/assets/img/repeated-sampling-elo-reference.png" alt="Repeated sampling forms a linear Elo reference line as log test-time compute increases" style="max-width: 60%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Repeated sampling gives a linear reference line in Elo versus log test-time compute.
</p>

## Agents Struggle, Humans Do More Than Sample

With this reference line in hand, we can ask what happens in real long-horizon tasks. We compare agent trajectories against the repeated-sampling line, and we also ask: <strong style="font-weight: 700;">how do they compare to top humans working on the same tasks?</strong>

We study [AtCoder Heuristic Contest 014: RectJoin](https://atcoder.jp/contests/ahc014/tasks/ahc014_a), <strong style="font-weight: 700;">a long-horizon coding and optimization contest in 2022</strong>. Human contestants write algorithms and can submit many code solutions during the contest, and the leaderboard keeps the best score they achieve. Since the contest happened before modern coding agents were widely available, these human trajectories are not assisted by AI agents. The task is open-ended: there is no known optimal solution, only better and worse scores.

At a high level, RectJoin starts with marked dots on a grid. A solver repeatedly chooses three existing dots and one empty grid point that form a valid axis-aligned or 45-degree rectangle, then marks the new point and draws the rectangle boundary. The objective is to maximize a weighted score over the final marked dots, where dots farther from the center have larger weight.

<img src="/assets/img/ahc014-rectjoin-example.gif" alt="AtCoder Heuristic Contest 014 RectJoin visualization" style="max-width: 62%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Visualization of RectJoin from <a href="https://atcoder.jp/contests/ahc014/tasks/ahc014_a">AtCoder Heuristic Contest 014</a>.
</p>

### Methodology

<em>Human trajectories.</em> For humans, we study two groups from the final standings: <strong style="font-weight: 700;">the top 10 contestants</strong> and <strong style="font-weight: 700;">the top 50 contestants</strong>. At each checkpoint, we compute prefix-best scores. This gives one vector for each human group at each checkpoint, where each entry is a contestant's best score up to that time.

<em>Agent setting.</em> We recreate the contest setting for agents. Using the [FrontierCS](https://frontier-cs.org/) evaluation layer, each agent runs in a continuous 24-hour loop. It can keep submitting candidates, observe scores, and revise its next attempt, just like a human contestant. If it stops early, we resume the same session rather than starting a fresh run.

We test two agent systems: <strong style="font-weight: 700;">Claude Opus 4.6 with Claude Code</strong>, and <strong style="font-weight: 700;">GPT-5.5 with Codex</strong>. For each agent system, we run five independent 24-hour trials. At every wall-clock checkpoint we care about, we collect the prefix-best score from each trial. This gives a length-5 vector for each agent system at each checkpoint.

Once we have these vectors, we can estimate pairwise win rates directly. For example, one vector might contain the prefix-best scores of the top 10 human contestants at 24 hours, while another contains the prefix-best scores from the five Claude Code trials at 5 hours. We want to know how often the 24-hour top-human scores beat the 5-hour Claude Code scores. If the two vectors are

$$
u = (u_1, \ldots, u_n), \qquad v = (v_1, \ldots, v_m),
$$

we define the empirical probability that $$u$$ beats $$v$$ by comparing all pairs:

$$
\widehat{\operatorname{Pr}}(u \text{ beats } v)
= \frac{1}{nm}\sum_{i=1}^{n}\sum_{j=1}^{m} \mathbf{1}[u_i > v_j].
$$

These pairwise win rates are the inputs to the Elo fit.

### Results

We fit Elo ratings from these pairwise win rates using [L-BFGS](https://doi.org/10.1007/BF01589116). All agent systems and human groups are placed in one joint Bradley-Terry fit, so their ratings are directly comparable. For agents, we use the 24-hour trajectories from our runs. For humans, we use the full trajectories from the official two weeks.

<img src="/assets/img/human-vs-agent-elo.png" alt="Elo trajectories comparing human contestants and agent systems" style="max-width: 100%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Elo trajectories for top humans and agent systems on <a href="https://atcoder.jp/contests/ahc014/tasks/ahc014_a">RectJoin</a>, the long-horizon coding task introduced above.
</p>

The result is sharp. Agents improve quickly in the first few hours, but their Elo curves flatten by the 24-hour mark, even though a single agent trial can use up to 100M tokens. <strong style="font-weight: 700;">Top humans improve more slowly at first, but they keep climbing for days and eventually pass the agent systems by a large margin. This suggests that current agents can sprint early, but they still lack the long-horizon test-time adaptation that strong human contestants use during an extended contest.</strong>

We can also ask a more local question for each participant system. If we only look at one system at a time, the repeated-sampling model gives a reference line for what would happen if that system simply drew more independent samples from its own output distribution. Comparing the observed Elo curve against this line tells us whether the system's test-time strategy is more or less efficient than repeated sampling from itself.

<img src="/assets/img/per-source-elo-vs-repeated-sampling.png" alt="Per-source Elo curves compared with the repeated-sampling reference line" style="max-width: 100%; display: block; margin: 1.5rem auto 0.75rem;">

<p style="text-align: center; font-size: 0.9rem; color: #777; margin-top: 0;">
Per-source Elo curves compared with the repeated-sampling reference line implied by the model.
</p>

The gray dashed line is the repeated-sampling reference. Curves above this line gain Elo faster than independent sampling from the same source distribution. Curves below it gain Elo more slowly. The agent systems become <strong style="font-weight: 700;">sublinear</strong> relative to this reference by the end of the 24-hour run. In contrast, the human curves become <strong style="font-weight: 700;">superlinear</strong> over longer horizons. <strong style="font-weight: 700;">Humans do not just sample; current agents still have a long way to go on long-horizon test-time scaling.</strong>

## Takeaways for Agentic Test-Time Scaling

<ul style="padding-left: 1.1rem; margin-left: 0;">
  <li><strong style="font-weight: 700;">Agents have their own test-time strategies.</strong> We should evaluate whether performance improves with more compute and what strategy produced that improvement.</li>
  <li style="margin-top: 0.65rem;"><strong style="font-weight: 700;">Use repeated sampling as a reference line.</strong> If an agent's Elo grows linearly with log compute, it may be doing little more than repeated sampling. Deviations from that line are the signal.</li>
  <li style="margin-top: 0.65rem;"><strong style="font-weight: 700;">Keep humans as a long-horizon reference.</strong> Top humans still show adaptive improvement over long horizons, which gives us a useful target for agentic test-time scaling.</li>
  <li style="margin-top: 0.65rem;"><strong style="font-weight: 700;">Study more open-ended long-horizon tasks.</strong> We need more tasks, longer run trajectories, and careful failure analysis to understand where agents still fall short.</li>
</ul>

## Citing Us

Our full paper is coming soon. In the meantime, please cite this blog post if you found it helpful. For discussion, contact <a href="mailto:qmang@berkeley.edu">qmang@berkeley.edu</a> or <a href="mailto:lky04@cs.washington.edu">lky04@cs.washington.edu</a>.

<div class="citation-code-block" markdown="1">

```bibtex
@misc{mang2026humansstillbeatagents,
  title  = {Humans Still Beat Agents in the Long Horizon: Revisiting Test-Time Scaling in the Agent Era},
  author = {Qiuyang Mang and Kaiyuan Liu and Bo Peng and Shreyas Pimpalgaonkar and Alex Dimakis and Alvin Cheung},
  year   = {2026},
  url    = {https://joyemang33.github.io/blog/2026/humans-dont-just-sample/}
}
```

</div>
