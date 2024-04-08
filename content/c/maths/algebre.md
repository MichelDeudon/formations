---
title: Algèbre II
date: '2023-01-23'
type: book
weight: 10
math: true
tags:
  - algebre linéaire
  - réduction de dimension
  - analyse en composante principale
  - factorisation de matrices
  - décomposition en valeur singulière
---

Algèbre II et analyse en composante principale.

<!--more-->

## Analyse en composante principale et Alg II

{{< icon name="clock" pack="fas" >}} 12h, 6x2h par semaine

{{< figure src="linguistics/img7.jpg" caption="Illustration de l'analyse en composante principale (ACP) appliquée à des phrases représentées par des distributions gaussiennes avec des matrices de covariance diagonales. Deudon, M. [Learning semantic similarity in a continuous space](https://papers.nips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf). Advances in neural information processing systems 31 (2018).">}}

## Cours

{{% staticref "u/TE62MI-Analyse-en-composante-principale.pdf" %}}ACP et reduction de dimension{{% /staticref %}} (pdf).

<b>1 Définitions et notations</b>

<b>2 L’ACP de 2D à 1D</b>

<b>3 L’ACP en 3D et plus</b>
- 3.1 Formulation du problème
- 3.2 Décomposition de matrices
- 3.3 Retour à l’ACP et approximation de rang inférieur

<b>4 L’ACP en pratique</b>
- 4.1 Prétraitement des données
- 4.2 Pseudo code
- 4.3 Notion de similarité

<b>5 Autres méthodes de factorisation matricielle</b>

<b>6 Préservation des distances</b>

<b>Conclusion</b>

## TP / Pratique 

{{< icon name="github" pack="fab" >}} [te62mi-algebre-bilineaire](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire)

1. TP [SVD](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/SVD.ipynb).
2. TP [ACP](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/PCA.ipynb).
3. TP [MDS](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/MDS.ipynb).

## TD / Exercices

À venir.

## Références
1. R. Bellman. The curse of dimensionality. Princeton. 1961.
2. P. Comon. [Independent component analysis, a new concept?](https://hal.science/hal-00417283/document) Signal processing. 1994.
3. P. Pentti et U. Tapper. [Positive matrix factorization: A non-negative factor model with optimal utilization of error estimates of data values](https://onlinelibrary.wiley.com/doi/10.1002/env.3170050203). Environmetrics. 1994.
4. A. J. Bell et T. J. Sejnowski. [An information-maximization approach to blind separation and blind deconvolution](https://www.inf.fu-berlin.de/lehre/WS05/Mustererkennung/infomax/infomax.pdf). Neural computation. 1995.
5. A. Hyvärinen et O. Erkki. [Independent component analysis: algorithms and applications](https://www.cs.helsinki.fi/u/ahyvarin/papers/NN00new.pdf). Neural networks. 2000.
6. J. Mairal, F. Bach et al. [Online learning for matrix factorization and sparse coding](https://www.di.ens.fr/~fbach/mairal10a.pdf). Journal of Machine Learning Research. 2010.
7. F. Pedregosa, G. Varoquaux et al. [Scikit-learn: Machine learning in Python](https://www.jmlr.org/papers/volume12/pedregosa11a/pedregosa11a.pdf). Journal of Machine Learning Research. 2011.
8. C.R. Harris, K.J. Millman et al. [Array programming with NumPy](https://www.nature.com/articles/s41586-020-2649-2). Nature. 2020.