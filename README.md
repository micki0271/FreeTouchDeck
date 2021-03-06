# FreeDeckTouch
For interfacing with Windows/macOS/Linux using an ESP32, a touchscreen and BLE.

### [User guide](https://github.com/DustinWatts/FreeTouchDeck/wiki)

# Pre-Alpha Version!

This version is in it's very early stages of development. Chances are that if you are not using the exact
same testup as I am, you will run in to problems. But that is what this version is for: finding out what is needed
to make FreeTouchDeck work across most ESP's and TFT screens. Also there is a lack of documentation which is gradually being written.

# Hardware used

The hardware I currenlty use is:

- an ESP32 DEVKIT V1 (WROOM32) (Partition scheme: NO OTA with 2MB app and 2MB SPIFFS)
- an 3.5" (480x320) TFT + Touchscreen with ILI9488 driver and XPT2046 touch controller

# !- Library Dependencies -!
- Adafruit-GFX-Library (version 1.10.0), available through Library Manager
- TFT_eSPI (version 2.2.14), available through Library Manager
- ESP32-BLE-Keyboard (latest version), download from: https://github.com/T-vK/ESP32-BLE-Keyboard
- ArduinoJson (version 6.16.1), available through Library Manager

# TFT_eSPI configuration

Before compiling and uploading the FreeTouchDeck.ino sketch, you will have to edit the **user_setup.h** file included with the TFT_eSPI library. This can be found in your Arduino skechtbook folder under "libraries". If you have not renamed the TFT_eSPI library folder, the file **user_setup.h** can be found in **TFT_eSPI-master**. Here you will have to uncomment the lines that apply to you hardware configuration. For example: if you have an TFT with an ILI9488 driver, you will have to uncomment that line under `Section 1`. Make sure all the other drivers are commented out!  

The next section is `Section 2`. This also depends on what hardware you are using. For example for an ESP32 you'll have to uncomment the correct #define(s) under `EDIT THE PIN NUMBERS IN THE LINES FOLLOWING TO SUIT YOUR ESP32 SETUP`. Also if your TFT has the blacklight control pin available you will have to uncomment the lines found under `#define TFT_BL` and `#define TFT_BACKLIGHT_ON`.  

"Section 3" can be left alone.   

# Help

You can join my Discord server where I have a dedicated #freetouchdeck channel. https://discord.gg/RE3XevS
