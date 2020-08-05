# PentairMQTTv2
Arduino sketch to interface with the Pentair EasyTouch system using MQTT as the backend.

This sketch was designed around the Adafruit Feather M0 WIFI (https://www.adafruit.com/product/3010) using a MAX3485
to communicate with the EasyTouch pool controller.  

The MAX3485 is connected to Serial1 on the feather using pin 9 as the control pin for Transmit/Recieve (High/Low respectively).

DE and -RE pins on MAX3485 are connected to pin 9 on feather

RO pin on MAX3485 is connected to RX pin on feather

DI pin on MAX3485 is connected to TX pin on feather

A pin on MAX3485 is connected to Pin 2/Green/DT- on EasyTouch 

B pin on MAX3485 is connected to Pin 3/Yellow/DT+ on EasyTouch 

I connected VCC to the 15V in the EasyTouch using a Buck converter.

This sketch requires:

WiFi101 library, detailed here: https://learn.adafruit.com/adafruit-feather-m0-wifi-atwinc1500/using-the-wifi-module

PubSubClient for MQTT: https://github.com/knolleary/pubsubclient
