# CAN-Based-ECU-Interface-for-Automotive-Control
This project demonstrates the implementation of inter-ECU communication using the **CAN (Controller Area Network)** protocol, widely used in automotive systems for robust and efficient data exchange.
  
**Date**: 18-05-2025.

## Overview

The goal of this project is to enable communication between two or more ECUs (Electronic Control Units) configured in a **multimaster** setup with minimal wiring complexity. The CAN protocol allows multiple nodes to communicate over a shared bus without a host computer, making it ideal for real-time automotive control applications.

## Working Video

https://github.com/user-attachments/assets/f2d31253-ad66-47df-94bc-f58fa19650fc

## Key Features

- **Multimaster Communication**: Each ECU can send and receive messages independently.
- **CAN Protocol Implementation**: Using LPC2129 microcontrollers with built-in CAN controllers.
- **Automotive Use Case**: Simulates headlight and indicator control in a vehicle.
- **Interrupt-Driven Handling**: Efficient message processing using interrupts.
- **Modular Design**: Easily extendable for more ECUs or control modules.

## Hardware Components

- 2 × **LPC2129 Microcontrollers**
- 2 × **MCP2551 CAN Transceivers** (Some development boards comes with built-in can transceivers, in that case find the canh and canl connections)
- 4 × Push Button Switches (Headlight, Left Indicator, Right Indicator, Hazard lights)
- 8 × LEDs to represent light outputs
- Power Supply (5V regulated)
- Common CAN Bus Wiring

## Use Case

- **ECU 1 (Control Unit)**: Reads input from switches (headlight, left/right indicators, Hazard lights) and sends corresponding CAN messages.
- **ECU 2 (Actuator Unit)**: Receives CAN messages and controls LEDs to represent the activation of headlights, indicators and Hazard lights.

## Connection Diagram
![Image](https://github.com/user-attachments/assets/653c22c2-8396-4d62-823d-8281b1eda03b)


## Future Improvements

- Support for additional ECUs (e.g., wiper control, brake lights)
- CAN message filtering and prioritization
- Fault detection and error handling
- Real-time display (LCD/OLED) for status monitoring
- Integration with diagnostic tools (OBD interface)

## Getting Started

To run this project:

1. Set up the LPC2129 development boards with MCP2551 CAN transceivers.
2. Flash the appropriate Hex file to ECU 1 (Node A) and ECU 2 (Node B).
3. Connect both nodes to a common CAN bus (CANH and CANL lines).
4. Power the boards using a stable 5V power supply.
5. Press the switches on ECU 1 (Node A) and observe LED responses on ECU 2 (Node B).

## -------Codes are uploaded in the respective folders-------




