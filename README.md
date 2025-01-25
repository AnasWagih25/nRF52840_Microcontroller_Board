# nRF52840 Board Schematic

This repository contains the schematic for a custom board based on the Nordic Semiconductor nRF52840 microcontroller. The design integrates various components to support USB connectivity, power management, debugging, and GPIO functionality.

## Features

1. **Microcontroller**:
   - **Chip**: nRF52840 (U2)
   - Supports BLE, USB, and a wide range of GPIO configurations.

2. **Power Management**:
   - **Regulator**: TPS7333 (U1)
   - Converts USB voltage (5V) to 3.3V for powering the nRF52840 and peripherals.
   - Includes decoupling capacitors for stable operation.

3. **USB Connectivity**:
   - USB Micro-B connector for power and data.
   - ESD protection via TVS diode (D1).
   - USB D+ and D- routed to the nRF52840.

4. **Debugging**:
   - SWD interface (J2) for programming and debugging the nRF52840.
   - Reset button for development convenience.

5. **I2C Interface**:
   - Pull-up resistors (R4, R5) on the SDA and SCL lines.
   - Includes a level-shifting IC (U3) for compatibility with external I2C devices.

6. **Indicators**:
   - Two LEDs (D2, D3) for power and status indication.
   - Resistors (R1, R2) to limit current to the LEDs.

## Usage

1. **Power Supply**: Connect a 5V power source via USB or an external regulated 3.3V supply to the board.
2. **Programming**: Use the SWD interface with a compatible programmer for flashing firmware.
3. **Peripheral Connections**: Utilize the GPIOs or I2C interface for external sensors and modules.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

