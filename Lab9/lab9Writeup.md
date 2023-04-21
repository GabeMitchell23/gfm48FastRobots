# Lab 9 Overview
In lab 9, students wrote code which mapped an arena in the lab. The code took ToF measurments inbetween in-place rotations that spanned 360 degrees. The robot executed the code at 5 spots throughout the map. By converting the position of the percieved obstacle in the robot's frame to the global frame, a map of the arena was developed.

<img src="map.PNG" class="img-responsive" alt="" width= 400>

## Code overview
Psuedo code for my mapping function is shown below. My code used a PD controller to change its orientation based upon feedback from the onboard ToF sensor. Once at a measurement location, 3 ToF sensor measurements were taken and averaged. ToF values were stored and returned to the robot via a notifcation handler. 

<img src="psuedo.PNG" class="img-responsive" alt="" width= 400>

The PD controller for yaw was borrowed from labs 6 and 8. As the robot rotates towards its target angular position, the duty cycle sent to the motors vary as seen in the graph below from lab 

<img src="Pduty.PNG" class="img-responsive" alt="" width= 400>

## Executing Code
The video below shows the robot
