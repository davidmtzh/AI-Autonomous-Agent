# 🤖 Arduino AI Roomba – Autonomous Agent

An Arduino-based autonomous mobile robot that navigates its environment using calibrated sensor input, motor control, and AI-inspired decision logic.

---

## 📌 Project Overview

This project implements an autonomous Roomba-style robot capable of interpreting real-world sensor data, making decisions in real time, and executing motion plans with calibrated motor control.  
The system emphasizes reliability, repeatability, and explainable autonomous behavior.

---

## 🧠 Core Concepts & Architecture

### 1. Sensor Evaluation & Calibration
- Evaluated raw sensor readings (distance, proximity, or line sensors)
- Calibrated thresholds to reduce noise and false positives
- Tuned sensor placement and orientation for optimal coverage
- Converted analog values into stable environmental states

---

### 2. Motor Control & Hardware Calibration
- Calibrated motor rotation speeds to ensure straight-line motion
- Corrected asymmetrical wheel behavior
- Tuned PWM values for consistent acceleration and turning
- Validated encoder feedback when available

---

### 3. Finite State Automaton (FSA) Decision Maker
The robot’s behavior is governed by a Finite State Automaton (FSA), enabling clean separation between perception, decision-making, and actuation.

Example states:
- `IDLE`
- `SEARCHING`
- `MOVING`
- `AVOIDING_OBSTACLE`
- `ROTATING`
- `RECOVERY`

State transitions are triggered by sensor events, allowing dynamic responses instead of scripted paths.

---

### 4. Search & Navigation Logic
- Implemented search-style behavior for environment exploration
- Combined reactive and state-based logic
- Integrated sensor feedback into navigation decisions
- Balanced exploration and obstacle avoidance

---

## 🧩 System Flow
Sensor Input
↓
Signal Filtering & Thresholding
↓
State Evaluation (FSA)
↓
Decision Logic
↓
Motor Commands
↓
Physical Movement
↺ (Feedback Loop)


---

## 🛠️ Technologies Used
- Arduino (C/C++)
- Embedded motor drivers
- Distance / proximity sensors
- PWM motor control
- Finite State Automaton (FSA)
- Search-based decision logic

---

## 🧪 Testing & Validation
- Incremental hardware testing (sensor → motor → integration)
- Real-world testing with obstacles and uneven surfaces
- Repeated calibration cycles
- Debugging via serial monitoring

---

## 🎯 Key Takeaways
- Practical experience with embedded robotics
- Real-world sensor noise handling and calibration
- AI-inspired decision-making on constrained hardware
- Modular, debuggable system design

---

## 🚀 Future Improvements
- Sensor fusion
- PID-based motion control
- Environment mapping
- Advanced path-planning algorithms

---

## 📂 Repository Structure

```text
/
├── FinalProject-Version1.0.ino   # Main Arduino entry point and system integration
├── PDController.cpp              # Proportional-Derivative motor control logic
├── PDController.h
├── PIDController.cpp             # PID controller for precise motion tuning
├── PIDController.h
├── odometry.cpp                  # Wheel encoder processing and position tracking
├── odometry.h
├── sonar.cpp                     # Ultrasonic sensor handling and distance estimation
├── sonar.h
├── printOLED.cpp                 # OLED output for debugging and state feedback
└── printOLED.h



---

## 📎 Why This Project Matters

This project demonstrates end-to-end autonomous system design, from low-level hardware calibration to high-level decision-making, reflecting real-world robotics engineering practices.

