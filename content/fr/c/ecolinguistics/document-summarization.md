---
title: Extraction de mots-clés
date: '2021-01-01'
type: book
weight: 50
math: true
tags:
  - Statistics
---

Analytise et synthése.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 per week, for 3 weeks

## Representing documents as...

Graphs have been successfully used in Information Retrieval to encompass relations between entities (e.g. PageRank [Page et al., 1999]).

Graph of Word (Vazirgiannis et al) is an approach for text mining which adresses the term independence assumption through the bag-of-word representation. It takes into account word dependence and word order through a graph based representation of a document (graph-of-word). Instead of the traditional bag-of-words (i.e. multiset of terms), we represent a document as a graph-of words to capture word order and word dependency.

{{< callout note >}}
As a reminder, a graph is made of nodes V and edges E.
{{< /callout >}}

In a graph of words, nodes are words and edges are dependencies between these words.

Note: Graph algorithms, for example Minimum Spanning Trees ou Min Vertex Cover can be applied to graph representations of documents to gather insights.

{{< figure src="linguistics/graph-of-words.jpg" caption="Graph of words.">}}

### Unweighted directed graph

The weight of a word in the document can be set to the number of neighbors in the graph -> favor words that occur with many different other words.

Pros/Cons: Robust to varying document length, weight of a word increases only with **new context** of co-occurrences.

### Directed graph

The weight of a word in the document can be set to **indegree** of each node. The weight of a term in a document is its indegree (numbers of incoming edges) in the **graph-of-word**. It represents the **number of distinct contexts of occurrence**. We store the document as a vector of weights in the direct index and similarly in the inverted index

For example: information retrieval is the activity of obtaining information resources relevant to an information need from a collection of information resources, gives the following nodes and weights:

information (5), retrieval (1), activity (2), obtaining (2), resources (3), relevant (2), need (2), collection (2).

## GoW for keywords extraction and document summarization

Keywords are used everywhere:
- looking up information on the Web (e. g., via a search engine bar)
- finding similar posts on a blog (e. g., tag cloud)
- for ads matching (e. g., AdWords’ keyword planner)
- for research paper indexing and retrieval (e. g., SpringerLink)
- for research paper reviewer assignment (e. g., ECIR ’15!)

Applications are numerous:
- **summarization** (to get a gist of the content of a document)
- **information filtering** (to select specific documents of interest)
- **indexing** (to answer keyword-based queries)
- **query expansion** (using additional keywords from top results)

Graph-based Keyword Extraction selects the most cohesive sets of words in the graph as keywords.

K-core decomposition retains the main core of the graph (weighted edges), and nodes based on their centrality and cohesiveness.

{{< figure src="linguistics/k-core-graph.png" caption="Graph of words.">}}

Evaluated against PageRank on scientific papers with keywords manually assigned by human annotators, in terms of precision, recall, F1-score, # of keywords.

## Quiz

{{< spoiler text="What is the parameter $\mu$?" >}}
The parameter $\mu$ is the mean or expectation of the distribution.
{{< /spoiler >}}

## Reference

> Michalis Vazirgiannis. Introduction to Text Mining & NLP. Ecole Polytechnique. 2017.
> F Rousseau, M Vazirgiannis. Main core retention on graph-of-words for single-document keyword extraction. European Conference on Information Retrieval. 2015.
> F Rousseau, M Vazirgiannis. Graph-of-word and TW-IDF: new approach to ad hoc IRF. Proceedings of the 22nd ACM CIKM. 2013.