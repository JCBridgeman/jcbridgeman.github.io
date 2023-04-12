---
layout: project
title: invertible bimodule categories
description: A simple, checkable critereon for determining when a given bimodule category is invertible
img: /assets/img/project_thumbs/associatorCMD.png
importance: 1
category: completed
arXiv: 2211.01947
github: https://github.com/JCBridgeman/skeletalData_Bimodule_VecG
publish: true
---
$$\def\cat#1{\mathcal{#1}}$$


#### a simple question

Given a pair of vector spaces $$V,\,W$$, we often want to know if they are isomorphic. One way to witness such an isomorphism is by providing an invertible matrix $$M$$ witnessing the isomorphism. This leads to the question:

> Given an $$ m\times n $$ matrix $$M$$, how can we determine whether it is invertible?

This question is answered in a first course on linear algebra. $$M$$ is invertible if and only if:
1. $$ m = n $$
2. $$ \det M \neq 0$$

---

#### an analogous question

Given a pair of fusion categories $$\cat{C},\, \cat{D}$$, we commonly want to know when they give rise to equivalent Turaev-Viro 3-manifold invariants (or equivalent Levin-Wen theories). 
This equivalence, commonly called *Morita equivalence* can be witnessed by providing an invertible bimodule category $${}_{\cat{C}}\cat{M}_{\cat{D}}$$. This leads to the question:

> Given (unitary) fusion categories $$\cat{C},\, \cat{D}$$, and a bimodule category $${}_{\cat{C}}\cat{M}_{\cat{D}}$$, how can we determine whether it is invertible.

In [arXiv:2211.01947](http://arxiv.org/abs/2211.01947), we give an easily checkable, iff condition for invertiblility in terms of associator data for $$\cat{M}$$. This condition arises from the representation theory of a certain algebra, called the annular algebra, associated to $$ {}_{\cat{C}}\cat{M} $$ as a module category.


