# Tsar

This repository contains Tsar flight computer that I have been developing for autonomous vehicles. The goal is to build a general-purpose & fully programmable flight computer that can be used for any autonomous model vehicles. The design is intended to be modular, cost-effective, and easy to manufacture.

The PCB is designed in KiCad and updated to version 8.0.3.

## Version History

### V3 [Latest Version]

![V3](./assets/v3.png)

The design is very similar to V2 but with different IO style and no pyro channels. The secondary chip is STM32G0 for a lower number of components. The design is still in progress.

#### Key Features:
- Main Dual core ESP32-S3
- Secondary STM32G0 as an IO extender
- 2.4GHz SX1280 radio
- Ublox-M10S GNSS
- BMI088 IMU (up to ± 24 g, ± 2000°/s)
- BMP390 barometer (up to 10KM), MMC5983MA magnetometer for heading
- SD card and flash (ESP32-S3 inbuilt) for data logging & storage
- 14 PWM channels (combined 3A)
- ~20 auxiliary outputs with SPI, I2C, analog, digital pins, etc.
- 6-16V power input, (reverse+over+under)-voltage, over-current protection
- Dimensions: 40mm width, 82mm height

### V2 [April 2024]

![V2](./assets/v2.png)

With learnings from V1, V2 was designed to be more cost-effective, less complex, and easier to manufacture. The BOM cost was around $60-80, and the board had 4 layers. With a trace width and minimum clearance of 0.2mm, QFN chips, and 0603 components, it was easier to manufacture and assemble. The board was manufactured and partially tested but not yet used in flight.

#### Key Features:
- Main Dual core ESP32-S3
- Secondary RP2040 as an IO extender
- 2.4GHz SX1280 radio
- Ublox-M10S GNSS
- BMI088 IMU (up to ± 24 g, ± 2000°/s)
- BMP390 barometer (up to 10KM), MMC5983MA magnetometer for heading
- 4 pyro channels (up to 16V, 4A) with continuity
- SD card and flash (ESP32-S3 inbuilt) for data logging & storage
- 14 PWM channels (combined 3A)
- 17 auxiliary outputs with SPI, I2C, analog, digital pins, etc.
- 6-16V power input, (reverse+over+under)-voltage, over-current protection
- Dimensions: 40mm width, 82mm height

### V1 [March 2024]

![V1](./assets/v1.png)

The first attempt at designing a flight computer. The design was powerful, using Teensy, but highly complex and less cost-effective. The BOM cost was around $120-150, and the board had 4 layers. With a trace width and minimum clearance of 0.127mm, BGA chips, and 0402 components, it was challenging to manufacture and assemble. This version was never manufactured or tested.

#### Key Features:
- Main Chip: NXP IMXRT106DVJ6B (Teensy 4.1)
- RP2040 as an IO extender
- 2.4GHz SX1280 radio
- Ublox-M10S GNSS
- BMI088 IMU (up to ± 24 g, ± 2000°/s)
- BMP390 barometer (up to 10KM), MMC5983MA magnetometer for heading
- 4 pyro channels (up to 16V, 4A) with continuity
- SD card and flash for data logging & storage
- 14 PWM channels (combined 3A)
- 30 auxiliary outputs with SPI, I2C, analog, digital pins, etc.
- 6-16V power input, (reverse+over+under)-voltage, over-current protection
- Dimensions: 50mm width, 100mm height
