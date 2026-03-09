## Objective

The goal of this project is to build a TinyML system capable of **recognizing motion patterns drawn with an Arduino board** using its built-in IMU sensor.

Instead of detecting generic vibrations, the system learns to recognize **specific motion shapes** performed by moving the Arduino in space.

In this implementation, two motion patterns are used:

- Drawing a **circle**
- Drawing a **square**

The model analyzes the IMU data (accelerometer and gyroscope) and predicts which motion pattern was performed.

The output of the system provides **a confidence percentage for each class**, for example:

Circle: 82%  
Square: 18%

This allows the system to determine which gesture was most likely performed.
## Example Output

During inference, the Arduino reads IMU data in real time and runs the trained TensorFlow Lite model.

Example serial output:

Circle: 0.87  
Square: 0.13

The class with the highest probability corresponds to the detected motion.
