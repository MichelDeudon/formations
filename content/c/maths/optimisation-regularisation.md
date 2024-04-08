---
title: Optimisation et Régularisation
date: '2023-01-23'
type: book
weight: 20
math: true
tags:
  - optimisation
  - regularisation
  - regression lineaire
  - regression logistique
  - descente de gradient (stochastique)
  - méthode de Newton
---

Optimisation et régularisation des modèles.

<!--more-->

## Optimisation et régularisation des modèles

{{< icon name="clock" pack="fas" >}} 12h, 6x2h par semaine

{{< figure src="super-resolution/img2.jpg" caption="Deudon, M., Kalaitzis, A., Goytom, I., Arefin, M. R., Lin, Z., Sankaran, K., ... & Bengio, Y. (2020). [Highres-net: Recursive fusion for multi-frame super-resolution of satellite imagery](https://arxiv.org/pdf/2002.06460.pdf). arXiv preprint arXiv:2002.06460.">}}

## Cours

{{% staticref "u/TW233MI-Optimisation-regularisation.pdf" %}}Optimisation et régularisation des modèles{{% /staticref %}} (pdf).

<b>1 Définitions et notations</b>
- 1.1 Rappel sur les fonctions
- 1.2 Dérivés

<b>2 Apprentissage en ML</b>

<b>3 Optimisation en ML</b>
- 3.1 Hypothèse iid
- 3.2 Algorithme de descente de gradient
- 3.3 Algorithme de Newton
- 3.4 Cas de la régression linéaire
- 3.5 Descente de Gradient Stochastique (SGD)

<b>4 Régression Logistique</b>
- 4.1 Iteratively Reweighted Least Squares (IRLS)

<b>5 Régularisation en ML</b>
- 5.1 Pourquoi régulariser?
- 5.2 Disgression sur l’évaluation en ML
- 5.3 Reformulation du problème d’optimisation
- 5.4 Autre forme de régularisation: Ensembling

<b>6 Optimisation sous contraintes</b>

<b>7 Méthodes bayésiennes</b>

## TP / Pratique 
{{< icon name="github" pack="fab" >}} [tw233mi-regularisation-optimisation](https://framagit.org/MichelDeudon/tw233mi-regularisation-optimisation)

1. TP [Régression logistique, de A à Z](https://framagit.org/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td1-logistic-regression-az.ipynb).
2. TP [Méthodes du premier ordre pour la régression logistique](https://framagit.org/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td2-regularized-logistic-regression.ipynb).
3. TP [Régression logistique régularisée, de A à Z](https://framagit.org/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td3-regularized-logistic-regression.ipynb).

## TD / Exercices

À venir.

## Références
1. J. Wallis. [A treatise of algebra, both historical and practical](https://royalsocietypublishing.org/doi/10.1098/rstl.1685.0053). London. 1685.
2. W. S. McCulloch & W. Pitts. [A logical calculus of the ideas immanent in nervous activity](https://www.cs.cmu.edu/~./epxing/Class/10715/reading/McCulloch.and.Pitts.pdf). The bulletin of mathematical biophysics. 1943.
3. Berkson, J. Application of the logistic function to bio-assay. Journal of the American statistical association. 1944.
4. C. Lanczos. [An Iteration Method for the Solution of the Eigenvalue Problem of Linear Differential and Integral Operators](https://nvlpubs.nist.gov/nistpubs/jres/045/jresv45n4p255_a1b.pdf), Journal of Research of the National Bureau of Standards. 1950.
5. H. Robbins & S. Monro. [A stochastic approximation method. The annals of mathematical statistics](https://www.columbia.edu/~ww2040/8100F16/RM51.pdf). 1951.
6. C. Lanczos. [Solution of Systems of Linear Equations by Minimized Iterations](https://nvlpubs.nist.gov/nistpubs/jres/049/jresv49n1p33_A1b.pdf). Journal of Research of the National Bureau of Standards. 1952.
7. M. R. Hestenes & E. L. Stiefel. [Methods of Conjugate Gradients for Solving Linear Systems](https://nvlpubs.nist.gov/nistpubs/jres/049/jresv49n6p409_a1b.pdf), Journal of Research of the National Bureau of Standards. 1952.
8. A. E. Hoerl & R. W. Kennard. [Ridge regression: Biased estimation for nonorthogonal problems](https://homepages.math.uic.edu/~lreyzin/papers/ridge.pdf). Technometrics. 1970.
9. R. Tibshirani. [Regression shrinkage and selection via the lasso](https://cs.nyu.edu/~roweis/csc2515-2006/readings/lasso.pdf). Journal of the Royal Statistical Society. 1996.
10. W. J. Fu. Penalized regressions: the bridge versus the lasso. Journal of computational and graphical statistics. 1998.
11. F. Pedregosa, G. Varoquaux, A. Gramfort et al. [Scikit-learn: Machine learning in Python](https://www.jmlr.org/papers/volume12/pedregosa11a/pedregosa11a.pdf). The Journal of Machine Learning Research. 2011.
12. N. Freitas. [CPSC540 lecture notes](https://www.cs.ubc.ca/~nando/540-2013/lectures.html). University of British Columbia. 2012.
13. R. Johnson & T. Zhang. [Accelerating stochastic gradient descent using predictive variance reduction](https://proceedings.neurips.cc/paper/2013/file/ac1dd209cbcc5e5d1c6e28598e8cbbe8-Paper.pdf). Advances in neural information processing systems. 2013.
14. A. Defazio, F. Bach, & S. Lacoste-Julien. [SAGA: A fast incremental gradient method with support for non-strongly convex composite objectives](https://proceedings.neurips.cc/paper_files/paper/2014/file/ede7e2b6d13a41ddf9f4bdef84fdc737-Paper.pdf). Advances in neural information processing systems. 2014.
15. D. P. Kingma & J. Ba. [Adam: A method for stochastic optimization](https://arxiv.org/pdf/1412.6980.pdf). International Conference for Learning Representations. 2015.
16. M. Vazirgiannis. INF554 lecture notes. Machine Learning 1. Polytechnique. 2016.
17. S. Gaiffas. MAP569 lecture notes. Machine Learning 2. Polytechnique. 2017.