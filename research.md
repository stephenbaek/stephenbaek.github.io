---
layout: post
title: Research Areas
author: "stephenbaek"
permalink: /research/
---

# Geometric Deep Learning

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


# Physics of Shapes

![](/assets/publications/chun2020gan.gif)

Shapes play a critical role in physics. Microstructural morphology determines mechano-chemical behavior of a material; aerodynamics of a vehicle is affected by the curve of a car silhouette; certain nano-scale texture patterns on a surface can create a liquid behavior that doesn't exist in nature; just to list a few. In the Visual Intelligence Laboratory, we are interested in discovering linkages between shapes and various physical phenomena using the tools of differential geometry and machine learning.

### Research Projects

<table>
<tr>
  <td colspan="2"><b>Investigating the Mechanisms of Particle Energization in Collisionless Heliospheric Shocks ($1.2M)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>National Aeronautics and Space Administration (NASA)</td></tr>
<tr><td width="180">Period</td><td>07/2020$\sim$06/2023</td></tr>
<!-- <tr><td width="180">Role</td><td>Co-Investigator (PI: Gregory Howes)</td></tr> -->
<tr><td width="180">Description</td><td>The goal of this project is to understand physics of collisionless heliospheric shocks by analyzing patterns from space experiments and simulations using convolutional neural networks.</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Integrating multiscale modeling and experiments to develop a meso-informed predictive capability for explosivessafety and performance ($7.5M)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Air Force Office of Scientific Research Multidisciplinary University Research Initiative Program</td></tr>
<tr><td width="180">Period</td><td>06/2019$\sim$05/2024</td></tr>
<!-- <tr><td width="180">Role</td><td>Co-Investigator (PI: Thomas Sewell)</td></tr> -->
<tr><td width="180">Description</td><td>The goal of this project is to develop machine learning capacities to predict safety and performance characteristics of explosives.</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Machine learning mesoscale structure-property-performance relationships of energetic materials for multiscale modeling of shock-induced detonation ($899,563)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Air Force Office of Scientific Research</td></tr>
<tr><td width="180">Period</td><td>06/2019$\sim$05/2022</td></tr>
<!-- <tr><td width="180">Role</td><td>Co-Principal Investigator (PI: H.S. Udaykumar)</td></tr> -->
<tr><td width="180">Description</td><td>In this project, we are looking to learn mesoscale structure-property-performance relationships of energetic materials, such as explosives, propellants, and fuels, using deep neural networks.</td></tr>
</table>

<br/>&nbsp;<br/>&nbsp;<br/>&nbsp;


# Human Performance Analysis

![](/assets/facility/studio360_1.jpg)
![](/assets/other/invehicle.png)

People produce a variety of visual cues both consciously and unconsciously. These visual cues include facial expressions, eye movements, body gestures, motion, and such.
When provided with a context, we can sense emotional and physical states of a person from these cues, such as joy, fatigue, anger, drowsiness, excitement, etc. For example, car companies these days are keen to integrate a technology to detect such visual cues into their advanced driver assistance systems (ADAS) to enhance safety and convenience.
For another example, many studies report that patterns of a body motion are correlated and are thus indicative of the person's performance. Furthermore, sometimes, subtle changes in such motion patterns can be a precursor to a musculoskeltal injury or a similar kind of ergonomic hazard.
Therefore, an accurate sensing and detection of such visual cues can become critical in many applications.
The Visual Intelligence Laboratory is pioneering the research to detect and understand visual cues exhibited by people under different contexts such as driving, manufacturing, etc., by combining state-of-the-art computer vision technologies with their geometric data analysis expertise.


<!--Each human body can be described through a set of numerical parameters which act similarly to one’s fingerprint. These body shape parameters can be used in a multitude of different scenarios. They can be used in movies, video games, virtual reality, and more to easily create highly realistic avatars and 3D models. These sets can also be analyzed to learn more about how people’s body type is related to their socioeconomic status. We use computational geometry and machine learning techniques to extract such numerical parameters from 3D scans, photographs, etc.-->

### Research Projects

<table>
<tr>
  <td colspan="2"><b>A study on user experience in autonomous driving scenarios ($221,398)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Hyundai Motor Company</td></tr>
<tr><td width="180">Period</td><td>04/2019$\sim$01/2020</td></tr>
<!-- <tr><td width="180">Role</td><td>Principal Investigator</td></tr> -->
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Driver State Detection via Deep Learning ($250,000)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Aisin Technical Center of America</td></tr>
<tr><td width="180">Period</td><td>10/2017$\sim$03/2019</td></tr>
<!-- <tr><td width="180">Role</td><td>Principal Investigator</td></tr> -->
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Developing Connected Simulation to Study Interactions between Drivers, Pedestrians, and Bicyclists ($1.8M)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>U.S. Department of Transportation Federal Highway Administration (FHWA) Exploratory Advanced Research Program</td></tr>
<tr><td width="180">Period</td><td>10/2017$\sim$09/2019</td></tr>
<!-- <tr><td width="180">Role</td><td>Co-Principal Investigator (PI: Daniel V. McGehee)</td></tr> -->
<tr><td width="180">Description</td><td>The goal of this project is to develop virtual reality technologies for interactive simulation among subjects within different simulation environments in order to study the road user behaviors for enhancing road safety.</td></tr>
</table>
  
<br/>&nbsp;<br/>&nbsp;<br/>&nbsp;

# Medical Image Analysis
![](/assets/other/tumor_features.png)

By studying shapes and textures of medical images, it is possible to detect disease and predict clinical outcomes more accurately.
To this end, we are interested in characterizing shapes and textures of diseases in medical images (X-rays, CT, PET, MRI, etc.) and correlate them with other clinical parameters.


### Research Projects
<table>
<tr>
  <td colspan="2"><b>NSF Convergence Accelerator - Track D: ImagiQ: Asynchronous and Decentralized Federated Learning for Medical Imaging ($999,770)</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>National Science Foundation</td></tr>
<tr><td width="180">Period</td><td>09/2020$\sim$05/2021 (Phase I)</td></tr>
<!-- <tr><td width="180">Role</td><td>Principal Investigator</td></tr> -->
<tr><td width="180">Description</td><td>The goal of this project is to innovate medical imaging by collaborative model development and validation. To eliminate the hurdle of direct patient data sharing, we advocate a novel decentralized, asynchronous federated learning (FL) scheme.</td></tr>
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Lung Cancer Outcome Prediction</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Pending</td></tr>
<tr><td width="180">Collaborators</td><td>Xiaodong Wu, PhD (Department of Electrical and Computer Engineering)<br/>
					   Brian J. Smith, PhD (Department of Biostatistics)<br/>
                       Yusung Kim, PhD, Bryan G. Allen, MD, PhD, John M. Buatti, MD (Department of Radiation Oncology)</td></tr>
<!-- <tr><td width="180">Role</td><td>Principal Investigator</td></tr> -->
</table>

<br/>

<table>
<tr>
  <td colspan="2"><b>Interstitial Lung Disease Quantification</b></td>
</tr>
<tr><td width="180">Funding Source</td><td>Pending</td></tr>
<tr><td width="180">Collaborator</td><td>Changhyun Lee, MD, PhD (Department of Radiology)</td></tr>
</table>
  