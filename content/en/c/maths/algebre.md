---
title: Algebra II
date: '2023-01-23'
type: book
weight: 10
math: true
tags:
  - linear algebra
  - dimensionality reduction
  - principal component analysis
  - matrix factorization
  - singular value decomposition
---

Linear algebra and Principal Component Analysis

<!--more-->

## Principal Component Analysis and Alg II

{{< icon name="clock" pack="fas" >}} 12h, 6x2h par semaine

{{< figure src="linguistics/img7.jpg" caption="Illustration of Principal Component Analysis (PCA) on sentences, represented as Gaussian distributions with diagonal covariance matrices. Deudon, Michel. [Learning semantic similarity in a continuous space](https://papers.nips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf). Advances in neural information processing systems 31 (2018).">}}

### Course

{{% staticref "uploads/TE62MI_Analyse_en_composante_principale.pdf" %}}ACP et reduction de dimension{{% /staticref %}}.

#### 1. Definitions and notations
#### 2 PCA from 2D to 1D
#### 3 PCA in 3D and more
##### 3.1 Formulation of the problem
##### 3.2 Decomposition of matrices
##### 3.3 Back to PCA and lower rank approximation
#### 4 PCA in practice
##### 4.1 Data preprocessing
##### 4.2 Pseudo code
##### 4.3 Concept of similarity
#### 5 Other Matrix Factorization Methods
#### 6 Preservation of distances
#### Conclusion

### TP / Pratique

{{< icon name="github" pack="fab" >}} [te62mi-algebre-bilineaire](https://github.com/MichelDeudon/te62mi-algebre-bilineaire)

#### TP1. [SVD](https://github.com/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/SVD.ipynb).
#### TP2. [PCA](https://github.com/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/PCA.ipynb).
#### TP3. [MDS](https://github.com/MichelDeudon/te62mi-algebre-bilineaire/blob/main/tp/MDS.ipynb).

### TD / Exercices

Coming soon.

### References
- 1. R. Bellman. The curse of dimensionality. Princeton. 1961.
- 2. P. Comon. Independent component analysis, a new concept? Signal processing. 1994.
- 3. P. Pentti et U. Tapper. Positive matrix factorization: A non-negative factor model with optimal utilization of error estimates of data values. Environmetrics. 1994.
- 4. A. J. Bell et T. J. Sejnowski. An information-maximization approach to blind separation and blind deconvolution. Neural computation. 1995.
- 5. A. Hyvärinen et O. Erkki. Independent component analysis: algorithms and applications. Neural networks. 2000.
- 6. J. Mairal, F. Bach et al. Online learning for matrix factorization and sparse coding. Journal of Machine Learning Research. 2010.
- 7. F. Pedregosa, G. Varoquaux et al. Scikit-learn: Machine learning in Python. Journal of Machine Learning Research. 2011.
- 8. C.R. Harris, K.J. Millman et al. Array programming with NumPy. Nature. 2020.