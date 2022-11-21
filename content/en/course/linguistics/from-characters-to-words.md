---
title: From alphabets to words
date: '2021-01-01'
type: book
weight: 40
highlight: true
tags:
  - Data Visualization
---

Encode, decode, transform text data.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 3 weeks

## The n-gram model

- **Culture**: Translating foreign words in Japanese. The Katakana alphabet.
- **Model**: Limit of bag of char (no order). n-gram model, a finer representation to describe words.
- **Theory**: Information compression, loss. *Entropy*. Code genetique. AGCT —> ACG —> Peptide
- **Tip**: When using n-gram models, value of n is important (min, max). Depends on your domain.
- **Usecase**:
    - Dna as a language
    - Pyfood, search and translate api
    - Money laundering & slavery. Rose, ctxt, info obfuscation. How is a word commonly mispelt?
    

## Zipf law

{{< figure src="zipflaw.png" >}}

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


## Reference

> Michel Deudon. [On food, bias and seasons: A recipe for sustainability](https://hal.archives-ouvertes.fr/hal-02532348). HAL-02532348. 2020.

> Frederic Nadal. [Modélisation en neurosciences - et ailleurs](http://www.lps.ens.fr/~nadal/Cours/MVA/). 2018.