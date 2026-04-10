# 🎮 FPGA Simon Game (Verilog)

## 📌 Overview
This project is a hardware implementation of the classic **Simon memory game**, built entirely on an FPGA using **Verilog HDL**. The game challenges users to remember and reproduce an increasingly long sequence of visual cues displayed through LEDs.

Designed with a focus on **digital logic design**, **finite state machines**, and **real-time user interaction**, this project demonstrates low-level system design without relying on high-level software abstractions.

---

## ⚙️ Features
- 🎯 Random sequence generation using hardware logic  
- 🔁 Progressive difficulty (sequence increases each round)  
- 💡 LED-based visual feedback  
- 🎮 User input via push buttons  
- ❌ Error detection and automatic reset  
- 🔄 Finite State Machine (FSM) for control flow  
- ⏱️ Clock division for human-readable timing  

---

## 🧠 System Design

### Core Components

**Finite State Machine (FSM)**
- Idle / Start  
- Sequence Display  
- User Input  
- Validation  
- Game Over  

**Sequence Generator**
- Pseudo-random sequence generation (LFSR or counter-based)
- Stored in registers

**Input Handler**
- Button debouncing  
- Real-time input capture  

**Comparator Logic**
- Matches user input with stored sequence  
- Determines correctness  

**Clock Divider**
- Slows FPGA clock for visible LED output  

---

## 🛠️ Technologies Used
- **Language:** Verilog HDL  
- **Platform:** FPGA Development Board (e.g., DE1-SoC)  
- **Tools:** Quartus Prime, ModelSim  

---

## 🚀 How It Works
1. Game initializes and generates a sequence  
2. LEDs display the sequence  
3. Player repeats the sequence using buttons  
4. System validates input:
   - ✅ Correct → sequence extends  
   - ❌ Incorrect → game resets  
5. Game continues with increasing difficulty  

---

## 🧪 Testing & Validation
- Simulated in ModelSim to verify:
  - FSM transitions  
  - Sequence generation  
  - Input correctness  
- Tested on FPGA hardware for:
  - Timing accuracy  
  - Responsiveness  
  - Stability  

---

## 📈 Key Learnings
- Designing finite state machines in hardware  
- Handling asynchronous inputs (button presses)  
- Implementing timing control using clock division  
- Debugging simulation vs real hardware behavior  

---

