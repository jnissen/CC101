# Peerhof-Uni CC1101

KiCad-Projekt für eine kompakte Trägerplatine, die einen **ESP8266 (Wemos D1 Mini)** mit einem **CC1101 Sub-GHz-Funkmodul** (z. B. 433/868 MHz) kombiniert. Die Platine dient als universelles Funk-Gateway bzw. -Sender/Empfänger und lässt sich z. B. zur Anbindung von 433-MHz-Sensoren, Aktoren oder Smarthome-Komponenten an WLAN nutzen.

<p>
  <img src="CC1101-ESP-8266-D1-Mini/images/cc1101-d1-mini.png" alt="CC1101 ESP8266 D1 Mini (Light)" height="250">
  <img src="CC1101-ESP8266-D1-Mini-With%20Power%20Supply/images/cc1101-d1-mini-withpowersupply.png" alt="CC1101 ESP8266 D1 Mini mit Netzteil" height="250">
</p>

## Projektvarianten

Das Repository enthält zwei Varianten desselben Designs:

- **[CC1101-ESP-8266-D1-Mini](CC1101-ESP-8266-D1-Mini/)** – *Light-Version*  
  Schlanke Variante ohne eigene Spannungsversorgung. Versorgung erfolgt direkt über den USB-Anschluss bzw. den 5-V-Pin des D1 Mini. Ideal, wenn bereits eine stabile 5-V-Quelle vorhanden ist.

- **[Peerhof-Uni-CC1101 - With Power Supply](Peerhof-Uni-CC1101%20-%20With%20Power%20Supply/)** – *Variante mit Netzteil*  
  Erweiterte Version mit zusätzlicher Bordspannungsversorgung für den autarken Betrieb (z. B. direkt aus einer höheren DC-Eingangsspannung).

## Funktionen / Merkmale

- ESP8266 auf Basis des Wemos D1 Mini (WLAN, einfache Programmierung über USB).
- CC1101-Funkmodul für Sub-GHz-Kommunikation (ASK/OOK, FSK, GFSK, MSK).
- Herausgeführte Stiftleisten:
  - `J2`: D4 / GND / 5 V
  - `J3`: D3 / D1 / GND / 5 V
  - `J4`: RX / TX / GND / 3,3 V (UART)
- Pad-Feld `AE1` für eine externe Antenne / Helix-Antenne.
- Status-LED `D1`.
- Zweilagiges PCB-Design, fertige Gerber-Daten liegen jeweils im Ordner `gerber/`.

## Verzeichnisstruktur

```
CC1101-ESP-8266-D1-Mini/                  KiCad-Projekt (Light)
Peerhof-Uni-CC1101 - With Power Supply/   KiCad-Projekt (mit Netzteil)
└── gerber/                               Fertigungsdaten (Gerber + Bohrdatei)
```

## Verwendung

1. Projekt in **KiCad** öffnen (`.kicad_pro`).
2. Schaltplan (`.kicad_sch`) und Layout (`.kicad_pcb`) prüfen bzw. anpassen.
3. Gerber-Daten aus dem jeweiligen `gerber/`-Ordner an einen PCB-Hersteller übermitteln.
4. Bestücken, ESP8266 mit gewünschter Firmware flashen (z. B. ESPHome, Tasmota mit CC1101-Patch, eigene Arduino-Skizze) und an SPI-Pins des D1 Mini anschließen.

## Lizenz

Dieses Projekt steht unter der **CERN-OHL-W-2.0** Lizenz: <https://ohwr.org/cern_ohl_w_v2.txt>



