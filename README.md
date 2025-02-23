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
- **Microcontroller/Processor**: Raspberry Pi (with ROS2 support)  
- **Motor Driver**: L298N / TB6612FNG  
- **Motors**: DC Motors with Encoder / Servo Motor  
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

| Component  | Connection to Raspberry Pi |
|------------|------------------------------|
| **L298N Motor Driver** | GPIO (PWM Pins) |
| **IR Sensors** | Digital GPIO Pins |
| **Ultrasonic Sensor** | GPIO (Trigger & Echo) |
| **LiDAR/Camera** | Serial/I2C Communication |
| **Bluetooth Module (HC-05)** | UART (Tx & Rx) |
| **Wi-Fi Module (ESP8266/ESP32)** | UART or SPI Interface |
| **RFID Module** | SPI/I2C Communication |
| **Battery** | Power Supply (12V or 5V) |

---

## ⚙️ Working Principle  
1️⃣ The **IR Sensors** detect the line (black/white surface) to follow the predefined path.  
2️⃣ The **Ultrasonic Sensors** or **LiDAR** detect obstacles and reroute the AGV if necessary.  
3️⃣ The **Raspberry Pi (ROS2)** processes the sensor data and sends control signals to the **Motor Driver (L298N)**.  
4️⃣ The **Motors (DC/Servo)** move the AGV based on the control signals.  
5️⃣ The **RFID Module** helps in predefined station stopping (if required).  
6️⃣ The AGV **communicates wirelessly** using Wi-Fi/Bluetooth/ZigBee for remote monitoring.  

---

## 🚀 Installation & Setup  

### 🖥️ **Prerequisites**  
Ensure you have **ROS2** installed on your Raspberry Pi:  
```bash
sudo apt update 
```

### 📦 **Building the ROS2 Package**  
```bash
colcon build --symlink-install
source install/setup.bash
```

### ▶ **Running the AGV**  
Launch the AGV 
  
## 🔧 Usage  
- **To control AGV manually:**  
  ```bash
  ros2 topic pub /cmd_vel geometry_msgs/Twist "{linear: {x: 0.5}, angular: {z: 0.0}}"
  ```



---

## 👨‍💻 Contributing  
Pull requests are welcome! If you find any issues or want to contribute, please open an issue or submit a PR.  

---

## 📜 License  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.  

---

## 📞 Contact  
For any queries, reach out via:  
📧 Email: Swathivishwakarma11@gmail.com  
🔗 GitHub: [Swathi-vishwakarma](https://github.com/Swathi-vishwakarma)  
