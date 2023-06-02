---
title: Langues, vocabulaire et alphabets
date: '2021-01-01'
type: book
weight: 30
highlight: true
tags:
  - Langues et alphabets
---

Donner du contexte historique.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 3 weeks

## Written archives, origins and evolutions

{{< youtube aCrmBRL4cJs>}}

Language is in constant evolution as testifies the evolution of writing since its invention around 3200-30BC. 
Originally, pictograms were used to describe symbols, for example to count and trade.
New words could be created by assembling characters, following the principle of compositionality.
The invention of non symbolic writing and the latin alphabet only came later, around XX BC.
Some languages like Japanese have multiple alphabets, namely kanji (symbols), hiragana and katana (non symbolic, used for foreign words and expressions).

Language is ambiguous by nature (look at the dog with one eye).

Meet Alice and Bob. Message passing. How to transform and pass some information with minimum loss and efforts? Principle of Least Effort, an introduction to Human Ecology, 1949.
Ideas from statistical physics, psychology and other fields. Information compression, loss. *Entropy*. Assumption. No info obfuscation as oppoed to counter money laundering or modern slavery (mispelt words like roses have a different meaning). Maxinfo. Optimal projection to reconstruct original message. Ex sms.
Semantic, style, intent, sarcasme, emotions… introducing latent variables. Words on cognitive biases.

## A first model, Boolean Vectors

Boolean Vector models are simple models which can be applied to study language. Each dimension of the vector space corresponds to a term from the collection alphabet or vocabulary.

{{< callout note >}}
See [linear algebra](https://www.mtpcours.fr/en/c/maths/algebre/) course for a refresher on vector spaces.
{{< /callout >}}

### Bag of characters

The words "computer" and "language" can be represented simply as a bag of characters using the latin alphabet. Each word is represented by a vector of length 26 with value <i>i</i> equal to 1 if character <i>i</i> is present in the word, 0 otherwise.

| Word 	        | a | b | c | d | e | ... | u | v | w | x | y | z |
| -----------   | - | - | - | - | - | -   | - | - | - | - | - | - |
| computer      | 0 | 0 | 1 | 0 | 1 | ... | 1 | 0 | 0 | 0 | 0 | 0 |
| language      | 1 | 0 | 0 | 0 | 1 | ... | 1 | 0 | 0 | 0 | 0 | 0 |

From the above representation, we can say that computer and language share two characters in common, the letters e and u. Given a 3rd word, e.g., "computational", we are also able to say the word is closer to "computer" than "language".

### Bag of words

The same model can be applied to decompose documents into words.

– Text 1: "This is the text lab of the M1 master course"
– Text 2: "This is a text course"

| Document      | This | is | a | the | text | lab | of | IS | master | course |
| -----------   | - | - | - | - | - | -   | - | - | - | - | - | - |
| Text 1        | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Text 2        | 1 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |

Bag of words / characters are simple but present several limits in practice. 
- Character frequency doesn't matter (two a or one a maps to the same representation)
- All characters have the same weight in the model (a and b are equally important)
These limits can be partly circumvented with Vector Space Models, which we present in the next section. 

## Vector Space Models

Vector Space Models represent the significance of each term for each document. The cell values are computed based on the terms' frequency. For the <i>i-th</i> character of a document, the cell value is no longer 0 or 1 but some number between 0 and 1. The most common approach is called TF-IDF and stands for term-frequency, inverse document frequency. It measures how frequently a character appears in a word to increase its value and how often it appears accross all words to decrease its value. Intuitively, in the previous example, the letter "g" which occurs twice in the word "language" (term frequency) and only once across the corpus (["language", "computer"]), is an informative feature or pattern for recognition.

| Word 	        | a   | b   | c   | d   | e   | ... | u   | v   | w   | x   | y   | z   |
| -----------   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   |
| computer      | 0 | 0| 0.2 | 0| 0.1 | ... | 0.1 | 0| 0| 0| 0| 0|
| language      | 0.2 | 0| 0| 0| 0.1 | ... | 0.1 | 0| 0| 0| 0| 0|


| Document      | This | is | a | the | text | lab | of | IS | master | course |
| -----------   | - | - | - | - | - | -   | - | - | - | - | - | - |
| Text 1        | 0.1 | 0.1 | 0 | 0.2 | 0.1 | 0.1 | 0.1 | 0.1 | 0.1 | 0.1 |
| Text 2        | 0.2 | 0.2 | 0.2 | 0 | 0.2 | 0 | 0 | 0 | 0 | 0.2 |

### First application: Spelling correction and document retrieval

Given a vocabulary of known words, for example "computer" and "language", bag of characters and vector space models can be used to map words like "compute", "computes" to "computer" and "languages", "linguistics" to "language". It is an example of dimensionality reduction (several words are mapped to one word). This is useful to understand mispellt words, extract ingredients from recipes using a list of known ingredients, and implemented with Scikit-learn TF-IDF and <i>cosine similarity</i> (more below) in [Pyfood](https://pyfood.readthedocs.io/en/latest/).

{{< figure src="linguistics/cosine.png" caption="Image vector distance and cosine.">}}

Document d and query q are represented as k-dimensional vectors d = (d1,d2, …, dk) and q = (q1, …, qk).
We compute the degree of similarity between d and q as the cosine of the angle between the two vectors $sim(q,d) = \frac{q.d}{|q||d|}$

Why not use the Euclidean distance to measure the similarity? 
Vector (a, b) and (10 x a, 10 x b) contain the same words but have large Euclidean distance. The Euclidean distance between vector may be a bad idea, and worsens with the magnitude / amplitude of the signals and the norm of the vectors.

Pseudo Algorithm: Ranked retrieval in the vector space model
- Represent the query as a weighted tf-idf vector
- Represent each document as a weighted tf-idf vector
- Compute the cosine similarity between the query vector and each document vector
- Rank documents with respect to the query
- Return the top K (e.g., K = 10) to the user

Assumptions of bag of words / characters and vector space models
– Independence between terms
- Order of words / characters doesn't matter

Applications: Text Mining, Information Retrieval. Ex Search engines, Google. Other topics like spam detection, summarization, translation… widely used today.

Next: Setup your environment (Framagit, Python) for the use cases and project

## Quiz

{{< spoiler text="Write Plotly code to render a bar chart" >}}

```python
import plotly.express as px
data_canada = px.data.gapminder().query("country == 'Canada'")
fig = px.bar(data_canada, x='year', y='pop')
fig.show()
```

{{< /spoiler >}}


## Reference

> Michalis Vazirgiannis. Introduction to Text Mining & NLP. Ecole Polytechnique. 2017.

> Christopher D. Manning et al. [Introduction to Information Retrieval](http://www-nlp.stanford.edu/IR-book/). Cambridge
University Press. 2008.

> S.Deerwester et al. Indexing by Latent Semantic Analysis. Journal of the Society for Information Science. 1990

> Soumen Chakrabarti. Mining the Web: Discovering Knowledge from Hypertext Data.

> Zipf

> Shannon
