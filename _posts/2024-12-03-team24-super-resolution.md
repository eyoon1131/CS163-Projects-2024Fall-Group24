---
layout: post
comments: true
title: Super Resolution
author: Eliot Yoon, Yubo Zhang, Ben Liang, William Park
date: 2024-12-03
---


> Super Resolution is an image processing technique that enhances/restores a low resolution image to a higher resolution. We will look at the design and architecture of one of the current cutting-edge models, HAT, and compare its performance to models with different architectures and features.


<!--more-->
{: class="table-of-content"}
* TOC
{:toc}

## Introduction
Super resolution is a classical low level image processing task that has been studied for decades. However, the classical model, which assumes a relatively simplistic degradation process from a high resolution to a low resolution image, fails to capture the complex image degradation process of the real world. Convolutional neural networks are better equipped to handle these issues, but still face their own limitations. The recent shift to transformer-based models in deep learning has led to cutting-edge performance in super resolution tasks by capturing long-range dependencies in images. This is the chosen architecture of the HAT model, which utilizes channel attention, self-attention, and overlapping cross-attention to activate more input pixels than other transformer-based models. In this paper we will take an in-depth look at these mechanisms and compare HAT to another transformer-based state-of-the-art model, DRCT, as well as the CNN-based model SRCNN.

Your survey starts here. You can refer to the [source code](https://github.com/lilianweng/lil-log/tree/master/_posts) of [lil's blogs](https://lilianweng.github.io/lil-log/) for article structure ideas or Markdown syntax. We've provided a [sample post](https://ucladeepvision.github.io/CS188-Projects-2022Winter/2017/06/21/an-overview-of-deep-learning.html) from Lilian Weng and you can find the source code [here](https://raw.githubusercontent.com/UCLAdeepvision/CS188-Projects-2022Winter/main/_posts/2017-06-21-an-overview-of-deep-learning.md)

## Basic Syntax
### Image
Please create a folder with the name of your team id under /assets/images/, put all your images into the folder and reference the images in your main content.

You can add an image to your survey like this:
![YOLO]({{ '/assets/images/UCLAdeepvision/object_detection.png' | relative_url }})
{: style="width: 400px; max-width: 100%;"}
*Fig 1. YOLO: An object detection method in computer vision* [1].

Please cite the image if it is taken from other people's work.


### Table
Here is an example for creating tables, including alignment syntax.

|             | column 1    |  column 2     |
| :---        |    :----:   |          ---: |
| row1        | Text        | Text          |
| row2        | Text        | Text          |



### Code Block
```
# This is a sample code block
import torch
print (torch.__version__)
```


### Formula
Please use latex to generate formulas, such as:

$$
\tilde{\mathbf{z}}^{(t)}_i = \frac{\alpha \tilde{\mathbf{z}}^{(t-1)}_i + (1-\alpha) \mathbf{z}_i}{1-\alpha^t}
$$

or you can write in-text formula $$y = wx + b$$.

### More Markdown Syntax
You can find more Markdown syntax at [this page](https://www.markdownguide.org/basic-syntax/).

## Reference
Please make sure to cite properly in your work, for example:

[1] Redmon, Joseph, et al. "You only look once: Unified, real-time object detection." *Proceedings of the IEEE conference on computer vision and pattern recognition*. 2016.

---
