I'd seen a friends Pin2DMD display and was inspired to create my own from scratch but dedicated to Classic Arcade Games instead. Thus this project was born. I initially found a project at https://www.brainy-bits.com/post/making-an-arduino-animated-frame-with-256-rgb-leds and proceeded down this path. Unfortunately the quality and reliability of the strips and joins were not good and I was constantly dealing with poor connections. I could have soldered the joins but thats a LOT of work and my soldering skills are awful!

The result was a working version that was more than a little touchy. I'd also used a Mega 2560 DEV Board and my original sprite animation filled the limited memory VERY quickly not giving me a lot of room to move so to speak. Enter some ESP32 Dev Baords with 4 times the capacity along with integrate WiFi and Buetooth. Coupling these with a now readily available pre-built 16 x 16 LED Matrix panels, I revisited this project with a more power and more flexibility.

I'm no programmer only ever doing small things with plenty of reading help. This code is roughly now made up of:

2% Brainy Bits Code

60% My Code

38% ChatGPT Code

This is my WIP 16 x 16 RGB LED MAtrix build I've done using an ESP32 WROOM Devlelopment Board

The file currently includes 18 selectable Animation effects with break code for new selections. 

NOTE: You must use Arduino IDE version less than version 2.0 as the modules being used have not been ported to the new format and when they have been are not complete. I'm currently using 1.8.19. You can have both versions installed side by side like I have

Modules include:

WiFi.h
WebServer.h
FS.h
SPIFFS.h
FastLED.h

The Arcade Sprite Animation routine currently has around 40 different animations running in a loop so it can take a while to see all sprites.
I am in the process of adding more and always tweaking the code for speed. The animations were built in a stop go style inside excel so
that the RGB Colour values would be generated automatically in the appropriate array format for pasting into the Arduino IDE.

The current code puts the ESP32 development board into AP mode for WiFi. This is purely for security as IOT devices are notoriously
insecure. Furthermore the current model I have won't connect to 5ghz and my home network is problematic with that. You can then connect
to the ESP with either your mobile phone or computer to load the Webpage for animation selection and control.

Enhancements to come.

The LED Control webpage code is VERY basic for now as I'm concentrating on the Arduino Sketch file first. 

This file MUST be located inside a folder called 'data' as a sub-directory of your Arduino Project Folder. 

This is where the ESP32 sketch data upload plugin expects to find it. The ESP32 sketch data upload plugin will then upload it to the appropriate directory on your ESP32.

See the finished product in action here: https://youtu.be/e1y0VzniGp8 and here: https://youtu.be/0bC53ncdpsY

Full construction journey here: https://www.aussiearcade.com/topic/96389-rgb-led-light-panel/#comment-1294442

