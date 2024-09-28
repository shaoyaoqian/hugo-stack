---
title: 相册
slug: image-gallery
description: 用 Markdown 创建一个漂亮的交互式相册
date: 2023-08-26 00:00:01+0000
image: 2153815980856311808.jpeg
categories:
    - gallery
---

插入图像可以使用三种 shortcodes, 分别是:
- 单幅居中
- 单行多幅等高排列
- 瀑布流的相册


## 单幅居中
```markdown
{ {< myfigure src="/p/image-gallery/2153815980856311808.jpeg" title="Image 1" percent="60%">} }
```
{{< myfigure src="/p/image-gallery/2153815980856311808.jpeg" title="Image 1" percent="60%">}}

## 等高排列
Stack 自带语法，参考了 [Typlog](https://typlog.com/), 使用了 [PhotoSwipe](https://photoswipe.com/). 
只支持本地图片，高度固定.

```markdown
![Image 1](2153815980856311808.jpeg) ![Image 2](1.jpg)

![Image 1](2153815980856311808.jpeg) ![Image 2](1.jpg) ![Image 3](2.jpg)
```

![Image 1](2153815980856311808.jpeg)

![Image 1](2153815980856311808.jpeg) ![Image 2](1.jpg)

![Image 1](2153815980856311808.jpeg) ![Image 2](1.jpg) ![Image 3](2.jpg)

## 瀑布流
参考：[Sulv's Blog](https://www.sulvblog.cn/posts/blog/hugo_gallery/)

{{< galleries >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202409232146523.webp" title="壁纸" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242589.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242666.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024439.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024719.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024726.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024839.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242612.webp" >}}
{{< gallery src="https://www.sulvblog.cn/image/17_IMG_20220430_202228.png" >}}
{{< gallery src="https://www.sulvblog.cn/image/19_IMG_20220430_200901.png" >}}
{{< gallery src="https://www.sulvblog.cn/image/16_IMG_20220430_202353.png" title="香克斯" >}}
{{< gallery src="https://www.sulvblog.cn/image/17_IMG_20220430_202228.png" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202409231723244.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152025509.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024158.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242094.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242450.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242688.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242398.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242234.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242455.webp" >}}
{{< gallery src="https://www.sulvblog.cn/image/19_IMG_20220430_200901.png" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202409231826659.webp" title="香克斯" >}}
{{< gallery src="https://www.sulvblog.cn/image/17_IMG_20220430_202228.png" >}}
{{< gallery src="https://www.sulvblog.cn/image/19_IMG_20220430_200901.png" >}}
{{< gallery src="https://www.sulvblog.cn/image/16_IMG_20220430_202353.png" title="香克斯" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024102.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024355.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152243274.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242382.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242599.webp" >}}
{{< gallery src="https://www.sulvblog.cn/image/17_IMG_20220430_202228.png" >}}
{{< gallery src="https://www.sulvblog.cn/image/19_IMG_20220430_200901.png" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202409231633231.webp" title="香克斯" >}}
{{< gallery src="https://www.sulvblog.cn/image/17_IMG_20220430_202228.png" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024001.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024132.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024062.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024391.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152024029.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152243681.webp" >}}
{{< gallery src="https://githubimages.pengfeima.cn/images/compressed/202306152242384.webp" >}}
{{< /galleries >}}

