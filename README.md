# Smart-Agriculture-Drone
To develop a drone-based AI and ML–powered system that estimates Actual Evapotranspiration (AET) at farm level, bridges the resolution and accuracy gap of satellite-based ET systems (especially under cloudy conditions), and provides actionable irrigation and water-use insights for sustainable farming.

---

## 🚀 Project Overview

This project aims to develop a **drone-based intelligent evapotranspiration (ET) sensing and irrigation water-use accounting system** to revolutionize **precision irrigation management** in Indian agriculture.

By integrating **AI/ML, drone-based imaging, and cloud-based analytics**, the system provides **real-time farm-level water auditing, crop health monitoring, and water-use efficiency assessment** — even under cloudy conditions where satellite data fail to deliver reliable results.

This project is a basic prototype for a Plant Disease Recognition System that uses AI/ML-based image classification to detect plant leaf diseases.
The prototype runs on a Windows laptop using a standard webcam to capture live images of leaves and identify possible diseases in real-time.
In the full-scale implementation, this system will be deployed on edge AI computers such as the NVIDIA Jetson Nano or Raspberry Pi 5, integrated with an onboard camera for autonomous field-level disease monitoring via drones or robotic platforms.

---

## 🧠 Problem Statement

Satellite-based AET estimation suffers from:

* **Low spatial resolution**
* **Reduced accuracy under cloud cover**
* **Lack of ground-level calibration**

This project bridges that gap by using **drone-mounted sensors** and **AI/ML-driven models** to enhance data accuracy and provide **localized water management insights**.

---

## 🌱 Proposed Solution

A **sophisticated drone system** that:

1. Uses **Intel RealSense D455** for 3D terrain and canopy depth mapping.
2. Integrates **AI/ML algorithms** on the **NVIDIA Jetson Nano** for real-time ET estimation, crop identification, and disease detection.
3. Employs **Pixhawk 2.4.8** as the flight controller for stability and mission control.
4. Synchronizes with **Google Earth Engine (GEE)** satellite data for calibration and analysis.
5. Sends results to a **cloud server** for visualization through a farmer-friendly **mobile/web application**.

---

## 💡 Key Features

| Feature                             | Description                                             |
| ----------------------------------- | ------------------------------------------------------- |
| 🌤️ **Accurate ET Estimation**      | Drone-based sensing combined with satellite data fusion |
| 🌾 **Crop Type & Health Detection** | AI models trained for leaf and canopy analysis          |
| 💧 **Irrigation Auditing**          | Water use tracking and efficiency analysis              |
| 📡 **Telemetry & IoT**              | LoRa and Wi-Fi data transmission to the ground station  |
| ⚙️ **Autonomous Operations**        | Pixhawk mission planning for 50–5000 ha command areas   |
| ☁️ **Cloud Integration**            | Real-time visualization for farmers and administrators  |

---

## ⚙️ System Architecture

```
             ┌──────────────────────────────┐
             │       Satellite Data (GEE)   │
             └──────────────┬───────────────┘
                            │
                            ▼
┌────────────┐       ┌──────────────────────────┐
│ Drone Unit │──────▶│  NVIDIA Jetson + D455    │
│ (Pixhawk)  │       │  Onboard AI Inference    │
└────────────┘       └──────────────────────────┘
                            │
                            ▼
                    ┌──────────────────────┐
                    │ Cloud Server / IoT DB│
                    │ (Firebase / MQTT)    │
                    └──────────────────────┘
                            │
                            ▼
                    ┌──────────────────────┐
                    │ Farmer’s Dashboard   │
                    │ (Mobile/Web App)     │
                    └──────────────────────┘
```

---

## 🧩 Hardware Components

