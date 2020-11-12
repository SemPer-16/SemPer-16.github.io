---
layout: post
title: Fluid Dynamics
subtitle: Pressure of the eye of the storm
tags: [Fluid Dynamics, Bernoulli Equation]
cover-img: /img/fluid_wallpaper.jpg
thumbnail-img: /img/fluid_icon.jpg
share-img: /img/fluid_wallpaper.jpg
comments: true
permalink: /Fluid_Dynamics/HW/4/
---

Bernoulli equation for normal to streamline is


$$
\frac{P}{\rho}+\int{\frac{V^2}{r}}dn+gz=C
$$


With ignoring the gravity, differentiate the equation.


$$
\require{cancel}
\frac{P}{\rho}+\int{\frac{V^2}{r}}dn+\cancelto{0}{gz}=C\\
\frac{dP}{\rho}+\frac{V^2}{r}dn=0\\
\therefore dP=-\frac{\rho V^2}{r}dn
$$


the coordinate n points in a direction oppositethat of the radial coordinate so,


$$
dn = -dr\\
\therefore dP=-\frac{\rho V^2}{r}dn=\frac{\rho V^2}{r}dr
$$

The velocity $V(r)$ is defined as

$$
V(r)=\left\{\begin{array}{lr}
V_{max}\cdot\frac{r}{R_0} & \text{for  } 0\leq r\leq R_0\\
V_{max}\cdot\frac{R_0}{r} & \text{for } r>R_0\end{array}\right\}\\
$$

The boundary condition for pressure is

$$
\lim_{r \to \infty }P(r)=P_{atm}
$$


To get $P(0)$


$$
\require{cancel}
\lim_{a \to \infty}\int^{P(a)}_{P(0)}dp=\lim_{a \to \infty}\int^a_0{\frac{\rho V^2}{r}}dr\\
P_{atm}-P(0)=\int^{R_0}_0{\frac{\rho V_{max}^2r}{R_0^2}}dr+\lim_{a \to \infty}\int^a_{R_0}{\frac{\rho V_{max}^2R_0^2}{r^3}}dr\\
= \frac{\rho V_{max}^2}{2R_0^2}(R_0^2-\cancelto{0}{0^2})-\lim_{a \to \infty}\frac{\rho(V_{max}R_0)^2}{2}(\cancelto{0}{\frac{1}{a^2}}-\frac{1}{R_0^2})\\
=\frac{\rho V_{max}^2}{2}+\frac{\rho V_{max}^2}{2}=\rho V_{max}^2\\
\therefore P(0)=P_{atm}-\rho V_{max}^2
$$