# Hi, I'm Özgün 👋

**Embedded Software Engineer** based in Istanbul. I build deterministic, low-latency firmware for avionics:
flight computers, sensor fusion and real-time telemetry on **STM32** and **ESP32**.

- 🚀 Software Team Lead at **Astra Rocket Team**. I developed flight computers that flew at **TEKNOFEST** three seasons in a row:
  - **5th** place and **Best Design Award** in 2024
  - **7th** place in 2025
  - **9th** place in 2026
- 🎓 B.Sc. Computer Engineering, Istanbul Kültür University (2026)
- 🔎 **Open to Embedded / Firmware Software Engineer roles** (Istanbul or remote)
- 📫 ozgunturkoz3@gmail.com · [LinkedIn](https://linkedin.com/in/ozgunturkozz)

## What I work with

| Area | Tools |
|---|---|
| Languages | C, C++, Python, C# (.NET) |
| MCUs & RTOS | STM32 (HAL/LL), ESP32 (ESP-IDF), FreeRTOS, bare-metal |
| Interfaces | SPI, I2C, UART, UDP, ESP-NOW |
| Sensors | IMU (BNO055, MPU6050), barometer (BMP280/BMP390), GNSS |
| Algorithms | Kalman filter, sensor fusion, finite-state machines, OpenCV / YOLO |
| Debug & test | ST-Link, JTAG/SWD, logic analyzer, Wireshark, Git |

## Featured projects

### 🛰️ Rocket Flight Computer: [architecture overview](https://github.com/ozgunturkoz/rocket-flight-computer)
STM32H7 + FreeRTOS avionics with 8 tasks and a strict mutex-ordering contract. A triple-barometer + IMU
**median → Kalman** fusion chain votes out faulty sensors, and an 8-state recovery FSM runs two-stage parachute
deployment over redundant pyro channels. It also has an independent watchdog, microSD black-box logging and
hardware-in-the-loop competition tests. *(Firmware is team-owned and private; the README documents the design.)*

### 📡 Rocket Ground Station 2026: [astra-ground-station](https://github.com/ozgunturkoz/astra-ground-station)
A C# telemetry station for the rocket and the payload. It parses binary frames with **CRC16-CCITT** and
checksum validation, and a sliding-buffer resync keeps it aligned on noisy RF links. The dashboard shows live
charts, satellite maps and 3D orientation, and the station forwards data to the referee ground station.
Earlier version: [astra-arayuz](https://github.com/ozgunturkoz/astra-arayuz).

### 🚗 ADAS Collision Warning (B.Sc. thesis): [adas-collision-warning](https://github.com/ozgunturkoz/adas-collision-warning)
Combines YOLOv8 + ByteTrack camera tracking with a TF02-Pro LiDAR (ESP32 nodes over ESP-NOW) and GPS speed.
Median + Kalman fusion estimates distance and time-to-collision, and the system raises staged warnings.
**4.9 % mean distance error, 69.2 % better than camera-only, 20–30 FPS.**
