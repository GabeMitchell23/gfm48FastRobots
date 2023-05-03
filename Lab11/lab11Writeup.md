# Lab 11 Overview
In lab 11, principles developed in [lab 10](https://gabemitchell23.github.io/gfm48FastRobots/Lab10/lab10Writeup.html) were moved over from a simulator to the physical robot. Rather than spinning the robot in the simulator, the physical robot was spun in the lab arena while collecting ToF data. The data was then transferred to a laptop, where it was analyzed with a Bayes filter to update the belief in the robot's pose. 

## Bayes Filter
The Bayes Filter consists of two steps, the math for which is shown below. The 3rd row is the prediction step, which changes the belief in the robot's pose based upon the likely hood of arriving all cells from all previous cells times the likelyhood of the previous cells. The 4th row is the update step, which first analyzes the likelyhood of each cell based upon how actual sensor measurements compare with expected sensor measurements. The update step then updates the likelyhood of the cell based upon the likelyhood as given by both dynamics and sensors. This logic was explored in depth by students in lab 10. For lab 11, students were provided with optimized code that ran the bayes filter as fast as possible. 

<img src="bayes_math.PNG" class="img-responsive" alt="" width= 800>

## Data Collection


