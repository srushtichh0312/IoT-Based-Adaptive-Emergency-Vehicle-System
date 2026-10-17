# 🚑 RAKSHAK YOJNA
### IoT-Based Adaptive Emergency Vehicle Management System

<p align="center">
  <b>🚦 Smart Traffic Signal Preemption | 📡 LoRa Communication Concept | 🗺️ Interactive Simulation</b>
</p>

---

## 📌 About the Project

**Rakshak Yojna** is an emergency vehicle management project designed to demonstrate how traffic signal priority can help an ambulance move through selected road junctions.

This repository contains the **software simulation** of the proposed system. It demonstrates ambulance movement, hospital selection, traffic junctions, and emergency-mode behavior through an interactive city interface.

## ✨ Simulation Features

- 🗺️ **Interactive City Map** — Displays the ambulance route, hospitals, and traffic junctions.
- 🏥 **Hospital Locations** — Shows three hospital locations in the simulation.
- 🚑 **Ambulance Movement** — Demonstrates ambulance movement along the selected route.
- 🚦 **Traffic Junctions** — Visualizes four junctions and their traffic-signal behavior.
- 🆘 **Emergency Mode** — Demonstrates the emergency workflow through the simulation controls.
- 📡 **LoRa Communication Visualization** — Illustrates the proposed wireless communication concept.
- 📊 **Status Dashboard** — Displays simulation status and related information.
- ▶️ **Demo Controls** — Includes automatic demo, normal driving, speed adjustment, and reset options.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| 🌐 HTML5 | Webpage structure |
| 🎨 CSS3 | Layout, styling, and visual design |
| ⚙️ JavaScript | Simulation logic and interactive controls |
| 🗺️ Canvas / SVG | Visual representation of map elements and graphics |

## ▶️ How to Run the Simulation

1. 📥 Download or clone this repository.
2. 📂 Open the `01_Software_Simulation` folder.
3. 📁 Open the `Simulation` folder.
4. 🌐 Double-click `index.html` to open it in a web browser.
5. 🚑 Use the on-screen controls to explore the simulation.

**No additional software installation is required** for the basic browser-based demo.

## 🔄 Simulation Workflow

1. 🏥 View the available hospital locations.
2. 🗺️ Observe the ambulance route on the city map.
3. 🚑 Start the ambulance movement using the available controls.
4. 🚦 Observe the traffic junctions during the simulated emergency workflow.
5. 📡 View the visualization of the proposed LoRa communication process.
6. 🔁 Reset or replay the simulation to demonstrate the workflow again.

## 🧩 Proposed System Architecture

```text
🚑 Emergency Vehicle / Transmitter
              |
              v
       📡 LoRa Module
              |
       Wireless Link
              |
              v
        📡 LoRa Module
              |
              v
      🚦 Receiver Unit
              |
              v
    Traffic Signal Indicators
```

*Note: This diagram represents the proposed hardware communication concept. The web simulation is a separate software demonstration.*

## ⚠️ Simulation Limitations

- The current webpage is a **simulation**, not a live traffic-control system.
- The displayed LoRa communication and signal behavior are visual demonstrations; they do not confirm actual wireless communication with the ESP32 hardware.
- Live GPS tracking, real-time traffic data, and direct website-to-hardware integration are not implemented in this simulation.

## 🚀 Future Enhancements

- 📍 Integrate real-time GPS location tracking.
- 📡 Establish communication between the web application and ESP32-based hardware.
- 🚦 Test emergency-priority behavior using physical traffic-signal indicators.
- 🏥 Explore hospital information and route-management integration.

## 🎓 Project Purpose

This simulation demonstrates the software-side concept of an adaptive emergency vehicle management system and supports the presentation of the proposed hardware workflow.

---

<p align="center">
  🚑 <b>RAKSHAK YOJNA</b><br>
  <i>Exploring smarter traffic management for emergency vehicles.</i>
</p>

