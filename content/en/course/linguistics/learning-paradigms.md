---
title: Learning paradigms
date: '2021-01-01'
type: book
weight: 40
math: true
tags:
  - Statistics
---

Compare learning paradigms in NLP.

<!--more-->

{{< icon name="clock" pack="fas" >}} 5h30 per week, for 4 weeks

## Learning paradigms

- Supervised learning (Linear, Logistic, RF, MLP)
- Unsupervised learning, e.g., clustering (see ML1, ML2 course)

## Other learning paradigms

- Semi-supervised learning, contrastive learning (cPCA, RBM), reinforcement learning, self-supervised, curiosity-driven learning, few-shot learning, active learning, federated learning…  Effort on model design or problem to solve, representation/task to learn, ?

## Why/when deep learning?

- CNN (log), RNN (linear), attention models, Bert (quadratic)
    - Limits of current models (lack of intrinsic uncertainty, interpolation in latent spaces)
    - Learning to repeat, reformulate, predict word from context… task influences representations
    - Semantic similarity: cosine, manh, kulb, w1 (OT, combinatorial complexity). Info Theory. Shannon (encode) vs Fisher (param)
- Simple preprocessing + ranking can solve your problem?
- Is it the solution or the problem that is wrong?
- **Usecase**:
    - Deduplicate database, build search/recommendation API… (faq)
    - Regulatory, media & political feedback
    - Summary (models, hypothesis, limits)


## From language to socio dynamics

- Behavioral psychology.
    - **Usecase**: Diversity & inclusion. Online Harassment. Twitter. Amnesty.
    - **Usecase**: Orthophonistes


The general form of the **normal** probability density function is:

$$
f(x) = \frac{1}{\sigma \sqrt{2\pi} } e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}
$$

{{< callout note >}}
The parameter $\mu$ is the mean or expectation of the distribution.
$\sigma$ is its standard deviation.
The variance of the distribution is $\sigma^{2}$.
{{< /callout >}}

## Quiz

{{< spoiler text="What is the parameter $\mu$?" >}}
The parameter $\mu$ is the mean or expectation of the distribution.
{{< /spoiler >}}
