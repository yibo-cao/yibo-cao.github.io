---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a graduating (graduation date: May 14th, 2020) research-based master student in the Mechanical Engineering Department at [Carnegie Mellon University](https://www.cmu.edu/), major in robotics. I'm a member of [Biorobotics Lab](http://biorobotics.ri.cmu.edu/index.php) in [the Robotics Institute](https://www.ri.cmu.edu/) and my advisor is Prof. [Howie Choset](https://www.cs.cmu.edu/~./choset/bio.html). My research topics are 3D semantic segmentation and perception for mobile robots. 

I'm interested in solving 3D perception problems (especially the semantic understanding of 3D environments) using both deep learning methods and geometric methods. 

Research
======

Real Time Semantic Segmentation for 3D LIDAR point clouds ([video1](https://drive.google.com/file/d/1i47W96V4gwl7YbkoEbO0dWUO-UkIkV25/view?usp=sharing), [video2](https://drive.google.com/file/d/1G4iSTo8E4pzox9Z60GI9-HixXoV3ia0V/view?usp=sharing))
------
<p align="center">
  <img height="60%" width="60%" src="/images/robot_semantic.png" />
</p>

This is my main research project. I proposed a multi-perspective CNN-based neural network for semantic segmentation on 3D LiDAR point clouds. This network can fuse the features of point cloud projection from both bird's eye view and sphere view, achieving a robust semantic segmentation result. Users can customize the fused feature layer number according to different inference time requirements. I also integrated this network, which I implemented using Tensorflow, with a SLAM algorithm to improve the segmentation performance on our hexapod robot. Now the robot can do real-time semantic segmentation with only a 16-line Velodyne LiDAR as a 3D perception sensor as shown in [video1](https://drive.google.com/file/d/1i47W96V4gwl7YbkoEbO0dWUO-UkIkV25/view?usp=sharing). [video2](https://drive.google.com/file/d/1G4iSTo8E4pzox9Z60GI9-HixXoV3ia0V/view?usp=sharing) is the semantic segmentation result on [Semantic3D dataset](http://www.semantic3d.net/view_results.php?chl=2).

Graph-based Semantic Segmentation for 3D point clouds([result](/images/kittiHotseg.jpg))
------
<p align="center">
  <img height="60%" width="60%" src="/images/graph_network_structure.png" />
</p>
In the project, we designed a hierarchical graph neural network based on [DGCNN](https://arxiv.org/pdf/1801.07829.pdf). This network utilizes both the local and global features of each point to do semantic inference on the given point clouds. The figure above shows how our hexapod robot utilizes this graph network. It has a 16-line Velodyne LiDAR to perceive the environment as global point clouds, while RGB cameras are mounted on its foot for reasoning local features. Then our network, which has learned the relationship between the local and global features, will do semantic inference on the whole point clouds. In this project, I wrote a functional API for 3D point cloud data processing, specially designed for graph-based network. I also collaborated with other group members on building this hierarchical graph network. Also, I customized our hexapod robot to let it be able to use this graph-based segmentation algorithm.

Depth Prediction with Monocular Images and 2D Laser Scans([arXiv](https://arxiv.org/pdf/1912.00096.pdf))
------
<p align="center">
  <img height="60%" width="60%" src="/images/framework_fusionmapping.png" />
</p>
In the project, we build a neural network for pseudo-LiDAR generation based on [Monodepth2](https://arxiv.org/pdf/1806.01260.pdf), which could predict accurate depth information with the assistance of monocular images and 2D laser scans. In this project, I collaborated with group members on building this neural network using Pytorch, I also conducted a series of experiments and results analysis.

Modular Perception Box for mobile robot([Robot system](/images/robotsystem.png))
------
<p align="center">
  <img height="60%" width="60%" src="/images/slambox.png" />
</p>
I designed and fabricated a modular perception box that has integrated LiDAR, RealSense camera and Intel NUC. We also integrated the SLAM system and Nvidia Xavier in this box, so that with this modular box mounted on any mobile robot, the robot can utilize the perception functions easily. As shown in this [link](/images/robotsystem.png), on our hexapod robot, this box can cooperate with other sensors to perform complex tasks.

Project
======

Comparison of ORB-SLAM2 and DeepVO([report](/files/slam_report.pdf))
------
<p align="center">
  <img height="60%" width="60%" src="/images/slam.gif" />
</p>
This is my course project of Robot Localization and Mapping. We implemented [ORB-SLAM2](https://arxiv.org/pdf/1610.06475.pdf) and [DeepVO](https://arxiv.org/pdf/1709.08429.pdf). ORB-SLAM2 uses a traditional bag of words method in its visual odometry module while DeepVO is a learning-based visual odometry module. We conducted an analysis and comparison between DeepVO and the visual odometry in ORB-SLAM2.

Object detection for LIDAR point clouds([video1](https://drive.google.com/file/d/1lLNbOVB8yLImudYwxUXmTbS7bCBBGV0V/view?usp=sharing), [video2](https://drive.google.com/file/d/1XVGshr7sVhUr9fab5wsR-MEQOrxzyvB1/view?usp=sharing))
------
<p align="center">
  <img height="60%" width="60%" src="/images/yolo.png" />
</p>
This is my course project of Computer Vision Couse. We manually generated the LiDAR point clouds with a mobile robot and labeled the objects in a bird’s eye view projections. We implemented the [YOLO](https://pjreddie.com/darknet/yolo/) object detection network and tested it with the manually labeled data. As shown in [video1](https://drive.google.com/file/d/1lLNbOVB8yLImudYwxUXmTbS7bCBBGV0V/view?usp=sharing), this is the result of detecting cars in [Kitti dataset](http://www.cvlibs.net/datasets/kitti/eval_3dobject.php). [Video2](https://drive.google.com/file/d/1XVGshr7sVhUr9fab5wsR-MEQOrxzyvB1/view?usp=sharing) shows the result of detecting small objects which are manually labeled by us.


Position analysis of robotic arm’s end-effector
------
<p align="center">
  <img height="60%" width="60%" src="/images/GPR2.gif" />
</p>
This project aims at predicting the position of a robot arm with very limited calibration data. We used machine learning algorithms to achieve the error feature beneath the robot arm. I implemented and optimized an iterative Gaussian Process Regression (GPR) algorithm to analyze the end-effector position of a high DoF (degree of freedom) industrial robotic arm, achieving prediction error below 0.068mm. I also implemented other machine learning methods, such as SVR (Support Vector Machine Regression) and Bayesian Inference to analyz the iterative GPR performance.
