---
layout: post
title: Fluid Dynamics
subtitle: Velocity difference for inside and outside of fluid
tags: [Fluid Dynamics, Bernoulli Equation]
cover-img: /img/fluid_wallpaper.jpg
thumbnail-img: /img/fluid_icon.jpg
share-img: /img/fluid_wallpaper.jpg
comments: true
permalink: /Fluid_Dynamics/across the streamline/
---


![img](https://semper-16.github.io/img/Fluid_Dynamics/River_flow.png){: .mx-auto.d-block :}


초기에 속력이 일정할 때의 안쪽을 1, 바깥쪽을 2라고 하고

꺾인 이후에 안쪽을 3, 바깥쪽을 4라고 해보자.



먼저 1,2 선상에서의 식을 세워보면 다음과 같다. 
$$
R \rightarrow \infin\\
\frac{P_1}{\rho}+\cancelto{0}{\int{\frac{V^2}{R}}dn}+\cancelto 0 {gz}=\frac{P_2}{\rho}+\cancelto{0}{\int{\frac{V^2}{R}}dn}+\cancelto 0 {gz}\\
\therefore P_1=P_2
$$
이후 안쪽 유선 즉 1 -> 3으로 흐르는 유선과 바깥쪽 유선 즉, 2 ->4로 흐르는 유선을 각각 생각해보면


$$
\frac{P_1}{\rho}+\frac12V_1^2+\cancelto0{gz}=C_{13}\\
\frac{P_2}{\rho}+\frac12V_2^2+\cancelto0{gz}=C_{24}\\
P_1=P_2,\ V_1=V_2\\
\therefore C_{13}=C_{24}
$$


이제, 교수님이 증명하셨듯이 3,4 선상에서의 식을 세워보면 다음과 같다.
$$
\frac{dP}{dR}=\frac{\rho V^2}{R}\\
V=V(R)=\alpha R^m\ \ (\alpha>0,m\in\mathbb{R})
$$
이 때, $V_3$와 $V_4$, $P_3$와 $P_4$의 관계는 다음과 같다.
$$
\frac{P_3}{\rho}+\frac12V_3^2=\frac{P_4}{\rho}+\frac12V_4^2\\
\because C_{13}=C_{24}\\
$$



$$
\frac{dP}{dR}=\frac{\rho V^2}{R}\\
\therefore P_3 <P_4\\
if \ P_3<P_4, V_4<V_3\\
\therefore V_4<V_3 \dots Ans
$$

