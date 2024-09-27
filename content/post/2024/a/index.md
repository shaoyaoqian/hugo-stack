---
title: 物质点方法
# description: Welcome to Hugo Theme Stack
slug: material-point-method
date: 2024-09-26 15:00:00
# lastmod: 2012-10-09 08:49:00
# image: WechatIMG415.jpg
categories:
tags:
comments: true
math: true
---



<!-- more -->

## 更新形变梯度

根据速度的欧拉描述和拉格朗日描述，
$$
\mathbf{v}(\mathbf{x},t)=\mathbf{V}\left(\chi^{-1}\left(\mathbf{x}, \mathrm{t}\right), \mathrm{t}\right)
\tag{1}
$$

$$
\mathbf{v}\left(\chi\left(\mathbf{X}, \mathrm{t}\right),t\right)=\mathbf{V}\left(\mathbf{X}, \mathrm{t}\right)
\tag{2}
$$

我们可以得到速度与形变梯度的关系:
$$
\frac{\partial}{\partial t} \mathbb{F}\left(\mathbf{X}, t\right)=\nabla_{\mathbf{X}}\mathbf{V}\left(\mathbf{X}, t\right)=\nabla_\mathbf{x} \mathbf{v}(\mathbf{x},t)\mathbb{F}\left(\mathbf{X}, t\right) .
$$

假设我们得到了$t_{n+1}$时刻定义在当前构型$B_{t_{n}}$上的速度为$\mathbf{v}\left(\chi\left(\mathbf{X}, \mathrm{t}\_{n}\right),t\_{n+1}\right)$, (在欧拉网格上求解速度，根据已知的$\chi(\mathbf{X},t_n)$求得), 采用时间离散:
$$
\frac{\partial}{\partial t} \mathbb{F}\left(\mathbf{X}, t_{n+1}\right)=\nabla_\mathbf{x} \mathbf{v}(\chi\left(\mathbf{X}, \mathrm{t}_{n}\right),t_{n+1})\mathbb{F}\left(\mathbf{X}, t_{n}\right) .\tag{6}
$$
将方程 (6) 代入下面式子，
$$
\frac{\partial}{\partial t} \mathbb{F}\left(\mathbf{X}, t^{n+1}\right) \approx \frac{\mathbb{F}^{n+1}-\mathbb{F}^n}{\Delta t}
$$

可以得到
$$
F_p^{n+1}=F_p^n+\Delta t \frac{\partial v^{n+1}}{\partial x}\left(x_p^n\right) F_p^n=\left(I+\Delta t \frac{\partial v^{n+1}}{\partial x}\left(x_p^n\right)\right) F_p^n
$$



and of course if we use the grid based interpolation formula for $\boldsymbol{v}^{\mathfrak{n}+1}$, i.e.,
$$
\begin{aligned}
v^{n+1}(x) & =\sum_i v_i^{n+1} N_i(x) \\
\frac{\partial v^{n+1}}{\partial x}(x) & =\sum_i v_i^{n+1}\left(\frac{\partial N_i}{\partial x}(x)\right)^{\top}
\end{aligned}
$$

then we have

$$
F_p^{n+1}=\left(I+\Delta t \sum_i v_i^{n+1}\left(\frac{\partial N_i}{\partial x}\left(x_p^n\right)\right)^{\top}\right) F_p^n
$$

as the update rule for ${F_p^{\mathfrak{p}}}^{n+1}$ given the $v_i^{n+1}$ and $F_{\mathfrak{p}}^n$.



## 更新位移

## 更新力