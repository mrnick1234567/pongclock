Pong Clock v 5.1, Aug 2016 by Nick Hall
Distributed under the terms of the GPL.

For help on how to build the pong clock see my blog:
http://123led.wordpress.com/


Release Notes for V5.1.

*Now compiles with Arduino IDE 1.6.5
*Fixed a bug in pong mode where the bat missed ball and it wasn't on the minute
*Fixed a bug in normal and slide mode where the date tens digit wasn't cleared when some months changed
*Fixed a bug where the display was corrupted when in digits and 12hr mode
*Addded lower case font. A tweaked version of the one courtesy of Richard Shipman
*Added full LED test on startup.
*Time is printed to serial port for testing
*Menu and set clock items reordered.


Release Notes for V5.0.

*Tested to be compatible with Arduino IDE 1.0.5
*Normal mode now has seconds
*New slide effect mode 
*Separate setup menu
*New pong “Ready?” message
*Daylight Savings mode (DST ADJ) adds / removes 1 hr.
*Time now set on upload 
*Various other display and code tweaks. Now using the RTClib from Adafruit

Thanks to all who contributed to this including:
SuperTech-IT over at Instructibles, Kirby Heintzelman, Alexandre Suter.


Release Notes for V4.02

*Added Brightness function.
*Added 12/24 Hour clock function
*Slightly quicker pong ball

Thanks to SuperTech-IT over at Instructibles for modifying the original code.
There are also a couple of features commented out in the code:

*A screen wipe effect in the pong() function
*An alternative power on screen in the printvers() function

***************************

Release Notes for V2.27 Dec 2010 - by Nick-h
* Initial version.

* Uses 2x Sure 2416 LED modules, arduino and DS1307 clock chip.
          
* Holtek HT1632 LED driver chip code:
* As implemented on the Sure Electronics DE-DP016 display board
* (16*24 dot matrix LED module.)
* Nov, 2008 by Bill Westfield ("WestfW")
* Copyrighted and distributed under the terms of the Berkely license
* (copy freely, but include this notice of original author.)

***************************

Instructions:

1)
Make sure you have version 1.6.5 of the Arduino software (IDE) installed on your computer. The clock code may work on earlier or later versions of the software but I’ve only tested on 1.6.5 (the latest at time of writing). It definitely wont work on pre 1.0 versions, e.g. 0023.

2)
Open your Arduino sketchbook folder. If there isn’t already a folder there called libraries create one. Then copy the 4 folders from the pongclock download in to it. I.e Button, Font, ht1632c & RTClib.

3)
If the Arduino software is already open, quit and relaunch it to pick up the 4 new libraries.

4)
Check the libraries are there. You should see all 4 listed when you go to the Sketch > Import Library menu. (You don't need to actually import them using that menu, just make sure they are listed.

Open the pongclock5_0.ino file. Click the check mark to check it compiles OK. 

5)
Set your board type and serial connection in the Tools -> Board and Tools -> Serial Port menu (Note: This sketch requires and Arduino with at least 32K RMA e.g. the ATMega 328 CPU

6)
Click the arrow to upload the code. If all is well the clock should start ticking.


Troubleshooting:

I get an error compiling:
*Check the libraries are installed and appear in the menu
*Check you have Arduino software version 1.6.5.

I get an error uploading:
*Check your board type and serial are set correctly in the Tools Menu

The clock doesn’t change:
*Normally a wiring issue. Check the LED on Pin 13 or the Arduino flashes. If not then the clock chip is not being read. Check your connections. You must have a battery connected for the DS1307 to work.

The displays don’t light up
* Check your wiring to the ribbon cables and check the display is getting enough power.

The 2 displays show the same half of the clock
*Check the DIP switch settings on the displays are as per my blog.


