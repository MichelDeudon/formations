---
title: Learning paradigms
date: '2021-01-01'
type: book
weight: 70
math: true
tags:
  - Statistics
---

Compare learning paradigms in NLP.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 4 weeks

## Learning paradigms

- Supervised learning (Linear, LDA/QDA, naive Bayes, Logistic, RF, MLP, SVM, Kernel)
- Unsupervised learning, e.g., clustering (see ML1, ML2 course)

## Other learning paradigms

- Semi-supervised learning, contrastive learning (cPCA, RBM), reinforcement learning, self-supervised, curiosity-driven learning, few-shot learning, active learning, federated learning, online learning…  Effort on model design or problem to solve, representation/task to learn, ?
- Generative vs. discriminative models.
- Parametric vs. non parametric
- Other tools : OT, ODE, 

## Why/when deep learning?

- CNN (log), RNN (linear), attention models, Bert (quadratic)
    - Limits of current models (lack of intrinsic uncertainty, interpolation in latent spaces)
    - Learning to repeat, reformulate, predict word from context… task influences representations
    - Semantic similarity: cosine, manh, kulb, w1 (OT, combinatorial complexity). Info Theory. Shannon (encode) vs Fisher (param)
- Simple preprocessing + ranking can solve your problem?
- Is it the solution or the problem that is wrong? Quote Einstein + Feynman.
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

## Reference

> Michel Deudon. [Learning semantic similarity in a continuous space](https://proceedings.neurips.cc/paper/2018/hash/97e8527feaf77a97fc38f34216141515-Abstract.html). Advances in neural information processing systems. vol 31. 2018.

> Gabriel Peyré and Marco Cuturi. [Computational Optimal Transport](https://optimaltransport.github.io/book/). ArXiv:1803.00567. 2018.

> Chloe Clavel. [Traitement automatique du langage naturel et fouille d’opinions](https://clavel.wp.imt.fr/teaching/)

> Michalis Vazirgiannis. INF554 - Machine learning I. 2016.

> Matt Kusner et al. [From word embeddings to document distances.](https://proceedings.mlr.press/v37/kusnerb15.pdf) International conference on machine learning. PMLR, 2015.

> Christopher Manning and Anna Goldie. [CS224n](https://web.stanford.edu/class/cs224n/). Stanford. 2000.

