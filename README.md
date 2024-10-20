This is my WIP code for a 16 x 16 RGB LED MAtrix build I've done using an ESP32 WROOM Devlelopment Board

The file currently includes 18 selectable Animation effects with break code for new selections. 

NOTE: You must use Arduino IDE version less than version 2.0 as the modules being used have not been ported to the new format and when they have been are not complete. I'm currently using 1.8.19. You can have both versions installed side by side like I have

Modules include:

#include <WiFi.h> //Includes the default Arduino WiFi Library
#include <WebServer.h> //Includes the default Arduino WebServer
#include <FS.h> //Includes the default Arduino File Server function
#include <SPIFFS.h> //Includes Arduino File Storage function
#include <FastLED.h> //Includes the FastLED Module for RGB light controls

The Arcade Sprite Animation routine currently has around 40 different animations running in a loop so it can take a while to see all sprites.
I am in the process of adding more and always tweaking the code for speed. The animations were built in a stop go style inside excel so
that the RGB Colour values would be generated automatically in the appropriate array format for pasting into the Arduino IDE.

The current code puts the ESP32 development board into AP mode for WiFi. This is purely for security as IOT devices are notoriously
insecure. Furthermore the current model I have won't connect to 5ghz and my home network is problematic with that. You can then connect
to the ESP with either your mobile phone or computer to load the Webpage for animation selection and control.

Enhancements to come.

The LED Control webpage code is VERY basic for now as I'm concentrating on the Arduino Sketch file 1st. This file MUST be located inside a folder called 'data' as a sub-directory of your Arduino Project Folder. This is where the ESP32 sketch data upload plugin expects to find it. The ESP32 sketch data upload plugin will then upload it to the appropriate directory on your ESP32.
