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
![Editing a markdown file for a talk](/images/editing-talk.png)
Real Time Semantic Segmentation for 3D LIDAR point clouds ([video](https://drive.google.com/file/d/1i47W96V4gwl7YbkoEbO0dWUO-UkIkV25/view?usp=sharing))
------
I proposed a multi-perspective CNN-based nueral newtwork structure for semantic segmentation on 3D LiDAR point clouds. This network can fuse the features from both bird's eye view projections and sphere view projections. User can also cutomize the fused layer number of these features. I also integrate this network with SLAM algorithm in order to improve its performance on mobile robot.

![Editing a markdown file for a talk](/images/editing-talk.png)
Graph-based Semantic Segmentation for 3D point clouds | Biorobotics Lab, Carnegie Mellon University
------
![Editing a markdown file for a talk](/images/editing-talk.png)

{% include base_path %}

{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}
