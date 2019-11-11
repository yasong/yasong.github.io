---
layout: post
title:  "Knowledge about Similarity"
date:   2019-11-08 19:18:36 +0530
categories: hash binary similarity
---
This blog is the note of learning the Similarity, which includes hash, Jaccard Index, LSH, Hungarian Method, MinHash, SimHash and etc.



#### 1. Jaccard Index (雅卡尔指数)
aka. **Intersection over Union**, **Jaccard similarity coefficient**    

**key word:**    

- gauge the similarity and deversity of sample sets.
- finite sample sets.


![Jaccard Index](https://raw.githubusercontent.com/yasong/pics/master/blog/JI.png) 
<img src="https://latex.codecogs.com/gif.latex?0\leq&space;J(A,B)\leq&space;1" title="0\leq J(A,B)\leq 1" />   

If **A** and **B** are both empty, define <img src="https://latex.codecogs.com/gif.latex?J(A,B)=&space;1" title="J(A,B)= 1" />

**Jaccard distance:**

measure the dissimilarity between sample sets.    

![Jaccard distance](https://raw.githubusercontent.com/yasong/pics/master/blog/JD.png) 

**Similarity of asymmetric binary attributes**

<img src="https://latex.codecogs.com/gif.latex?J&space;=&space;\frac{M_{11}}{M_{01}&plus;M_{10}&plus;M_{11}}" title="J = \frac{M_{11}}{M_{01}+M_{10}+M_{11}}" />    

<img src="https://latex.codecogs.com/gif.latex?d_J&space;=&space;\frac{M_{0}&plus;M_{10}}{M_{01}&plus;M_{10}&plus;M_{11}}&space;=&space;1&space;-&space;J" title="d_J = \frac{M_{0}+M_{10}}{M_{01}+M_{10}+M_{11}} = 1 - J" />

#### 2. Simple matching coefficient (简单匹配系数SMC)

<img src="https://latex.codecogs.com/gif.latex?SMC&space;=&space;\frac{number&space;\&space;of&space;\&space;matching&space;\&space;attributes}{number&space;\&space;of&space;\&space;attributes}\\\\=&space;\frac{M_{00}&plus;M_{11}}{M_{00}&plus;M_{01}&plus;M_{10}&plus;M_{11}}" title="SMC = \frac{number \ of \ matching \ attributes}{number \ of \ attributes}\\\\= \frac{M_{00}+M_{11}}{M_{00}+M_{01}+M_{10}+M_{11}}" />

![SMC](https://raw.githubusercontent.com/yasong/pics/master/blog/SMC.png) 

**simple matching distance (SMD)**, which measures dissimilarity between sample sets, is given by **1 - SMC** 

**Difference with the Jaccard index:**    

SMC calcutes the attribute without in both sets.

#### 3. Hamming distance （汉明距离）
In information theory, the Hamming distance between two strings of equal length is the number of positions at which the corresponding symbols are different.  In other words, it measures the minimum number of substitutions required to change one string into the other, or the minimum number of errors that could have transformed one string into the other. In a more general context, the Hamming distance is one of several string metrics for measuring the edit distance between two sequences. It is named after the American mathematician Richard Hamming.    
For example:    
```
"karolin" and "kathrin" is 3.
"karolin" and "kerstin" is 3.
1011101 and 1001001 is 2.
2173896 and 2233796 is 3.
```
#### 4. MinHash


#### 5. LSH (Locality-Sensitive Hashing, LSH)
Reference:     
1. [Locality_Sensitive Hashing](https://towardsdatascience.com/understanding-locality-sensitive-hashing-49f6d1f6134)
2. [Wikepedia: Locality-sensitive hashing](https://en.wikipedia.org/wiki/Locality-sensitive_hashing)

In computer science, **locality-sensitive hashing (LSH)** is an algorithmic technique that hashes similar input items into the same "buckets" with high probability.


![Hash](https://raw.githubusercontent.com/yasong/pics/master/blog/hash.png) 
From above figure, obviously we can  know the difference between general hashing and locality-sensitive hashing. After two adjacent data in the high-dimensional data space are mapped to the low-dimensional data space, there will be a great probability of remaining adjacent. And two data that are not adjacent to each other will also have a high probability of not adjacent to each other in the low-dimensional space.    
**传统哈希算法**：通过哈希函数尽量让不同的数据映射到不同的桶内，避免冲突的发生。    
**局部哈希算法**：通过哈希函数尽量将两个原先相邻的两个数据能够以较高的概率映射到同一个桶内，相似度低的以极低的概率映射到同一个桶内。

Definition of Locality-sensitive hashing (from wikipedia):
![LSH](https://raw.githubusercontent.com/yasong/pics/master/blog/LSHdefinition.png) 

#### 5. Hungarian Method


- #### SimHash