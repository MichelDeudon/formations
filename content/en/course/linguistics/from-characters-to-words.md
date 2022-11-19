---
title: From alphabets to words
date: '2021-01-01'
type: book
weight: 30
highlight: true
tags:
  - Data Visualization
---

Learn how to visualize data with Plotly.

<!--more-->

{{< icon name="clock" pack="fas" >}} 4h30 per week, for 3 weeks

## A primer on languages and alphabets

- **Culture**: A primer on languages and alphabets
- **Model**: Bag of char (word embed)
- **Theory**: Message passing. How to transform and pass some information with minimum loss and memory footprint? Ideas from statistical physics, psychology and other fields. No need to be a computer scientist to study computational linguistics.
- **Tip**: Apply minimum steps. Simpler models are better. Ask the right question. Einstein, Feynman
- **Homework**: Setup your environment (Github, Python) for the course use cases

## From alphabets to words - part A

- **Culture**: Translating foreign words in Japanese. The Katakana alphabet.
- **Model**: Limit of bag of char (no order). n-gram model, a finer representation to describe words.
- **Theory**: Information compression, loss. *Entropy*. Code genetique. AGCT —> ACG —> Peptide
- **Tip**: When using n-gram models, value of n is important (min, max). Depends on your domain.
- **Usecase**:
    - Dna as a language
    - Pyfood, search and translate api
    - Money laundering & slavery. Rose, ctxt, info obfuscation. How is a word commonly mispelt?
    

## From alphabets to words - part B

- **Culture**: Zipf law
- **Model**: Limit of n-gram. Dimensionality problem. Visualisation. Quote Hinton 14d. PCA.
- **Theory**: Maxinfo. Optimal projection to reconstruct original message.
- **Tip**: Preprocessing. Lower. Rm accents. Center data. Other methods exists ICA, t-SNE…
- **Usecase**:
    - Find latin roots from French, Italian, Spanish words. Embed words with n-grams/tfidf + pca.
    - Language evolution. Word context. W2vec, Glove (300d, oov) → fastvec (next chapter)
- **Summary of part 1** (models, hypothesis, limits, information theory)

## Quiz

{{< spoiler text="When is a heatmap useful?" >}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{{< /spoiler >}}

{{< spoiler text="Write Plotly code to render a bar chart" >}}

```python
import plotly.express as px
data_canada = px.data.gapminder().query("country == 'Canada'")
fig = px.bar(data_canada, x='year', y='pop')
fig.show()
```

{{< /spoiler >}}
