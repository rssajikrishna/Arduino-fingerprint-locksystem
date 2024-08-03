---

# Fingerprint Lock System

This repository contains the code and diagrams for a Fingerprint Lock System using an Arduino. The project leverages a fingerprint sensor module to secure access to a lock system, allowing only authorized users to unlock it.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Circuit Diagram](#circuit-diagram)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The Fingerprint Lock System is a security project that utilizes a fingerprint sensor to grant or deny access. The system is designed to work with an Arduino microcontroller and is ideal for securing doors, lockers, or any other space that requires restricted access.

## Features
- **Fingerprint Authentication**: Only pre-registered fingerprints can unlock the system.
- **User Management**: Add or delete fingerprints from the system.
- **Visual Indicators**: LEDs and an LCD display provide visual feedback.
- **Easy Integration**: Can be integrated with existing locking mechanisms.

## Hardware Requirements
- Arduino Uno or compatible microcontroller
- Fingerprint sensor module (e.g., R305, GT-521F52)
- 16x2 LCD display
- LEDs (Red and Green)
- Resistors (220Ω)
- Push buttons
- Breadboard and jumper wires
- Servo motor (optional for locking mechanism)
- Power supply

## Software Requirements
- [Arduino IDE](https://www.arduino.cc/en/software)
- Adafruit Fingerprint Sensor Library

## Installation
### Setup
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/Fingerprint_Lock_System.git
   cd Fingerprint_Lock_System
   ```

2. **Install the necessary Arduino libraries**:
   - Open the Arduino IDE.
   - Go to `Sketch` -> `Include Library` -> `Manage Libraries`.
   - Search for "Adafruit Fingerprint Sensor" and install it.

3. **Upload the code to Arduino**:
   - Connect your Arduino to your computer.
   - Open `fingerprint_lock.ino` in the Arduino IDE.
   - Select the appropriate board and port.
   - Click the upload button.

## Usage
1. **Register a Fingerprint**:
   - Run the system and follow the instructions on the LCD display.
   - Place your finger on the sensor when prompted to register.

2. **Unlock the System**:
   - Place a registered finger on the sensor to unlock the system.
   - The servo motor (if connected) will rotate to unlock the lock.

3. **Manage Fingerprints**:
   - Use the provided buttons to add or delete fingerprints.

## Circuit Diagram
The following diagram illustrates the connections:

![Circuit Diagram](path/to/circuit_diagram.png)

- **Fingerprint Sensor**:
  - Vcc -> 5V
  - GND -> GND
  - TX -> Pin 2
  - RX -> Pin 3

- **LCD Display**:
  - Vcc -> 5V
  - GND -> GND
  - SDA -> A4
  - SCL -> A5

- **LEDs**:
  - Red LED: Anode -> Pin 8, Cathode -> GND (via 220Ω resistor)
  - Green LED: Anode -> Pin 9, Cathode -> GND (via 220Ω resistor)

- **Buttons**:
  - Connected to digital pins with pull-down resistors.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request with any improvements or new features.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
