---
layout: post
title: "On Neural Networks"
description: "Experimentally + Theoretically testing everything I have been told about Neural Networks"
date: 2018-07-01
comments: true
---

Have been handed a laundry list of heuristics for Neural Networks.
Now, I will systematically examine the theory and experiment with it.

TL;DR: Neural Network research is remarkably ad hoc.

---

## MNIST DATASET

- data normalization and standardization
  (and watching for standardization post and pre split - else  different representations)
  (also what is group sparsity)
- pca and decorrelation etc of data + how it helps representation wise

- weight initializations and effects
- regularization - l1, l2, etc. max norm etc.
- stochastic regularization ie dropout baby

- learning rate decay - step size shebang
  (and using early stopping + why early stopping works)

- different and custom loss functions
- different activation functions (convex functions vs noncon?)
- different optimizers, ruder article
- wtf is batch normalization + effects
- hyperparameter jazz - and selection methods
- minibatch vs. stochastic learning approach (noise as a regularizer)
- batchsize and gradient descent with varying batch size vs epochs
(very large batch can reduce generlization ability according to https://arxiv.org/abs/1609.04836)

- vanishing gradient and training *deep* neural networks
- add more layers - and how neural topology changes shit
- transfer learning and pretraining
- data augmentation for robustness + adverserial attacks!

## CUSTOM DATASET FOR N=1 CASE EXPERIMENTS

- pca and decorrelation etc of data + how it helps representation wise
- does removing the bias have any effect
- pca into 2 dimensions and then viz vs viz 2 dimensional data to check
- gradient descent vs searching weight spaces - c.o.dimensionality
- trying random data to check for generalization

- shuffling your dataset and how that impacts training vs deterministic order
- universal approximation theorems & breakdown

- locla minima: deterministic parameters for the mnist data
- the way the decision boundary outside the learnt space fluctates - karpathy like experiment
- can you predict a structure like approximating a variance matrix for some data distribution?
- identity function saving in parameters deal - from goodfellow?

---

Also - check out as a reference (http://theorangeduck.com/page/neural-network-not-working) and the general template.



---
