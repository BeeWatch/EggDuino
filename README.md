Fork to support a 1.000mw Laserdiode:
I added a laserpin (Arduino Pin 11), which ist set as OUTPUT and on digital low signal when the "Pen" is raised and on high when the "PEN" is lowered. The Signal ist used to switch a relay. As alternativ the idea to set a PWM Signal via analog write command is implemented as well bout outcommented. On the ardunio CNC shield pin 11 is wired to the Z-Endstop.  
Tested with Inkscape 0.92.4 https://inkscape.org/ and EggBot Inkscape Plugin Software: Version 2.8.1 https://github.com/evil-mad/EggBot/releases/

=======

Eggduino
====

Arduino Firmware for Eggbot / Spherebot with Inkscape-Integration

Version 1.6a
tested with Inkscape Portable 0.91, Eggbot Extension and patched eggbot.py

Regards: Eggduino-Firmware by Joachim Cerny, 2015

Thanks for the nice libs ACCELSTEPPER and SERIALCOMMAND, which made this project much easier. Thanks to the Eggbot-Team for such a funny and enjoyable concept! Thanks to my wife and my daughter for their patience. :-)

Features:

- Implemented Eggbot-Protocol-Version 2.1.0
- Turn-on homing: switch-on position of pen will be taken as reference point.
- No collision-detection!!
- Supported Servos: At least one type ;-) I use Arduino Servo-Lib with TG9e- standard servo.
- Full Arduino-Compatible. I used an Arduino Uno
- Button-support (3 buttons)

Tested and fully functional with Inkscape.

Installation:

- Upload Eggduino.ino with Arduino-IDE or similar tool to your Arudino (i.e. Uno)
- Disable Autoreset on Arduinoboard (there are several ways to do this... Which one does not matter...)
- Install Inkscape Tools with Eggbot extension. 

1. Download and install the latest version of Inkscape (Version 0.91 or newer)
2. Download and install EggBot_250A.exe from:
https://github.com/evil-mad/EggBot/releases/tag/v2.5.0
3. Download my patched ebb_serial.py from:

https://github.com/plex3r/plotink/tree/master/libraries

4. Replace the existing ebb_serial.py in your inkscape extensions folder with the patched version.

Ensure there are no other usb / com devices plugged in apart from your Eggbot.

Start inskscape and it should now be able to connect to your eggbot.
