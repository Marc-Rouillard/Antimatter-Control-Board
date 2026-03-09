# Antimatter Control Board

This project is a custom control board for antweight combat robots and other small robots.

The key features of the PCB include:
* Integrated battery connector and power switch
* MCU with integrated wireless capabilities
* LSM6DSO32 6-axis IMU (accelerometer and gyro)
* IIS2MDC 3-axis magnetometer
* 2x brushed motor drivers

It is designed to have several advantages over the simple PWM receivers that are common in small RC robots, including:
* simplified wiring by integrating all components in one board
* custom control algorithms can be implemented on the microcontroller
* ability to track robot orientation using IMU and magnetometer
* improved telemetry and logging to aid in development and diagnosing issues
* allows custom data to be sent to controller, such as estimated orientation/location from camera setup outside arena

## Component selection rationale
* LSM6DSO32 - cheap, available from Mouser, lower noise and wider acceleration range than similar alternatives
* IIS2MDC - low cost, available from Mouser
