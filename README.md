# Mini Autonomous Car

## Video Demonstration

For a visual demonstration of this project, please refer to the video linked below:

[Project Video Demonstration](https://youtu.be/VjgShMirpmE)

[![Project Video Demonstration](https://img.youtube.com/vi/VjgShMirpmE/0.jpg)](https://www.youtube.com/watch?v=rVjgShMirpmE)


## Overview

This project involves the development of a Mini Autonomous Car equipped with two primary features: line following and traffic sign detection with response capabilities. The car is designed to autonomously navigate by following a designated colored line and responding to specific traffic signs using a combination of hardware and software components.

## Specifications

- **Processor:** Jetson Nano (4GB RAM, 64GB memory)
- **Camera:** Astra Pro Camera
- **Sensors:** Lidar
- **Motors:** 333 rpm motors
- **Wheels:** Mecanum wheels for omnidirectional movement

## System Architecture

### Hardware Components

- **Astra Pro Camera:** Captures high-resolution images (720p) for line and traffic sign detection.
- **Motors and Motor Driver:** Controls the movement of the car.
- **Mecanum Wheels:** Allows for smooth and flexible movement in all directions.
- **Batteries:** Powers the car and its components.

### Software Components

- **Operating System:** Linux
- **Framework:** ROS2 (Robot Operating System)
- **Programming Language:** Python
- **Libraries:** OpenCV for image processing
- **Machine Learning Model:** YOLO v5 for traffic sign detection

### Inputs and Outputs

- **Input:** Camera image (with blue line and traffic signs)
- **Output:** Motor velocities for line following and traffic sign response

## System Features

1. **Line Following:**
   - Detection of a blue-colored line using OpenCV.
   - PID controller for smooth line tracking.

2. **Traffic Sign Detection and Response:**
   - Custom trained YOLO v5 model for detecting four different traffic signs.
   - The car can respond to two specific signs: "Go Straight" and "Stop."
   - Detection accuracy ranges from 80% to 95%.
   - Signs are detected at a distance of 15-20 inches.
   - One sign detection in the frame at a time.
   - Image capture resolution is 720p.

3. **Communication and Control:**
   - Uses ROS2 packages for communication between different components.
   - Runs on hotspot mode for wireless communication.

## Project Scope

1. **Line Following:**
   - Can follow any colored line with proper calibration.

2. **Traffic Sign Detection:**
   - Detects four different traffic signs.
   - Responds to "Go Straight" and "Stop" signs.

3. **Performance:**
   - Sign detection has a lag of 15-20 seconds due to processing overhead.
   - Inference is performed on the Jetson Nano; training should be conducted separately.

4. **Limitations:**
   - No obstacle detection implemented.
   - Detection and response have potential challenges such as CPU overloading, battery life, and calibration issues.

## Potential Challenges

- **Lag in Real-Time Detection and Response:** Processing time can cause delays.
- **CPU Overloading:** High processing requirements may overload the CPU.
- **Velocity Value Overlapping:** Ensuring accurate velocity control.
- **Battery Life:** Managing power consumption for prolonged operation.
- **Calibration of Color:** Requires specific environmental conditions for accurate color detection.
- **Camera Angle:** Proper positioning is crucial for accurate image capture.

## Getting Started

### Prerequisites

- **Hardware:** Jetson Nano, Astra Pro Camera, Lidar, motors, motor driver, Mecanum wheels, batteries.
- **Software:** ROS2, Python, OpenCV, YOLO v5

### Running the Project

1. **Start ROS2:**
   - Initialize ROS2 and set up the necessary nodes for communication.

2. **Launch Line Following and Sign Detection:**
   - Run the provided launch files to start the line following and traffic sign detection nodes.

3. **Operate the Car:**
   - Place the car on a track with a blue line and the predefined traffic signs.
   - Monitor the car's response to the line and traffic signs.

## Conclusion

The Mini Autonomous Car project demonstrates a practical implementation of basic autonomous vehicle features using affordable and accessible hardware and software. While the system faces challenges such as processing lag and calibration requirements, it provides a foundation for further development and enhancement of autonomous navigation capabilities.

## Presentation

![Presentation Preview](Presentation.pdf)
