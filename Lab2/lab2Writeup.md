# Lab 2 Overview 
MAE 5190 Lab 1 introduced students to the Artemis Nano board. I ran exisiting example functions to complete simple tasks. I then wrote my own file to complete a task.

## Bluetooth Setup 
For my computer to communicate with the artemis nano via bluetooth, the nano's MAC address was printed by running ble_arduino.ino. 

<img src="mac_address.PNG" class="img-responsive" alt="" width= 450>

The MAC address was then written into a python file that is queried when attempting to connect via bluetooth. Importantly, any single digit number between colons needs to be preceeded by a 0.

Python code was then run to generate a UUID, which was then input into arduino code running on the artemis and python code on my computer. A unique UUID distinguishes a particlar artemis nano, allowing my computer to connect to the corret board. 

Once both the UUID and MAC address were correctly defined, the code below was run to establish bluetooth connection. Python generated outputs as shown.

<img src="bluetooth_connection.PNG" class="img-responsive" alt="" width= 450>
