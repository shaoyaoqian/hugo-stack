---
title: "Navier Stokes 算例"
description: 一些 Navier Stokes 算例
slug: navier-stokes-demos
date: 2024-09-28 22:42:25
lastmod: 2024-09-29 22:42:25
math: true
draft: false
hidden: false
comments: true
readingTime: true
image:
categories:
tags:
toc: true
---




## 二维解析解

1. 

$$
\Omega=[ 0, 1 ] \times[ 0, 1 ], \, \mathrm{T}=0. 1 \mathrm{s},
$$

$$
\left\{\begin{array} {l} {{{u_{1} ( x, y, t )=-\operatorname{e x p} ( t ) x^{2} ( x-1 )^{2} y ( y-1 ) ( 2 y-1 ) / 2 5 6}}} \\ {{{u_{2} ( x, y, t )=\operatorname{e x p} ( t ) x ( x-1 ) ( 2 x-1 ) y^{2} ( y-1 )^{2} / 2 5 6}}} \\ {{{p ( x, y, t )=\operatorname{e x p} ( t ) ( x^{3}-1 / 4 )}}} \\ \end{array} \right.
$$

2. 

$$
\Omega=[0,1] \times[0,1], \mathrm{T}=0.1 \mathrm{~s},
$$

$$
\begin{aligned}
& \qquad\left\{\begin{array}{l}
u_1(x, y, t)=\exp (t) \sin ^2(\pi x) \sin (2 \pi y) \\
u_2(x, y, t)=-\exp (t) \sin (2 \pi x) \sin ^2(\pi y) \\
p(x, y, t)=\exp (t)(\sin (\pi y)-2 / \pi)
\end{array}\right.
\end{aligned}
$$

3. 

$$
\Omega=[0,1] \times[0,1], \mathrm{T}=0.1 \mathrm{~s}
$$

$$
\begin{aligned}
\qquad\left\{\begin{array}{l}
u_1(x, y, t)=20 x^2(x-1)^2 y(y-1)(2 y-1) t \\
u_2(x, y, t)=-20 x(x-1)(2 x-1) y^2(y-1)^2 t \\
p(x, y, t)=10(2 x-1)(2 y-1)
\end{array}\right.
\end{aligned}
$$

4. 

$$
\Omega=[0,1] \times[0,1], \mathrm{T}=0.1 \mathrm{~s}
$$

$$
\begin{aligned}
& \qquad\left\{\begin{array}{l}
u_1(x, y, t)=20 x^2(x-1)^2 y(y-1)(2 y-1) t \\
u_2(x, y, t)=-20 x(x-1)(2 x-1) y^2(y-1)^2 t \\
p(x, y, t)=10(2 x-1)(2 y-1) t
\end{array}\right.
\end{aligned}
$$

5. 

$$
\Omega=[0,1] \times[0,1], \mathrm{T}=0.1 \mathrm{~s}
$$

$$
\begin{aligned}
\qquad\left\{\begin{array}{l}
u_1(x, y, t)=2 \pi \sin ^2(\pi x) \sin (\pi y) \cos (\pi y) \cos (t) \\
u_2(x, y, t)=-2 \pi \sin (\pi x) \cos (\pi x) \sin ^2(\pi y) \cos (t) \\
p(x, y, t)=\cos (\pi x) \cos (\pi y)
\end{array}\right.
\end{aligned}
$$

7. [p. 389.] [^1]

$$
\begin{aligned}
& u=\left[\begin{array}{c}
\sin (4 \pi x) \cos (4 \pi y) \\
-\cos (4 \pi x) \sin (4 \pi y)
\end{array}\right] \\
& p=\pi \cos (4 \pi x) \cos (4 \pi y)
\end{aligned}
$$

8. Taylor–Green vortex[^2]
$$
\Omega=[-1,1] \times[-1,1], \mathrm{T}=0.5, \nu=0.01
$$

$$
\begin{aligned}
& u(x, y, t)=\left(\cos (\pi x) \sin (\pi y) e^{-2 t v \pi^2}, \cos (\pi y) \sin (\pi x) e^{-2 t v \pi^2}\right) \\
& p(x, y, t)=-0.25(\cos (2 \pi x)+\cos (2 \pi y)) e^{-4 t v \pi^2}
\end{aligned}
$$

8. 

$$
\Omega=[0,2] \times[-1,1], \mathrm{T}=0.1, \mu=0.01 .
$$

$$
\begin{aligned}
& \qquad\left\{\begin{array}{l}
u=2 \cos (\pi y) \sin (\pi x) \sin t \\
v=-2 \sin (\pi y) \cos (\pi x) \sin t \\
p=2 \sin (\pi y) \sin (\pi x) \cos t
\end{array}\right.
\end{aligned}
$$

9. 

$$
\Omega=[0,1] \times[-0.25,0], \mathrm{T}=0.1 \mathrm{~s}
$$

$$
\begin{aligned}
& \qquad\left\{\begin{array}{l}
u_1=\left(x^2 y^2+e^{-y}\right) \cos (2 \pi t) \\
u_2=\left[-\frac{2}{3} x y^3+2-\pi \sin (\pi x)\right] \cos (2 \pi t) \\
p=-[2-\pi \sin (\pi x)] \cos (2 \pi y) \cos (2 \pi t)
\end{array}\right.
\end{aligned}
$$

10. 

$$
\begin{aligned}
&u_{1}=\left(x^{2} y^{2}+e^{-y}\right) \cos (2 \pi t) \\
&u_{2}=\left[-\frac{2}{3} x y^{3}+2-\pi \sin (\pi x)\right] \cos (2 \pi t) \\
&p=-[2-\pi \sin (\pi x)] \cos (2 \pi y) \cos (2 \pi t)
\end{aligned}
$$

11. Kovasznay flow [^4], 用于验证SAV方法的无条件能量稳定

$$
\left\{\begin{array}{l}
u=1-e^{\lambda x} \cos (2 \pi y) \\
v=\frac{\lambda}{2 \pi} e^{\lambda x} \sin (2 \pi y) \\
p=\frac{1}{2}\left(1-e^{2 \lambda x}\right)
\end{array}\right.
$$





## 三维解析解

1. 
$$
\begin{aligned}
p(x) &=\cos \left(\pi x_{1}\right) \cos \left(\pi x_{2}\right) \cos \left(\pi x_{3}\right), \\
u_{1}(x) &=\pi^{2}\left(\sin \left(\pi x_{1}\right)\right)^{2} \sin \left(2 \pi x_{2}\right) \sin \left(2 \pi x_{3}\right), \\
u_{2}(x) &=-0.5 \pi^{2} \sin \left(2 \pi x_{1}\right)\left(\sin \left(2 \pi x_{2}\right)\right)^{2} \sin \left(\pi x_{3}\right), \\
u_{3}(x) &=-0.5 \pi^{2} \sin \left(2 \pi x_{1}\right) \sin \left(2 \pi x_{2}\right)\left(\sin \left(\pi x_{3}\right)\right)^{2} .
\end{aligned}
$$

2. 

$$
\begin{aligned}
&\left.\boldsymbol{u}=\left(y^{4}+z^{2}\right) e^{-t},\left(z^{4}+x^{2}\right) e^{-t},\left(x^{4}+y^{2}\right) e^{-t}\right) . \\
&p=(2 x-1)(2 y-1)(2 z-1) e^{-t},
\end{aligned}
$$

3. Beltrami flow[^3]，由 Ethier 和 Steinmann 于1994年提出，计算区域为 [-1,1]x[-1,1]x[-1,1] ，它速度和压强的精确解为


$$
\begin{aligned}
&u(x, y, z, t)=-a\left[e^{a x} \sin (a y+d z)+e^{a z} \cos (a x+d y)\right] e^{-d^{2} t} \\
&v(x, y, z, t)=-a\left[e^{a y} \sin (a z+d x)+e^{a x} \cos (a y+d z)\right] e^{-d^{2} t} \\
&w(x, y, z, t)=-a\left[e^{a z} \sin (a x+d y)+e^{a y} \cos (a z+d x)\right] e^{-d^{2} t} 
\end{aligned}
$$

$$
\begin{aligned}
p(x, y, z, t)=-a^{2} e^{-2 d^{2} t}\left(e^{2 a x}+e^{2 a y}+e^{2 a z}\right)(& \sin (a x+d y) \cos (a z+d x) e^{a(y+z)} \\
&\left.+\sin (a y+d z) \cos (a x+d y) e^{a(x+z)}+\sin (a z+d x) \cos (a y+d z) e^{a(x+y)}\right)
\end{aligned}
$$


## 泊肃叶流(WIP)



## 方腔驱动流(WIP)



## 圆柱绕流(WIP)



























[^1]: [Automated Solution of Differential Equations by the Finite Element Method. p. 389.]
[^2]: [Automated Solution of Differential Equations by the Finite Element Method. Chapter. 21.4.4] 
[^3]: [Automated Solution of Differential Equations by the Finite Element Method. Chapter. 21.4.6]
[^4]: Numerical approximation of incompressible Navier-Stokes equations based on an auxiliary energy variable
