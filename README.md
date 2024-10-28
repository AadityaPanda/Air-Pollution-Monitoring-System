# Air Pollution Monitoring System

This project demonstrates an IoT-based air pollution monitoring system using the MQ135 air quality sensor. The system measures the air quality index (AQI) and displays the results on an LCD screen while providing visual and auditory alerts based on the AQI levels.

## Features

- Measures air quality using the MQ135 sensor.
- Displays real-time AQI on a 16x2 LCD.
- Color-coded LED indicators for different AQI levels:
  - Green LED for "Good" AQI.
  - Blue LED for "Moderate" AQI.
  - Red LED for "Unhealthy" and above AQI.
- Buzzer alerts for hazardous air quality levels.
- Serial monitor output for debugging and real-time monitoring.

## Hardware Required

- Arduino board (e.g., Arduino Uno)
- MQ135 air quality sensor
- 16x2 LCD
- Green, Blue, and Red LEDs
- Buzzer
- Resistors (appropriate values for LEDs)
- Breadboard and jumper wires

## Circuit Diagram

![digital-pin-11-of-Arduino-1024x597](https://github.com/user-attachments/assets/c143ca86-55e7-4e5c-b48e-0cb4628d1c0c)

## Hardware Setup

1. Connect the MQ135 sensor to the analog pin A0 on the Arduino.
2. Connect the LCD pins as follows:
   - RS -> Pin 2
   - EN -> Pin 3
   - D4 -> Pin 4
   - D5 -> Pin 5
   - D6 -> Pin 6
   - D7 -> Pin 7
3. Connect the green LED to Pin 8, the blue LED to Pin 9, and the red LED to Pin 10 with appropriate resistors.
4. Connect the buzzer to Pin 11.
5. Connect the power and ground pins accordingly.

![LCD-Output-1024x722](https://github.com/user-attachments/assets/cba20a6c-5953-4d32-aa7a-1465ce32ce3e)

## Result Shown in Serial Monitor

Upon uploading the code and powering the system, you will see real-time AQI readings in the Serial Monitor. The output will indicate the air quality level based on the readings from the MQ135 sensor.

Example Serial Monitor Output:
```
Air Quality: 45
AQI Good
Air Quality: 78
AQI Moderate
Air Quality: 150
AQI Unhealthy
```

## Usage

1. Upload the code to your Arduino board.
2. Open the Serial Monitor to view the AQI readings.
3. Observe the LED indicators and buzzer alerts based on the AQI levels.
