# Sensor_Warning_System

## Project Overview
The Sensor_Warning_System is an Internet of Things (IoT) based safety solution that combines Field-Programmable Gate Array (FPGA) hardware processing with ESP32 microcontroller wireless communication capabilities. This system implements real-time environmental monitoring and emergency alert functionality through the integration of multiple sensor technologies. The project provides comprehensive fire safety monitoring by combining temperature/humidity detection, smoke sensing, and wireless connectivity in a unified platform.

<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/cd19d085-2c94-48a5-9917-24aa6ef45135" />



Smart Fire Alarm Monitoring System is an electronic system that uses sensors to detect abnormal conditions in the environment or equipment, processes the collected data, and generates warning signals to notify users in order to prevent risks and accidents.

**Video project** : https://youtu.be/CG1zkX-FkQo?si=CjR44xusNYt4jImB
## Key Features

### Multi-Sensor Integration
- **DHT11 Sensor**: Real-time temperature and humidity monitoring with FPGA-based precision timing control
- **MQ-2 Smoke Sensor**: Analog and digital smoke detection with configurable sensitivity thresholds
- **ESP32 Processing**: Advanced data processing and wireless communication capabilities

### Dual Communication Architecture
- **UART Communication**: High-speed data transfer between FPGA and ESP32 processors
- **WiFi Connectivity**: Cloud integration via ThingsBoard IoT platform
- **Real-time Telemetry**: Continuous data streaming to cloud dashboard

### Intelligent Alert System
- **Multi-level Warning**: Visual (LED indicators), audible (buzzer), and remote notifications
- **Configurable Thresholds**: Dynamic adjustment of alarm parameters through cloud interface
- **Emergency Calling**: GSM-based automatic emergency dialing system activation

### Advanced Display Interfaces
- **LCD Display**: I2C-controlled 16×2 LCD for local sensor readings
- **7-Segment Display**: Four-digit LED display for smoke concentration values
- **Real-time Updates**: Simultaneous local and remote data visualization

<img width="1454" height="776" alt="image" src="https://github.com/user-attachments/assets/0d9cd662-8021-493c-8626-54cc209025b8" />
<img width="1162" height="895" alt="image" src="https://github.com/user-attachments/assets/d1ee96e2-9bf3-4eb3-adf1-c633d4e2a59f" />


## System Architecture

### FPGA Subsystem (Verilog Implementation)
- **Sensor Management**: Precise timing control for DHT11 communication protocol
- **Data Processing**: Real-time sensor data acquisition and validation
- **Display Control**: LCD and 7-segment display drivers
- **UART Communication**: Efficient data packaging and transmission to ESP32

### ESP32 Subsystem (C++ Implementation)
- **Wireless Connectivity**: WiFi management and cloud communication
- **Data Aggregation**: Collection and processing from multiple sensor sources
- **Cloud Integration**: ThingsBoard telemetry and Remote Procedure Call (RPC) command handling
- **Emergency Response**: GSM-based calling system activation

## Technical Specifications

### Hardware Components
- **FPGA Board**: Main processing unit with sensor interfaces
- **ESP32**: WiFi/BLE module for wireless communication
- **DHT11**: Digital temperature and humidity sensor
- **MQ-2**: Analog smoke/gas detection sensor
- **LCD Display**: I2C 16×2 character display
- **7-Segment Display**: Four-digit LED display module
- **GSM Module**: SIM800L for emergency calling functionality

<img width="559" height="789" alt="image" src="https://github.com/user-attachments/assets/2dd197b8-bf75-4e4f-a978-54b3a12382de" />


### Communication Protocols
- **UART**: FPGA ↔ ESP32 data exchange (9600 baud rate)
- **I2C**: LCD display control interface
- **SPI**: 74HC595 shift register interface for 7-segment display
- **HTTP/RPC**: Cloud communication with ThingsBoard platform
<img width="2550" height="1191" alt="image" src="https://github.com/user-attachments/assets/0510148a-1876-4abc-be76-8ad370fc2c0a" />

### Performance Parameters
- **Sampling Interval**: 2 seconds for environmental sensors
- **Response Time**: <100 milliseconds for alarm conditions
- **Temperature Accuracy**: ±2°C
- **Humidity Accuracy**: ±5%
- **Communication Latency**: <1 second for cloud telemetry

<img width="2231" height="1245" alt="image" src="https://github.com/user-attachments/assets/43ae2cba-2066-4bf3-a7b9-3746d9d0dec1" />
<img width="1899" height="1129" alt="image" src="https://github.com/user-attachments/assets/4b494bb2-43a4-4a40-8922-5670f62df08e" />


## Implementation Details

### FPGA Code Structure
The FPGA implementation consists of modular Verilog components:
1. **Clock Management**: Frequency division for precise timing
2. **Sensor Interface**: DHT11 protocol state machine
3. **Display Controllers**: LCD and 7-segment driver modules
4. **Communication Interface**: UART transmitter for ESP32 communication

<img width="1578" height="889" alt="image" src="https://github.com/user-attachments/assets/b6b9d784-468b-409c-b324-e3e859f99eb0" />
<img width="987" height="593" alt="image" src="https://github.com/user-attachments/assets/65f81d88-c550-4c93-8953-b17c3c9f3d2c" />

### ESP32 Software Architecture
The ESP32 firmware includes:
1. **WiFi Management**: Connection handling and network stability
2. **Cloud Communication**: ThingsBoard MQTT client implementation
3. **Data Processing**: Sensor data aggregation and formatting
4. **Emergency System**: GSM module control and call management

<img width="1920" height="922" alt="image" src="https://github.com/user-attachments/assets/f7abfaf1-5b64-471e-913c-6658729b3f51" />


## Safety Features
1. **Data Validation**: Checksum verification for sensor communications
2. **Redundant Alerts**: Multiple independent warning systems
3. **Manual Override**: Physical button control for warning mode
4. **Fault Detection**: Communication timeout and error handling

## Applications
- Residential fire safety systems
- Industrial environmental monitoring
- Laboratory safety equipment
- Educational IoT demonstrations

<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/295415eb-a6fd-458c-acf9-4aa1649b3b8c" />

  
