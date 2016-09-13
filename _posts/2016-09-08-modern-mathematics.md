---
layout: post
title: Lecture Notes on Modern Mathematics
categories: Mathematics
tags: [Set theory ,Topology]
---

薛江维：数院303，email: xue\_j@whu.edu.cn

教材：*An Introduction to Differential Manifolds and Riemannian Geometry* by *Wiliam W. Boothy*

------

## 集合论
1. 幂集：所有子集组成的集合

	e.g. $$A$$的幂集：$$2^{A}$$
2. 映射：
 - 单射：$$f: A \rightarrow B$$
 - 满射：$$f: A \twoheadrightarrow B$$
 - 双射：$$f: A \leftrightarrow B$$
3. 定义：集合元素个数称为集合的基数（势），记为$$\vert A \vert$$

	命题：如果$$\vert A \vert < \infty$$，则$$\vert 2^A \vert = 2^{\vert A \vert}$$
	1. $$\vert A \vert = \vert b \vert$$，当且仅当存在双射$$f: A \leftrightarrow B$$
	2. 称$$\vert A \vert \leqslant \vert B \vert$$，若存在单射$$f: A \rightarrow B$$
	3. 若$$\vert A \vert \leqslant \vert B \vert$$且$$\vert B \vert \leqslant \vert A \vert$$，则$$\vert A \vert = \vert B \vert$$

4. 定义：满足如下条件之一的集合称为可数集
    1. 如果$$\vert A \vert < \infty$$
    2. 存在$$f: \mathbb{N} \leftrightarrow A$$（无穷可数）

    基本性质：

    1. 可数集的子集一定可数
    2. 可数个可数集的并集一定可数
    3. 有限个可数集的直积可数

    若 $$\underset{ 1 \leqslant i \leqslant n }{S_i}$$ 可数，则 $$S_1\times S_2 \times S_3 \times \dots \times S_n$$ 可数
        
    证明：只要证明$$n=2$$（$$n>2$$归纳）

    e.g. $$Q=\frac{a}{b}.a,b\in \mathbb{Z},b>0,gcd(a,b)=1$$,$$Q$$为可数集

5. 定理：设X={0，1}为两个元素的集合，则。。。
	证明：反证法
6. 定理：设A为一个集合，则 ，即不存在由A到 的满射
	证明：设。。。

## 拓扑学
1. 定义：设X为一个非空集合，X上的一个拓扑T是满足以下性质的子集族
	1. T包含空集及X
	2. T中任意多个元素的并集仍属于T
	3. T中有限个元素的交集仍属于T
	有序对(X,T)被称为一个拓扑空间（若T给定，则简称X为一个拓扑空间），T中的元	素称为开集，开集的补集称为闭集
	e.g. X=R
	* 平凡拓扑
	* 离散拓扑
2. 定义：若T与T'为X上的两个拓扑，如果T'&gt;T，则称T'比T精细，T比T'粗糙
### 拓扑基
1. 定义：称。。。 

