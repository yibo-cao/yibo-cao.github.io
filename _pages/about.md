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
<p align="center">
  <img height="60%" width="60%" src="/images/robot_semantic.png" />
</p>

I proposed a multi-perspective CNN-based nueral newtwork for semantic segmentation on 3D LiDAR point clouds. This network can fuse the features of point cloud projection from both bird's eye view and sphere view to provide robust semantic segmentation results. Users can cutomize the fused feature layer numbers according to different inference time requirements. I also integrated this network with SLAM algorithm in order to improve the segmentation performance on our hexapod robot. Now the robot can do real time semantic segmentation with only a 16-line Velodyne LiDAR as 3D perception sensor as shown in the video.

Graph-based Semantic Segmentation for 3D point clouds([result](/images/kittiHotseg.png))
------
<p align="center">
  <img height="60%" width="60%" src="/images/graph_network_structure.png" />
</p>
In the project, we designed a hierarchical graph neural network, which is adopted from [DGCNN](https://arxiv.org/pdf/1801.07829.pdf). This network utilizes both the local and global features of each point to do semantic inference on the given point clouds. The figure above shows how our hexapod robot utilizes this graph network. It has a 16-line Velodyne LiDAR to perceive the environment as global point clouds, while RGB cameras are mounted on its foot for reasoning local features. Then our network, which has learned the relationship between the local and global features, will do semantic inference on the whole point clouds. In this project, I wrote a functional API for 3D point cloud data processing, specially designed for graph-based network. I also collaborated with other group members on building this hierarchical graph network. Also, I customized this hexapod robot to let it be able to use this graph-based segmentation algorithm.

