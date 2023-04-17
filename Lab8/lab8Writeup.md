# Lab 8 Coolest Video Submission
After completing Lab 8, I taped my phone to my robot, as shown in the photos below. 

<img src="cam1.jpg" class="img-responsive" alt="" width= 350> <img src="cam2.jpg" class="img-responsive" alt="" width= 350> 

This allowed me to record a first person view of the robot as it completed its stunt. This video is linked below.

[Coolest Stunt Video, Robot POV](https://youtu.be/qYq4uiy29VA)


# Lab 8 Late Submission Date
I submitted lab 8 before 8am on 4/17. I therefore used 5 slip days.

# Lab 8 Overview
In lab 8 students built upon progress made in [lab 6](Lab6/lab8Writeup.html) and [lab 7](Lab7/lab8Writeup.html). The goal is to complete the stunt in as little time as possible. The state estimation from lab 7 helped the robot recognize when it 1 meter away from the wall as quickly as possible. Additionally, implementing a stunt for the first time in lab 6 allowed students to learn from mistakes and improve upon their code.

## Taped Wheels
One problem I had in lab 6 was very erratic behavior when the robot turned. Another issue was the right set of wheels not being able to turn unless being given a very very high duty cycle. Adding tape to the wheels solved both problems. The taped wheels reduced friction with the ground. This reduced the force that worked against the robot when rotating about its vertical axis. The friction-reducing tape also reduced torque that each wheel needed to begin rotation. The Robot with its newly taped wheels is pictured below. 

<img src="wheel_tape.jpg" class="img-responsive" alt="" width= 650> 

## Changes to Initial Stunt Code - State Estimation
My code did not use the kalman filter designed in lab 7 to update my belief in the robot's pose. Rather, I used simple extrapolation which was intermittently corrected by a ToF reading. The ToF readings were treated as the ground truth, so when there was a ToF reading, the state estimator placed the robot at the exact pose specified by the sensor reading. Extrapolation was done by assuming the current speed of the robot was the average speed between the two most recent ToF sensor measurements. This quantity multiplied by the change in time since the most recent ToF reading extrapolated the robot's pose. This simple state estimator was used in place of the kalman filter because it was much easier to implement, and it did not comprimise performance. A diagram of the new, simple state estimator is shown below. 



## Changes to Initial Stunt Code - Closed Loop Control for Driving Forward.



https://youtube.com/shorts/O7jtek9dTOw?feature=share

