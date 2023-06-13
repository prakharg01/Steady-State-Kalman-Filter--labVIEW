# Steady State Kalman Filter - LabVIEW

This repository contains an implementation of a Steady State Kalman Filter for orientation estimation using LabVIEW and STM32. The Kalman filter is utilized to accurately estimate the final state based on inaccurate and noisy measurement data from the MPU9250 IMU (Inertial Measurement Unit) - a 9-axis sensor that includes an accelerometer, gyroscope, and magnetometer. The goal of this project is to estimate the pitch angle at each timestep.

## Overview
Various MEMS devices available in the market provide built-in accelerometers, gyroscopes, and magnetometers for measuring orientation in space. However, the raw measurements from these sensors are often unstable and cannot be effectively used as is. The Kalman filter serves as an observer that can accurately estimate the final state based on noisy and inaccurate measurement data.

In this project, the Steady State Kalman Filter is implemented using LabVIEW. The MPU9250 IMU is used to collect the sensor data, which is then transmitted to LabVIEW through the STM32 microcontroller via the SPI interface. LabVIEW, in turn, utilizes a VI (Virtual Instrument) to visualize both the raw data and the estimated data from the Kalman filter.

## Demonstration
A demonstration of the Steady State Kalman Filter implementation can be found on YouTube at the following link: [Steady State Kalman Filter Demo](https://www.youtube.com/watch?v=gj9Wb53A2nI).

## Usage
The expected input to the VISA (Virtual Instrument Software Architecture) driver is a comma-separated value sent through the serial port. The format of the input should be as follows: `ax,ay,az,gx,gy,gz`, where:
- `ax`: Accelerometer X-axis measurement
- `ay`: Accelerometer Y-axis measurement
- `az`: Accelerometer Z-axis measurement
- `gx`: Gyroscope X-axis measurement
- `gy`: Gyroscope Y-axis measurement
- `gz`: Gyroscope Z-axis measurement

Please make sure to configure the serial port settings and connections appropriately for communication between the STM32 and LabVIEW.
# Note: This repo doesnt contain the source code to read imu values and send it over to the serial port, it builds on top of this functionality

## Repository Contents
- `report/`: This contains the implementation details and the maths involved
- `.vi_files`: Includes the labview files

## License
The code in this repository is licensed under the [MIT License](LICENSE).

## Acknowledgements
The Steady State Kalman Filter implementation for orientation estimation using LabVIEW and STM32 was developed by [Your Name]. If you find this project useful or have any questions, feel free to reach out.

[Prakhar Goel]: [https://www.linkedin.com/in/prakhar-goel-4616501a5/]
