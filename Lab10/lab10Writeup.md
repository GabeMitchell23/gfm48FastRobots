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

<img src="prediction.PNG" class="img-responsive" alt="" width= 800>

## Simulator Overview 
The simulator 