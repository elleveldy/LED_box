# LED_box

Using [FastLED](https://github.com/FastLED/FastLED) library to control ws2812b LEDs.

Connecting the Arduino Mega to the ws2812b LED strip:

![alt text](https://cdn-learn.adafruit.com/assets/assets/000/030/892/medium640/leds_Wiring-Diagram.png "Arduino Mega to ws2812b LED strip")

## ArduinoMega
Arduino code for making simple patterns. Not controlled by serial. 

## ArduinoMega_serial
An extension of the above code, including listning to serial so a PC, the Pioneer LX or Raspberry Pi can send commands to the Arduino.

## nodeMCU_serial
Arduino code for the nodeMCU ESP8266 (currently replaced by the Arduino Mega) developed by EiT.

## Other information
If you have access trouble when updating code to your Arduino within Linux, you have to set privlages in terminal:
```
$ sudo chmod 666 /dev/ttyACM0
```
