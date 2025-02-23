# 🚗 Automated Guided Vehicle (AGV) Project  

## 📌 Introduction  
The **Automated Guided Vehicle (AGV)** is a self-navigating robotic system designed for industrial and warehouse automation. It can autonomously follow a predefined path, avoid obstacles, and transport loads efficiently. AGVs are widely used in manufacturing, logistics, and smart factories to improve operational efficiency and reduce human intervention.  

---

## 🌟 Features  
- **Autonomous Navigation** – Uses IR, LiDAR, or camera-based path following.  
- **Obstacle Avoidance** – Equipped with ultrasonic and LiDAR sensors.  
- **Wireless Control** – Remote operation via Wi-Fi, Bluetooth, or IoT.  
- **Load Handling** – Can carry and transport materials.  
- **Real-time Monitoring** – Data transmission to a dashboard for live tracking.  
- **Power Management** – Smart battery management for efficient power consumption.  
- **Multiple AGV Coordination** – Can work in fleets with collision avoidance.  

---

## 🔩 Components Used  

### **1️⃣ Hardware Components**  
- **Microcontroller/Processor**: Raspberry Pi / Arduino Mega / STM32  
- **Motor Driver**: L298N / TB6612FNG (for controlling motors)  
- **Motors**: DC Motors with Encoder / Servo Motor (for precise movement)  
- **Sensors**:  
  - IR Sensors (Line following)  
  - Ultrasonic Sensors (Obstacle detection)  
  - LiDAR / Camera (Advanced navigation)  
  - IMU (Inertial Measurement Unit for stability)  
- **Battery**: 12V Li-ion / Lead Acid Battery  
- **RFID Module**: For location-based navigation  
- **Communication Modules**:  
  - Wi-Fi (ESP8266/ESP32 for IoT-based control)  
  - Bluetooth (HC-05 for remote control)  
  - ZigBee/RF Module (For long-range communication)  
- **LCD Display**: OLED Display for status updates  

---

## 🛠️ Circuit Connection  

| Component  | Connection to Microcontroller |
|------------|------------------------------|
| **L298N Motor Driver** | PWM Pins (for speed control) |
| **IR Sensors** | Digital Pins (for line tracking) |
| **Ultrasonic Sensor** | Trigger & Echo Pins (Obstacle detection) |
| **LiDAR/Camera** | Serial/I2C Communication |
| **Bluetooth Module (HC-05)** | Tx & Rx (Serial Communication) |
| **Wi-Fi Module (ESP8266/ESP32)** | UART or SPI Interface |
| **RFID Module** | SPI/I2C Communication |
| **Battery** | Power Supply (12V or 5V) |


---

## ⚙️ Working Principle  
1️⃣ The **IR Sensors** detect the line (black/white surface) to follow the predefined path.  
2️⃣ The **Ultrasonic Sensors** or **LiDAR** detect obstacles and reroute the AGV if necessary.  
3️⃣ The **Microcontroller (Arduino/Raspberry Pi)** processes the sensor data and sends control signals to the **Motor Driver (L298N)**.  
4️⃣ The **Motors (DC/Servo)** move the AGV based on the control signals.  
5️⃣ The **RFID Module** helps in predefined station stopping (if required).  
6️⃣ The AGV **communicates wirelessly** using Wi-Fi/Bluetooth/ZigBee for remote monitoring.  

