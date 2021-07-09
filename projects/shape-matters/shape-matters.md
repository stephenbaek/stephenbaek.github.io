---
layout: post
title: "Shape Matters"
author: "stephenbaek"
permalink: /projects/shape-matters/
categories: projects
---

# Shape Matters: Evidence from Machine Learning on Body Shape-Income Relationship

<center>
<b><span style="font-size:larger;">Suyong Song</span> <sup>1</sup></b> and <b><span style="font-size:larger;">Stephen Baek</span> <sup>2</sup></b><br/>
<sup>1</sup> Department of Economics, The University of Iowa<br/>
<sup>2</sup> Department of Industrial and Systems Engineering, The University of Iowa<br/>
{suyong-song, stephen-baek} (at) uiowa (dot) edu
</center>

<br/>&nbsp;

![](/projects/shape-matters/img/graphAE.png)

### Abstract
The association between physical appearance and income has been of central interest in social science. However, most previous studies often measured physical appearance using classical proxies from subjective opinions based on surveys. In this study, we use novel data, called CAESAR, which contains three-dimensional (3D) whole-body scans to mitigate possible reporting and measurement errors. We demonstrate the existence of significant nonclassical reporting errors in the reported heights and weights by comparing them with measured counterparts, and show that these discrete measurements are too sparse to provide a complete description of the body shape. Instead, we use a graphical autoencoder to obtain intrinsic features, consisting of human body shapes directly from 3D scans and estimate the relationship between body shapes and family income. We also take into account a possible issue of endogenous body shapes using proxy variables and control functions. The estimation results reveal a statistically significant relationship between physical appearance and family income and that these associations differ across genders. This supports the hypothesis on the physical attractiveness premium in labor market outcomes and its heterogeneity across genders.

**Keywords:**  Physical attractiveness premium, non-Euclidean data, deep machine learning,  graphical autoencoder

<br/>&nbsp;

![](/projects/shape-matters/img/summary.png)
<b>Figure 1.</b> Summary of the estimation results for family income equation. Estimated coefficients and bootstrapped 90% confidence bands are reported. The left panel presents results from the conventional body measures and the right panel reports results from the deep-learned body parameters through the graphical autoencoder.

<br/>&nbsp;

![](/projects/shape-matters/img/reporting_error_height2.png)
![](/projects/shape-matters/img/reporting_error_weight2.png)
<b>Figure 2.</b> Conditional expectation of the reporting errors in height conditional on the true height (<i>top</i>) and weight conditional on the true weight (<i>bottom</i>).

<br/>&nbsp;

![](/projects/shape-matters/img/shape_param.png)
<b>Figure 3.</b> Body shape parameters derived from the graphical autoencoder for male (<i>left</i>) and female (<i>right</i>). 3D body shape models are arranged in accordance with their body shape parameters, with increments of -3 std., -1.5 std., 0, 1.5 std., and 3 std. with respect to the mean in each direction.

<br/>&nbsp;

### Publications

#### Journals & Proceedings

0. **Body Shape Matters: Evidence from Machine Learning on Body Shape-Income Relationship**<br/>
Song, S. & Baek, S.<br/>
*Working Paper*

0. **Economic models with non-Euclidean data**<br/>
Baek, S. & Song, S.<br/>
In *Proceedings of the 2018 Joint Statistical Meetings (JSM2018), Vancouver, Canada, July, 2018.*
{:reversed="reversed"}


#### Conference Presentations

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Baek, S. & Song, S.<br/>
In *Meeting of the Canadian Econometric Study Group, Montreal, Canada, October, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Baek, S. & Song, S.<br/>
In *North American Summer Meeting of Econometric Society, Seattle, WA, June, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Baek, S. & Song, S.<br/>
In *Econometrics Mini-conference at the University of Iowa, Iowa City, IA, May, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Baek, S. & Song, S.<br/>
In *88th Southern Economic Association Annual Meetings (SEA2018), Washington, D.C., November, 2018.*
 
0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Baek, S. & Song, S.<br/>
In *28th Annual Meeting of Midwest Econometrics Group (MEG2018), Madison, WI, October, 2018.*

0. **Estimation of economic models with non-Euclidean data**<br/>
Baek, S. & Song, S.<br/>
In *New Frontiers in Econometrics 2018, Stamford, CT, June, 2018.*
{:reversed="reversed"}


#### Invited Talks/Seminars

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*Korea University, Department of Economics, Seoul, Korea, August, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*Korea Development Institute, Sejong, Korea, August, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*New York University, Stern School of Business, New York City, NY, February, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*Federal Reserve Bank of Kansas City, Kansas City, MO, January, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*Georgia Institute of Technology, Department of Economics, Atlanta, GA, January, 2019.*

0. **Shape matters: Evidence from machine learning on body shape-income relationship**<br/>
*Microsoft Research, Redmond, WA, December, 2018.*
{:reversed="reversed"}



<br/>&nbsp;

### Download

- [Data](data.csv)