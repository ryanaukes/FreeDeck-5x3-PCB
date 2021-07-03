# FreeDeck-5x3-PCB
This is my PCB design for the 5x3 FreeDeck

DISCLAIMER:
~~Currently I am having problems with one of my builds. I am not sure what the problem is. Soon some other people will try making a 5x3 FreeDeck with this pcb, hopefully they can help me solve the problem. Probably there is just something wrong with my particular build, but it might also be a power issue when using 15 screens.~~

**Update:** Multiple people have made a 5x3 FreeDeck with this PCB design without any problems. Also, my build which was having problems now works fine, so it seems like it is working! I think it was the sd card reader which was broken.


You will need:
- Arduino Pro Micro (32u4 16mhz 5v)
- 2x 74HC4067 Multiplexer Breakout Board
- 15x SSD1306 OLEDs
- 15x 6x6x4.3mm buttons
- SPI-SDcard Reader

The firmware and configurator are developed by Koriwi / FreeYourStream UG (https://github.com/FreeYourStream).
The firmware and configurator can be found here:
- Firmware: https://github.com/FreeYourStream/freedeck-ino
- Configurator: https://github.com/FreeYourStream/freedeck-configurator


To make this PCB work, you will need to make sure that the variables in the settings.h file of the firmware are set to:
- #define BD_COUNT 15
- #define CUSTOM_ORDER // Make sure this is uncommented!
- #define ADDRESS_TO_SCREEN { 15, 10, 5, 14, 9, 4, 13, 8, 3, 12, 7, 2, 11, 1, 6 }
- #define ADDRESS_TO_BUTTON { 15, 10, 5, 14, 9, 4, 3, 8, 13, 12, 11, 6, 1, 7, 2 }
- #define BUTTON_PIN 5
- #define S0_PIN 6
- #define S1_PIN 7
- #define S2_PIN 8
- #define S3_PIN 9

If you have any questions, feedback or ideas for improvement, please let me know!

This work is licensed under Attribution-NonCommercial-NoDerivatives 4.0 International. 
To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-nd/4.0/
