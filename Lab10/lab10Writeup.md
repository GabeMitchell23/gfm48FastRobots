# Lab 10 Overview

In lab 10, students implemented a Bayes filter to localize a robot in a simulator as it moves around a map. The filter was informed by odometry and a depth sensor. Poses within the map were discretized for analysis.  

## Bayes Filter
The Bayes filter is comprised of two steps, a prediciton step (1) and an update step (2). The math for the two steps is shown below. 

<img src="bayes_math.PNG" class="img-responsive" alt="" width= 800>

## Prediction
The prediction step determines the probability of each pose based upon odometry and the previous belief. The probability of the ith pose is a sum of terms, one for every previous pose. For every previous pose j, the jth term in the sum is equal to the probability of the jth pose times the likelyhood that the robot reached the ith current pose from the jth previous pose. After the update step, all belief bar terms are normalized to sum to one.

<img src="prediction.PNG" class="img-responsive" alt="" width= 800>

## Update
The updated belief in each position k is the product of the belief bar of pose k and the likelyhood of the current sensor measurments given the predicted pose. To find the second probability in the product, current sensor measurments are compared with expected sensor measurments, which are calculated using the inverse sensor model. 

<img src="update.PNG" class="img-responsive" alt="" width= 800>

## Simulator Overview 
The simulator (picture below) allowed the user to manually steer the robot or create a predefined path. As the robot moved around the map, the Bayes filter estimated the pose. 

<img src="simulate.PNG" class="img-responsive" alt="" width= 800>

# Code Overview
Students were provided with code to interact with data output by the simulator, namely odometry and sensors. Students were also provided a code skeleton in which to implement different parts of the Bayes filter. The code skeleton called functions which students completed.

## compute_control
The first funntion was compute control, which took two robot positions as input and output odometry data. The odometry data had 3 terms: rotation 1, translation, and rotation2. The three terms are defined as in the diagram below. Pseudo code for the function is also shown below. 

<img src="compute_control.PNG" class="img-responsive" alt="" width= 800> <img src="compute_control_pseudo.PNG" class="img-responsive" alt="" width= 800>

## odom_motion_model
The second function, odom_motion_model, took two positions and a control as input. The code output the probability that the robot started at one positions and ended at the other given the control. The form of the control was the same as that in compute control: rotation 1, translation, and rotation2.

<img src="odom_motion_model_pseudo.PNG" class="img-responsive" alt="" width= 800>

## prediction_step
The third function was prediction_step, which executed the prediciton step of the bayes filter and defined bel_bar. The function had six nest for loops in total: the outer three loops iterated through all previous positions. The inner three for loops iterated through all current positions. For each set of previous and current position, the function found the probability of getting from the previous to the current and multiplied that quanity by the belief in the previous position. Pseudo code for the function is shown below. 

<img src="prediction_step_pseudo.PNG" class="img-responsive" alt="" width= 800>

## sensor_model
The fourth function, sensor_model, determines how likely the actual sensor measurements are if the robot were in a position which returned the sensor readings given in the input. This is the inverse sensor model. Pseudo code for the inverse sensor model is below.

<img src="sensor_model_pseudo.PNG" class="img-responsive" alt="" width= 800>

## update_step
The last function was update_step, which executed the update step of the bayes filter and updated the belief in the state. The function iterated through every current pose. For each pose, the existing belief of the pose (from bel_bar) was multiplied by the likelyhood of the pose as determined by the inverse sensor model function. The pseudo code for the update step is shown below. 

<img src="update_step_pseudo.PNG" class="img-responsive" alt="" width= 800>

# Code
In the simulator, I used code written by Anya Parabow from the previous year's class. Her lab report for this lab as well as her code are linked [here](https://anyafp.github.io/ece4960/labs/lab11/).

# State Estimation
When Implemented, the bayes filter estimated the state as shown below. The estimation with just odometry is in red, the truth pose is in green, and the belief is in blue.
<img src="plot.PNG" class="img-responsive" alt="" width= 800>
