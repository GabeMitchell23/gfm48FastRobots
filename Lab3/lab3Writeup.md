# Deez

## Lab 3 Overview
During Lab 3, students worked with time of flight (ToF) sensors, which send out a signal and keep time until it returns after bouncing off an object. Based upon the speed of the signal (be it light or sound) the sensor can discern how far away the detected object is. Students began the lab by soldering the ToF sensors to QWIIC cables to facilitate communication with the artemis nano via I2C. Once wired, the artemis queried the ToF sensors for range data. Lastly, two ToF sensors were connected to the artemis, which required a specific setup to prevent confusion between the two sensors.

## Two sensor setup 
The default I2C address of the ToF sensor is 0x52. For this reason, when two are wired on the same I2C bus, there is no way to distinguish between them. One ToF sensor must be shut off while the other recieves commands to change its I2C address.  
