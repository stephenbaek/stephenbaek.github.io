---
layout: post
title: "ZerNet"
author: "stephenbaek"
permalink: /projects/zernet/
categories: projects
---

# Zernike Convolutional Neural Networks on Arbitrary Surfaces

<center>
<b><span style="font-size:larger;">Zhiyu Sun</span> <sup>1</sup></b>, <b><span style="font-size:larger;">Ethan Rooke</span> <sup>2</sup></b>, <b><span style="font-size:larger;">Yusen He</span> <sup>1</sup></b>, <b><span style="font-size:larger;">Jia Lu</span> <sup>3</sup></b>, and <b><span style="font-size:larger;">Stephen Baek</span> <sup>1</sup></b><br/>
<sup>1</sup> Department of Industrial and Systems Engineering, The University of Iowa<br/>
<sup>2</sup> Applied Mathematical and Computational Sciences, The University of Iowa<br/>
<sup>3</sup> Department of Mechanical Engineering, The University of Iowa<br/>
{zhiyu-sun, ethan-rooke, yusen-he, jia-lu, stephen-baek} (at) uiowa (dot) edu
</center>

<br/>&nbsp;

![](/projects/zernet/img/zernike_convolution.png)

### Abstract
In many fields of science and engineering, geometric features play a key role in understanding certain quantity or phenomena. Thus, an ability to codify geometric features into a mathematical quantity can be critical. Recently, convolutional neural networks (CNNs) have been shown to possess a promising capability of extracting and codifying features from visual information. However, the application of such capable CNNs has been quite limited to mostly computer vision problems where the visual information is inherently given on a grid-like structure. This, unfortunately, was not the case for the geometry processing community, where many visual recognition problems are defined on arbitrary surfaces (2D-manifolds). Technical difficulties hindering the generalization of CNNs to arbitrary-shaped manifold are rooted in the lacks of such key elements including the canonical grid-like representation, the notion of consistent orientation, and a compatible local topology across the domain. Unfortunately, except for a few pioneering works, only very little has been studied in this regard. To this end, in this paper, we propose a novel mathematical formulation to extend CNNs onto two-dimensional (2D) manifold domains. More specifically, we approximate a tensor field defined over a manifold using orthogonal basis functions, called Zernike polynomials, on local tangent spaces. We prove that the convolution of two functions can be represented as a simple dot product between Zernike polynomial coefficients. We also prove that a rotation of a convolution kernel equates to a set of $2\times2$ rotation matrices applied to Zernike polynomial coefficients, which can be critical in manifold domains. As such, the key contribution of this work resides in a concise but rigorous mathematical generalization of the CNN building blocks. Furthermore, comparative to the other state-of-the-art methods, our method demonstrates substantially better performance on both classification and regression tasks.

**Keywords:**  Geometric deep learning, non-Euclidean data, Zernike convolution,  manifold convolutional neural networks

<br/>&nbsp;

![](/projects/zernet/img/manifold_cnn_challenges.png)
<b>Figure 1.</b> Problems associated with manifolds when expanding the notion of convolution. (a) a topological sphere cannot have a grid defined on it without a singularity ($S$); (b) a vector ($v_b$) parallel-transported along a loop ($l$) on a manifold might end up in a different orientation ($v_e$); (c) irregularity of a grid causes varying-size receptive fields.
<br/>&nbsp;

![](/projects/zernet/img/decomposition.png)
<b>Figure 2.</b> Zernike decomposition of a function.

<br/>&nbsp;

![](/projects/zernet/img/FeaStNet_geodesic_error.png)
![](/projects/zernet/img/ZerNet_geodesic_error.png)
<b>Figure 3.</b> Point-wise geodesic error (in percentage of the shape diameter) of ZerNet vs [FeaStNet](https://arxiv.org/abs/1706.05206) on the [FAUST human dataset](http://faust.is.tue.mpg.de).

<br/>&nbsp;

### Publications

#### Journals & Proceedings

0. **ZerNet: Convolutional Neural Networks on Arbitrary Surfaces via Zernike Local Tangent Space Estimation**<br/>
Sun, Z., Rooke, E., He, Y., Lu, J., & Baek, S.<br/>
[arXiv:1812.01082](https://arxiv.org/abs/1812.01082)<br/>
*Working Paper*
{:reversed="reversed"}


#### Conference Presentations

0. **Wall stress estimation in cerebral aneurysm via geometric convolu-tional neural network**<br/>
Baek, S., Sun, Z., & Lu, J.<br/>
In *The 8th World Congress of Biomechanics (WCB2018), Dublin, Ireland, July, 2018.*
{:reversed="reversed"}


<!-- #### Theses/Dissertations

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*New York University, Stern School of Business, New York City, NY, February, 2019.*
{:reversed="reversed"}
-->


<br/>&nbsp;

### Downloads

[PDF](https://arxiv.org/pdf/1812.01082)

Source Code: Will be available soon.