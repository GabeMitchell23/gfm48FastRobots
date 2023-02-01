## Setup/Task 1
I downloaded Arduino IDE and I downloaded the Apollo 3 Arduino package, 

## Task 2
I used Arduino example code to make the LED on the Artemis nano blink. The existing code set the LED pin to output in its setup section. It then changed the value between high and low every second. When high, current passed through the LED, causing it to light up. The LED on and off is pictured below. 

<img src="LED on.jpg" class="img-responsive" alt="" width= 300> <img src="LED on.jpg" class="img-responsive" alt="" width=300>

## Task 3
I used the Arduino example Example2_Serial to print anything I typed into the Serial Monitor. I typed “Hello World” into the “send message line” and it appeared on the serial monitor after I hit enter. My Baud rate needed to be set to 115200 (as specified in the example program).


## Task 4
I used the Arduino example Example4_analogRead to print out readings from sensors on the board. All sensor readings (including the temperature sensor) were printed to the serial monitor. When the board was exposed to the ambient room temperature, the temperature sensor read roughly 32700. When I blew hot air onto the board, the temperature sensor read roughly 33500



## Task 5
I used the Arduino example Example1_MicrophoneOutput to print out the highest frequency that the board was registering at that time. When the board was exposed to ambient noise in the lab. The highest frequency at any time was seemingly random. However, when I whistled near the board, the highest frequency was consistent over time. 



## 5000 task 
