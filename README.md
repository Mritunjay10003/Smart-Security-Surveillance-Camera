# Smart Surveillance and Security Cam

A low-cost, IoT-based smart surveillance solution developed using ESP32-CAM and Telegram Bot API for real-time intrusion alerts and remote monitoring. This project was built to enhance home security through automation, cost-effectiveness, and ease of deployment.

---

## 📌 Introduction

Modern lifestyles and rising urbanization demand enhanced safety systems, especially for unattended homes. Conventional CCTV systems, though efficient, are often costly and require human intervention for monitoring. Our solution leverages the ESP32-CAM microcontroller, which interfaces with a PIR sensor and transmits intruder images directly to the user via Telegram, making it cost-effective and remotely operable.

This system ensures real-time surveillance and allows homeowners to monitor their premises from any location through smartphones or other internet-enabled devices.

---

## 🧩 System Design

The system architecture is designed with two core modules: hardware and software.

### 🔧 Hardware Components
- **ESP32-CAM AI Thinker Module**: Acts as the microcontroller and camera unit.
- **PIR Motion Sensor (AM312)**: Detects motion in the surrounding environment.
- **BME280 Sensor**: Optional; captures temperature, humidity, and pressure.
- **FTDI to TTL Converter**: Required to program the ESP32-CAM as it lacks a built-in USB interface.

### 💻 Software Tools
- **Arduino IDE**: For code development and uploading to ESP32-CAM.
- **Telegram App + Bot API**: Sends real-time alerts and images to the user.
- **MQTT (optional)**: Can be used for advanced control via cloud protocol.

---

## 🛠️ Implementations

### 🔌 Hardware Implementation
- The ESP32-CAM is interfaced with the PIR sensor on GPIO 13.
- BME280 Sensor uses I2C communication via GPIO 14 (SDA) and GPIO 15 (SCL).
- A PCB shield was designed for compact integration and ease of mounting.

### 💾 Software Implementation
- Telegram bot is created using BotFather and configured with a unique token and user ID.
- The bot listens for commands such as `/start`, `/photo`, and `/flash`, and returns captured images or toggles LED.
- Motion detection triggers image capture and instant upload to the Telegram bot, notifying the user.

Example features:
- Image capture via `/photo` command
- Motion-triggered alerts with real-time photos
- Flash LED toggle via `/flash` command

---

## 📈 Results and Discussions

- The system successfully captured and transmitted intruder photos via Telegram with **100% reliability** in testing scenarios.
- Integration with the Telegram app proved to be user-friendly and responsive.
- PIR motion detection worked accurately within a range of 1.6 meters, effectively triggering alerts.
- The system supports additional sensors, allowing for future expandability.
---

## ✅ Conclusion and Future Scope

This project demonstrates a practical and economical approach to smart home surveillance using IoT and open-source tools. By integrating ESP32-CAM and Telegram API, real-time intruder detection and alerts were achieved without depending on high-cost systems.

### 🔮 Future Scope
- Integrate more sensors (gas, fire, vibration) for a complete smart home solution.
- Enable cloud storage of captured images.
- Add AI for facial recognition and anomaly detection.
- Develop an Android/iOS app for better UI and control.
- Improve security by using end-to-end encrypted platforms.

---

## ⚠️ Limitations
- Requires FTDI module for programming (no native USB port).
- Telegram API isn't fully end-to-end encrypted.
- Limited camera resolution and sensor detection range.

---


> 👨‍💻 Developed by: Mritunjay Kumar Singh



