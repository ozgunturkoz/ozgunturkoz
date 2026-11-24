" çizgisinden sonraki her şeyi yapıştır.
    3) Profil > Edit profile > Bio kısmına şunu yaz:
       Embedded Software Engineer · STM32 · FreeRTOS · C/C++ · Avionics · TEKNOFEST rocket flight computer
    4) "Pinned" alanına uçuş bilgisayarı, yer istasyonu (astra-arayuz) ve ADAS tezi depolarını sabitle.
  Köşeli parantezli [ ] yerleri, ilgili depolar hazır olunca dolduracağız.
-->
-----

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

### 🛰️ Rocket Flight Computer (firmware is team-owned and private; happy to walk through the architecture in an interview)
A mission-critical flight computer in C/C++ on STM32 and ESP32. It reads IMU and barometer data over SPI/I2C
and estimates altitude and velocity with a Kalman filter. It uses dual-sensor redundancy, and an FSM-based recovery
algorithm decides when to deploy the parachutes. The firmware is interrupt-driven and fault-tolerant.

### 📡 Rocket Ground Station 2026: [astra-ground-station](https://github.com/ozgunturkoz/astra-ground-station)
A C# telemetry station for the rocket and the payload. It parses binary frames with **CRC16-CCITT** and
checksum validation, and a sliding-buffer resync keeps it aligned on noisy RF links. The dashboard shows live
charts, satellite maps and 3D orientation, and the station forwards data to the referee ground station.
Earlier version: [astra-arayuz](https://github.com/ozgunturkoz/astra-arayuz).

### 🚗 ADAS Sensor Fusion (B.Sc. thesis)
Fuses monocular camera object tracking (OpenCV + YOLO) with raw telemetry through a Kalman filter
to estimate the distance to a target vehicle in time-critical validation scenarios.
