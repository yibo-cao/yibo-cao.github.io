---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a graduating (graduation date: May 14th) research-based master student in the Mechanical Engineering Department at [Carnegie Mellon University](https://www.cmu.edu/), major in robotics. I'm a member of [Biorobotics Lab](http://biorobotics.ri.cmu.edu/index.php) in [the Robotics Institute](https://www.ri.cmu.edu/) and my advisor is Prof. [Howie Choset](https://www.cs.cmu.edu/~./choset/bio.html). My research topics are 3D semantic segmentation and perception for mobile robots. 

I'm interested in solving 3D perception problems (especially the semantic understanding of 3D environments) using both deep learning methods and geometric methods. 

Research
======

Real Time Semantic Segmentation for 3D LIDAR point clouds ([video](https://drive.google.com/file/d/1i47W96V4gwl7YbkoEbO0dWUO-UkIkV25/view?usp=sharing))
------

<img style="float:left; margin:0 10px 10px 0" markdown="1" height="40%" width="40%" src="/images/robot_semantic.png" >

: I proposed a multi-perspective CNN-based nueral newtwork for semantic segmentation on 3D LiDAR point clouds. This network can fuse the features from both bird's eye view projections and sphere view projections, then providing robust semantic segmentation results. Users can cutomize the fused layer number of these features under different time limitation requirements. I also integrated this network with SLAM algorithm (by using a LiDAR odometry algorithm to get a stable and dense point cloud) in order to improve its performance on our hexapod mobile robot. Now the robot can do real time semantic segmentation with only a 16-line Velodyne LiDAR as 3D perception sensor as shown in the video.
