# OpenVampireESP32 v0.12.19

ESP32 Web Interface for Vampire Solar Controller

## Features

- Web monitoring
- Real-time telemetry
- Complete Vampire configuration
- Vampire firmware update
- ESP32 OTA update
- Bluetooth bridge
- Automatic AP shutdown after Wi-Fi connection
- Wi-Fi LED indication
- Fuse configuration
- MPPT configuration

## What's new

### OTA

- Stable ESP32 OTA update
- Automatic browser reconnect after OTA

### Vampire Update

- Stable local firmware upload
- Correct bootloader detection
- Reliable firmware flashing

### Wi-Fi

- OpenVampire AP automatically switches off after 5 minutes
  when ESP32 is connected to a router.

### UI

- Improved update pages
- Improved telemetry
- Fixed regulator settings
- Improved fuse configuration page

## Memory Usage

Flash: 1683873 bytes (95.2%)

RAM: 60004 bytes (18.3%)

## Requirements

ESP32 DevKit V1

PlatformIO

Arduino Framework

## Version

0.12.19



# OpenVampireESP32 v0.12.20

No Bluetooth Stability Test

## Purpose

This version completely removes Bluetooth support to verify long-term
stability of the web interface.

## Features

- Web monitoring
- Real-time telemetry
- Complete Vampire configuration
- Vampire firmware update
- ESP32 OTA update
- Wi-Fi LED
- Automatic AP shutdown
- Fuse configuration
- MPPT configuration

## Removed

- BluetoothSerial
- Bluetooth bridge
- Bluetooth service
- Bluetooth background tasks

## Advantages

Much lower memory usage

Flash:

919305 bytes

RAM:

45840 bytes

Large free space for future features such as MQTT.

## Version

0.12.20

# OpenVampireESP32 v0.12.22

No Bluetooth + MQTT Test

## Features

- Web monitoring
- Real-time telemetry
- Vampire firmware update
- ESP32 OTA update
- MQTT support
- Wi-Fi LED
- Automatic AP shutdown
- Fuse configuration
- MPPT configuration

## MQTT

Settings:

- Enable
- Broker
- Port
- Username
- Password
- Publish period

Topic

tele/VAMPIRE/SV-xxxxxxxx/STATE

Published values

- PV1
- PV2
- PC1
- PC2
- PW1
- PW2
- BAT
- SOC
- CHR
- DSC
- LOAD
- OUT

Publish period

Per = 0

→ every 60 seconds

Per > 0

→ every Per seconds

## Memory Usage

Flash:

935777 bytes

RAM:

46040 bytes

## Version

0.12.22
# OpenVampireESP32 v0.12.24

## Overview

OpenVampireESP32 is an ESP32-based web interface for the Vampire Solar Controller.

This firmware provides real-time monitoring, configuration, firmware updates and MQTT support through a modern web interface without requiring additional software.

---

## Features

- Web-based monitoring
- Real-time telemetry
- Vampire configuration
- Fuse configuration
- MPPT configuration
- ESP32 OTA update
- Vampire firmware update
- Wi-Fi configuration
- MQTT support
- Automatic Wi-Fi Access Point management
- Wi-Fi signal indicator
- Uptime display

---

## New in v0.12.24

### Wi-Fi Status Indicator

The header now includes a graphical Wi-Fi signal indicator similar to a mobile phone.

Features:

- Four-level signal indicator
- Active bars are blue
- Inactive bars are light gray
- RSSI displayed in dBm
- Automatic signal level update

Signal levels:

| RSSI | Bars |
|------|------|
| ≥ -55 dBm | ████ |
| -56…-67 dBm | ███□ |
| -68…-80 dBm | ██□□ |
| -81…-90 dBm | █□□□ |
| < -90 dBm | □□□□ |

When the controller operates in Access Point mode, the indicator displays **WiFi AP**.

---

## Header Information

The top status bar now displays:

- Vampire Serial Number
- Wi-Fi Signal Strength
- RSSI (dBm)
- ESP32 Uptime

Second line:

- Vampire Firmware Version
- ESP32 Firmware Version
- IP Address

---

## MQTT

MQTT is optional and can be enabled or disabled from the web interface.

Published topic:

```
tele/VAMPIRE/SV-xxxxxxxx/STATE
```

Published values:

- PV1
- PV2
- PC1
- PC2
- PW1
- PW2
- BAT
- SOC
- CHR
- DSC
- LOAD
- OUT

---

## Firmware Updates

Supported:

- ESP32 OTA update
- Vampire firmware update

Both update methods have been tested and verified.

---

## Memory Usage

Flash:

```
935777 bytes
```

RAM:

```
46040 bytes
```

This version provides a large amount of free memory for future development.

---

## Hardware

- ESP32 DevKit V1
- Vampire Solar Controller

---

## Build

PlatformIO

Arduino Framework

---

## Version

```
0.12.24-wifi-bars-test
```

---

## Changelog

### Added

- Graphical Wi-Fi signal indicator
- Uptime display in header
- Mobile-style signal bars

### Improved

- Header status information
- User interface readability

### Previous Features

- Stable ESP32 OTA
- Stable Vampire firmware update
- MQTT support
- Automatic AP shutdown
- Web configuration
- Real-time telemetry

OpenVampire ESP32 v0.12.39 – Unified SVG Logo & UI Improvements
Statistics

Energy statistics improvements from previous test versions remain available:

Daily power graph.
Monthly energy bar chart.
Yearly energy bar chart.
Selectable displayed parameter.
Daily / Monthly / All-time summaries.
CSV export.
