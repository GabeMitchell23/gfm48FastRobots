# Lab 3 Overview
During Lab 3, students worked with time of flight (ToF) sensors, which send out a signal and keep time until it returns after bouncing off an object. Based upon the speed of the signal (be it light or sound) the sensor can discern how far away the detected object is. Students began the lab by soldering the ToF sensors to QWIIC cables to facilitate communication with the artemis nano via I2C. Once wired, the artemis queried the ToF sensors for range data. Lastly, two ToF sensors were connected to the artemis, which required a specific setup to prevent confusion between the two sensors.

## Two sensor setup 
The default I2C address of the ToF sensor is 0x52. For this reason, when two are wired on the same I2C bus, there is no way to distinguish between them. One ToF sensor must be shut off while the other recieves commands to change its I2C address. I will place one ToF sensor on the front of the robot, and one ToF sensor on the right side. When turning left or backing up, the robot may not detect obstacles. If this setup becomes too problematic, sensors can be moved and wires can be resoldered. The schematic for two ToF sensors is pictured below. Along with QWIIC cables, there are two wires (green) going from GPIO pins on the artemis to the XSHUT pin on the ToF sensors. When the pins are set to low, the ToF sensors shut off. 

<img src="schematic.PNG" class="img-responsive" alt="" width= 450>

The physical system is pictured below. For any script where only one sensor is utilized, either of the two ToF sensors could be unplugged from the QWIIC multiport. 

<img src="wire.JPEG" class="img-responsive" alt="" width= 450>

## Single Sensor Data

