# Parking_System_MicroController
•	General Overview:
In this project, Assembly language will be used to design a control system aimed to act as parking control system which will show how many cars in each floor (floor G and floor B).
To achieve the above functions, PIC16F877A and several 7-segments using the Proteus software, and here comes the roles as it can be get every can entered or exits each floor to calculate the car counts, and control the lights for each floor
First of all, I must calculate the ambient light in the G floor to detect if I need to turn light on or off and feed the signal to the Analog to digital converter module in the microcontroller.
 
Using an LDR and a resistor to make a voltage divider to get the required voltage to feed it to the ADC module at pin RA0 for Channel 0.
The real values of voltages and ADC values will be like the - using most significant 8Bits of ADC - to make the calculation as easy as possible - values only.


Now, I have to connect some buttons to simulate car entrance/exits by using pull-up resistor to get button values
 
In the code of m2 I have to display values of car count in each floor using 7-segment display
I used two double 7-seg displays to show count for each floor and I drive them using m2 controller

The two controllers connected to each other using their serial ports (USART) 

The floor lights will be controlled using a transistor and a relay 
 


Now I can start writing code to get the system run as I want as this requirement

 

The schematic shows all system parts, like the microcontrollers 
ed and the 7-Segment display, and the LAMP shows the floor lights and the four buttons used (Floor G In, Floor G Out, Floor B In, Floor B Out) the other components
I used a resistor as Pull-up resistor to ensure that the input value will always be specific value if the button/switch not pressed, in this case if the button in off state, the voltage on the output will be 5V always (logic 1), but if I press the button the voltage will be zero (logic 0), to get a specific value and now way to get float input on the microcontroller pin.
