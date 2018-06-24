---
layout: post
title: "Taxonomizing Machine Learning Research Part I "
description: "A walk through Statistical Learning Theory and the Supervised side of things."
category: articles
comments: false
---

# A Taxonomic Breakdown of Machine Learning Research

## Part I: Statistical Learning (Supervised)

<div class="message">
  This needs to redirect from some central page which has a more in depth overview of this series + why this is being undertaken.
  Like a Ben-Rechtish template in his overview of ML article.
</div>

# Statistical Learning

This is characterized by rigor, a general hate for empiricism - which it substitutes with hardcore theoretical justifications for everything that happens within this space. This is overwhelming concerned with statistical inference surrounding the hypothesis space of our Machine Learning models.

FILL THIS OUT

## Statistical Learning Theory

This is a highly theoretical, mathematically intense approach to Machine Learning. Most introductory Machine Learning courses and textbooks (such as ESL) essentially serve up a diluted version of this branch. Within this framework we look at ML as a task in functional/parametric estimation and we seek probabilistic guarantees on the hypotheses that we learn. All learning algorithms are examined with a heavy emphasis on error bounds and are coupled with rigorous guarantees about the distribution of parameters - and how this distribution varies as we increase the amount of data/when we know about certain properties about the sample data.

! Insert some visual aid.

Topics which fall under this mandate include: the Bias-Variance breakdown of a given family of hypotheses, the nature of the estimators, examining the behavior of a learning algorithm with a rigorous characterization of generalization, overfitting and other defined performance metrics. This also includes concepts like consistency - which are probabilistic guarantees on the convergence of parameters. Examining consistency yields valuable insights into the rate at which learning algorithms generalize (as we vary the size of the dataset), which in turn allows us to construct learning processes which generalize faster.

! P(abs(theta_m  - theta) > epislon) tends to 0 as m tends to infty (where m is the sample size)

