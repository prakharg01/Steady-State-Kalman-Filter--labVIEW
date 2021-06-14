# Steady-State-Kalman-Filter--labVIEW
Various MEMS devices are available in market that have built in accelerometers, gyroscopes  and magnetometers for measuring the orientation in space, but the measurements are not  stable and can’t be used raw effectively. Kalman filter does a great job in playing the role of  an observer that can accurately estimate the final state based on inaccurate and noisy  measurement data. Here I propose to study one such Kalman filter - Steady state Kalman  filter, that is used with the MPU9250 IMU – 9 axis sensor that has a built-in accelerometer,  gyroscope and a magnetometer. Pitch angle is estimated at each timestep. STM32 is used to  collect the IMU data through SPI interface, this data is sent serially to LabVIEW, where a VI  is used to visualize the raw data and the estimated Kalman filter data.

Here is the demonstration 
https://www.youtube.com/watch?v=gj9Wb53A2nI


Expected input to the VISA driver is a comma sepereted value sent through serial port 
Example : ax,ay,az,gx,gy,gz
