# Lab 12 Overview
In lab 12, students had their robot navigate to waypoints in a map with obstacles. The path that the robot was supposed to follow is pictured below. Students could have their robot follow the path in any way they saw fit. 
<img src="map.PNG" class="img-responsive" alt="" width= 800>

## Strategy
To follow the path, the robot either drove forward from one node to another, or it rotated toward the next node. When driving forward, the robot was controlled by a PD controller which ensured it stayed straight. The robot stopped driving forward when its depth sensor reached a specified value. When rotating, the robot rotated a specified amount while being controlled by a PD controller. The PD controller for driving straight and rotating a specified amount were developed during lab 8, and they are described in greater detail in the [lab 8 report](https://gabemitchell23.github.io/gfm48FastRobots/Lab8/lab8Writeup.html). For the code to run, I passed in a set of angles that the robot needed to rotate and a set of depths at which the robot began turns. Pseudo code for the navigation function is pictured below. 

<img src="pseudo.PNG" class="img-responsive" alt="" width= 800>

## Strategy Options Not Used
A possible navigation solution that I did not use was bayes filter localization, as developed in [lab 11](https://gabemitchell23.github.io/gfm48FastRobots/Lab11/lab11Writeup.html). It would have been most intuitive to implement this solution after driving forward and before turning. Before each turn, the robot could have in thoery relocalized. However, the performance of the bayes filter in lab 11 was severely hampered by my robot's inability to stay in one location while rotating, as shown in the video below. Because the bayes filter could not be run on my robot in particular, I did not incorporate it into my navigation function. 


