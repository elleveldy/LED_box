# LED_box

Using [FastLED](https://github.com/FastLED/FastLED) library to control ws2812b LEDs.

Connecting the Arduino Mega to the ws2812b LED strip:

![alt text](arduino_ws2812b_schematic.png "Arduino Mega to ws2812b LED strip")

## ArduinoMega
Arduino code for making simple patterns. Not controlled by serial. 

## ArduinoMega_serial
An extension of the above code, including listning to serial so a PC, the Pioneer LX or Raspberry Pi can send commands to the Arduino. The PC, Pioneer or Raspberry should be able to set light mode, connect to the MEA server, and send MEA recordings to the Arduino.

## nodeMCU_serial
Arduino code for the nodeMCU ESP8266 (currently replaced by the Arduino Mega) developed by EiT.

## Other information
### Trouble uploading to Arduino in Linux
If you have access trouble when updating code to your Arduino within Linux, you have to set USB privlages in terminal:
```
$ sudo chmod 666 /dev/ttyACM0
```

### Visualizing an MEA recording
Download a MCS recording from Box: "MEA recordings" folder. Convert the mcs format to ASCII or HDF5 using the MCS DataManager, also on Box: "MEA software". If using Python, the [Pandas](http://pandas.pydata.org/) library is recomended to handle the data.

Convert either raw voltage data or spike data into light shows with the LEDs. E.g. since there are 60 electrodes and 240 LEDs, assign 4 LEDs to each electrode value. 

_Note: A database is currently under development which will store all data in .hdf5 format for easy access and usage._  

### Streaming data from the MEA server
To be implemented. An MEA client must be developed to aquire the live datastream from the MEA server. See [MEAclient](https://github.com/thentnucyborg/MEAclient).
