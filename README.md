# IoTBasedCarControl
A Wi-Fi-enabled remote control car built with NodeMCU and BLynk IoT, enabling wireless smartphone-based movement control

##  Project Objectives

- To develop a Wi-Fi-controlled car using NodeMCU and DC motors
- To implement real-time motion control via a smartphone interface
- To integrate cloud-based control through the Blynk platform
- To provide adjustable speed and directional control

---

##  Key Features

-  Smartphone-based wireless control (Forward, Backward, Left, Right, Stop)
-  Wi-Fi connectivity using NodeMCU ESP8266
-  Speed control using a slider widget
-  Simple and modular code written in Arduino (C++)
-  Suitable for academic demonstrations, exhibitions, and prototyping

---

##  Hardware Requirements

| Component                | Quantity |
|--------------------------|----------|
| NodeMCU ESP8266          | 1        |
| L298N Motor Driver Module| 1        |
| DC Motors                | 2        |
| Motor Chassis            | 1 set    |
| Li-ion Battery Pack      | 1        |
| Jumper Wires             | As needed|
| Smartphone with Blynk App| 1        |

---

##  Circuit Diagram Overview

| NodeMCU Pin | L298N Motor Driver |
|-------------|---------------------|
| D0          | ENA                 |
| D1          | IN1                 |
| D2          | IN2                 |
| D3          | IN3                 |
| D4          | IN4                 |
| D5          | ENB                 |

Ensure common GND between NodeMCU, motor driver, and power supply.

---

##  Blynk App Configuration (Legacy)

1. Install **Blynk Legacy** app from Play Store / App Store.
2. Create a new project:
   - Device: **ESP8266**
   - Connection type: **Wi-Fi**
3. Note the **Auth Token** sent via email.
4. Add the following widgets:
   - **Button (V0)** – Forward
   - **Button (V1)** – Backward
   - **Button (V2)** – Left
   - **Button (V3)** – Right
   - **Slider (V4)** – Speed control (range 0–1023)
5. Save and run the project after uploading the code.

---

##  Arduino IDE Setup

1. Install the following libraries from Library Manager:
   - `Blynk`
   - `ESP8266WiFi`
2. Replace placeholders in the code:
   ```cpp
   char auth[] = "YourAuthToken";
   char ssid[] = "YourWiFiSSID";
   char pass[] = "YourWiFiPassword";

##  Future Upgrades

This project provides a strong foundation for IoT-based robotics and can be further enhanced with the following features:

- **Obstacle Detection and Avoidance**  
  Integrate ultrasonic sensors to detect objects and automatically stop or reroute the car.

- **Live GPS Tracking**  
  Add a GPS module to track the car’s real-time location on a map interface.

- **Voice-Controlled Operation**  
  Enable voice commands using Google Assistant, Alexa, or offline voice modules.

