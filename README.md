# How to use Core Motion in iOS using Swift

Users generate motion events when they move, shake, or tilt the device. These motion events are detected by the device hardware, specifically, the accelerometer and the gyroscope. The Core Motion framework lets your application receive motion data from device hardware and process that data.

![alt tag](https://raw.github.com/maximbilan/iOS-CoreMotion-Example/master/images/1.png)

To get started import the Core Motion framework like this:

Now create an instance of CMMotionManager object. The app can use it to receive four types of motion: raw accelerometer data, raw gyroscope data, raw magnetometer data, and processed device-motion data (which includes accelerometer, rotation-rate, and attitude measurements).

For starting accelerometer updates you need to call the next method:

Finally, read the accelerometer data as often as you want.

You can change accelerometerUpdateInterval, the interval, in seconds, for providing accelerometer updates to the block handler.

The same story for Gyroscope, Magnetometer and Device motion.

The source code of example using Core Motion can found here.

Happy coding!
