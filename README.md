## Overview

This project is a custom RP2040-based **Power Distribution Board**, designed for use in an avionics stack comprising three CAN-connected PCBs:  
- Sensor Board  
- Power Distribution Board **(this board) ** 
- GPS Board

The system is intended for **high-power model rocketry**, and this board’s primary role is to **distribute power** to the rest of the system while also managing essential subsystems such as communication, monitoring, and recovery signaling.

---

## 📡 PCB Features

- High-current 3.3 V synchronous buck converter (up to 3 A), operating at 1.5 MHz and ~95% efficiency  
- Low-noise LDO with 60 dB PSRR @ 100 Hz, delivering up to 500 mA at 3.3 V  
- Single-cell Li-ion/LiPo battery protection IC with over-voltage, under-voltage, and over-current protection  
- CAN controller and transceiver  
- RP2040 microcontroller  
- USB-C interface  
- Onboard status LEDs for buck converter, MCU status, and USB-C diagnostics  
- External 128 Mbit W25Q128JVS flash memory  
- MAX98357A I²S digital amplifier connected to a speaker for audible recovery


---

## ✅ PCB Design Criteria

This board was designed to meet the following system-level criteria:

- **Stable, low-noise 3.3 V rail** for analog/digital loads — supports up to 500 mA with minimal line/load regulation (target: ±0.1%)
- **High-current 3.3 V rail** capable of supplying up to 3 A to downstream PCBs
- **Battery protection** for a 1S LiPo cell, including self-recovery from under-voltage and short-circuit protection
- **CAN bus communication interface** to enable modular system design with multiple nodes
- **Audible recovery system** — implemented using the **MAX98357A I²S Class-D amplifier**, which drives a speaker directly from the RP2040 using digital audio

---

## 📷 Media

**Schematic**  
<img width="1198" height="825" alt="Schematic" src="https://github.com/user-attachments/assets/0feec0ab-8769-4062-970b-4b7c44f42931" />

**PCB Layout**  
<img width="727" height="726" alt="PCB" src="https://github.com/user-attachments/assets/56e3cc84-d94c-4757-b918-3196ad6e1237" />

**3D Model**  
<img width="897" height="824" alt="3D Model" src="https://github.com/user-attachments/assets/790dbb87-3a3d-4196-b3ab-e01e4494cdfc" />
