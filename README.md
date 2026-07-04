# ESP32 Production Firmware Workshop

> **By Analog Data** · Instructor: [Rajath Kumar K S](https://analogdata.io)

Production-grade ESP32 firmware development using **ESP-IDF**, **FreeRTOS**, **WiFi**, and **MQTT** — from first principles to deployable embedded systems.

---

## Prerequisites

- **ESP-IDF v6.0.1** installed via [EIM (ESP-IDF Installer Manager)](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html)
- **VS Code** with the [ESP-IDF Extension](https://marketplace.visualstudio.com/items?itemName=espressif.esp-idf-extension)
- **Hardware** — any ESP32 board: DevKit / XIAO S3 / C3 SuperMini / PCB Cupid ESP32C6  
  _or_ use the [Wokwi simulator](https://wokwi.com) (no hardware needed)

---

## Quick Start

```bash
git clone https://github.com/analogdatacorp/b2-esp32-prod-firmware-workshop.git
cd b2-esp32-prod-firmware-workshop
```

---

## Repository Structure

```
b2-esp32-prod-firmware-workshop/
├── day1/
│   ├── 01-why-esp-idf/              # Why ESP-IDF over Arduino
│   ├── 02-esp32-architecture/       # ESP32 internals & memory map
│   ├── 03-cmake-menuconfig/         # Build system & Kconfig
│   ├── 04-gpio-production-patterns/ # GPIO with error handling & RTOS
│   └── 05-i2c-uart-peripherals/     # I2C & UART sensor integration
├── day2/                            # Day 2 sessions (WiFi, MQTT, OTA)
└── docs/
    ├── cheatsheet/                  # ESP-IDF quick reference
    ├── datasheets/                  # Component datasheets
    └── Pin Out Diagrams/            # Board pinout references
```

Each session folder contains:
- **Session Notes** (`.md` + `.pdf`)
- **`experiments/`** — hands-on code examples
- **`README.md`** — session-specific guide

---

## Building & Flashing a Project

```bash
# Navigate into any experiment folder
cd day1/04-gpio-production-patterns/experiments/<project-name>

# Activate ESP-IDF environment
get_idf

# Set your target chip (esp32 / esp32s3 / esp32c3 / esp32c6)
idf.py set-target esp32

# Build
idf.py build

# Flash and open serial monitor (replace PORT with your serial port)
idf.py -p PORT flash monitor
```

> **Tip:** Press `Ctrl+]` to exit the serial monitor.

---

## Wokwi Simulation

Every experiment that supports simulation includes a `wokwi/` subfolder with a `diagram.json`.

1. Open [wokwi.com](https://wokwi.com)
2. Click **Open from file** and load `diagram.json`
3. Build the project and upload the firmware binary

No physical hardware required.

---

## Workshop Details

| | |
|---|---|
| **Instructor** | Rajath Kumar K S |
| **Platform** | Zoom (Online) |
| **Website** | [analogdata.io](https://analogdata.io) |
| **Workshop Portal** | [build.analogdata.io](https://build.analogdata.io) |

---

*© Analog Data. All rights reserved.*
