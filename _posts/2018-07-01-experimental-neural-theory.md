---
layout: post
title: "On Neural Networks"
description: "Examining the ideas that make Neural Networks better"
date: 2018-07-01
comments: true
draft: true
---

Why am I writing this?

What will this provide to the average reader?

Have been handed a laundry list of heuristics for Neural Networks. Now, I will systematically examine the theory and experiment with it.

TL;DR: Neural Network research is remarkably ad hoc.

---

## MNIST DATASET

I will first code everything up in pyTorch (using only the array functionality) and subsequently train multiple models in Tensorflow to generat

### Prior to Starting Training

- data normalization and standardization
  (and watching for standardization post and pre split - else  different representations)
  (also what is group sparsity)
- pca and decorrelation etc of data + how it helps representation wise
- weight initializations and effects
- vanishing gradient and training *deep* neural networks
- add more layers - and how neural topology changes shit
- transfer learning and pretraining
- data augmentation for robustness + adverserial attacks!
- shuffling your dataset and how that impacts training vs deterministic order

### Changes to the Computation - Regularization

- regularization - l1, l2, etc. - weight penalties
- weight constraints such as max norm etc.; combinations
- stochastic regularization ie dropout baby
- learning rate decay - step size shebang
  (and using early stopping + why early stopping works)
- different and custom loss functions
- wtf is batch normalization + effects

### Design Considerations

- different activation functions (convex functions vs noncon?)
- different optimizers, ruder article
- hyperparameter jazz - and selection methods
- minibatch vs. stochastic learning approach (noise as a regularizer)
- batchsize and gradient descent with varying batch size vs epochs
(very large batch can reduce generlization ability according to https://arxiv.org/abs/1609.04836)
- Baggings and Boosting


## Things that I have been thinking about for a minute

- pca and decorrelation etc of data + how it helps the data - representation wise
- does removing the bias have any effect
- pca into 2 dimensions and then viz vs viz 2 dimensional data to check
- gradient descent vs searching weight spaces - c.o.dimensionality
- trying random data to check for generalization - Generalization Theory Paper

- universal approximation theorems & breakdown
- different locla minima: deterministic parameters for the mnist data

- the way the decision boundary outside the learnt space fluctates - karpathy like experiment
- can you predict a structure like approximating a variance matrix for some data distribution?

---

Also - check out as a reference (http://theorangeduck.com/page/neural-network-not-working) and the general template.

https://blog.slavv.com/37-reasons-why-your-neural-network-is-not-working-4020854bd607

https://machinelearningmastery.com/improve-deep-learning-performance/



---
