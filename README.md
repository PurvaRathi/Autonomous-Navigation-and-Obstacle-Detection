# 🤖 COST EFFICIENT AUTONOMOUS DISASTER-RESPONSE ROVER

This repository contains the Arduino codes for a 6-wheel autonomous rover capable of autonomous navigation and dynamic obstacle avoidance using ultrasonic sensors and an L298N motor driver.  
The system is designed to operate without human control and make real-time movement decisions based on detected obstacles.

## 🧭 Overview
This repository demonstrates how an Arduino Uno can control a six-wheel rover to:
- Move autonomously using motor control logic.
- Detect and avoid obstacles dynamically using ultrasonic distance measurement.
- Execute smooth turns and reversals when an obstacle is detected ahead.

---

## ⚙️ System Architecture

| Component | Function |
|------------|-----------|
| **Arduino Uno** | Central controller for navigation and motor control |
| **L298N Motor Driver** | Controls the left and right side motors |
| **6 BO Motors (300 RPM)** | Provides locomotion (3 motors per side connected in parallel) |
| **HC-SR04 Ultrasonic Sensor** | Detects obstacles and measures distance |
| **Li-ion/LiPo Battery (7.4V–12V)** | Powers motors and L298N module |

## 🧠 Working Logic

1. The ultrasonic sensor continuously measures distance ahead.  
2. When no obstacle is detected within a safe range, the rover moves forward.  
3. If an obstacle is detected:
   - The rover stops.
   - Moves backward for a short distance.
   - Turns left or right to avoid the obstacle.
4. The rover resumes forward motion once the path is clear.
