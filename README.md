# 🚦 Traffic Light Control Unit using Verilog HDL

<p align="center">
  <img src="https://img.shields.io/badge/Language-Verilog-blue">
  <img src="https://img.shields.io/badge/Simulation-ModelSim-green">
  <img src="https://img.shields.io/badge/Status-Completed-success">
</p>

---

# 📌 Introduction

Traffic congestion is one of the major challenges in modern transportation systems. Traffic Light Control Units are used to manage vehicle movement efficiently at road intersections by controlling signal timings.

This project implements a **Traffic Light Control Unit** using **Verilog HDL**. The controller automatically switches traffic signals between **Red, Yellow, and Green** states in a predefined sequence using digital logic and finite state machine (FSM) concepts.

The design is simulated and verified using Verilog testbench and waveform analysis.

---

# 🎯 Project Objectives

The objectives of this project are:

- Design a Traffic Light Controller using Verilog HDL
- Implement signal state transitions
- Control Red, Yellow, and Green LEDs
- Understand FSM (Finite State Machine) concepts
- Verify functionality using simulation
- Analyze timing waveforms

---

# 🚦 Traffic Light System Overview

A traffic light controller manages traffic signals at road intersections.

The signal sequence follows:

```text
RED → GREEN → YELLOW → RED
```

Each signal remains active for a fixed duration before transitioning to the next state.

---

# 🧠 Finite State Machine (FSM)

The Traffic Light Controller is implemented using a **Finite State Machine (FSM)**.

The FSM contains different states representing traffic light conditions.

---

# 📌 FSM States

| State | Signal |
|-------|---------|
| S0 | RED |
| S1 | GREEN |
| S2 | YELLOW |

---

# 🔄 State Transition Diagram

```text
       ┌────────┐
       │  RED   │
       └────┬───┘
            │
            ▼
       ┌────────┐
       │ GREEN  │
       └────┬───┘
            │
            ▼
       ┌────────┐
       │ YELLOW │
       └────┬───┘
            │
            ▼
          RED
```

---

# 📂 Project Structure

```text
Traffic_Light_Control_Unit/
│
```

# 🛠️ Tools Used

| Tool | Purpose |
|------|----------|
| Verilog HDL | Hardware Design |
| ModelSim | Simulation |

---

# 🚀 Applications

Traffic Light Controllers are widely used in:

- Smart Cities
- Highway Junctions
- Railway Crossings
- Automated Road Systems
- Urban Traffic Management
- Embedded Control Systems

---

# ✅ Advantages

- Simple digital design
- Efficient traffic management
- Reduces manual control
- Improves road safety
- Easy implementation using FSM

---

# 👨‍💻 Author

## Adith Soragu

Electronics and Communication Engineering

---



