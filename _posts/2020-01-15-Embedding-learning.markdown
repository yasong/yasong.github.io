---
layout: post
title:  "Embedding Learning"
date:   2020-01-15 15:46:36 +0530
categories: machine-learning
---

This blog is the note of learning the embedding.

#### 1. What is embedding?
In mathematics, an embedding (or imbedding) is one instance of some mathematical structure contained within another instance, such as a group that is a subgroup. 在数学上，嵌入是一些数学结构的实例包括另一个实例，例如作为子组的组。或者理解为一个数学结构经过映射包含另一个结构。

In the context of neural networks, embeddings are low-dimensional, learned continuous vector representations of discrete variables. 在深度学习中，嵌入是将离散的高纬度空间向量映射为一个维数较低连续的向量空间。广为人知的词嵌入（Word Embedding）是自然语言处理中语言模型与表征学习技术的统称，概念上是指把一个维数为所有词的数量的高维空间嵌入到一个维数低得多的连续向量空间中，每个单词或词组被映射为实数域上的向量。<sup>[维基百科](https://zh.wikipedia.org/wiki/%E8%AF%8D%E5%B5%8C%E5%85%A5)</sup>

Embedding likes locality sensitive hash. Embedding的性质是使得在距离上相近的两个实例在映射后仍具有相近的含义。例如“数学”的embedding和“语文”的embedding的距离很相近。

此外Embedding还具有数学运算的特性。

