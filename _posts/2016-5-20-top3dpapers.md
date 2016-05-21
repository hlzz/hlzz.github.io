---
layout: post
title: Recent Papers in 3D Computer Vision
---

\*   - slightly related
**  - related
*** - very much related 

Lists and details to be extended...

---

![]({{ site.baseurl }}/images/cvpr2016.png)

## CVPR 2016

### Reconstruction:
* ***Vo, M., Narasimhan, S. G., & Sheikh, Y. Spatiotemporal Bundle Adjustment for Dynamic 3D Reconstruction.

*[Project website](http://www.cs.cmu.edu/~ILIM/projects/IM/STBA/), 强烈推荐[video](https://www.youtube.com/watch?v=2m5-IS_xsno)，演员十分癫狂...*

* Hao Wang, Jun Wang, Wang Liang. Online Reconstruction of Indoor Scenes From RGB-D Streams.

* Ali Osman Ulusoy, Michael J. Black, Andreas Geiger. Patches, Planes and Probabilities: A Non-Local Prior for Volumetric 3D Reconstruction.

* Olivier Saurer, Marc Pollefeys, Gim Hee Lee. Sparse to Dense 3D Reconstruction From Rolling Shutter Images.

### Structure-from-Motion:
* A Consensus-Based Framework for Distributed Bundle Adjustment. (no paper yet)

* A Direct Least-Squares Solution to the PnP Problem With Unknown Focal Length. (no paper yet)

* [Mirror Surface Reconstruction under an Uncalibrated Camera](http://i.cs.hku.hk/~kykwong/publications/khan_cvpr16.pdf)

### Feature and Correspondence:
* [Using Spatial Order to Boost the Elimination of Incorrect Feature Matches](http://www.faculty.idc.ac.il/moses/papers/UsingSpatialOrderCameraReady.pdf) 

* Angjoo Kanazawa, David W. Jacobs, Manmohan Chandraker. WarpNet: Weakly Supervised Matching for Single-View Reconstruction.

* Jin Xie, Meng Wang, Yi Fang. Learned Binary Spectral Shape Descriptor for 3D Shape Correspondence.

### Stereo:
* Alex Locher, Michal Perdoch, Luc Van Gool. Progressive Prioritized Multi-View Stereo.

* Cédric Verleysen, Christophe De Vleeschouwer. Piecewise-Planar 3D Approximation From Wide-Baseline Stereo.

### Segmentation and Scene Understanding:
* Ole Johannsen, Antonin Sulc, Bastian Goldluecke. What Sparse Light Field Coding Reveals About Scene Structure.

### Calibration

* Ian Schillebeeckx, Robert Pless. Single Image Camera Calibration With Lenticular Arrays for Augmented Reality.

* Andrey Bushnevskiy, Lorenzo Sorgi, Bodo Rosenhahn. Multicamera Calibration From Visible and Mirrored Epipoles.

### Pose, Rolling Shutter & Other:
* Eric Brachmann, Frank Michel, Alexander Krull, Michael Ying Yang, Stefan Gumhold, Carsten Rother. Uncertainty-Driven 6D Pose Estimation of Objects and Scenes From a Single RGB Image.

* Cenek Albl, Zuzana Kukelova, Tomas Pajdla. Rolling Shutter Absolute Pose Problem With Known Vertical Direction.

* [Optimal Relative Pose with Unknown Correspondences](http://www2.maths.lth.se/vision/publdb/reports/pdf/fredriksson-larsson-etal-ccvpr-16.pdf)

* *Compute epipolar geometry and correspondences at the same time, theoretically interesting.*

* Luca Magri, Andrea Fusiello. Multiple Model Fitting as a Set Coverage Problem.

* Matthew Trager, Martial Hebert, Jean Ponce. Consistency of Silhouettes and Their Duals.

---

![]({{ site.baseurl }}/images/iccv2015.png)

## ICCV 2015

### Tracking and Localization:
* Joseph Tan, D., Tombari, F., Ilic, S., & Navab, N. (2015). A Versatile Learning-Based 3D Temporal Tracker: Scalable, Robust, Online. 

*A tracking algorithm using depth images*

### Optimization
* Diamond, S., & Boyd, S. (2015). Convex Optimization With Abstract Linear Operators. 

*[CVX](https://github.com/cvxgrp/cvxpy), Cone programming, linear transform*

### SfM and Visual SLAM
* Jose Tarrio, J., & Pedre, S. (2015). Realtime Edge-Based Visual Odometry for a Monocular Camera. 

*Edge feature based visual odometry with [code](https://github.com/JuanTarrio/rebvo)*

* Johannsen, O., Sulc, A., & Goldluecke, B. (2015). On Linear Structure from Motion for Light Field Cameras. 

*An application of [Lytro](https://www.lytro.com) cinema.

### Stereo
* Benjamin Ummenhofer and Thomas Brox. Global, Dense Multiscale Reconstruction for a Billion Points.

*Multi-scale surface reconstruction. [Video](https://www.youtube.com/watch?v=y5n7enhxCyo)*

### Reconstruction

* Martin-Brualla, R., Gallup, D., & Seitz, S. M. (2015). 3D Time-Lapse Reconstruction from Internet Photos. 

*Given an Internet photo collection of a landmark, we compute a 3D time-lapse video sequence where a virtual camera moves continuously in time and space. [Project website](http://grail.cs.washington.edu/projects/timelapse3d/)*

* Ikehata, S., Yang, H., & Furukawa, Y. (2015). Structured Indoor Modeling. 

*[Project website](http://www.cse.wustl.edu/~sikehata/sim/), with matlab code and datasets.*

### Pose, Point Cloud & Others
* Katz, S., & Tal, A. (2015). On the Visibility of Point Clouds. 

*determine the visible subset of points directly from a given point cloud*

* Rhodin, H., Robertini, N., Richardt, C., Seidel, H. P., & Theobalt, C. (2015). [A Versatile Scene Model with Differentiable Visibility Applied to Generative Pose Estimation](https://gvv.mpi-inf.mpg.de/projects/DiffVis/). 

* Ventura, Jonathan, Clemens Arth, and Vincent Lepetit. "An Efficient Minimal Solution for Multi-Camera Motion." 

---

![]({{ site.baseurl }}/images/cvpr2015.jpg)

## CVPR 2015

### SfM and Localization:
* Lin, Tsung-Yi, et al. "Learning deep representations for ground-to-aerial geolocalization."

* Song, S., & Chandraker, M. (2015). Joint SFM and detection cues for monocular 3D localization in road scenes. 

### Reconstruction:
* **Choi, Sungjoon, Qian-Yi Zhou, and Vladlen Koltun. "Robust reconstruction of indoor scenes." 

*Indoor scene reconstruction from RGB-D video, with [code and dataset](http://vladlen.info/publications/robust-reconstruction-of-indoor-scenes/) available.*

### Stereo:
* Savinov, Nikolay, Christian Hane, and Marc Pollefeys. "Discrete optimization of ray potentials for semantic 3D reconstruction."

* Jung, J., Lee, J. Y., & Kweon, I. S. (2015, June). One-day outdoor photometric stereo via skylight estimation. 

* Xie, W., Dai, C., & Wang, C. C. (2015, June). Photometric stereo with near point lighting: A solution by mesh deformation. 

* Li, Zhuwen, et al. "Simultaneous video defogging and stereo reconstruction."

### Feature and Matching:
* \*Litman, Roee, et al. "Inverting RANSAC: Global Model Detection via Inlier Rate Estimation." 

* Dong, Jingming, and Stefano Soatto. "Domain-size pooling in local descriptors: DSP-SIFT." 

<http://vision.ucla.edu/~jingming/proj/dsp/>

* **Yumin Suh, Kamil Adamczewski, Kyoung Mu Lee. "Subgraph Matching Using Compactness Prior for Robust Feature Correspondence"

* Yanchao Yang, Zhaojin Lu, Ganesh Sundaramoorthi. "Coarse-To-Fine Region Selection and Matching"

* Faraki, Masoud, Mehrtash T. Harandi, and Fatih Porikli. "More About VLAD: A Leap from Euclidean to Riemannian Manifolds."

### Retrieval:
* ***Li, Xinchao, Martha Larson, and Alan Hanjalic. "Pairwise geometric matching for large-scale object retrieval."

* Jiang, Ke, Qichao Que, and Brian Kulis. "Revisiting kernelized locality-sensitive hashing for improved large-scale image retrieval." 

### 3D with Sensors:
* Ye, M., Zhang, Y., Yang, R., & Manocha, D. "3d reconstruction in the presence of glasses by acoustic and stereo fusion."

* Gupta, S., Arbeláez, P., Girshick, R., & Malik, J. "Aligning 3D models to RGB-D images of cluttered scenes."

### Segmentation and Scene Understanding:
* Wang, S., Fidler, S., & Urtasun, R. (2015, June). Holistic 3d scene understanding from a single geo-tagged image. 

* Martinovic, Andelo, et al. "3d all the way: Semantic segmentation of urban scenes from start to end in 3d." 

<https://bitbucket.org/amartino/facade3d>

