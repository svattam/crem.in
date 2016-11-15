---
layout: post
title: "l<sub>p</sub>sub> matrix row sampling"
---

Representing data as matrices is ubiquitous in Machine Learning. But the challenge for scalable ML systems is that these structures can become enormous, with millions or hundred of millions of rows. One way to mitigate this problem is to reduce the size of the matrices by leaving out a bunch of rows. But in order for computations on them to yield approximately the right results, the remaining rows have to be in some sense representative of those that were omitted. [Cohen and Peng (2014)](http://arxiv.org/abs/1412.0588) have developed an algorithm to efficiently sample the rows of a matrix while preserving the p-norms of its product with vectors, finding the smallest possible approximation of the original matrix that guarantees reliable computations. They demonstrate that their algorithm is optimal for condensing matrices under any norm. This is an important contribution towards making ML more scalable.
