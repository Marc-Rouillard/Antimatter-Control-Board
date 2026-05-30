# Antimatter Control Board

The Antimatter Control Board is a custom control board for 150 g antweight combat robots and other small robots, currently in development.

The key features of the PCB include:
* nRF52833 MCU with integrated radio
* LSM6DSO32TR 6-axis IMU (accelerometer and gyro)
* IIS2MDC 3-axis magnetometer
* 2x brushed motor drivers
* Integrated battery connector and screw power switch

It is designed to have several advantages over the simple PWM receivers that are common in small RC robots, including:
* simplified wiring by integrating all components in one board
* custom control algorithms can be implemented on the microcontroller
* ability to track robot orientation and correct drive drift or use different drive schemes
* improved telemetry and logging to aid in development and diagnosing issues
* allows custom data to be sent to the device, such as estimated pose from camera setup outside arena

Communication uses the Nordic Enhanced Shockburst protocol so a custom controller/link is required to interface with the device, although it could also be programmed to use BLE to connect directly to a phone or laptop.

## Component selection rationale
* nRF52833 (QDAA-B) - relatively low cost, available from Mouser, integrated radio transceiver supporting Nordic Enhanced Shockburst protocol (same as the popular nRF24L01+ - lower latency and better data rate than alternatives like BLE and even ESP-NOW), small package (5x5 mm), 512 kB integrated flash memory, enough GPIO pins, floating-point unit for controls and sensor-fusion algorithms. The nRF52833 also supports BLE-based OTA updates, which may be implemented in the future
* LSM6DSO32TR - cheap, available from Mouser, lower noise and wider acceleration range than similar alternatives
* IIS2MDC - low cost, good performance, available from Mouser
* DRV883
