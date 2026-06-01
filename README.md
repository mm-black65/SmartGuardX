# SmartGuardX – IoT Security & Environmental Monitoring Rover

## Overview

SmartGuardX is an ESP32-powered IoT rover designed for remote surveillance, environmental monitoring, and autonomous obstacle detection. The rover can be controlled through a web browser over Wi-Fi while simultaneously collecting and publishing sensor data to a cloud dashboard using MQTT.

The system integrates multiple sensors, real-time monitoring, cloud connectivity, and autonomous safety features, making it a practical project for learning robotics, embedded systems, IoT, and networking.

---

## Features

### Remote Control

* Wi-Fi based control
* Web browser interface
* No mobile application required
* Real-time movement commands using WebSockets

### Environmental Monitoring

* Temperature Monitoring (DHT22)
* Humidity Monitoring (DHT22)
* Light Intensity Detection (LDR)
* Rain Detection Sensor

### Autonomous Safety

* HC-SR04 Ultrasonic Obstacle Detection
* Servo-Based Environmental Scanning
* Automatic Stop when obstacle is detected
* Semi-Autonomous Patrol Mode

### Security Features

* MPU6050 Tilt Detection
* Impact Detection
* Anti-Tampering Alerts
* Fall Detection

### Notifications

* Active Buzzer Alerts
* MQTT-Based Notifications
* Cloud Dashboard Monitoring

### Cloud Connectivity

* MQTT Communication
* Node-RED / ThingsBoard Integration
* Real-Time Sensor Visualization
* Historical Data Logging

---

## Hardware Components

### Controller

* ESP32 Development Board

### Mobility

* 4WD Robot Chassis
* 4x DC Geared Motors
* L298N Motor Driver

### Sensors

* DHT22 Temperature & Humidity Sensor
* HC-SR04 Ultrasonic Sensor
* SG90 Servo Motor
* LDR Light Sensor
* Rain Sensor Module
* MPU6050 Accelerometer & Gyroscope

### Output Devices

* Active Buzzer

### Power System

* 2 × 18650 Lithium-Ion Batteries
* Buck Converter (5V)

---

## System Architecture

Sensors collect environmental and motion data which is processed by the ESP32.

The ESP32:

* Controls motors
* Reads sensors
* Performs obstacle detection
* Publishes MQTT data
* Hosts a web control interface

Sensor data is sent to a cloud MQTT broker and visualized through Node-RED or ThingsBoard dashboards.

---

## Pin Configuration

| Component      | ESP32 Pin |
| -------------- | --------- |
| L298N IN1      | GPIO 26   |
| L298N IN2      | GPIO 27   |
| L298N IN3      | GPIO 14   |
| L298N IN4      | GPIO 12   |
| L298N ENA      | GPIO 25   |
| L298N ENB      | GPIO 33   |
| HC-SR04 TRIG   | GPIO 5    |
| HC-SR04 ECHO   | GPIO 18   |
| Servo Signal   | GPIO 13   |
| DHT22 Data     | GPIO 4    |
| Rain Sensor AO | GPIO 34   |
| LDR AO         | GPIO 35   |
| MPU6050 SDA    | GPIO 21   |
| MPU6050 SCL    | GPIO 22   |
| Active Buzzer  | GPIO 23   |

---

## Operating Modes

### Manual Mode

The rover is controlled through a web interface hosted on the ESP32.

### Patrol Mode

The rover moves autonomously while continuously monitoring:

* Obstacles
* Temperature
* Humidity
* Rain
* Light Levels
* Motion/Tilt Events

---

## Future Improvements

* GPS Tracking
* ESP-NOW Communication
* AI-Based Anomaly Detection
* Camera Integration
* ROS 2 Integration
* Mobile Application
* Multi-Rover Coordination

---

## Learning Outcomes

This project demonstrates:

* Embedded C++
* ESP32 Development
* PWM Motor Control
* Sensor Integration
* FreeRTOS Multitasking
* MQTT Communication
* WebSocket Communication
* IoT Dashboard Development
* Robotics Navigation
* Cloud Connectivity
* Real-Time Monitoring

---

## Project Status

Current Version: SmartGuardX V1

An IoT-enabled security and environmental monitoring rover capable of remote operation, autonomous obstacle avoidance, cloud-based monitoring, and motion-based security alerts.
