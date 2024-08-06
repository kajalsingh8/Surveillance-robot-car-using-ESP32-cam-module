# Surveillance-Robot-Car-using-ESP32-Cam - Eye rover 

This project utilizes the ESP32-CAM module to create a car that can be controlled via a web interface. The car is equipped with a camera to stream live video and capture images, and it has controls for movement and LED lights.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Hardware Required](#hardware-required)
- [Software Required](#software-required)
- [Setup and Configuration](#setup-and-configuration)
- [Important Libraries](#important-libraries)


## Introduction

The ESP Eye Rover Project is an IoT project that combines the power of the ESP32 microcontroller with a camera module to create a car that can be controlled remotely. The car can move forward, backward, left, and right, and it can also stream live video to a web interface.

## Features

- Live video streaming from the ESP32-CAM module.
- Capture still images.
- Control the car's movement (forward, backward, left, right).
- Turn on/off LED lights on the car.
- Simple web interface for controlling the car.

## Hardware Required

- ESP32-CAM module
- Motor driver module (L298N or similar)
- Chassis for the car
- Battery pack

## Software Required

- Arduino IDE
- ESP32 board package installed in Arduino IDE

## Setup and Configuration

1. *Install Arduino IDE*: Download and install the Arduino IDE from the [official website](https://www.arduino.cc/en/Main/Software).

2. *Install ESP32 Board Package*:
   - Open the Arduino IDE.
   - Go to File > Preferences.
   - In the "Additional Board Manager URLs" field, add the following URL:
     
     https://dl.espressif.com/dl/package_esp32_index.json
     
   - Go to Tools > Board > Board Manager.
   - Search for "ESP32" and install the latest version.

3. *Connect the Hardware*:
   - Connect the ESP32-CAM module to the motor driver and the DC motors.
   - Connect the LED lights to the appropriate GPIO pins on the ESP32-CAM module.
   - Power the setup using a suitable battery pack.

4. *Upload the Code*:
   - Open the provided ESP32CAM_Car.ino file in the Arduino IDE.
   - Make sure to select the correct board and port under Tools > Board and Tools > Port.
   - Upload the code to the ESP32-CAM module.

## Important Libraries

- *ESP32 Camera*: This library is used for interfacing with the camera module.
- *ESP HTTP Server*: This library is used to create a web server on the ESP32 for streaming video and handling controls.
- *Arduino*: Standard Arduino library for basic functionalities.

```cpp
#include "esp_http_server.h"
#include "esp_timer.h"
#include "esp_camera.h"
#include "img_converters.h"
#include "camera_index.h"
#include "Arduino.h"
