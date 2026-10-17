# ESP32 LoRa Receiver Unit

## 1. Overview

The receiver unit is part of the **IoT-Based Adaptive Emergency Vehicle Management System**. It uses an ESP32 DevKit V1 and an SX1278 RA-02 LoRa module to receive wireless packets from the transmitter unit.

The receiver is intended to demonstrate emergency vehicle priority through a traffic signal LED arrangement.

## 2. Hardware Components

- ESP32 DevKit V1
- SX1278 RA-02 LoRa module
- Traffic signal LEDs
- Current-limiting resistors
- 74HC595 shift registers, where used in the implemented circuit
- Jumper wires and breadboard, as required
- USB cable for programming and power

## 3. Working Principle

The ESP32 initializes the LoRa receiver and waits for incoming wireless packets.

When a packet is received, the receiver firmware processes it and performs the programmed output action. For the basic communication demonstration, this action may be a brief LED indication confirming packet reception.

Traffic signal control can be implemented through direct ESP32 GPIO outputs or through cascaded 74HC595 shift registers, depending on the final circuit configuration.

## 4. Communication Interface

The SX1278 communicates with the ESP32 using SPI. Chip-select, reset, and other required control signals must match the receiver firmware configuration.

If 74HC595 shift registers are used, the ESP32 controls their serial data, shift clock, and latch signals to update the connected LED outputs.

## 5. Hardware Connections

### A. ESP32 DevKit V1 to SX1278 RA-02

The receiver uses the SX1278 RA-02 module to receive wireless packets from the transmitter. The LoRa module is connected to the ESP32 through SPI.

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

### B. Traffic Signal LED Connections

The following table describes the direct GPIO connections for the two traffic signal groups.

| Signal | LED Colour | ESP32 GPIO |
|---|---|---|
| Signal 1 | Red | GPIO 4 |
| Signal 1 | Yellow | GPIO 13 |
| Signal 1 | Green | GPIO 21 |
| Signal 1 | Blue | GPIO 22 |
| Signal 2 | Red | GPIO 25 |
| Signal 2 | Yellow | GPIO 27 |
| Signal 2 | Green | GPIO 32 |
| Signal 2 | Blue | GPIO 33 |

### Connection Notes

- Connect each LED with a suitable current-limiting resistor.
- Connect the LED circuit ground to ESP32 GND.
- Confirm that the LED GPIO assignments match the receiver firmware.
- The LED table describes a direct GPIO arrangement and does not represent a 74HC595 shift-register connection.
- Verify the wiring before powering the circuit.

## 6. Software Requirements

- Arduino IDE
- ESP32 board support package
- Compatible LoRa library
- Additional libraries, if required by the implemented firmware

## 7. Testing Procedure

1. Connect the receiver ESP32 to the computer.
2. Select the correct board and serial port.
3. Upload the receiver firmware.
4. Open Serial Monitor using the baud rate specified in the code.
5. Confirm successful LoRa initialization.
6. Start the transmitter and verify that the receiver detects incoming packets.
7. Check the LED response programmed for packet reception.

## 8. Expected Demonstration

The receiver waits for packets from the transmitter. Upon receiving a valid packet, it performs the corresponding programmed LED action.

The basic communication test demonstrates wireless packet reception. Route-specific traffic signal prioritization should only be described as operational if it has been implemented and tested.

## 9. Project Scope and Limitations

The receiver demonstrates LoRa communication and LED-based output control. Integration with live GPS data, the website, or real traffic infrastructure is outside the verified scope unless separately implemented and tested.

The prototype is intended for demonstration and educational purposes.

## 10. Folder Contents

- `README.md` – Receiver unit overview, hardware connections, and working principle.
- `receiver.ino` – Receiver source code.
- `wiring_diagram.png` – Receiver hardware connection diagram.

