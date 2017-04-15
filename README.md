# MyHomeAutomation
Based on instructables Uber Home Automation, and updates made by https://github.com/abouillot/HomeAutomation

plans started as those project did, to use Raspi as the Hab for the home automation, 
based on OpenHab.

major steps i faced along the way:
- install OpenHab2 (needed to change from OpenHab1 approach and implement it)
- use abouillot code for PiGateway (found a bug and fixed it)
- use Mosquitto MQTT broker on the Pi
- use RFM modules for the 433Mhz transmissions - as Uber states strong long distance support
Arduino
- use Arduino Pro Mini 3.3v instead of Arduino Uno Clone 3.3v version
- Update PIR notifications based on "on change" events to OpenHab2, plus time proxy to update "no movement".
- update Temperature sensor using DS18B20 instead of DHT (using OneWire.h instead of DHT.h)
- Adding Relay to switch lights or outlets

Plans
- because of 2/3 way switch in the house, and decision to leave them and not replace with smart touch switches, i need to add 2 relays to control 4 way switch (original 2 + remote).
- learn IR codes of A/C, TVs, ... and use it with IR transmits on the sensor node.
- expand the MQTT network with Sonoff devices that require to hack the ESP8266 board on the sonoff and then connect it to MQTT based on http subscription/publish. using either SuperHouse video or others https://github.com/mgaman/Sonoff-modified.
- how will IP camera will interact with the openhab and MQTT network?
