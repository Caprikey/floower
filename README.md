# [![Floower](https://floower.io/wp-content/uploads/2020/04/floower.png)](https://floower.io)

The most advanced flower in the world. Electrical & Mechanical flower lamp that blooms with all the colors of rainbow thanks to the set of RGB LEDs. Flooware is what we called Smart Art. We are aiming to create a technology with soul. That everybody will love.

[floower.io](https://floower.io)

![Everblooming Flowers](https://github.com/jpraus/floower/blob/master/doc/floower.jpeg?raw=true)

## Features

* 6 petals that open and close - operated by servo motor inside the flowerpot
* 7 RGB LEDs in the center of the blossom
* capacitive touch sensor in the leaf
* ESP32 microcontroller
* Arduino IDE or MicroPython support
* Bluetooth & WiFi connectivity
* USB-C interface for programming (CP2102N USB-to-UART)
* 1600 mAh LIPO battery (TP4056 charging IC)
* deep sleep mode to extend battery life
* red charging and blue activity LEDs in the flowerpot

## How do I Get One?

Visit [floower.io](https://floower.io).

## Understanding Floower Hardware

### Logic Boards History

* **Revision 5**
  * Serial numbers 0001 - 0018, 0021, 0022
  * The history starts here
* **Revision 6**
  * Serial numbers 0019, 0020, 0023 - 0132
  * Added USB power detection circuitry
* **Revision 7**
  * Serial numbers 0133 +
  * Ability to charge from quick/smart charges

## Upgrading the Flooware

The Floower firmware is called Flooware. We aim to provide all the Flooware with the latest updates to get the latest features and new seasonal updates. The new age of Smart Art has just begun! [Upgrade your Floower with latest Flooware](https://floower.io/upgrading-floower/).

## Playing With the Code

Flooware is written in Arduino code. It's super easy to understand and develop. If you wish to adjust your Flooware in a unique way. Feel free to clone the project and start writing the code! Any bug-fixes, improvements, or new features are welcomed! Follow up on the next steps to get your IDE setup for Flooware development.

### Installing Prerequisites

Floower can be programmed using the Arduino IDE. However, the ESP32 microcontroller is not supported by default, so you need to install & configure it:

* Prerequisites: [Arduino IDE](https://www.arduino.cc/en/main/software) Installed
* Install [CP2102 Universal Driver](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
  * If you already have a CP2102 driver please make sure you update to the latest version available
* Install ESP32 Add-on in Arduino IDE:
  * Open **File > Preferences**
  * Enter **https://dl.espressif.com/dl/package_esp32_index.json** into the **Additional Board Manager URLs** field and click **OK** button. (If you already have other boards URL, separate the URLs with a comma)

![Additional Board Manager URLs](https://github.com/jpraus/floower/blob/master/doc/arduino-ide-preferences.png?raw=true)

* Open **Tools > Boards > Boards Manager...** and search for esp32
* Click Install button for the **ESP32 by Espressif Systems**. It should be installed after a few seconds.

![Installing ESP32 by Espressif Systems](https://github.com/jpraus/floower/blob/master/doc/arduino-ide-boards-manager.png?raw=true)

* Open **Tools > Boards** and select **DOIT ESP32 DEVKIT V1**

![Selecting DOIT ESP32 DEVKIT V1 board](https://github.com/jpraus/floower/blob/master/doc/arduino-ide-board.png?raw=true)

### Uploading code

* Download / Clone this code repository

![Code repository](https://github.com/jpraus/floower/blob/master/doc/github-code.png?raw=true)

* Open src/flower-esp32/[flower-esp32.ino](src/flower-esp32/flower-esp32.ino) project file with Arduino IDE (it will automatically load all the project files)
* Install following Arduino libraries to full-fill dependencies:
  * Open **Tools > Manage Libraries**, search and install following dependencies:
  * **ESP32Servo** (version 0.9.0 tested)
  * **NeoPixelBus By Makuna** (version 2.6.0 tested)
* Connect your Floower to your computer via USB-C data cable. Make sure you are using smart/data USB cable, some of the cables are power only and thus cannot transfer data at all. Select the port of your Floower **Tools > Port**. It should be the one that just appeared.

![Arduino IDE Port](https://github.com/jpraus/floower/blob/master/doc/arduino-ide-port.png?raw=true)

* Run **Sketch > Upload**. You should get a sweet *'Hard resetting via RTS pin...'* message at the end of the console.
* Now you can make your own personalized Floower.

![Arduino IDE Upload](https://github.com/jpraus/floower/blob/master/doc/arduino-ide-upload.png?raw=true)
