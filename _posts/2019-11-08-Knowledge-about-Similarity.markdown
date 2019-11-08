---
layout: post
title:  "Knowledge about Similarity"
date:   2019-11-08 19:18:36 +0530
categories: hash binary similarity
---
This blog is the note of learning the Similarity, which includes hash, Jaccard Index, LSH, Hungarian Method, MinHash, SimHash and etc.



- #### Jaccard Index (雅卡尔指数)
aka. **Intersection over Union**, **Jaccard similarity coefficient**</br>
**key word:**
- gauge the similarity and deversity of sample sets.
- finite sample sets.


![Jaccard Index](https://raw.githubusercontent.com/yasong/pics/master/blog/JI.png) 
$0 \leq J(A, B) \leq 1.$ If $A$ and $B$ are both empty, define $J(A,B) = 1$</br>

**Jaccard distance:**</br>
measure the dissimilarity between sample sets.
![Jaccard distance](https://raw.githubusercontent.com/yasong/pics/master/blog/JD.png) 

**Similarity of asymmetric binary attributes**

$$J = \frac{M_{11}}{M_{01}+M_{10}+M_{11}}$$
$$d_J = \frac{M_{0}+M_{10}}{M_{01}+M_{10}+M_{11}} = 1 - J$$
- #### Simple matching coefficient (简单匹配系数SMC)

$$SMC = \frac{number \ of \ matching \ attributes}{number \ of \ attributes}\\\\= \frac{M_{00}+M_{11}}{M_{00}+M_{01}+M_{10}+M_{11}}$$
![SMC](https://raw.githubusercontent.com/yasong/pics/master/blog/SMC.png) 

**simple matching distance (SMD)**, which measures dissimilarity between sample sets, is given by $$1 - SMC$$ 
- #### LSH (Locality-Sensitive Hashing, LSH)

- #### Hungarian Method

- #### MinHash

- #### SimHash