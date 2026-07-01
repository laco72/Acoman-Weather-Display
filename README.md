# 🌤️ Acoman Weather Display

Modern ESP32 Weather Display firmware with OTA updates and a multilingual web interface.

---

## ✨ Features

- OTA firmware updates (.bin)
- Web-based configuration
- Current weather conditions
- Multi-day weather forecast
- Powered by Open-Meteo API
- Photo slideshow
- RGB LED effects
- Display brightness control
- Automatic Night Mode
- Multilingual web interface

### 🌍 Supported Languages

- 🇬🇧 English
- 🇸🇰 Slovak
- 🇩🇪 German
- 🇫🇷 French
- 🇪🇸 Spanish
- 🇮🇹 Italian
- 🇸🇪 Swedish
- 🇹🇷 Turkish

---

## ☁️ Weather Data

Weather data is provided by the free Open-Meteo API.

### Benefits

- No API key required
- Free weather service
- Current weather conditions
- Multi-day weather forecast
- Reliable weather data

https://open-meteo.com/

---

## 🔧 Supported Hardware

Currently tested only with:

- ESP32E 2.8" Display
- Resolution: 240 × 320
- LCD Driver: ST7789
- Touch Controller: RTP

**SKU:** E32R28T-1

> Other ESP32 display boards have not been tested yet and may require code modifications.

---

## 📥 Firmware

Download the latest firmware from the **Releases** section.

The firmware is provided as a **.bin** file.

Future updates can be installed directly from the built-in OTA web interface without using Arduino IDE.

---

## 📦 First Installation (New Device)

### Requirements

- ESP32E 2.8" Display (SKU: E32R28T-1)
- USB cable
- [ESP32 Flash Download Tool v3.9.10](https://docs.espressif.com/projects/esp-test-tools/en/latest/esp32/production_stage/tools/flash_download_tool.html)

### Step 1 — Flash the firmware (one time only via USB)

Download all 4 files from the **Releases** section and flash them using ESP32 Flash Download Tool:

| File | Address |
|------|---------|
| `bootloader.bin` | `0x1000` |
| `partitions.bin` | `0x8000` |
| `boot_app0.bin` | `0xE000` |
| `firmware.bin` | `0x10000` |

**Flash Download Tool settings:**
- ChipType: `ESP32`
- WorkMode: `Develop`
- SPI Speed: `80MHz`
- SPI Mode: `DIO`
- Baud: `921600`

Click **START**. When finished, disconnect and reconnect the USB.

---

### Step 2 — WiFi Setup

On first boot, the device creates a temporary WiFi network:

1. Connect your phone to **`Acoman-Setup`** (Password: `12345678`)
2. Open your browser → go to `192.168.4.1`
3. Select your home WiFi network and enter the password
4. The device restarts and connects to your WiFi

---

### Step 3 — Open Settings

Long press the display → IP address appears.  
Open `http://[IP address]` in your browser to configure:

- Location / city
- Language
- Display brightness
- RGB LED
- Photos

---

### ⬆️ Future Updates (OTA — no USB needed)

After the first installation, all future firmware updates can be done wirelessly:

1. Open `http://[IP address]` in your browser
2. Scroll down to **Firmware** section
3. Click **Update firmware**
4. Select the new `.bin` file
5. Click **Upload and flash**

The device restarts automatically with the new firmware. ✅

---

## 📖 User Guide

The complete English User Guide is available here:

**docs/User_Guide_EN.pdf**

---

## 🖼️ 3D Printed Enclosure

This repository contains **firmware only**.

The 3D enclosure is **NOT included**.

The enclosure was designed by another creator and can be downloaded from MakerWorld:

https://makerworld.com/cs/models/1382304-aura-smart-weather-forecast-display

**Full credit for the enclosure goes to the original designer.**

---

## 🚀 Future Development

This project is actively under development.

Support for additional ESP32 display boards will be added as new hardware becomes available for testing.

If you would like to support the project, your Ko-fi donations help fund the purchase of additional ESP32 display modules for development, testing and compatibility improvements.

### Planned hardware support

- ESP32-2432S028R
- ESP32-3248S035 (3.5")
- ESP32-8048S043
- ESP32-8048S070
- Other ESP32 display boards

Future plans also include:

- Additional display sizes
- More language translations
- New display themes
- More weather information
- Performance improvements
- Bug fixes

Every contribution helps make this project better.

Thank you for your support! ❤️

---

## ☕ Support

If you enjoy this project and would like to support future development, you can buy me a coffee on Ko-fi.

**Ko-fi**  
https://ko-fi.com/acoman72

Your support helps fund:

- New ESP32 display boards
- Development and testing
- New firmware features
- Compatibility improvements
- Long-term project maintenance

Thank you very much for your support! ❤️

---

## 📜 License

Copyright © 2026 Acoman72

This repository contains documentation and firmware releases.

The firmware is provided **as is**, without warranty of any kind.

All product names, trademarks and registered trademarks are the property of their respective owners.