| Component                      | Description              | Approx. Price (INR) |
| ------------------------------ | ------------------------ | ------------------- |
| Pixhawk 2.4.8                  | Flight Controller        | 10,446              |
| S550 Hexacopter Frame          | Drone Body               | 3,879               |
| EMAX MT2213 (935kV) x6         | Brushless Motors         | 3,409               |
| Emax BLHeli ESC x6             | Motor Controllers        | 7,995               |
| APM/Pixhawk Power Module       | Power Management         | 526                 |
| 433 MHz Radio Telemetry Kit    | Long-Range Communication | 6,322               |
| Carbon Fiber Propellers (8045) | CW/CCW Props             | 1,789               |
| NEO-M8N GPS with Compass       | GPS Module               | 2,296               |
| NVIDIA Jetson Nano             | Onboard AI Computer      | 27,000              |
| Intel RealSense D455           | Depth Camera             | 45,000              |
| LiPo 3S 35C 10,000 mAh         | Battery                  | 9,000               |
| FlySky FS-iA6B Tx-Rx           | Remote Controller        | 5,000               |
| **Total Cost**                 |                          | **≈ ₹1,22,667**     |

---

## 🧮 Software Stack

| Domain           | Tools / Languages            |
| ---------------- | ---------------------------- |
| Programming      | Python, C++, MATLAB, Arduino |
| AI / ML          | TensorFlow, PyTorch          |
| Embedded Control | Arduino IDE, Mission Planner |
| GIS              | Google Earth Engine, QGIS    |
| Cloud / IoT      | Firebase, MQTT, ThingSpeak   |
| Vision           | OpenCV, RealSense SDK        |

---

## ⚙️ Feasibility and Risk Mitigation

| Challenge                | Strategy                                            |
| ------------------------ | --------------------------------------------------- |
| Long-range connectivity  | Ground-based telemetry and LoRa mesh network        |
| Power endurance          | Modular battery system + ground recharging station  |
| Groundwater measurement  | Depth camera + AI inference in place of soil probes |
| Large farm data handling | Common ground stations and cloud data management    |

---

## 🌎 Sustainability & Impact

### ✅ **Environmental Impact**

* Efficient water use → reduced wastage and soil salinization
* Enhanced crop resilience under drought

### ✅ **Farmer Empowerment**

* Real-time data access and decision support
* Reduced dependency on third-party analysis

### ✅ **Economic Viability**

* Cost-effective (₹1.5 Lakh vs ₹5+ Lakh DJI multispectral)
* ~70% cost reduction with open hardware approach

---

## 📈 Expected Outcomes

* **Accurate farm-level ET maps**
* **Improved Water Use Efficiency (WUE)**
* **AI-based crop and irrigation insights**
* **Actionable water-saving recommendations**
* **Scalable model for 50–5000 ha irrigation commands**

---

## 🧪 Prototype Results

* Integrated **SMAP satellite data** with drone images.
* Demonstrated **leaf and crop detection** using trained ML model.
* Achieved high accuracy in canopy water-content mapping.

📂 **GitHub Repository for ML Model (Linked Work):**
👉 [SIH-PSID-SIH1571](https://github.com/shashi162003/SIH-PSID-SIH1571)

---

## 📸 Visuals

| Demo                      | Description                                    |
| ------------------------- | ---------------------------------------------- |
| 🌾 Drone Prototype        | Hexacopter with RealSense + Jetson integration |
| 🧠 Model Detection Output | Leaf and canopy detection results              |
| 🛰️ SMAP Integration      | ET data calibration via satellite              |

---

## 🧑‍💻 Team GLITCH

| Name                       | Role                                 |
| -------------------------- | ------------------------------------ |
| Harshit Kachhap            | System Architect & AI/ML Integration |
| Shashi Kumar               | Computer Vision & Drone Control      |
| [Team Members Placeholder] | Hardware & Software Integration      |

---

## 📚 References

* [A Pilot Study of Smart Agricultural Irrigation using UAVs and IoT-Based Cloud System](https://www.jouav.com/blog/agriculture-drone.html)
* [ICAR eMagazine Vol. 2, Issue 1](https://iiss.icar.gov.in/eMagazine/v2i1/5.pdf)
* [Garuda Aerospace - Kisan Drone](https://www.garudaaerospace.com/garudas-kisan-drone-agri-drone/)
* [SMAP Satellite Data](https://smap.jpl.nasa.gov/)
* [Component Pricing Source - Robu.in](https://robu.in/)

---

## 📬 Contact

For collaborations, technical queries, or documentation requests:
🌐 **Project Lead:** [Harshit Kachhap](mailto:harshitkachhap@example.com)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---
