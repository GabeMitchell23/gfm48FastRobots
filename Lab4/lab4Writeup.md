# Lab 4 Overview
During Lab 4, students worked with an inertial measurment unit (IMU) to calculate angular position. The gyroscope and accelerometer on the IMU were utilized. Then, students queried data from both the IMU and the ToF sensor from lab 3. The sensors as wired for the majority of the lab are pictured below.  

<img src="wiring.jpg" class="img-responsive" alt="" width= 600> 

At the end of the lab, the electronics were removed from my laptop and plugged into a separate battery. The artemis, battery, and sensors were then fastened onto the RC car, where they querieid and transferred data as the car performed a stunt. The electronics on the car are pictured below. 

<img src="car_wiring.jpg" class="img-responsive" alt="" width= 600> 

An accelerometer works by placing a capacitor plate on a spring. If the IMU accelerates in the direction of the spring, the force will move the capacitor plate, causing the capacitance to change. This change is quantifiable with additional circuitry and can be related to the acceleration. Gyroscopes detect the angular speed of the IMU. The reading can therefore be integrated to find the change in angular position with respect to a reference. The convention that this lab follows is as pictured below. The "forward" direciton of the vehcile and IMU is the positive x direction, the y direction points to the right, and z therefore must point down. The pitch, role, and yaw are as drawn. 

<img src="convention.PNG" class="img-responsive" alt="" width= 600> 

## Setup
First, students ran example code provided in the IMU library to verify functionality. The sample code successfully queried accelerometer, gyroscope magnetometer, and thermometer data, all of which are embedded in the IMU. The output of the example function is shown below. In the example code, there is a value AD0_VAL set to 1. This is the last bit of the IMU's I2C address. 

<img src="imu_example.PNG" class="img-responsive" alt="" width= 600> 


## Task 1: Accelerometer
Students were tasked with using the accelerometer to calculate the 
