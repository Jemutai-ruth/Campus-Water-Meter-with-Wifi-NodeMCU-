# Campus-Water-Meter-with-Wifi-NodeMCU-
<b> Objective </b><br/>
<b> This project aims to get real time data of water flowing through a pipe on a real time database</b><br/><br/>

IoT Based Water Flow Meter using ESP8266 & Water Flow Sensor This project we are creating an IOT based water flow sensor using ESP8266 and water flow sensor. We will display the water flow rate, total volume and the current liquid flowing. The water flow rate, total volume and the current liquid flowing will be uploaded to firebase where it can be viewed/monitored from anywhere. The sensor uses the principles of electromagnetism, such that, when liquids flow through the sensor, the flow action impacts the fins of a turbine in the sensor, causing the wheel to spin. The shaft of the turbine wheel is connected to a hall effect sensor so that with every spin, a pulse is generated, and by monitoring that pulse with a microcontroller, the sensor can be used in determining the volume of fluid passing through it. <br/><br/> 

<b>Components required<br/></b><br/><br/> 
Following are the components required for making this project. <b>1.1	Hardware:</b><br/>
1.NodeMCU- ESP8266-12E Board
2.Water Flow Sensor
3.Connecting Wires- Jumpers
4.Breadboard 
5.Micro USB cable 

1.2	Software: Arduino IDE - https://www.arduino.cc/en/Main/Software 

1.3 Supporting Softwares For data collection from sensors and storage will use a cloud service that is - https://firebase.google.com/  

<b>2.0 Circuit connection</b> 
The yellow wire(signal/pulse) connect to pin D2 The black wire(ground) connects to GND pin The red wire connects to pin 3v 
![image](https://user-images.githubusercontent.com/80382198/111437538-46b08000-8714-11eb-9308-7e950233247d.png)


<b>3.0 Code </b>
The main objective is to monitor the signal pin of the YF-S201 (Hall Effect Water Flow Meter / Sensor) to detect when the hall sensor is triggered (flow is detected) and increment a variable to show the increased inflow. However, to do that efficiently and accurately, we will use the interrupt feature of the ESP8266 such that whenever the hall sensor detects the rotating magnet, a rising edge interrupt is fired and registered by the ESP8266. The total number of interrupts fired over a particular time is then used in generating the flowrate and the total volume of liquid that has traveled through the flow meter.
See the code in the code folder:=
