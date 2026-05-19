*[Deutsch](README.MD) | English*

# Peerhof-Uni CC1101

KiCad project for a compact carrier board that combines an **ESP8266 (Wemos D1 Mini)** with a **CC1101 sub-GHz radio module** (e.g. 433/868 MHz). The board acts as a universal radio gateway / transmitter / receiver and can, for example, be used to bridge 433 MHz sensors, actuators, or smart home components to Wi-Fi.

<p>
  <img src="CC1101-ESP-8266-D1-Mini/images/cc1101-d1-mini.png" alt="CC1101 ESP8266 D1 Mini (Light)" height="250">
  <img src="CC1101-ESP8266-D1-Mini-With%20Power%20Supply/images/cc1101-d1-mini-withpowersupply.png" alt="CC1101 ESP8266 D1 Mini with power supply" height="250">
</p>

## Project variants

The repository contains two variants of the same design:

- **[CC1101-ESP-8266-D1-Mini](CC1101-ESP-8266-D1-Mini/)** – *Light version*  
  Slim variant without onboard power supply. Powered directly via the USB connector or the 5 V pin of the D1 Mini. Ideal if a stable 5 V source is already available.

- **[CC1101-ESP8266-D1-Mini-With Power Supply](CC1101-ESP8266-D1-Mini-With%20Power%20Supply/)** – *Variant with power supply*  
  Extended version with an additional on-board power supply for standalone operation (e.g. directly from a higher DC input voltage).

## Features

- ESP8266 based on the Wemos D1 Mini (Wi-Fi, easy programming via USB).
- CC1101 radio module for sub-GHz communication (ASK/OOK, FSK, GFSK, MSK).
- Broken-out pin headers:
  - `J2`: D4 / GND / 5 V
  - `J3`: D3 / D1 / GND / 5 V
  - `J4`: RX / TX / GND / 3.3 V (UART)
- Pad area `AE1` for an external antenna / helical antenna.
- Status LED `D1`.
- Two-layer PCB design; ready-to-use Gerber files are provided in each `gerber/` folder.

## Directory structure

```
CC1101-ESP-8266-D1-Mini/                  KiCad project (Light)
CC1101-ESP8266-D1-Mini-With Power Supply/ KiCad project (with power supply)
└── gerber/                               Manufacturing data (Gerber + drill file)
```

## Usage

1. Open the project in **KiCad** (`.kicad_pro`).
2. Review or modify the schematic (`.kicad_sch`) and layout (`.kicad_pcb`).
3. Send the Gerber files from the corresponding `gerber/` folder to a PCB manufacturer.
4. Populate the board, flash the ESP8266 with the firmware of your choice (e.g. ESPHome, Tasmota with CC1101 patch, your own Arduino sketch) and connect it to the SPI pins of the D1 Mini.

## License

This project is licensed under **CERN-OHL-W-2.0**: <https://ohwr.org/cern_ohl_w_v2.txt>
