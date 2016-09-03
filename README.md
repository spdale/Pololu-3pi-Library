# Pololu 3pi Robot Library

_This is the Pololu Orangutan and 3pi Robot add-on for the Arduino IDE reorganized to make it usable/compatible with the Arduino IDE 1.6.x and 1.7.x as the code provided from Pololu does not work out of the gate._

To implement the library, all you have to do is:

1. Get the Arduino IDE from either http://www.arduino.org/downloads or https://www.arduino.cc/en/Main/Software
2. Download the library and unzip it.
3. Move the "libraries" folder into your Arduino folder (if you already have a "libraries" folder, just copy the contents of this folder into your pre-existing folder). When you're done it'll look like this: ` /Users/<user>/Documents/Arduino/libraries/PololuLib `
4. Move the "hardware" folder into your Arduino folder, which should be located in your documents folder. When you're done it'll look like this: ` /Users/<user>/Documents/Arduino/hardware/PololuHardware `

__All Done__. That's it. Pretty simple. To make sure everything is installed correctly check these things:
- You should see several new entries in the "Examples" menu, like "OrangutanMotors" and "OrangutanLCD".
- You should see entries for the Orangutans in the Board menu.
- You should see an entry for the Pololu USB AVR Programmer in the Programmer menu.

## Using the Code
Using this library, you can import any of the library code into your own Arduino projects.


For example, I have a project I'm working on stored in:
```
/Users/<user>/Documents/Arduino/no_bugs_bunny/no_bugs_bunny.ino
```
And in that file I have this code so that I can control my 3pi robot:
```cpp
#include <Pololu3pi.h>
#include <PololuQTRSensors.h>
#include <OrangutanMotors.h>
#include <OrangutanAnalog.h>
#include <OrangutanLEDs.h>
#include <OrangutanLCD.h>
#include <OrangutanPushbuttons.h>
#include <OrangutanBuzzer.h>

Pololu3pi robot;
unsigned int sensors[5]; // an array to hold sensor values
```

### Once You've Written the Code
Once you've written your code and are ready to upload it to your 3pi, make sure to select "**Pololu Orangutan or 3pi robot w/ ATmega328P**" under *Tools > Board* in the menu, as well as "**Pololu USB AVR Programmer**" under *Tools > Programmer* in the menu. Then under *Tools > Port* select something that looks like: **/dev/tty.usbmodem00146721**, making sure to choose the lowest number.

## Demo Code
I've also included the demo code for the 3pi (the code that is installed on the 3pi when you first get it), which Pololu never wrote for the Arduino language.

*Note that it was translated from c code to .ino code by Richard Firth at https://forum.pololu.com/t/3pi-demo-code-on-arduino/8731*



Important: I lay no claim to the library as my own code, I've simply reorganized it to be compatible with Arduino. I've also included the original license.txt in both parts of the library. The original code can be found at:  https://www.pololu.com/docs/0J17