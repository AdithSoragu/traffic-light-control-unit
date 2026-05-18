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
├── traffic_light.v      # Traffic Light Controller Design
├── tb_traffic_light.v   # Testbench File
├── dump.vcd             # Waveform Dump File
└── README.md            # Documentation
```

---

# ⚙️ Project Specifications

| Parameter | Value |
|-----------|-------|
| Design Type | Synchronous |
| HDL Used | Verilog HDL |
| Clock Type | Single Clock |
| Reset | Active Low |
| Output Signals | Red, Yellow, Green |

---

# 🛠️ Tools Used

| Tool | Purpose |
|------|----------|
| Verilog HDL | Hardware Design |
| ModelSim | Simulation |
| QuestaSim | Verification |
| GTKWave | Waveform Viewing |

---

# 📌 Input Signals

| Signal | Type | Description |
|--------|------|-------------|
| clk | Input | System Clock |
| rst_n | Input | Active Low Reset |

---

# 📌 Output Signals

| Signal | Description |
|--------|-------------|
| red | Red Light Signal |
| yellow | Yellow Light Signal |
| green | Green Light Signal |

---

# 🔄 Working Principle

The traffic controller changes traffic signals sequentially based on clock cycles.

---

## 🔴 RED State

- Stops vehicle movement
- Red LED turns ON
- Green and Yellow remain OFF

---

## 🟢 GREEN State

- Allows vehicle movement
- Green LED turns ON
- Red and Yellow remain OFF

---

## 🟡 YELLOW State

- Warning state before RED
- Yellow LED turns ON
- Red and Green remain OFF

---

# 🧩 Verilog Design Explanation

## State Declaration

```verilog
parameter RED = 2'b00,
          GREEN = 2'b01,
          YELLOW = 2'b10;
```

Defines different FSM states.

---

## State Register

```verilog
reg [1:0] state;
```

Stores current traffic light state.

---

## Sequential Logic

```verilog
always @(posedge clk or negedge rst_n)
```

Updates state at every positive edge of clock.

---

## State Transition Logic

```verilog
case(state)
```

Controls transition between traffic light states.

---

# 🧪 Testbench Description

The testbench verifies:
- State transitions
- Signal timing
- Reset operation
- Proper sequence of traffic lights

---

# ▶️ Simulation Procedure

## Step 1: Compile Files

```bash
vlog traffic_light.v tb_traffic_light.v
```

---

## Step 2: Start Simulation

```bash
vsim tb_traffic_light
```

---

## Step 3: Run Simulation

```bash
run -all
```

---

## Step 4: View Waveform

```bash
gtkwave dump.vcd
```

---

# 📊 Expected Output Sequence

```text
RED → GREEN → YELLOW → RED
```

The sequence continuously repeats.

---

# 📈 Waveform Analysis

The waveform verifies:
- Proper FSM operation
- Correct signal transitions
- Clock synchronization
- Reset behavior
- Sequential traffic control

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

# 📚 Learning Outcomes

This project helps in understanding:

- Finite State Machines (FSM)
- Sequential circuit design
- Verilog HDL coding
- Traffic signal control logic
- Digital system simulation
- Waveform verification

---

# 🔮 Future Enhancements

The project can be extended by adding:

- Timer-based signal control
- Vehicle density sensors
- Emergency vehicle priority
- Pedestrian crossing system
- Smart traffic monitoring
- FPGA implementation

---

# 👨‍💻 Author

## Adith Soragu

Electronics and Communication Engineering

---

# ⭐ GitHub Repository

If you found this project useful, consider giving it a ⭐ on GitHub.


