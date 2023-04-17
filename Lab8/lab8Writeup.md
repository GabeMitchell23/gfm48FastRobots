# Lab 8 Coolest Video Submission
After completing Lab 8, I taped my phone to my robot, as shown in the photos below. 

This allowed me to record a first person view of the robot as it completed its stunt. This video is linked below.

# Lab 8 Late Submission Date
I submitted lab 8 before 8am on 4/17. I therefore used 5 slip days.

# Lab 8 Overview
In lab 8 students built upon progress made in [lab 6](Lab6/lab8Writeup.html) and [lab 7](Lab7/lab8Writeup.html). The goal is to complete the stunt in as little time as possible. The state estimation from lab 7 helped the robot recognize when it 1 meter away from the wall as quickly as possible. Additionally, implementing a stunt for the first time in lab 6 allowed students to learn from mistakes and improve upon their code. 

# Changes to Initial Stunt Code

## State Estimation
My code did not use the kalman filter designed in lab 7 to update my belief in the robot's pose. Rather, I used simple extrapolation which was intermittently corrected by a ToF reading. The ToF readings were treated as the ground truth, so when there was a ToF reading, the simple state estimator placed the robot at the exact pose specified by the sensor reading. Interpolation was done by estimating the instantaneous speed of the robot as the average speed between the two most recent ToF sensor measurements. 

## Closed Loop Control for Driving Forward.



