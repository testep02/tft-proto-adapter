TFT-Proto Adapters
=================================================================================
The files in this repository are schematics and boards for use in Eagle that provide an easy connection for the TFT-Proto from MikroE to the STM32F4 Discovery. There are 3 different variations of the board in this repository. All of these designs have been verified to work. They can easily be printed through OshPark.

Features
---------------------------------------------------------------------------------
-  TFT backlight connected to a pin to allow PWM control
-  Backlight powered from 5V instead of 3.3V to allow for brighter viewing
-  Backlight controlled through a transistor to prevent driving the LEDs directly from a pin
-  Reset pin also routed through a transistor and connected to a pin for software control

Variations
---------------------------------------------------------------------------------
-  16-bit FSMC Portrait
	-  This version of the board mounts the TFT in portrait mode
	-  The connection to the STM32F4 Discovery is 16-bit parallel and uses FSMC.
-  16-Bit FSMC Landscape
	-  Same as the above variation, except with this one the board is laid out so that the screen is in landscape configuration. This is the variatioon I use.
-  16-bit GPIO
	-  Uses entire GPIOE port for data lines
	-  Uses sme pins on the GPIOB port for control
	-  IM[3:0] are connected to header pins to allow configuration between 16-bit and 8-bit
	-  Is not connected to the FSMC pins, so bit-banging is required

Code Examples
---------------------------------------------------------------------------------
Examples of driving the TFT-Proto can be found in my other repository. The drivers include all init code and basic drawing functions.
