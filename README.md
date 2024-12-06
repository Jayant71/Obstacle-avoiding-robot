# Obstacle-Avoiding Robot

This project demonstrates the implementation of an obstacle-avoiding robot using an Arduino microcontroller. The robot uses ultrasonic and infrared sensors to detect obstacles and autonomously navigates around them. It incorporates servo motors for directional sensing and motor drivers for movement control.

## Features

- Autonomous navigation to avoid obstacles.
- Utilizes ultrasonic sensors for distance measurement.
- Infrared sensors for edge or obstacle detection.
- Smooth directional movement using BO motors and L298 motor driver.

## Components Used

- **Arduino**: Microcontroller for logic and processing.
- **Ultrasonic Sensor**: Distance measurement.
- **Infrared Sensors**: Detect edges or obstacles.
- **Servo Motor**: Controls directional sensing.
- **L298N Motor Driver**: Controls the BO motors.
- **BO Motors**: For movement.
- **Li-ion Batteries**: Power supply.

## Circuit Connections

1. **Ultrasonic Sensor**:
   - Trigger Pin → A1
   - Echo Pin → A2
2. **IR Sensors**:
   - Left IR Sensor → Pin 2
   - Right IR Sensor → Pin 3
3. **Motors**:
   - Left Motor Forward → Pin 7
   - Left Motor Backward → Pin 6
   - Right Motor Forward → Pin 4
   - Right Motor Backward → Pin 5
4. **Servo Motor**:
   - Signal Pin → Pin 10

## How It Works

- The ultrasonic sensor measures distance to detect obstacles in front of the robot.
- Infrared sensors detect obstacles on the left and right sides or edges.
- Based on sensor inputs:
  - The robot stops and assesses the surroundings.
  - Turns left or right based on the obstacle-free direction.
  - Moves forward when no obstacles are detected.

## Code Explanation

The Arduino code includes:

- **Sensor Reading**: Reads distance from the ultrasonic sensor and input from the IR sensors.
- **Decision Making**: Determines the direction based on sensor readings.
- **Movement Functions**:
  - `moveForward()`: Moves the robot forward.
  - `moveBackward()`: Moves the robot backward.
  - `turnLeft()` / `turnRight()`: Turns the robot to avoid obstacles.
  - `moveStop()`: Stops the robot.
- **Servo Control**: Moves the servo to scan left or right for obstacles.

## Installation

1. Upload the provided code to the Arduino using the Arduino IDE.
2. Assemble the robot with the listed components.
3. Power the robot using Li-ion batteries.

## Usage

1. Place the robot on a flat surface.
2. Power it on.
3. The robot will autonomously navigate, avoiding obstacles and finding a clear path.

## Future Improvements

- Add Bluetooth or Wi-Fi control for manual override.
- Integrate a camera for advanced object recognition.
- Use more efficient motor drivers or advanced microcontrollers.

## License

This project is licensed under the MIT License.
