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

Algèbre II et analyse en composante principale

<!--more-->

## Analyse en composante principale et Alg II

{{< icon name="clock" pack="fas" >}} 12h, 6x2h par semaine

{{< figure src="linguistics/img7.jpg" caption="Illustration de l'analyse en composante principale (ACP) appliquée à des phrases représentées par des distributions gaussiennes avec des matrices de covariance diagonales. Deudon, M. [Learning semantic similarity in a continuous space](https://papers.nips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf). Advances in neural information processing systems 31 (2018).">}}

### Cours

{{% staticref "uploads/TE62MI_Analyse_en_composante_principale.pdf" %}}ACP et reduction de dimension{{% /staticref %}}.

#### 1. Définitions et notations
#### 2 L’ACP de 2D à 1D
#### 3 L’ACP en 3D et plus
##### 3.1 Formulation du problème
##### 3.2 Décomposition de matrices
##### 3.3 Retour à l’ACP et approximation de rang inférieur
#### 4 L’ACP en pratique
##### 4.1 Prétraitement des données
##### 4.2 Pseudo code
##### 4.3 Notion de similarité
#### 5 Autres méthodes de factorisation matricielle
#### 6 Préservation des distances
#### Conclusion

### TP / Pratique 

{{< icon name="github" pack="fab" >}} [te62mi-algebre-bilineaire](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire)

#### TP1. [SVD](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/SVD.ipynb).
#### TP2. [ACP](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/PCA.ipynb).
#### TP3. [MDS](https://framagit.org/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/MDS.ipynb).

### TD / Exercices

À venir.

### Références
- 1. R. Bellman. The curse of dimensionality. Princeton. 1961.
- 2. P. Comon. Independent component analysis, a new concept? Signal processing. 1994.
- 3. P. Pentti et U. Tapper. Positive matrix factorization: A non-negative factor model with optimal utilization of error estimates of data values. Environmetrics. 1994.
- 4. A. J. Bell et T. J. Sejnowski. An information-maximization approach to blind separation and blind deconvolution. Neural computation. 1995.
- 5. A. Hyvärinen et O. Erkki. Independent component analysis: algorithms and applications. Neural networks. 2000.
- 6. J. Mairal, F. Bach et al. Online learning for matrix factorization and sparse coding. Journal of Machine Learning Research. 2010.
- 7. F. Pedregosa, G. Varoquaux et al. Scikit-learn: Machine learning in Python. Journal of Machine Learning Research. 2011.
- 8. C.R. Harris, K.J. Millman et al. Array programming with NumPy. Nature. 2020.