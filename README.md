# Soldering Station 907 Arduino
DIY 907 arduino soldering station using Arduino Pro Mini
based on Sasiskas Soldering Station on [Youtube](https://www.youtube.com/watch?v=PnqGLrhWQqc)

## Changes :
Using I2C 16x02 LCD instead of Parallel 16x02 LCD \
Added some minor filtering for temperature reading \
Cleaning some text bug

Pinout = \
HeaterPin = D9 \
BuzzerPin = D10 \
ProbePin = A0 \
EncoderA = 3 \
EncoderButton = 2 \
EncoderB = 4

## Diagram :

![Diagram](	/Schematic.png)

Soldering Iron Connector using GX16 5 pin \
pin 1 = Sensor + \
pin 2 = Sensor - \
pin 3 = NC \
pin 4 = Heater - \
pin 5 = Heater + 

board made with donut board \
The Mosfet and D9 wire must be far from MCP602 and analog wire to prevent high frequency feedback \
0.1uF decoupling capacitor is optional but recommended to add for stability on encoder and analog wire \
Mosfet is IRF520n with small heatsink instead of IRFZ44n for simpler driving circuit \
Diode must be fast recovery type if using other than UF5408

## Calibration :
Set default setting when first usage \
Need external thermocouple that can reach atleast 300C \
Go to Tune Screen in Setting \
Using external thermocouple check the current tip temperature \
Add some solder to tip to get more accurate temperature reading \
Control the power and until external thermocouple read 300C \
trim the potentiometer near the MCP602 until the reading is around 751 \
Finish

You can use Calibration Screen to fine tune the reading of temperature on the screen 
