---
layout: post
title: Nano Mechanical Engineering HW#2
subtitle: Derivation the Hamiltonian of a particle in electric and magnetic fields
tags: [Nano Mechanical Engineering,Lagrangian Mechanics,Lagrange equation,Hamiltonian Mechanics]
comments: true
permalink: /Nano_Mechanical_Engineering/HW/2/
---

## HW #2

#### 2016145001 김승규

The Lagrangian of a particle in electric and magnetic fields is given as

$$
L=\sum_i{\frac12m\dot{x}_i^2}-qV(x_i)+q\sum_i{\dot{x_i}\cdot A_i(x_i)}\\i=1,2,3
$$


We know that the generalized momentum is calculated by

$$
p_k=\frac{\partial{L}}{\partial\dot{q_k}}
$$


So, Generalized momentum will be

$$
p=\begin{bmatrix}\frac{\partial{L}}{\partial{\dot{x_1}}}\\\frac{\partial{L}}{\partial{\dot{x_2}}}\\\frac{\partial{L}}{\partial{\dot{x_3}}}\end{bmatrix}\\=\begin{bmatrix}m\dot{x_1}+qA_1(x_1)\\m\dot{x_2}+qA_2(x_2)\\m\dot{x_3}+qA_3(x_3)\\\end{bmatrix}
$$

Then, we can set the velocity as

$$
\dot{x}=\begin{bmatrix}\frac{p_1-qA_1(x_1)}{m}\\\frac{p_2-qA_2(x_2)}{m}\\\frac{p_3-qA_3(x_3)}{m}\\\end{bmatrix}
$$

On the other hand, the definition of Hamiltonian is

$$
H(p_i,q_i)=\sum_i{p_i\dot{q_i}(p_i,q_i)-L(q_i,\dot{q_i})}
$$

the left-hand side means that we need to change all the velocity in momentum and position.

Then the Hamiltonian will be

$$
H(p_i,q_i)=\sum_i{p_i\cdot(\frac{p_i-qA_i(x_i)}{m})}-\frac{\{p_i-qA_i(x_i)\}^2}{2m}+qV(x_i)-qA_i(x_i)\frac{p_i-qA_i(x_i)}{m}
$$

Finally, simplify the Hamiltonian,

$$
H(p_i,q_i)=\sum_i{\frac{\{p_i-qA_i(x_i)\}^2}{2m}+qV(x_i)}
$$
