# ESP32 LoRa Transmitter Unit

## 1. Overview

The transmitter unit is a hardware component of the **IoT-Based Adaptive Emergency Vehicle Management System**. It uses an ESP32 microcontroller and an SX1278 RA-02 LoRa module to transmit wireless packets to the receiver unit.

## 2. Hardware Components

- ESP32 DevKit V1
- SX1278 RA-02 LoRa module
- USB cable for programming and power
- Jumper wires and breadboard, as required

## 3. Working Principle

The ESP32 executes the transmitter firmware and initializes the LoRa module. After successful initialization, the transmitter sends data packets wirelessly using LoRa communication.

The receiver unit is designed to receive these packets and respond according to its programmed logic.

The transmitter and receiver must use compatible LoRa communication settings and packet formats.

## 4. Communication Interface

The SX1278 communicates with the ESP32 through the SPI interface. Additional control signals, such as chip select, reset, and DIO0, are connected according to the firmware configuration.

## 5. Hardware Connections

### ESP32 DevKit V1 to SX1278 RA-02

The SX1278 RA-02 LoRa module communicates with the ESP32 through the SPI interface. The following pin configuration is used for the transmitter unit.

| SX1278 RA-02 Pin | ESP32 DevKit V1 Pin |
|---|---|
| VCC | 3.3V |
| GND | GND |
| SCK | GPIO 18 |
| MISO | GPIO 19 |
| MOSI | GPIO 23 |
| NSS / CS | GPIO 5 |
| RESET | GPIO 14 |
| DIO0 | GPIO 26 |

### Connection Notes

- Use a regulated 3.3V supply for the RA-02 module.
- Connect the ESP32 and LoRa module grounds together.
- Ensure that the pin assignments match the transmitter firmware.
- Verify all connections before powering the circuit.

**Important:** The RA-02 operates at 3.3 V. Connect its power and signal pins carefully, and verify the wiring before powering the circuit.

## 6. Software Requirements

- Arduino IDE
- ESP32 board support package
- Compatible LoRa library, such as the library used by the transmitter firmware

## 7. Testing Procedure

1. Connect the transmitter ESP32 to the computer.
2. Select the correct ESP32 board and serial port in Arduino IDE.
3. Upload the transmitter firmware.
4. Open Serial Monitor at the baud rate specified in the code.
5. Check whether LoRa initialization succeeds.
6. Verify packet transmission and test reception using the receiver unit.

## 8. Expected Demonstration

The transmitter sends LoRa packets, and the receiver should respond only after successfully receiving a valid packet, according to the implemented firmware logic.

## 9. Project Scope

This module demonstrates wireless communication for the emergency vehicle management project. Live GPS transmission and direct integration with the website should only be claimed when implemented and verified.

## Folder Contents

- `README.md` – Transmitter unit overview, hardware connections, and working principle.
- `transmitter.ino` – Transmitter source code.
- `wiring_diagram.png` – Hardware connection diagram.

