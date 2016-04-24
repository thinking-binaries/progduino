# progduino
A zero-install python based flash programmer for Arduino chips

This is a placeholder, where I plan to surface an open-source version of this (currently) closed source code:

http://blog.whaleygeek.co.uk/raspberry-pi-peek-a-boo-camera/

http://blog.whaleygeek.co.uk/raspberry-pi-neopixels-colour-mixer/

Both of these projects have a 'progduino' module inside them, and it is currently closed source. I plan to open source this so that others in the community can build projects based around it.

ProgDuino is a clean-room implementation, in Python, of an AT328 flash and eeprom programmer. With it you can download and run (with no install of any tools) a python script that flashes a named .hex file into the arduino chip over the SPI port. This is directly compatible with these two products:

PiDuino from skpang: http://skpang.co.uk/catalog/piduino-kit-p-1337.html

RasPIO duino from RasPi.TV:  http://rasp.io/duino/

ArduBerry from Dexter Industries: http://www.dexterindustries.com/arduberry/
(The schematics for ArduBerry show that the Raspberry Pi SPI port is correctly wired through to the SPI port of the AT328P, so this should just work as with the other boards): https://github.com/DexterInd/ArduBerry/blob/master/Hardware/ArduBerry%20V6_b.pdf


The plan is to make it really easy for others to use and even write 'soft peripherals' on the arduino platform, where these end up being a 'coprocessor' to the Raspberry Pi. It is really easy to write small, low level, fast code on the Arduino platforms. It's generally quite hard to do this on the Raspberry Pi without delving into kernel drivers. So the combination of RaspberryPi+Arduino is a great one (and a common architecture used in many industrial projects too). The separation of concerns between the two processing platforms is perfect - use the Raspberry Pi for the 'big brain' stuff like internet access, big number crunching, and camera. Use the Arduino for the 'little brain' stuff, such as acquiring data from sensors or driving GPIO's fast and furious in a way that is not easily affected by the timing of a big OS like Linux.


