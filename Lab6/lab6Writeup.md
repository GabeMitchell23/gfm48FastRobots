# Lab 6 Overview
In Lab 6, students had the option to implement PID control to aid the robot complete one of two tasks: either approaching and stopping exactly 1m in front of a wall, or rapidly approaching a wall, spinning exactly 180 degrees, and then driving away from the wall in the opposite direction. I chose the latter task. I started by developing the code infrastructure by running it with a simple set of parameters: slow speeds and only P control. P control was not satisfactory on its own; after I tailored parameters as best as I could, I added integral and dirivative terms, which made the robot turn closer to 180 degrees in less time. 

## Code Overview 
The code for my 180 degree turn has two primary functions: an actuation and data collection function, and then a data transmission function. Psuedo code for the actuation and collection function is shown below. Note in the 

<img src="psuedo1.PNG" class="img-responsive" alt="" width= 600> 

## P Control Issues

## P Control Most Successful Run

## PID Control
