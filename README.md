# Introduction to WIMP

WIMP stands for Where Is My Professor. WIMP is an IoT-based system that enables students to track the availability of their professors in real-time based on the data collected using IoT devices. This system collects data from various IoT devices, such as sensors, cameras, buddy robot, and smartwatches, to learn where professors are located inside the university building and other pertinent information. The system can offer an automated response on the professor's availability by analyzing the collected data.

WIMP project is composed of multiple components, each designed to perform specific functions. To maintain modularity and streamline development, every component is housed in its own repository. Below, we provide a summary of all the components along with the URLs to their respective repositories, ensuring easy access and management for development and collaboration.

# Devices (WIMP-Devices)

WIMP interacts with various devices. Currently, we have two devices: Buddy the robot and Fitbit Smart watch.

## Buddy the robot

To access the code of buddy robot, visit our repository https://github.com/baptiste2k8/buddytherobot/tree/master

## Fitbit Watch
Fitbit devices collect health data like heart rate and step count. This data is sent to the Fitbit app on your phone using Bluetooth. In our setup, we also use a small program called the "companion" app that runs alongside the Fitbit app. The companion app's job is to take the data from Fitbit and send it to another system called WIMP.

To send the data from the companion app to WIMP, we use secure methods like HTTPS (which is what makes sure your data is safely sent over the internet). Sometimes, we use a different method, which involves running a small local server directly on the Android phone using NanoHTTPD. This is because Fitbit doesn’t have a built-in way to communicate directly with Android apps. So, NanoHTTPD helps the companion app talk to other Android apps securely and efficiently. Below figure shows the process of getting data from Fitbit watches.

<img src="rq2Approach.svg>

To access the code of the fitbit watches, visit the following repositories:

### Fitbit App 

This repository consists of the code for both fitbit app and companion part and the code is available at https://github.com/baptiste2k8/fitbitwatchapp/tree/master

### Mobile App

This repository consists of the code for android app to receive the data from companion and send the data to WIMP-app. You can access this repository at https://github.com/baptiste2k8/fitbitwatchserverapp/tree/master 

# Application Layer (WIMP-App)

  The WIMP app is a system developed using a combination of technologies, including Node.js for the server-side logic, MariaDB for database management, and WebSocket for real-time communication. The primary function of the WIMP app is to receive data from various Internet of Things (IoT) devices, such as sensors and smart devices. This data might include information like temperature readings, motion detection, or location tracking. Once the data is received, the app processes it to determine specific actions that need to be performed by other connected devices. Additionally, the WIMP app can be used in educational settings to inform students about the availability of their professors based on the geolocation data received from fitbit watch worn by the professor. By integrating with scheduling systems or location-based devices, the app can notify students when their professors are in their offices or available for meetings. This integration of IoT data processing and real-time communication makes the WIMP app a versatile and useful tool in both smart environments and educational contexts.

  To access the repository of the app, visit our repository https://github.com/baptiste2k8/wimp-app/tree/master 

# Testing Tool (TestRunner)

This repository contains code to prepare a payload, validate it, send it to the System Under Test (SUT) for execution, and request the response from the execution. Source code and documentation are available at https://github.com/baptiste2k8/TestRunner


