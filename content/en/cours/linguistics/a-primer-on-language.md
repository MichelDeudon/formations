---
title: A primer on languages and alphabets
date: '2021-01-01'
type: book
weight: 30
highlight: true
tags:
  - Languages and alphabets
---

On the origins

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 3 weeks

## Written archives, origins and evolutions

{{< youtube aCrmBRL4cJs>}}

From symbolic writing (pictograms) to non symbolic writing

(new) Words are created by assembling characters.

Language is in constant evolution.

Language is ambiguous (look at the dog with one eye)

## A simple boolean vector model, bag of characters

The words "computer" and "language" can be represented simply as a bag of characters, a vector of length 26 with value <i>i</i> equal to 1 if character i is present in the word, 0 otherwise.

| Word 	        | a | b | c | d | e | ... | u | v | w | x | y | z |
| -----------   | - | - | - | - | - | -   | - | - | - | - | - | - |
| computer      | 0 | 0 | 1 | 0 | 1 | ... | 1 | 0 | 0 | 0 | 0 | 0 |
| language      | 1 | 0 | 0 | 0 | 1 | ... | 1 | 0 | 0 | 0 | 0 | 0 |

From the above representation, we can say that computer and language share two characters in common, the letters e and u. Given a 3rd word, e.g., "computational", we are also able to say the word is closer to "computer" than "language".

| Word 	        | a   | b   | c   | d   | e   | ... | u   | v   | w   | x   | y   | z   |
| -----------   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   | -   |
| computer      | 0.0 | 0.0 | 0.2 | 0.0 | 0.1 | ... | 0.1 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 |
| language      | 0.2 | 0.0 | 0.0 | 0.0 | 0.1 | ... | 0.1 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 |


Limits of the boolean vector model
- Character frequency doesn't matter (two a or one a maps to the same representation)
- All characters have the same weight in the model (a and b are equally important)

These limits can be circumvented with Vector Space Model. For the <i>i-th</i> character, the cell value is no longer 0 or 1 but some number between 0 and 1. The most common approach is called TF-IDF and stands for term-frequency, inverse document frequency. It measures how frequently a character appears in a word to increase its value and how often it appears accross all words to decrease its value. Intuitively, a character like "g" in "language", which occurs twice (term frequency) and only in the word "language" (no "g" in "computer"), means it is an informative feature. Indeed knowing the word contains "g" means the word is "language" and directly identifies the word (which isn't true for the letter e).

Vector Space Model
• Document d and query q are represented as k-dimensional vectors d = (w1,d, …,
wk,d) and q = (w1,q, …, wk,q)
– Each dimension corresponds to a term from the collection vocabulary
– Independence between terms
– wi,q is the weight of i-th vocabulary word in q
• Is Euclidean distance appropriate to measure the similarity?
• Vector (a, b) and (10 x a, 10 x b) contain the same words but have large Euclidean distance
• Degree of similarity between d and q is the
cosine of the angle between the two vectors
sim(q,d) = q*d/(|q|*|d|)

[Image vector distance and cosine]


Ranked retrieval in the vector space model
§Represent the query as a weighted tf-idf vector
§Represent each document as a weighted tf-idf vector
§Compute the cosine similarity between the query vector and
each document vector
§Rank documents with respect to the query
§Return the top K (e.g., K = 10) to the user


- **Theory**: Message passing. How to transform and pass some information with minimum loss and efforts? Ideas from statistical physics, psychology and other fields. No need to be a computer scientist to study computational linguistics.
- **Tip**: Simpler models are better. Ask the right question. Einstein, Feynman
- **Homework**: Setup your environment (Github, Python) for the course use cases
- Use case: Mispellt words

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

> Christopher D. Manning et al. [Introduction to Information Retrieval](http://www-nlp.stanford.edu/IR-book/). Cambridge
University Press. 2008.

> Michalis Vazirgiannis. INF582 - Introduction to Text Mining & NLP. 2017.

> S.Deerwester et al. Indexing by Latent Semantic Analysis. Journal of the Society for Information Science. 1990

> Soumen Chakrabarti. Mining the Web: Discovering Knowledge from Hypertext Data.
