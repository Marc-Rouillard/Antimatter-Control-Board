# Antimatter Control Board

This project is a custom control board for antweight combat robots and other small robots.

The key features of the PCB include:
* Integrated battery connector and power switch
* STM32C011 MCU
* nRF24L01+ 2.4 GHz transceiver
* 6-axis IMU
* 3-axis magnetometer
* 2x brushed motor drivers

It is designed to have several advantages over the simple PWM receivers that are common in small RC robots, including:
* simplified wiring by integrating all components in one board
* ability to track robot orientation using IMU and magnetometer
* custom control algorithms can be implemented on the microcontroller
* improved telemetry and logging to aid in development and diagnosing issues
