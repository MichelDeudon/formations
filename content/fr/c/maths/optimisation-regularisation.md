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

Optimisation et régularisation des modèles

<!--more-->

## Optimisation et régularisation des modèles

{{< icon name="clock" pack="fas" >}} 12h, 6x2h par semaine

{{< figure src="super-resolution/img2.jpg" caption="Deudon, M., Kalaitzis, A., Goytom, I., Arefin, M. R., Lin, Z., Sankaran, K., ... & Bengio, Y. (2020). [Highres-net: Recursive fusion for multi-frame super-resolution of satellite imagery](https://arxiv.org/pdf/2002.06460.pdf). arXiv preprint arXiv:2002.06460.">}}

### Cours

{{% staticref "uploads/TW233MI_Optimisation_regularisation.pdf" %}}Optimisation et régularisation des modèles{{% /staticref %}}.

#### 1 Définitions et notations
##### 1.1 Rappel sur les fonctions
##### 1.2 Dérivés
#### 2 Apprentissage en ML
#### 3 Optimisation en ML
##### 3.1 Hypothèse iid
##### 3.2 Algorithme de descente de gradient
##### 3.3 Algorithme de Newton
##### 3.4 Cas de la régression linéaire
##### 3.5 Descente de Gradient Stochastique (SGD)
#### 4 Régression Logistique
##### 4.1 Iteratively Reweighted Least Squares (IRLS)
#### 5 Régularisation en ML
##### 5.1 Pourquoi régulariser?
##### 5.2 Disgression sur l’évaluation en ML
##### 5.3 Reformulation du problème d’optimisation
##### 5.4 Autre forme de régularisation: Ensembling
#### 6 Optimisation sous contraintes
#### 7 Méthodes bayésiennes

### TP / Pratique 

{{< icon name="github" pack="fab" >}} [tw233mi-regularisation-optimisation](https://github.com/MichelDeudon/tw233mi-regularisation-optimisation)

#### TP1. [Régression logistique, de A à Z](https://github.com/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td1-logistic-regression-az.ipynb)
#### TP2. [Méthodes du premier ordre pour la régression logistique](https://github.com/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td2-regularized-logistic-regression.ipynb)
#### TP3. [Régression logistique régularisée, de A à Z](https://github.com/MichelDeudon/tw233mi-regularisation-optimisation/blob/main/td/td3-regularized-logistic-regression.ipynb)

### TD / Exercices

À venir.

### Références
- 1. J. Wallis. A treatise of algebra, both historical and practical. London. 1685.
- 2. W. S. McCulloch & W. Pitts. A logical calculus of the ideas immanent in nervous activity. The bulletin of mathematical biophysics. 1943.
- 3. Berkson, J. Application of the logistic function to bio-assay. Journal of the American statistical association. 1944.
- 4. C. Lanczos. An Iteration Method for the Solution of the Eigenvalue Problem of Linear Differential and Integral Operators, Journal of Research of the National Bureau of Standards. 1950.
- 5. H. Robbins & S. Monro. A stochastic approximation method. The annals of mathematical statistics. 1951.
- 6. C. Lanczos. Solution of Systems of Linear Equations by Minimized Iterations. Journal of Research of the National Bureau of Standards. 1952.
- 7. M. R. Hestenes & E. L. Stiefel. Methods of Conjugate Gradients for Solving Linear Systems, Journal of Research of the National Bureau of Standards. 1952.
- 8. A. E. Hoerl & R. W. Kennard. Ridge regression: Biased estimation for nonorthogonal problems. Technometrics. 1970.
- 9. R. Tibshirani. Regression shrinkage and selection via the lasso. Journal of the Royal Statistical Society. 1996.
- 10. W. J. Fu. Penalized regressions: the bridge versus the lasso. Journal of computational and graphical statistics. 1998.
- 11. F. Pedregosa, G. Varoquaux, A. Gramfort et al. Scikit-learn: Machine learning in Python. The Journal of Machine Learning Research. 2011.
- 12. N. Freitas. CPSC540 lecture notes. University of British Columbia. 2012.
- 13. R. Johnson & T. Zhang. Accelerating stochastic gradient descent using predictive variance reduction. Advances in neural information processing systems. 2013.
- 14. A. Defazio, F. Bach, & S. Lacoste-Julien. SAGA: A fast incremental gradient method with support for non-strongly convex composite objectives. Advances in neural information processing systems. 2014.
- 15. D. P. Kingma & J. Ba. Adam: A method for stochastic optimization. International Conference for Learning Representations. 2015.
- 16. M. Vazirgiannis. INF554 lecture notes. Machine Learning 1. Polytechnique. 2016.
- 17. S. Gaiffas. MAP569 lecture notes. Machine Learning 2. Polytechnique. 2017.