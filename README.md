# MPU6050-Sensor-Integration-with-STM32F446RE-using-I2C-Protocol
Integrated the MPU6050 accelerometer and gyroscope sensor with STM32F446RE microcontroller using I2C communication protocol. Implemented real-time sensor data acquisition and calculated Pitch &amp; Roll angles using embedded C in STM32CubeIDE.



# MPU6050 Integration with STM32F446RE using I2C

## Overview

This project demonstrates interfacing the MPU6050 Accelerometer and Gyroscope sensor with the STM32F446RE microcontroller using the I2C communication protocol.

The system reads raw Accelerometer and Gyroscope data from the MPU6050 sensor and processes it to calculate Pitch and Roll angles in real time using Embedded C and STM32 HAL drivers.

---

## Features

- I2C communication with MPU6050
- MPU6050 sensor initialization
- WHO_AM_I register verification
- Accelerometer data acquisition
- Gyroscope data acquisition
- Pitch and Roll angle calculation
- STM32 HAL driver implementation
- UART debugging support
- Real-time sensor monitoring

---

## Hardware Requirements

- STM32F446RE Nucleo Board
- MPU6050 Sensor Module
- Breadboard
- Jumper Wires
- USB Cable

---

## Software Requirements

- STM32CubeIDE
- STM32 HAL Drivers
- Embedded C

---

## Hardware Connections

| MPU6050 Pin | STM32F446RE Pin |
|-------------|-----------------|
| VCC         | 3.3V            |
| GND         | GND             |
| SDA         | PB7             |
| SCL         | PB6             |

---

## I2C Configuration

- I2C Peripheral: I2C1
- SDA Pin: PB7
- SCL Pin: PB6
- Communication Speed: 100kHz

---

## Important MPU6050 Registers

| Register Name | Address |
|----------------|---------|
| WHO_AM_I       | 0x75    |
| PWR_MGMT_1     | 0x6B    |
| ACCEL_XOUT_H   | 0x3B    |
| GYRO_XOUT_H    | 0x43    |

---

## Project Workflow

1. Initialize STM32 peripherals
2. Configure I2C1 interface
3. Wake up MPU6050 from sleep mode
4. Verify sensor connection using WHO_AM_I register
5. Read Accelerometer and Gyroscope raw data
6. Convert raw sensor values
7. Calculate Pitch and Roll angles
8. Display/debug data through UART

---

## Pitch and Roll Calculation

### Roll Formula

\[
Roll = \tan^{-1}\left(\frac{Ay}{Az}\right) \times \frac{180}{\pi}
\]

### Pitch Formula

\[
Pitch = \tan^{-1}\left(\frac{-Ax}{\sqrt{Ay^2 + Az^2}}\right) \times \frac{180}{\pi}
\]

---

