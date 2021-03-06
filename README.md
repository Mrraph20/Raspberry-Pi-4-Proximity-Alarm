# Sounding an alarm if an object comes too close and then displaying "Too Close!" onto a LCD. Coded with C and a Raspberry Pi 4.
A project that sounds an alarm if an object comes too close and then displays "Too Close!" on an LCD. 
For GPIO pin mapping, I used WiringPi (Made by Gordon Henderson under GNU-LGPL) to simplify. Link: http://wiringpi.com/

***WiringPi Note: The author has discontinued public releases of WiringPi. The last update was 2.52 for the Raspberry Pi 4B.***
Although WiringPi is preinstalled on Raspbian systems, the code for installation is as follows:
```
sudo apt-get install wiringpi
```
Use:
```
gpio -v
```
to check if your version is 2.52.

For more details visit http://wiringpi.com/download-and-install/

To upgrade, visit http://wiringpi.com/wiringpi-updated-to-2-52-for-the-raspberry-pi-4b/

Hardware components used:
- (1) HC-SR04 
- (1) Buzzer
- (1) I2C LCD1602 Module
- (1) 1k Ohm Resistor
- (8) Male to Female Cables
- (6) Male to Male Jumper Cables
- (1) NPN transistor (S8050) 
- (1) Breadboard
- Raspberry Pi 4B Rev. 1.2

When compiling the code, run the following commands in terminal at the location of the file:
```
sudo bash
gcc ProximityAlarm.c -o ProximityAlarm -lwiringPi -lm -lpthread -lwiringPiDev
./ProximityAlarm
```
This project was possible through an electronics kit I purchased from Freenove that provided me with all of the components I used. 
If interested, it is the "Freenove Ultrasonic Starter Kit for Raspberry Pi" (FNK0024).
