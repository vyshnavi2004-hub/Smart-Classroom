# Smart Classroom Energy Monitoring and Automation System

## Overview

The Smart Classroom Energy Monitoring and Automation System is an AI-powered solution designed to reduce energy wastage in classrooms by automatically controlling electrical devices based on real-time occupancy detection.

The system uses a CCTV or webcam feed and a YOLOv8 object detection model to count the number of people present in a classroom. Based on occupancy levels, lights can be automatically adjusted to optimize energy consumption while maintaining a comfortable learning environment.

---

## Features

- Real-time classroom occupancy detection
- Person detection using YOLOv8
- Automatic light control based on occupancy
- Stable occupancy tracking to avoid frequent switching
- Energy-saving estimation
- Live monitoring dashboard on video feed
- Low-cost and scalable architecture

---

## Technology Stack

### Software
- Python
- OpenCV
- YOLOv8 (Ultralytics)
- NumPy

### Hardware (Prototype)
- Laptop/Desktop
- Webcam or CCTV Camera

### Future Hardware Deployment
- Raspberry Pi
- ESP32
- Relay Module
- Existing Classroom CCTV Infrastructure

---

## System Workflow

1. Capture live video stream from CCTV/Webcam.
2. Detect people using YOLOv8.
3. Count the number of occupants.
4. Apply occupancy-based control logic.
5. Determine lighting level:
   - OFF → No occupants
   - LOW → 1–5 occupants
   - MEDIUM → 6–20 occupants
   - FULL → More than 20 occupants
6. Display occupancy and light status.
7. Estimate energy savings.

---

## Occupancy-Based Light Control

| Occupancy Count | Light Status |
|---------------|-------------|
| 0 | OFF |
| 1 – 5 | LOW |
| 6 – 20 | MEDIUM |
| > 20 | FULL |

---

## Stability Mechanism

To prevent lights from switching frequently due to temporary detection fluctuations:

- A rolling history buffer stores recent occupancy counts.
- Average occupancy is calculated.
- Light status changes only after remaining stable for a predefined duration.

This improves reliability in real-world classroom environments.

---

## Project Structure
