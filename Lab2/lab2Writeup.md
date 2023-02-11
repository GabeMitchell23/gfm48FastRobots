# Lab 2 Overview 
MAE 5190 Lab 1 introduced students to the Artemis Nano board. I ran exisiting example functions to complete simple tasks. I then wrote my own file to complete a task.

## Bluetooth Setup 
For my computer to communicate with the artemis nano via bluetooth, the nano's MAC address was printed by running ble_arduino.ino. 

<img src="mac_address.PNG" class="img-responsive" alt="" width= 450>

The MAC address was then written into a python file that is queried when attempting to connect via bluetooth. Importantly, any single digit number between colons needs to be preceeded by a 0.

Python code was then run to generate a UUID, which was then input into arduino code running on the artemis and python code on my computer. A unique UUID distinguishes a particlar artemis nano, allowing my computer to connect to the corret board. 

Once both the UUID and MAC address were correctly defined, python bluetooth functions were imported and ran to establish bluetooth connection. Python generated outputs as shown.

<img src="import_func.PNG" class="img-responsive" alt="" width= 450>   <img src="bluetooth_connection.PNG" class="img-responsive" alt="" width= 450>

## Demo
Python code was provided to students to verify bluetooth communication with the artemis. The code executed arduino functions on the artemis which then communicated back to my laptop. The first two functions queried the values of the characteristic string and characteristic float.


<img src="recieve_float.PNG" class="img-responsive" alt="" width= 450>   <img src="recieve_string.PNG" class="img-responsive" alt="" width= 450>

The next function redefined the value of the characteristic string to "PING". When the value of characteristic string was queired again, python showed that its value had changed. The message send off was confirmed in the Arduino serial monitor.

<img src="ping_pong.PNG" class="img-responsive" alt="" width= 450> <img src="ping_pong_arduino.PNG" class="img-responsive" alt="" width= 450>

The last demo function sent two integers to the artemis, which were then printed into the serial monitor.

<img src="send2ints.PNG" class="img-responsive" alt="" width= 450> <img src="send2ints_arduino.PNG" class="img-responsive" alt="" width= 450>
