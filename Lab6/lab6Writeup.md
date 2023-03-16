# Lab 6 Overview
During Lab 5, students used motor drivers to control motors on the car. The motor drivers received signals from the artemis, which determined which motors to power and what direction to spin. The motors were at first powered by a power supply to verify functionality. Afterwards, the motor drivers and all other electronics were integrated into the car, at which point the motor drivers were powered by a battery. After electronics integration, the motor duty cycles were augmented to drive the car in a straight line and drive the car as slowly as possible with the wheels still spinning constantly. 

## Prelab

Before the lab, students determined how they would integrate the motor drivers. My schematic is shown below. Note that the motors are receiving current from two output pins on the driver, allowing them to spin faster. Note also that there are two batteries, one for the motors, and one for the artemis. There are separate power sources because the artemis and the sensors plugged into it have much smaller power needs than the motors.

<img src="schematic.PNG" class="img-responsive" alt="" width= 600> 
