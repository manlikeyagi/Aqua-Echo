#  AquaEcho: Acoustic-Based Smart Water Monitoring System

**AquaEcho** is a low-cost, AI-powered water infrastructure monitoring system built around the **Seeed Studio Wio Terminal**. It uses **acoustic sensing** and **Edge AI** to detect water flow patterns, leaks, and groundwater depletion  making it ideal for rural or underserved areas.

---

##  Project Overview

AquaEcho captures ambient sound from water systems (e.g., pipes, tanks, boreholes) and uses an on device AI model to classify conditions such as **normal flow**, **leak**, or **dry pipe**. Data is logged locally and transmitted via **WiFi**, **LoRa**, or **4G** to a web/mobile dashboard for real-time monitoring and alerts.

---

## 🛠️ System Architecture

### 📦 Hardware Components

| Component                     | Function                                                   |
|------------------------------|------------------------------------------------------------|
| Wio Terminal                 | Main microcontroller with LCD, WiFi, BLE, microSD          |
| Waterproof MEMS Mic / Hydrophone | Captures underwater/pipe acoustic data               |
| microSD Card                 | Stores logs and audio samples                              |
| Grove Ultrasonic Sensor (optional) | Measures water level as a backup                    |
| LoRa / 4G / WiFi Module      | Sends data to cloud dashboard                              |
| Solar Battery Pack           | Powers system for remote deployment                        |
| Waterproof Enclosure         | Protects components in field conditions                    |

### 💻 Software Components

- **Firmware**: Arduino-based C++ code for Wio Terminal  
- **Signal Processing**: FFT & Spectrogram extraction  
- **Edge AI Model**: TensorFlow Lite Micro (trained on Edge Impulse or manually)  
- **Dashboard**: Blynk, Node-RED, or ThingsBoard  
- **Cloud Backend**: Firebase, AWS IoT Core, or MQTT broker (optional)

---

## ⚙️ How It Works

1. **Sound Collection**: Acoustic sensors capture signals (flow, leak, silence, echo).
2. **Signal Preprocessing**: Noise filtering, frequency and amplitude analysis.
3. **On-Device AI Inference**: Wio Terminal classifies sound types (flow / leak / dry).
4. **Data Logging**: Logs saved to SD card with timestamps.
5. **Communication**: Key events transmitted wirelessly to a dashboard.
6. **Visualization**: Users view data and receive alerts via a web or mobile app.

---

## 🔧 Build Process

### Phase 1: Hardware Setup
- Connect microphone or hydrophone to Wio Terminal.
- Insert microSD card.
- Add optional ultrasonic sensor.
- Assemble waterproof casing.

### Phase 2: Software + AI
- Collect and label sound samples.
- Train a classification model on Edge Impulse.
- Convert to `.tflite` and flash to Wio Terminal.
- Program firmware to handle sound processing, inference, and communication.

### Phase 3: Dashboard Integration
- Set up Blynk/Node-RED/ThingsBoard.
- Visualize flow states, leaks, and alerts.
- Enable SMS/email notifications.

---

## 🖥️ User Interface

### 🟦 Wio Terminal Display

- ✅ **Status**: Normal / Leak / No Flow  
- 📊 **Signal Strength** and Spectrogram  
- ⚠️ **Fault Alerts**  
- 💾 **Logging Confirmation**

### 🌐 Online Dashboard

- Real-time monitoring per location  
- Leak history and timestamps  
- Water level and table trendlines  
- Waveform & spectrogram viewer  
- Echo delay chart (for aquifer shift detection)

---

## 📅 Implementation Roadmap

| Month | Activities                                                |
|-------|-----------------------------------------------------------|
| 1     | Hardware setup and sensor calibration                     |
| 2     | Data collection (flow, leaks, dry pipes)                  |
| 3     | AI model training + firmware development                  |
| 4     | Field testing in boreholes, tanks, and pipes              |
| 5     | Dashboard and alert system integration                    |
| 6     | Pilot deployment + community onboarding                   |

---

## 📸 Screenshots & Diagrams

### 🔧 System Schematic

![Schematic Diagram](schematics/aquaecho_circuit.png)

### 📱 Dashboard Preview

  <h3 align="center">🔧 AgriSmart station</h3>
<p align="center">
  <img src ="images/aqua echo.png" width="400"/>
</p>




---

## 🌍 Impact & Scalability

AquaEcho aims to provide:

- ✅ Affordable diagnostics for rural water systems  
- ✅ Early warning for drought and infrastructure failure  
- ✅ Non-invasive aquifer monitoring  
- ✅ Community empowerment through data-driven insights  
- ✅ Scalable deployment across low-resource regions

---

## 👨‍💻 Author

**Temitope Okunbamu Ridwan**  
IoT Engineer | Morrebs ICT Solutions  
📧 [okunbamuyagi@gmail.com]  
🔗 [https://www.linkedin.com/in/okunbamu-temitope-122a37226/]

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

**“Listen to the water. Learn its story. Protect its future.” – AquaEcho**
