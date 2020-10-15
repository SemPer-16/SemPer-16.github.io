---
layout: post
title: Inner Product 
subtitle: Covariance and R square
tags: [Data Science,Theory,Covariance,inner product,Basic]
comments: true
permalink: /Data_Science/Theory/1/
---

## Derive covariance is inner product and R$^2$ by dot product

<br>


### 1. Covariance == inner product?



Let vector space $V'=Span_\mathbb{R}(Z_1,Z_2,Z_3...Z_n), n\in \mathbb{R}$

Then, we need to prove that $cov(Z_i,Z_j), i\neq j, (i,j)\in\mathbb{R}^2$ is inner product on $V'$

<br>

##### Inner product [^1]

Assume that there is a bilinear mapping $\Omega$ which is linear in each argument.

i.e., in vector space $V$ which holds that for all $\boldsymbol{x},\boldsymbol{y},\boldsymbol{z} \in V, \lambda, \psi \in \mathbb{R}$,

$$
\Omega(\lambda\boldsymbol{x}+\psi \boldsymbol{y},\boldsymbol{z})=\lambda \Omega(\boldsymbol{x},\boldsymbol{z})+\psi \Omega(\boldsymbol{y},\boldsymbol{z}) \\
\Omega(\boldsymbol{x},\lambda \boldsymbol{y}+\psi \boldsymbol{z})=\lambda \Omega(\boldsymbol{x},\boldsymbol{y})+\psi \Omega(\boldsymbol{x},\boldsymbol{z})
$$

<br>

###### symmetric, positive definite

Continue that $V$ is a vector space and $\Omega\ : \ V\times V \rightarrow \mathbb{R}$ is a bilinear mapping Then

- $\Omega$ is called $symmetric$ if $\Omega(\boldsymbol{x},\boldsymbol{y})=\Omega(\boldsymbol{y},\boldsymbol{x}),\ \forall \boldsymbol{x},\boldsymbol{y} \in V$.
- $\Omega$ is called $positive\ definite$ if

$$
\forall \boldsymbol{x}\in V\setminus\{\boldsymbol{0}\} : \Omega(\boldsymbol{x},\boldsymbol{x})>0, \ \ \Omega(\boldsymbol{0},\boldsymbol{0})=0
$$


- A  positive definite, symmetric bilinear mapping $\Omega\ : \ V\times V \rightarrow \mathbb{R}$ is called an $inner\ product$ on $V$, writing $\Omega(\boldsymbol{x},\boldsymbol{y})$ as $\langle \boldsymbol{x},\boldsymbol{y}\rangle$


<br>

#### Proof

We know that covariance is linear and symmetric bilinear mapping by properties of covariance.[^2]

For positive definite is

$$
\forall Z \in V'\setminus \{\boldsymbol{0}\}:Cov(Z,Z)=E[(z-\mu)^2]>0, Cov(\boldsymbol{0},\boldsymbol{0})=0\iff \forall Z_i,Z_j \in V, \ Z_i \bot \bot Z_j
$$

$$
\therefore \ \forall Z_i,Z_j ,\ [Cov(Z_i,Z_j) \Rightarrow \langle Z_i,Z_j\rangle ]\iff \in V', \ Z_i \bot \bot Z_j
$$

So, Covariance is inner product when principle components are statistically independent.

<br>

### 2. Relation of R^2 and $\vec{\hat{Y}},\vec{Y}$


$\vec{\hat{Y}}$ is estimated $Y$ vector and $\vec{Y}$ is original $Y$ vector as

$$
(\vec{\hat{Y}},\ \vec{Y}) = ((\hat{Y_1}.....,\hat{Y_n}) ,(Y_1.....,Y_n))
$$

Translate as

$$
(\vec{\hat{Y}},\ \vec{Y}) := (\vec{\hat{Y}},\ \vec{Y}) \rightarrow (\vec{\hat{Y}}-\vec{\bar{Y}},\ \vec{Y}-\vec{\bar{Y}})
$$

Then, dot product of $\vec{\hat{Y}},\ \vec{Y}$ is

$$
\vec{\hat{Y}}\cdot \vec{Y}=\sum_i(\hat{Y_i}-\bar{Y})(Y_i-\bar{Y})=\sqrt{\sum_i{(\hat{Y_i}-\bar{Y})^2}}\cdot\sqrt{\sum_i{(Y_i-\bar{Y})^2}}\cdot cos\phi
$$

$$
\therefore cos\phi = \frac{\sum_i(\hat{Y_i}-\bar{Y})(Y_i-\bar{Y})}{\sqrt{\sum_i{(\hat{Y_i}-\bar{Y})^2}}\cdot\sqrt{\sum_i{(Y_i-\bar{Y})^2}}}=r(Y,\hat{Y})
$$

And as we know, $r^2(Y,\hat{Y})$ is $R^2$.

$$
\therefore \ cos^2\phi_{\vec{\hat{Y}}\cdot \vec{Y}}=R^2
$$

<br>

***

***

[^1]: A. Aldo Faisal, Cheng Soon Ong, and Marc Peter Deisenroth (2020), Mathematics for Machine Learning, Cambridge. p. 59-60. ISBN 978-1-108-45514-5.  
[^2]: [https://www.hindawi.com/journals/isrn/2011/323864/](https://www.hindawi.com/journals/isrn/2011/323864/)

