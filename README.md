# GY_91
![unknown](https://user-images.githubusercontent.com/30243097/28285524-153628ee-6b03-11e7-9925-ec0eec3e6dc1.jpeg)

The GY-91 is a 10 degrees of freedom module.It contains the MPU9250 which is a 9 axis Gyro, Accelerometer and Compass; the GY-91 also contains a BMP280 which is a barometric pressure sensor.

I owe credit to Kris Winer the original author of this code (April 1, 2014) and Brent Wilkins who modified this code in (July 19, 2016). I too have made my own modifications to this code to suite my needs. 

The GY_91_Alternate_Calibration.ino is my attempt at an alternative and quicker solution to calibration. In STAGE 1: you must hold the IMU level during the calibration setup. Initial value spikes that tend to show up within the first 30 pitch and roll value-read's are removed from the calibration. The code removes the first 60 values just to be sure. In STAGE 2: pitch and roll values are summed up for 50 values. In STAGE 3: pitch_sum and roll_sum are averaged (divided by 50) to recieve the adjustment values pitch_adjustment and roll_adjustment. This techniques brings the GY-91 to a level value (0.0 pitch, 0.0 roll) whenever it is in this position. Therefore if you were to hold the GY-91 at a 45 degree pitch angle and upload the code then this would be your assumed 0.0 pitch axis, 0.0 roll axis.

The GY_91_Example_Code.ino is the code that I use in my YouTube video: https://www.youtube.com/watch?v=N1Mva_A5D7s where I review this small IMU.


