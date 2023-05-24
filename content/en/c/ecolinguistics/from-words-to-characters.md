---
title: From alphabets to words and sentences
date: '2021-01-01'
type: book
weight: 40
highlight: true
tags:
  - Data Visualization
  - Statistics
---

Encode, decode information and meaning.

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

{{< figure src="linguistics/img4.png" >}}

- **Culture**: Zipf law
- **Model**: Limit of n-gram. Dimensionality problem. Visualisation. Quote Hinton 14d. PCA.
- **Theory**: Maxinfo. Optimal projection to reconstruct original message.
- **Tip**: Preprocessing. Lower. Rm accents. Center data. Other methods exists ICA, t-SNE…
- **Usecase**:
    - Find latin roots from French, Italian, Spanish words. Embed words with n-grams/tfidf + pca.
    - Language evolution. Word context. W2vec, Glove (300d, oov) → fastvec (next chapter)
- **Summary of part 1** (models, hypothesis, limits, information theory)


## From words to sentences & topics - part A

Learn powerful representations

- **Culture:** Search engines. Research in Information Retrieval. Ex Google. Other topics like spam detection, summarization, translation… widely used today.
- **Model:** Bag of word, tfidf, pLSI (doc embed)
- **Theory**: Linear algebra. NMF. SVD. Spectral decomposition.
- **Tip:**
- **Usecase**:
    - Recommender system. Help Alice and Bob meet to save the world!
    - Extract influencial groups, co-authors…
    - Text Mining, an introduction

Outline (or move to part 1)
• Document collection preprocessing
• Feature Selection
• Indexing
• Query processing & Ranking
• Retrieval evaluation

Boolean Vector Model -> to VSM
• Boolean model
– Text 1: “This is the text lab of the M1 master
course”
– Text 2: “This is a text course”

Tokenization
• Split text in sequences of tokens which are candidates to be
indexed
• But, pay attention to
– Abbreviations: U.N. and UN (United Nations or 1 in French)
– New York as one or two tokens
– c++ as one token, but not c+
– Apostrophes
– Hyphenation: one-man-show, Hewlett-Packard
– Dates: 2011/05/16, May 16th, 2011
– Numbers: (+33) 8203-911
– Accents: Ελλάδα / Ελλαδα, Université

Stop-words
• Very frequent words that do not carry semantic
information
– the, a, an, and, or, to
• Stop-words can be removed to reduce index size
requirements and to speed-up query processing
• But
– Improvements in compression and query processing can
offset the impact from stop-words
– Stop-words are useful for certain queries submitted to
Web search engines
• “The The”, “Let it be”, “To be or not to be”

Lemmatization & Stemming
• Lemmatization
– Reduce inflected forms of a word so that they are treated as a single
term: am, were, being, been -> be
– Requires knowledge of context, grammar, part of speech
• Stemming: reduces tokens to a “root” form
– Porter’s Stemming Algorithm
• Applicable to texts written in English
• Removes the longest-matching suffix from words
agreed - agree,but feed - feed
plastered - plaster, but bled - bled
motoring - motor, but sing - sing
• Limitation: resulting terms are not always readable


Miscellaneous
- **Culture:** Semantic, style, intent, sarcasme, emotions… introducing latent variables
- **Model**: GMM, HMM, Lda. PGM
- **Theory:** Probability review. Bayesian learning.
- **Tip:**
- **Usecase**:
    - Melody harmonisation. Ableton. Music.


## Reference

> Laure Delisle et al. [A large-scale crowdsourced analysis of abuse against women journalists and politicians on Twitter](https://arxiv.org/abs/1902.03093). 2019.

> Michel Deudon. [On food, bias and seasons: A recipe for sustainability](https://hal.archives-ouvertes.fr/hal-02532348). HAL-02532348. 2020.

> Local Seasonal. [Pyfood: A Python package to process food](https://pyfood.readthedocs.io/en/latest/). Pypi.