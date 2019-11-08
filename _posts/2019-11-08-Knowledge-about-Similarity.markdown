---
layout: post
title:  "Knowledge about Similarity"
date:   2019-11-08 19:18:36 +0530
categories: hash binary similarity
---
This blog is the note of learning the Similarity, which includes hash, Jaccard Index, LSH, Hungarian Method, MinHash, SimHash and etc.



- #### Jaccard Index (雅卡尔指数)
aka. **Intersection over Union**, **Jaccard similarity coefficient**
**key word:**
- gauge the similarity and deversity of sample sets.
- finite sample sets.


![Jaccard Index](https://raw.githubusercontent.com/yasong/pics/master/blog/JI.png) 
<img src="https://latex.codecogs.com/gif.latex?0\leq&space;J(A,B)\leq&space;1" title="0\leq J(A,B)\leq 1" /> 
If **A**$** and **B** are both empty, define <img src="https://latex.codecogs.com/gif.latex?J(A,B)=&space;1" title="J(A,B)= 1" />

**Jaccard distance:**
</br>
measure the dissimilarity between sample sets.
![Jaccard distance](https://raw.githubusercontent.com/yasong/pics/master/blog/JD.png) 

**Similarity of asymmetric binary attributes**

<img src="https://latex.codecogs.com/gif.latex?J&space;=&space;\frac{M_{11}}{M_{01}&plus;M_{10}&plus;M_{11}}" title="J = \frac{M_{11}}{M_{01}+M_{10}+M_{11}}" />
</br>
<img src="https://latex.codecogs.com/gif.latex?d_J&space;=&space;\frac{M_{0}&plus;M_{10}}{M_{01}&plus;M_{10}&plus;M_{11}}&space;=&space;1&space;-&space;J" title="d_J = \frac{M_{0}+M_{10}}{M_{01}+M_{10}+M_{11}} = 1 - J" />

- #### Simple matching coefficient (简单匹配系数SMC)

<img src="https://latex.codecogs.com/gif.latex?SMC&space;=&space;\frac{number&space;\&space;of&space;\&space;matching&space;\&space;attributes}{number&space;\&space;of&space;\&space;attributes}\\\\=&space;\frac{M_{00}&plus;M_{11}}{M_{00}&plus;M_{01}&plus;M_{10}&plus;M_{11}}" title="SMC = \frac{number \ of \ matching \ attributes}{number \ of \ attributes}\\\\= \frac{M_{00}+M_{11}}{M_{00}+M_{01}+M_{10}+M_{11}}" />

![SMC](https://raw.githubusercontent.com/yasong/pics/master/blog/SMC.png) 

**simple matching distance (SMD)**, which measures dissimilarity between sample sets, is given by **1 - SMC** 

**Difference with the Jaccard index:**
SMC calcutes the attribute without in both sets.

- #### LSH (Locality-Sensitive Hashing, LSH)

- #### Hungarian Method

- #### MinHash

- #### SimHash