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
