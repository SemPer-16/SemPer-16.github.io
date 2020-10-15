---
layout: post
title: Nano Mechanical Engineering HW#1
subtitle: Derivation of Lorentz force by Lagrange equation
tags: [Nano Mechanical Engineering,Lagrangian Mechanics,Lagrange equation]
comments: true
permalink: /Nano_Mechanical_Engineering/HW/1/
---
## How to derive the equation of motion of Lorentz force by using Lagrange equation
### 14SEP20
<br>

Lagrangian of a particle in electric and magnetic field is


$$
L=\frac12m \dot{\vec{r}}\cdot\dot{\vec{r}}-qV(\vec{r},t)+q\dot{\vec{r}}\cdot\vec{A}({\vec{r}},t)
$$


Lagrange equation is


$$
\frac{d}{dt}\frac{\partial{L}}{\partial{\dot{x}}}=\frac{\partial{L}}{\partial{x}}
$$


In this case,


$$
\dot{x}\rightarrow\dot{\vec{r}} \\
x\rightarrow\vec{r}
$$


So, the equation of motion is


$$
\frac{d}{dt}\frac{\partial{L}}{\partial{\dot{\vec{r}}}}=\frac{\partial{L}}{\partial{\vec{r}}}
$$



On the left-hand side,


$$
\frac{\partial{L}}{\partial{\dot{\vec{r}}}} = m\dot{\vec{r}}+q\cdot\vec{A}(\vec{r},t) \\ \frac{d}{dt}\frac{\partial{L}}{\partial{\dot{\vec{r}}}} = \frac{dm\dot{\vec{r}}}{dt}+q\cdot\frac{d{\vec{A}}}{d{t}} \\\frac{d\vec{A}}{dt}=\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\frac{d{\vec{r}}}{d{t}}+\frac{\partial{\vec{A}}}{\partial{t}} \\ \therefore \frac{d}{dt}\frac{\partial{L}}{\partial{\dot{\vec{r}}}} = \frac{dm\dot{\vec{r}}}{dt}+q\cdot(\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\frac{d{\vec{r}}}{d{t}}+\frac{\partial{\vec{A}}}{\partial{t}})
$$


On the right-hand side,


$$
\frac{\partial{L}}{\partial{\vec{r}}}=-q\cdot\frac{\partial{V}}{\partial{\vec{r}}}+q\cdot\frac{\partial({\dot{\vec{r}}\cdot\vec{A})}}{\partial{\vec{r}}} \\
\frac{\partial{V}}{\partial{\vec{r}}} = \vec{\nabla}V\\\frac{\partial({\dot{\vec{r}}\cdot\vec{A})}}{\partial{\vec{r}}}=\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})\\ \therefore \frac{\partial{L}}{\partial{\vec{r}}}=-q\cdot\vec{\nabla}V+q\cdot\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})
$$


Then, the Equation of motion will be


$$
\frac{dm\dot{\vec{r}}}{dt}+q\cdot(\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\cdot\dot{\vec{r}}+\frac{\partial{\vec{A}}}{\partial{t}}) =-q\cdot\vec{\nabla}V+q\cdot\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A}) \\ \rightarrow\frac{dm\dot{\vec{r}}}{dt} =-q\cdot(\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\cdot\dot{\vec{r}}+\frac{\partial{\vec{A}}}{\partial{t}})-q\cdot\vec{\nabla}V+q\cdot\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})\\
=q\cdot(-\vec{\nabla}V-\frac{\partial{\vec{A}}}{\partial{t}})+q\cdot(\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})-\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\cdot\dot{\vec{r}})
$$



 On the right-hand side, the second term divided by q became


$$
if \ \ \vec{r}=(x,y,z),\\\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})-\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\cdot\dot{\vec{r}}=\begin {bmatrix}\dot{x}\frac{\partial{A_x}}{\partial{x}}+\dot{y}\frac{\partial{A_y}}{\partial{x}}+\dot{z}\frac{\partial{A_z}}{\partial{x}}\\ \dot{x}\frac{\partial{A_x}}{\partial{y}}+\dot{y}\frac{\partial{A_y}}{\partial{y}}+\dot{z}\frac{\partial{A_z}}{\partial{y}}\\ \dot{x}\frac{\partial{A_x}}{\partial{{z}}}+\dot{y}\frac{\partial{A_y}}{\partial{z}}+\dot{z}\frac{\partial{A_z}}{\partial{z}}\end{bmatrix}-\begin{bmatrix}\dot{x}\frac{\partial{A_x}}{\partial{x}}+\dot{y}\frac{\partial{A_x}}{\partial{y}}+\dot{z}\frac{\partial{A_x}}{\partial{z}}\\ \dot{x}\frac{\partial{A_y}}{\partial{x}}+\dot{y}\frac{\partial{A_y}}{\partial{y}}+\dot{z}\frac{\partial{A_y}}{\partial{z}}\\ \dot{x}\frac{\partial{A_z}}{\partial{{x}}}+\dot{y}\frac{\partial{A_z}}{\partial{y}}+\dot{z}\frac{\partial{A_z}}{\partial{z}}\end{bmatrix}\\
=\begin{bmatrix}\dot{y}(\frac{\partial{A_y}}{\partial{x}}-\frac{\partial{A_x}}{\partial{y}})+\dot{z}(\frac{\partial{A_z}}{\partial{x}}-\frac{\partial{A_x}}{\partial{z}})\\ \dot{x}(\frac{\partial{A_x}}{\partial{y}}-\frac{\partial{A_y}}{\partial{x}})+\dot{z}(\frac{\partial{A_z}}{\partial{y}}-\frac{\partial{A_y}}{\partial{z}})\\\dot{x}(\frac{\partial{A_x}}{\partial{z}}-\frac{\partial{A_z}}{\partial{x}})+\dot{y}(\frac{\partial{A_y}}{\partial{z}}-\frac{\partial{A_z}}{\partial{y}})\end{bmatrix} \\=\dot{\vec{r}}\times\vec{B}\\\because\vec{B}=\vec{\nabla}\times\vec{A}=\begin {bmatrix}\frac{\partial{A_z}}{\partial{y}}-\frac{\partial{A_y}}{\partial{z}}\\\frac{\partial{A_x}}{\partial{z}}-\frac{\partial{A_z}}{\partial{x}}\\\frac{\partial{A_y}}{\partial{x}}-\frac{\partial{A_x}}{\partial{y}}\end{bmatrix}
$$

Also,


$$
\vec{F} = \frac{dm{\dot{\vec{r}}}}{dt} = \frac{dm{\vec{v}}}{dt}\\ \vec{E}=-\vec{\nabla}V-\frac{\partial{\vec{A}}}{\partial{t}}
$$

Finally,


$$
\frac{dm{\dot{\vec{r}}}}{dt}=q\cdot(-\vec{\nabla}V-\frac{\partial{\vec{A}}}{\partial{t}})+q\cdot(\vec{\nabla}(\dot{\vec{r}}\cdot\vec{A})-\frac{\partial{\vec{A}}}{\partial{\vec{r}}}\cdot\dot{\vec{r}}) \\\rightarrow\vec{F}=q\vec{E}+q\vec{v}\times\vec{B}
$$

