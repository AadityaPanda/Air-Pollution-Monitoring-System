# 🌬️ Air Pollution Monitoring System

[![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white)](https://www.arduino.cc/)
[![IoT](https://img.shields.io/badge/IoT-Project-blue?style=for-the-badge)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> **Real-time air quality monitoring with visual and audio alerts**

An IoT-based air pollution monitoring system that provides real-time air quality measurements using the MQ135 sensor. The system displays AQI (Air Quality Index) values on an LCD screen and provides intuitive color-coded alerts to help users understand air quality conditions at a glance.

## 🚀 Features

- 📊 **Real-time AQI monitoring** using MQ135 air quality sensor
- 🖥️ **LCD display** showing current air quality readings
- 🚨 **Multi-level alert system** with color-coded LED indicators:
  - 🟢 **Green LED** → Good air quality (AQI: 0-50)
  - 🔵 **Blue LED** → Moderate air quality (AQI: 51-100)
  - 🔴 **Red LED** → Unhealthy air quality (AQI: 101+)
- 🔊 **Audio alerts** via buzzer for hazardous conditions
- 💻 **Serial monitor output** for debugging and data logging

## 🛠️ Hardware Components

| Component | Quantity | Purpose |
|-----------|----------|---------|
| Arduino Uno | 1 | Main microcontroller |
| MQ135 Air Quality Sensor | 1 | Air quality measurement |
| 16x2 LCD Display | 1 | Data visualization |
| LEDs (Green, Blue, Red) | 3 | Status indicators |
| Buzzer | 1 | Audio alerts |
| Resistors | 3 | LED current limiting |
| Breadboard | 1 | Circuit assembly |
| Jumper Wires | Multiple | Connections |

## 📋 Pin Configuration

### Arduino Connections

| Component | Arduino Pin | Notes |
|-----------|-------------|-------|
| **MQ135 Sensor** | A0 | Analog input |
| **LCD Display** | | |
| ├─ RS | 2 | Register select |
| ├─ EN | 3 | Enable |
| ├─ D4 | 4 | Data bit 4 |
| ├─ D5 | 5 | Data bit 5 |
| ├─ D6 | 6 | Data bit 6 |
| └─ D7 | 7 | Data bit 7 |
| **Green LED** | 8 | Good AQI indicator |
| **Blue LED** | 9 | Moderate AQI indicator |
| **Red LED** | 10 | Unhealthy AQI indicator |
| **Buzzer** | 11 | Audio alert |

## 🔧 Circuit Diagram

![Circuit Diagram](https://github.com/user-attachments/assets/c143ca86-55e7-4e5c-b48e-0cb4628d1c0c)

*Complete circuit schematic showing all component connections*

## 🔨 Assembly Instructions

1. **Sensor Connection**
   - Connect MQ135 VCC to Arduino 5V
   - Connect MQ135 GND to Arduino GND
   - Connect MQ135 analog output to Arduino pin A0

2. **LCD Setup**
   - Wire LCD according to the pin configuration table above
   - Connect LCD VDD to 5V and VSS to GND
   - Connect V0 to a potentiometer for contrast adjustment

3. **LED Indicators**
   - Connect each LED's anode to its respective digital pin through a 220Ω resistor
   - Connect all LED cathodes to GND

4. **Buzzer Connection**
   - Connect buzzer positive to pin 11
   - Connect buzzer negative to GND

5. **Power Connections**
   - Ensure all components share common ground
   - Verify 5V power distribution to all components

## 📊 AQI Classification

| AQI Range | Air Quality Level | LED Indicator | Buzzer |
|-----------|-------------------|---------------|--------|
| 0-50 | Good | 🟢 Green | Off |
| 51-100 | Moderate | 🔵 Blue | Off |
| 101-150 | Unhealthy for Sensitive Groups | 🔴 Red | Off |
| 151-200 | Unhealthy | 🔴 Red | On |
| 201-300 | Very Unhealthy | 🔴 Red | On |
| 301+ | Hazardous | 🔴 Red | On |

## 🖥️ System Output

![LCD Display Output](https://github.com/user-attachments/assets/cba20a6c-5953-4d32-aa7a-1465ce32ce3e)

*Real-time AQI display on LCD screen*

### Serial Monitor Output Example

```
🌬️ Air Quality Monitoring System Started
======================================
Air Quality: 45 PPM
Status: Good ✅
AQI Level: Green

Air Quality: 78 PPM  
Status: Moderate ⚠️
AQI Level: Blue

Air Quality: 150 PPM
Status: Unhealthy 🚨
AQI Level: Red
Alert: Buzzer Activated
```

## 🚀 Getting Started

### Prerequisites
- Arduino IDE installed on your computer
- Basic knowledge of Arduino programming
- Required libraries: `LiquidCrystal.h` (included in Arduino IDE)

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/AadityaPanda/Air-Pollution-Monitoring-System.git
   cd Air-Pollution-Monitoring-System
   ```

2. **Open Arduino IDE**
   - Load the `air_pollution_monitor.ino` file
   - Select your Arduino board and COM port

3. **Upload the code**
   - Verify the code compiles without errors
   - Upload to your Arduino board

4. **Monitor the system**
   - Open Serial Monitor (115200 baud rate)
   - Observe real-time AQI readings and system status

## 🔧 Calibration

The MQ135 sensor requires a warm-up period of 24-48 hours for accurate readings. For precise measurements:

1. Allow the sensor to stabilize in clean air
2. Adjust the calibration values in the code if necessary
3. Compare readings with a reference air quality meter

## 🎯 Applications

- **Home Monitoring**: Track indoor air quality
- **Office Environments**: Monitor workplace air conditions
- **Educational Projects**: Learn about IoT and environmental monitoring
- **Health Awareness**: Alert users to poor air quality conditions

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Arduino community for extensive documentation
- MQ135 sensor manufacturers for technical specifications
- Contributors and testers who helped improve this project

## 📞 Support

If you encounter any issues or have questions:
- 📧 Email: aadityapanda23@gmai.com
- 💬 Issues: [Create an issue](https://github.com/AadityaPanda/Air-Pollution-Monitoring-System/issues)
- 📚 Documentation: [Project Wiki](https://github.com/AadityaPanda/Air-Pollution-Monitoring-System/wiki)

---

<div align="center">
  <p>⭐ Star this repository if you found it helpful!</p>
  <p>Made with ❤️ for cleaner air and better health</p>
</div>