[https://openreview.net/pdf?id=rkMt1bWAZ] This is an interesting paper I came across on OpenReview - it breaks down the Bias Variance decomposition for Boltzmann machines - and makes the case that "variance does not necessarily increase when more parameters are included in Boltzmann machines, while the bias always decreases". Insights like these are guarantees on the behavior of "Deep Learning" architectures - which are not always easy to come across.

I imagine that there is a lot of scope for similar work and analysis centered around the more complex, novel learning algorithms which are being put forth at a very high rate and being utilized aggressively in industry. Further areas of research within the domain revolve around the nature of estimators such as in the case of Stochastic Gradient Descent - where we employ an unbiased estimator for the batch gradient at each step.

## Learning Theory

## Regularization Theory

Regularization is the process of limiting your Hypothesis space independently of any beliefs that you might have about the Data. It can be viewed as either expressing a preference for certain sets of Hypotheses with specific parametric properties or as instituting some beliefs about your parameter space in the form of a prior distribution (Maximum A-Posteriori Estimation!). Regularization theory approaches this concept through yet another lens - one that institutes smoothness upon the learned function. The nature of analysis is within the scope of Statistical Learning Theory - wherein learning is viewed as a task in Risk Minimization.

[http://www.svms.org/regularization/EPPV.pdf]
Insert Hilbert Norm Regularization latex definition!
Insert picture of Regularized and Non Regularized functions.

Phenomenon like Early Stopping with gradient based optimizers are also instances of Regularization - as we are limiting the complexity and nuance of the function that is learnt by imposing a constraint in the time domain. For example, this "relatively" recent paper shows that early stopping on Adaboost helps guarantee consistency - and thereby curb overfitting behavior. A high t may cause the learning algorithm to asymptotically converge to a value of prediction error that is larger than Bayes Error.

[https://projecteuclid.org/download/pdf_1/euclid.aos/1079120128]
lim inf PE for adaboost = Bayes Error

This branch of research is open ended - as one may examine regularization and the manner in which it helps curb overfitting for a large number of learning algorithms. Additionally, one may create new forms of regularization for any given learning algorithm too. For example, in Prof. Hastie's paper on Elastic Net regularization [https://web.stanford.edu/~hastie/Papers/B67.2%20(2005)%20301-320%20Zou%20&%20Hastie.pdf], he
starts with an examination of existing methods and the shortcomings - on how LASSO tends to randomly select between variables which have high pairwise correlations. In turn, he proposes a method which selects groups of correlated variables altogether.

Stochastic Regularization Techniques - such as Dropout - have yielded some very impressive results recently.

## Sparsity Enforcing Methods

This ties into the previous sub-taxonomy very tightly.
Sparsity in High Dimensional Spaces.
Group Sparsity .


## Generalization Theory

Allows us to examine the representational capacity and the optimal representational infrastructure for a learning algorithm. Statistical efficiency also creeps into cases like these. The above three areas are basically one and the same - and all fall under the umbrella of Statistical Learning Theory basically. Rate of generalization with increasing dataset sizes.




## Bayesian Methods in Learning

## Causal Inference:

Specifically interesting within the context of Probabilistic Graphical Models (which is yet to appear). This is the rivaling view to the point-estimate "Maximum Likelihood Estimation" manner of doing things.  

## Applied Probability Theory, Stochastic Analysis

## Information Theoretic Approaches


## Imputation

## Denoising

## Kernel Method

This ties very heavily into Representation Learning - and is explored with much greater emphasis within that section. Here, I am going to delve into the Statistical Learning Theoretic exploration of Kernel Methods.


## Metric Learning

## Ranking and Preference Learning

## Similarity and Distance Learning

## Association Rule Learning

## Large Margin Methods



## High Dimensional Statistics

As we move into high dimensional spaces, seemingly large amounts of data becomes surprisingly insufficient with regards to the information it provides about the space it exists in. Intuition breaks down as per the "Curse of Dimensionality": where as the volume of the space increases exponentially - the number of data points become very sparse in comparison to it. Therefore - as a rule of thumb, with every dimension increase in the data space the number of training points should also increase exponentially for good convergence of learning algorithms.

The field of High Dimensional Statistics deals with data such that the ratio "p/n" of the dimension "p" to the sample size "n" is roughly constant - therefore bringing such problems as the above into play. In such cases - the model tends to parameters greater than equal to the number of points within the dataset - which is something to watch out for in the case of prediction. You want to learn sparse decision vectors such that Statistical Theory and Random Vectors are very prominent tools within this field.

Feature Selection and Efficient Bases of Representation of Underlying Data. These considerations are still a very much active considerations within the fields of Statistical Learning - however a lot of the previous compute time concerns have been assuaged. Deep Learning doesn't suffer from the Curse of Dimensionality - due to the Manifold Hypothesis an important result within representation learning.

Curse of Dimensionality and its associated problems are also a subclass within this space. One of the prominent points of contention in this space is the computational complexity and the feasibility of the learning algorithms derived within the space of high dimensional statistics.

## Nonparametric Learning Models:

## Covariance Estimation

Estimating covariance matrices is of pertinence to many statistical methods - ranging from Component/Factor Analysis to certain methods of Regression Analysis and is a of great significance to Economic and Financial Quantitative Researchers. In cases where one has Multivariate Random Variables - one is often required to have a covariance matrix for the corresponding multivariate distribution. Covariance estimation deals with the construction of statistically efficient estimators on the basis of samples from such a multivariate population. Precision Matrices are just the inverse of the covariance matrix (and are essentially meant to symbolize the degree of certainty about the particular component in question) are also important by-products of efficient Covariance Matrix estimators.

This was pretty unexpectedly interesting - and an area that I may certainly want to read about again. Seems like a much more active area of research than one would anticipate it to be.






## Game Theory and Computational Economics

## Hardness of Learning and Approximations

While Statistical Learning Theory does work with Neural Networks, other complex parametric estimation techniques - it is not the central focus or a defining principle of this group.

Active Areas of Research with Statistical Learning Theory and What I am missing here.
