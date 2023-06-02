---
title: Words, topics and sentences
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

The n-gram model partly circuments the limits of bag of characters / words in which terms are independent. 
By capturing dependencies between characters and words, for example between pair of words or triplet of characters, it allows for a finer representation, useful for instance to read DNA sequences (ACGT -> ACT -> Peptide) or understand and translate ingredients with [Pyfood](https://pyfood.readthedocs.io/en/latest/).

Note: When using n-gram models, the value of n is important (min, max) and depends on your domain of application.

Application:
- Find latin roots from French, Italian, Spanish words. Embed words with n-grams/tfidf + pca.
- Study language evolution. Word context. W2vec, Glove (300d, oov) → fastvec (next chapter)

{{< figure src="linguistics/img4.png" caption="Illustration of Zipf Law.">}}

A challenge with n-gram models is related to the curse of dimensionality.

## Corpus and query preprocessing steps

| Preprocessing step  | Description | Beware |
| -----------         | -           | - |
| Tokenization        | Split text in sequences of tokens | Abbreviations (U.N.), Hyphenation (New-York), Apostrophes, Accents, Dates, Numéros/nombres |
| Stop-words          | Frequent words that do not carry semantic information (the, a, an, and, or, to) are removed, reducing dimension and distances | "Let it be", "To be or not to be" |
| Case-insensitive    | Lower case words, reducing dimension and distances | "Let it be", "To be or not to be" |
| Lemmatization       | Reduce inflected forms of a word: am, were, being, been -> be (requires knowledge of grammar, part of speech) | - |
| Stemming            | Reduces tokens to a "root" form, for example Porter Algorithm in English | Resulting terms are not always readable |

## Reference

> Laure Delisle et al. [A large-scale crowdsourced analysis of abuse against women journalists and politicians on Twitter](https://arxiv.org/abs/1902.03093). 2019.

> Michel Deudon. [On food, bias and seasons: A recipe for sustainability](https://hal.archives-ouvertes.fr/hal-02532348). HAL-02532348. 2020.

> Local Seasonal. [Pyfood: A Python package to process food](https://pyfood.readthedocs.io/en/latest/). Pypi.