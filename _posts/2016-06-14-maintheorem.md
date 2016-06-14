---
layout: post
author: Dong Yuan
title: 主方法的思考
---

在准备算法考试过程对主方法的学习笔记，并且观察的《算法导论》和_Dasgupta, C._的《Algorithms》上对主方法的一些差异进行一些分析。

## Master Theorem

在CLRS中Master Theorem的写法：

对于$T(n)=aT(n/b) + f(n)$而言，其中$a\geq1$，$b>1$：
1. 若对于某常数$\epsilon$，有$f(n)=O(n^{\log_b{a-\epsilon}})$，则$T(n)=\Theta(n^{\log_ba})$
2. 若$f(n)=\Theta(n^{\log_b{a-\epsilon}})$，则$T(n)=\Theta(n^{\log_ba}\lg{n})$
3. 若对于某常数$\epsilon>0$，有$f(n)=\Omega(n^{\log_b{a-\epsilon}})$，且对常数$c<1$与所有足够大的$n$，有$af(n/b) \leq cf(n)$，则$T(n) = \Theta(f(n))$


在《Algorithms》中写法：

对于$T(n)=aT(\lceil n/b \rceil) + O(n^d)$而言，并且其中$a>0$， $ b>1$ 并且 $d \geq 0$：

$
T(n) = 
\begin{cases}
O(n^d)					& \text{if} d > \log_ba \\
O(n^d\log {n}) 		& \text{if} d = \log_ba \\
O(n^{\log_ba})		& \text{if} d < \log_ba \\
\end{cases}
$

## 主定理的证明

## 两者不同的原因