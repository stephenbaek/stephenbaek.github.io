---
layout: post
title: Research Areas
author: "stephenbaek"
permalink: /research/
---

# Geometric Data Analysis

![](/projects/zernet/img/zernike_convolution.png)
![](/projects/shape-matters/img/graphAE.png)


Convolutional neural networks (CNN) have demonstrated an unprecedented success in a variety of visual cognition tasks.
Such a success, however, has been concentrated in mostly computer vision and image/signal processing applications,
where one can enjoy a nice, grid-like structure of the data set (signal=1D grid of amplitudes, image=2D grid of pixel values, and such).
Meanwhile, there is a large number of problems that could not benefit much from such powerful CNNs due to the non-Euclidean nature of the data set. 
For instance, graphical models, such as computer graphics objects or computer-aided design (CAD) parts, 
often exist as a boundary representation (B-rep) model in which the geometry of the model is represented by a thin, arbitrary-shaped boundary surface
(2D manifold), rather than a grid-like representation. Hence, there is no canonical way of representing such data in a tensor format as expected by CNNs and, thus, the standard CNNs cannot analyze such data. Point clouds from 3D scanners or LiDAR systems, graphs from social network data, molecular structures of pharmaceutical compounds, protein foldings, and many other non-image type geometric data fall into this category. At the Visual Intelligence Laboratory, we aim to develop mathematical foundations and scalable algorithms to expand CNNs to a variety of different geometric domains. Many scientific studies may benefit from such new capability, including computer-aided design and manufacturing (CAD/CAM), computer graphics, 3D sensing systems on autonomous vehicles, the brain mapping problem in neuroscience, and computational mechanics, just to list a few.


<!--It is hardly a stretch of logic to say many problems in science and engineering begin with reasoning of shapes. We are interested in teaching a computer such “geometric reasoning,” like what human designers and engineers would do when they solve a real-world problem. With an advanced machine cognition, designers and engineers will be able to focus more of their time and power on innovation and better design solutions. Furthermore, we could also learn complex patterns around geometric data that are beyond our cognitive capacity.-->


### Research Projects

<table>
<tr>
  <td colspan="2"><b>Integrating multiscale modeling and experiments to develop a meso-informed predictive capability for explosivessafety and performance ($7.4M)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Air Force Office of Scientific Research Multidisciplinary University Research Initiative Program</td></tr>
<tr><td width="180">Period</td><td>06/2019$\sim$05/2024</td></tr>
<tr><td width="180">Role</td><td>Co-Investigator (PI: Thomas Sewell)</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Machine learning mesoscale structure-property-performance relationships of energetic materials for multiscale modeling of shock-induced detonation ($899,563)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Air Force Office of Scientific Research</td></tr>
<tr><td width="180">Period</td><td>06/2019$\sim$05/2022</td></tr>
<tr><td width="180">Role</td><td>Co-Principal Investigator (PI: H.S. Udaykumar)</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Shape Matters: Evidences from Machine Learning on Body Shape-Income Relationship</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Pending</td></tr>
<tr><td width="180">Project Page</td><td><a href="/projects/shape-matters/">link</a></td></tr>
<tr><td width="180">Collaborator</td><td>Suyong Song, PhD (Department of Economics)</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>ZerNet: Zernike Convolutional Neural Networks</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Old Gold Summer Fellowship</td></tr>
<tr><td width="180">Project Page</td><td><a href="/projects/zernet/">link</a></td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Allen Brain Atlas Project</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Pending</td></tr>
<tr><td width="180">Collaborator</td><td>Thomas Nickl-Jockschat, MD (Department of Psychiatry)</td></tr>
</table>
  
<br/>&nbsp;<br/>&nbsp;<br/>&nbsp;


# Human Performance Analysis

![](/assets/other/invehicle.png)

<!--Each human body can be described through a set of numerical parameters which act similarly to one’s fingerprint. These body shape parameters can be used in a multitude of different scenarios. They can be used in movies, video games, virtual reality, and more to easily create highly realistic avatars and 3D models. These sets can also be analyzed to learn more about how people’s body type is related to their socioeconomic status. We use computational geometry and machine learning techniques to extract such numerical parameters from 3D scans, photographs, etc.-->

### Research Projects

<table>
<tr>
  <td colspan="2"><b>A study on user experience in autonomous driving scenarios ($221,398)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Hyundai Motor Company</td></tr>
<tr><td width="180">Period</td><td>04/2019$\sim$01/2020</td></tr>
<tr><td width="180">Role</td><td>Principal Investigator</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Driver State Detection via Deep Learning ($250,000)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Aisin Technical Center of America</td></tr>
<tr><td width="180">Period</td><td>10/2017$\sim$03/2019</td></tr>
<tr><td width="180">Role</td><td>Principal Investigator</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Developing Connected Simulation to Study Interactions between Drivers, Pedestrians, and Bicyclists ($1.8M)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Department of Transportation Federal Highway Administration (FHWA) Exploratory Advanced Research Program</td></tr>
<tr><td width="180">Period</td><td>10/2017$\sim$09/2019</td></tr>
<tr><td width="180">Role</td><td>Co-Principal Investigator (PI: Daniel V. McGehee)</td></tr>
<tr><td width="180">Summary</td><td>The goal of this project is to develop virtual reality technologies for interactive simulation among subjects within different simulation environments in order to study the road user behaviors for enhancing road safety.</td></tr>
</table>
  
<br/>&nbsp;<br/>&nbsp;<br/>&nbsp;

# Medical Image Analysis

By studying shapes and textures of medical images, it is possible to detect disease and predict clinical outcomes more accurately.
To this end, we are interested in characterizing shapes and textures of diseases in medical images (X-rays, CT, PET, MRI, etc.) and correlate them with other clinical parameters.

- **Lung Cancer Outcome Prediction**
  - **Funding Source**: NIH R21
  - **Collaborators**: Xiaodong Wu, PhD (Department of Electrical and Computer Engineering)<br/>
					   Brian J. Smith, PhD (Department of Biostatistics)<br/>
                       Yusung Kim, PhD, Bryan G. Allen, MD, PhD, John M. Buatti, MD (Department of Radiation Oncology)

- **Interstitial Lung Disease Quantification**
  - **Collaborators**: Changhyun Lee, MD, PhD (Department of Radiology)
  