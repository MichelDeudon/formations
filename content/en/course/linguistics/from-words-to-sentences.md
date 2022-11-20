---
title: From words to sentences
date: '2021-01-01'
type: book
weight: 50
math: true
tags:
  - Statistics
---

Learn powerful representations.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 3 weeks

## From words to sentences & topics - part A

- **Culture:** Search engines. Research in Information Retrieval. Ex Google. Other topics like spam detection, summarization, translation… widely used today.
- **Model:** Bag of word, tfidf, pLSI (doc embed)
- **Theory**: Linear algebra. NMF. SVD. Spectral decomposition.
- **Tip:**
- **Usecase**:
    - Recommender system. Help Alice and Bob meet to save the world!
    - Extract influencial groups, co-authors…

## From words to sentences & topics - part B

- **Culture:** Semantic, style, intent, sarcasme, emotions… introducing latent variables
- **Model**: GMM, HMM, Lda. PGM
- **Theory:** Probability review. Bayesian learning.
- **Tip:**
- **Usecase**:
    - Melody harmonisation. Ableton. Music.

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

> Laure Delisle et al. [A large-scale crowdsourced analysis of abuse against women journalists and politicians on Twitter](https://arxiv.org/abs/1902.03093). 2019.

> Francis Bach. [Introduction to Probabilistic Graphical Models](https://www.di.ens.fr/~fbach/courses/fall2018/). 2018.