---
title: 流固耦合运动绘图
slug: paraview-plot-deformation
# description: 画双心室的纤维图
date: 2024-09-24 00:00:00+0000
lastmod: 2024-09-25 22:36:00+0000
categories:
    - paraview
tags:
image: 2153815980797591552.jpeg
---
浏览量：<span id="ArtalkCount"></span>
评论数：<span id="ArtalkPV"></span>

需要画流体的流线图和固体的形变图。
流线图用 Mask Points 和 Stream Tracer With Custom Source 绘制, 这两个 Filter 的使用可以参考[画双心室的纤维图](https://hugo.pengfeima.cn/p/paraview-plot-streamline/)。形变图用 Warp By Vector 绘制。


{{< myfigure src="https://githubimages.pengfeima.cn/images/compressed/202409252219613.webp" title="导入流体和固体的数据" percent="60%">}}

{{< myfigure src="https://githubimages.pengfeima.cn/images/compressed/202409252220375.webp" title="计算固体形变" percent="60%">}}





- WIP：下面这些图的教程

![image-20240928105008567](https://githubimages.pengfeima.cn/images/202409281050653.png)



![image-20240928104922924](https://githubimages.pengfeima.cn/images/202409281049017.png)



![image-20240928104742963](https://githubimages.pengfeima.cn/images/202409281047106.png)


- 速度等高图
![image-20240928110037029](https://githubimages.pengfeima.cn/images/202409281100167.png)
![image-20240928110253889](https://githubimages.pengfeima.cn/images/202409281102000.png)
![image-20240928104852205](https://githubimages.pengfeima.cn/images/202409281048332.png)



下载数据: [paraview-fsi-plot.001.zip](https://pan.quark.cn/s/461a633eb6b4)


