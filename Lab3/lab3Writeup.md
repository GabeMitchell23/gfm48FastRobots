# Lab 3 Overview
During Lab 3, students worked with time of flight (ToF) sensors, which send out a signal and keep time until it returns after bouncing off an object. Based upon the speed of the signal (be it light or sound) the sensor can discern how far away the detected object is. Students began the lab by soldering the ToF sensors to QWIIC cables to facilitate communication with the artemis nano via I2C. Once wired, the artemis queried the ToF sensors for range data. Lastly, two ToF sensors were connected to the artemis, which required a specific setup to prevent confusion between the two sensors.

## Two sensor setup 
The default I2C address of the ToF sensor is 0x52. For this reason, when two are wired on the same I2C bus, there is no way to distinguish between them. One ToF sensor must be shut off while the other recieves commands to change its I2C address. I will place one ToF sensor on the front of the robot, and one ToF sensor on the right side. When turning left or backing up, the robot may not detect obstacles. If this setup becomes too problematic, sensors can be moved and wires can be resoldered. The schematic for two ToF sensors is pictured below. Along with QWIIC cables, there are two wires (green) going from GPIO pins on the artemis to the XSHUT pin on the ToF sensors. When the pins are set to low, the ToF sensors shut off. 

<img src="schematic.PNG" class="img-responsive" alt="" width= 450>

The physical system is pictured below. For any script where only one sensor is utilized, either of the two ToF sensors could be unplugged from the QWIIC multiport. 

<img src="wiring.jpg" class="img-responsive" alt="" width= 450>

## Single Sensor Connection

The example code Example1_ReadDistance will pause until the function distanceSensor.begin() returns true, meaning the artemis nano is communicating with the ToF sensor via I2C. If the sensor fails to connect, the code will output as shown below to the left. When the sensor does connect, the code will disply as shown below to the right. 

<img src="failed2connect.PNG" class="img-responsive" alt="" width= 450>     <img src="connected.PNG" class="img-responsive" alt="" width= 450>

## Single Sensor Data

I analyzed sensor performance by taking depth measurements at offsets equal to 4", 8", 12", 16", and 20" in light and dark conditions. I used the default long range sensor setting, and I used the bluetooth communicaiton setup described in BLANK to transfer data from the artemis to my laptop. The results of the experiment are shown in the graph and table below.

<img src="cool_graph.PNG" class="img-responsive" alt="" width= 450> <img src="cool_table.PNG" class="img-responsive" alt="" width= 450> 

For all sets of data, the average measurement varied from the offset by a 50 thousanths to a 300 thousanths of an inch. The sensor consistenly measured over the expected measurement, which I attribute to me pointint the sensor in a direction slightly off-normal form the detected surface. Given that the error was due to me pointing the sensor slightly  off, it is difficult to tell if performance in light or dark is better. However, the standard deviation in the measurments was consistently larger in the dark, so light measurements are more precise. For any one data set, the one second interval over which data was collected yielded 9 data points. The slow rate can be attributed to each data point being sent to the computer before the next one was taken.
