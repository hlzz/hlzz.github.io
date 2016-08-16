---
layout: post
title: Recent Papers in 3D Computer Vision
---

\*   - slightly related
**  - related
*** - very much related 

Lists and details to be extended...

---

![]({{ site.baseurl }}/images/eccv2016.png)

**Update (July 30, 2016): ECCV 2016 is coming! Though the full accepted paper list has not been released, I have collected some new papers released by authors via homepages and Arxiv. Of course, they are all related to 3D computer vision.**

## ECCV 2016

### Structure-from-Motion:
* Tianwei Shen, Siyu Zhu, Tian Fang, Runze Zhang, Long Quan, [Graph-Based Consistent Matching for Structure-from-Motion](https://home.cse.ust.hk/~tshenaa/files/pub/eccv2016_graph_match.pdf).

*As you have noticed, this is my paper :). We propose a new method of matching image collections for SfM, which improves the matching efficiency as well as coping with ambiguous scenes. Leave a comment (at the bottom of this page) if you are interested.*

### Stereo:
* [Efficient Multi-view Surface Refinement with Adaptive Resolution Control](http://home.cse.ust.hk/~slibc/pdf/arc.pdf)

*This is kind of a promotion for my friend and labmate Shiwei's work. They have done excellent work on multi-view stereo which powers the 3D reconstruction engine of [Altizure](https://www.altizure.com/explore), take a look the paper if you are interested:).*

* [Pixelwise View Selection for Unstructured Multi-View Stereo](http://people.inf.ethz.ch/jschoenb/papers/schoenberger2016mvs.pdf)

*The results are quite impressive, including a [video](https://www.youtube.com/watch?v=GRW2APWn9wY) for demonstration.*

### Reconstruction:

* Indoor-Outdoor 3D Reconstruction Alignment

### Feature and Matching:
* [LIFT: Learned Invariant Feature Transform](http://arxiv.org/abs/1603.09114) (DL)

*This is a very interesting work that obtains local feature with deep neural nets. I am looking forward to the code.*

---

![]({{ site.baseurl }}/images/cvpr2016.png)

## CVPR 2016

### Reconstruction:
* ***Vo, M., Narasimhan, S. G., & Sheikh, Y. Spatiotemporal Bundle Adjustment for Dynamic 3D Reconstruction.

*[Project website](http://www.cs.cmu.edu/~ILIM/projects/IM/STBA/), 强烈推荐[video](https://www.youtube.com/watch?v=2m5-IS_xsno)，演员十分癫狂...*

* Hao Wang, Jun Wang, Wang Liang. Online Reconstruction of Indoor Scenes From RGB-D Streams.

* Ali Osman Ulusoy, Michael J. Black, Andreas Geiger. Patches, Planes and Probabilities: A Non-Local Prior for Volumetric 3D Reconstruction.

* Olivier Saurer, Marc Pollefeys, Gim Hee Lee. Sparse to Dense 3D Reconstruction From Rolling Shutter Images.

* **Filip Radenovic, Johannes L. Schönberger, Dinhuang Ji, Jan-Michael Frahm, Ondrej Chum, Jiri Matas. From Dusk till Dawn: Modeling in the Dark

*A method to cope with illumination changes in Internet dataset. After camera registration, a clustering method is applied and seperate the scene graph into the Day cluster and the Night cluster. Dense models are reconstruction seperately, following a fusion process. (sparse -> dense)*

### Structure-from-Motion:

* ***Johannes L. Schönberger, Jan-Michael Frahm. Structure-From-Motion Revisited.

[Code](https://colmap.github.io)

* [A Consensus-Based Framework for Distributed Bundle Adjustment](http://roboticvision.org/~anders/papers/eriksson-etal-cvpr-2016.pdf)

* A Direct Least-Squares Solution to the PnP Problem With Unknown Focal Length. 

* [Mirror Surface Reconstruction under an Uncalibrated Camera](http://i.cs.hku.hk/~kykwong/publications/khan_cvpr16.pdf)

* Marco Crocco, Cosimo Rubino, Alessio Del Bue. Structure From Motion With Objects.

### Feature and Matching:
* [Using Spatial Order to Boost the Elimination of Incorrect Feature Matches](http://www.faculty.idc.ac.il/moses/papers/UsingSpatialOrderCameraReady.pdf) 

* ***Tsun-Yi Yang, Yen-Yu Lin, Yung-Yu Chuang. Accumulated Stability Voting - A Robust Descriptor From Descriptors of Multiple Scales.

[Project website](http://shamangary.logdown.com/posts/587520): worth trying since there is [code](https://github.com/shamangary/ASV) available.

* Swarna K. Ravindran, Anurag Mittal. CoMaL - Good Features to Match on Object Boundaries.

* Yuan-Ting Hu, Yen-Yu Lin. Progressive Feature Matching With Alternate Descriptor Selection and Correspondence Enrichment.

* Angjoo Kanazawa, David W. Jacobs, Manmohan Chandraker. WarpNet: Weakly Supervised Matching for Single-View Reconstruction. (DL)

* Jin Xie, Meng Wang, Yi Fang. Learned Binary Spectral Shape Descriptor for 3D Shape Correspondence.

* Zhou, Tinghui, et al. "Learning Dense Correspondence via 3D-guided Cycle Consistency." (DL)

[Project page](http://people.eecs.berkeley.edu/~tinghuiz/projects/learnCycle/)

### Retrieval:

* Haomiao Liu, Ruiping Wang, Shiguang Shan, Xilin Chen. Deep Supervised Hashing for Fast Image Retrieval. (DL)

* Eng-Jon Ong, Miroslaw Bober. Improved Hamming Distance Search Using Variable Length Substrings.

* Jae-Pil Heo, Zhe Lin, Xiaohui Shen, Jonathan Brandt, Sung-eui Yoon. Shortlist Selection With Residual-Aware Distance Estimator for K-Nearest Neighbor Search.

* Xiaojuan Wang, Ting Zhang, Guo-Jun Qi, Jinhui Tang, Jingdong Wang. Supervised Quantization for Similarity Search .

* Patrick Wieschollek, Oliver Wang, Alexander Sorkine-Hornung, Hendrik P. A. Lensch. Efficient Large-Scale Approximate Nearest Neighbor Search on the GPU.

* Ting Zhang, Jingdong Wang. Collaborative Quantization for Cross-Modal Similarity Search.

* Thi Quynh Nhi Tran, Hervé Le Borgne, Michel Crucianu. Aggregating Image and Text Quantized Correlated Components.

* Artem Babenko, Victor Lempitsky. Efficient Indexing of Billion-Scale Datasets of Deep Descriptors.

* ***Ahmet Iscen, Michael Rabbat, Teddy Furon. Efficient Large-Scale Similarity Search Using Matrix Factorization.

* Theodora Kontogianni, Markus Mathias, Bastian Leibe. Incremental Object Discovery in Time-Varying Image Collections.

### Stereo:
* Alex Locher, Michal Perdoch, Luc Van Gool. Progressive Prioritized Multi-View Stereo.

[code](https://github.com/alexlocher/hpmvs)

* Cédric Verleysen, Christophe De Vleeschouwer. Piecewise-Planar 3D Approximation From Wide-Baseline Stereo.

* John Flynn, Ivan Neulander, James Philbin, Noah Snavely. DeepStereo: Learning to Predict New Views From the World’s Imagery.

*Accepted in CVPR 2016 but released a year ago (2015), see the [video](https://www.youtube.com/watch?v=cizgVZ8rjKA)*

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

*An application of [Lytro](https://www.lytro.com) cinema.*

* Cui, Zhaopeng, and Ping Tan. "Global Structure-from-Motion by Similarity Averaging." 

*Yet another global method for SfM*

### Stereo
* Benjamin Ummenhofer and Thomas Brox. Global, Dense Multiscale Reconstruction for a Billion Points.

*Multi-scale surface reconstruction. [Video](https://www.youtube.com/watch?v=y5n7enhxCyo)*

### Reconstruction

* Martin-Brualla, R., Gallup, D., & Seitz, S. M. (2015). 3D Time-Lapse Reconstruction from Internet Photos. 

*Given an Internet photo collection of a landmark, we compute a 3D time-lapse video sequence where a virtual camera moves continuously in time and space. [Project website](http://grail.cs.washington.edu/projects/timelapse3d/)*

* Ikehata, S., Yang, H., & Furukawa, Y. (2015). Structured Indoor Modeling. 

*[Project website](http://www.cse.wustl.edu/~sikehata/sim/), with matlab code and datasets.*

* Zheng, Enliang, et al. Minimal Solvers for 3D Geometry from Satellite Imagery. 

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

* **Johnson, Justin, et al. "Image retrieval using scene graphs." Computer Vision and Pattern Recognition (CVPR), 2015.

sementic image retrieval

### 3D with Sensors:
* Ye, M., Zhang, Y., Yang, R., & Manocha, D. "3d reconstruction in the presence of glasses by acoustic and stereo fusion."

* Gupta, S., Arbeláez, P., Girshick, R., & Malik, J. "Aligning 3D models to RGB-D images of cluttered scenes."

### Segmentation and Scene Understanding:
* Wang, S., Fidler, S., & Urtasun, R. (2015, June). Holistic 3d scene understanding from a single geo-tagged image. 

* Martinovic, Andelo, et al. "3d all the way: Semantic segmentation of urban scenes from start to end in 3d." 

<https://bitbucket.org/amartino/facade3d>

