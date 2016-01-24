# How to use Core Motion in iOS using Swift

Users generate motion events when they move, shake, or tilt the device. These motion events are detected by the device hardware, specifically, the accelerometer and the gyroscope. The <i><a href="https://developer.apple.com/library/ios/documentation/CoreMotion/Reference/CoreMotion_Reference/">Core Motion</a></i> framework lets your application receive motion data from device hardware and process that data.

![alt tag](https://raw.github.com/maximbilan/iOS-CoreMotion-Example/master/images/1.png)

To get started import the <i><a href="https://developer.apple.com/library/ios/documentation/CoreMotion/Reference/CoreMotion_Reference/">Core Motion</a></i> framework like this:

<pre>
import CoreMotion
</pre>

Now create an instance of <i><a href="https://developer.apple.com/library/ios/documentation/CoreMotion/Reference/CMMotionManager_Class/">CMMotionManager</a></i> object. The app can use it to receive four types of motion: raw accelerometer data, raw gyroscope data, raw magnetometer data, and processed device-motion data (which includes accelerometer, rotation-rate, and attitude measurements).

<pre>
let motionManager = CMMotionManager()
</pre>

For starting accelerometer updates you need to call the next method:

<pre>
func startAccelerometerUpdates()
</pre>

Finally, read the accelerometer data as often as you want.

<pre>
if let accelerometerData = motionManager.accelerometerData {
}
</pre>

You can change accelerometerUpdateInterval, the interval, in seconds, for providing accelerometer updates to the block handler.

The same story for Gyroscope, Magnetometer and Device motion.

<pre>
func startGyroUpdates()
func startMagnetometerUpdates()
func startDeviceMotionUpdates()
</pre>

The source code of example using <i><a href="https://developer.apple.com/library/ios/documentation/CoreMotion/Reference/CoreMotion_Reference/">Core Motion</a></i> can found here.

Happy coding!
