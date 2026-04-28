# Hardware Inventors - Course Project 2026

> **Project Overview**
> * **Board:** Dual-MCU Control & Sensor Interface Board (ESP32 + STM32)
> * **Developer:** [Youssef Adel Wahba Boutros](https://www.linkedin.com/in/youssefadell11/) | *Mechatronics and Robotics Engineering*
> * **Guided by:** [Eng. Mahmoud Arafa](https://www.linkedin.com/in/mahmoud-arafa-63b1531a2/)
> * **Notion Workspace:** [Project Documentation](https://www.notion.so/Hardware-Inventors-Course-Project-2026-7ea26675174749a98fd0bd589b33706b?source=copy_link)

---

## System Architecture: Dual-MCU Topology

### 1. ESP32 Subsystem
This subsystem maps the ESP32 module's role as the primary sensor interface and communication hub. It details the I2C and SPI connections to the BME280 and LIS3DH sensors, analog input from the LDR circuit, and the core power and debug routing. The ESP32 handles environmental data collection and communicates with the main STM32 controller via a dedicated UART bus.

### 2. STM32 Subsystem
This subsystem outlines the STM32F407's core responsibilities, focusing on hardware control, high-speed memory, and external bus interfacing. It traces the logic paths for the 12V motor drive via BJT, external CAN bus communication, ADC signal conditioning for V-BUS sensing, and the QSPI interface for the W25Q512JEIQ flash memory.

### 3. Power Distribution Network
Both 5V and 3.3V voltage rails feature dedicated Power Status LEDs.

---

## Component BOM (Bill of Materials) 

| Component / MPN   | Category | Function / Description                     |
| :---------------- | :------- | :----------------------------------------- |
| **STM32F407VGT6** | MCU      | Primary Motor & System Controller          |
| **ESP32 Module**  | MCU      | Sensor Hub & UART Interface                |
| **W25Q512JEIQ**   | Memory   | QSPI Flash Memory (512Mb)                  |
| **BME280**        | Sensor   | Digital Environmental Sensor (I2C)         |
| **LIS3DH**        | Sensor   | 3-Axis Accelerometer (SPI)                 |
| **LDR Circuit**   | Sensor   | Analog Darkness Sensing (ADC)              |
| **TPS62130RGTR**  | Power    | Step-Down Buck Converter (12V➔5V, 5V➔3.3V) |

---
