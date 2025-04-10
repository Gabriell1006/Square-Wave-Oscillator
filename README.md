# Square Wave Signal Generator

Project developed for the **Electronic Devices and Circuits** course  
**University Politehnica of Bucharest** – Faculty of Electronics, Telecommunications and Information Technology

## 📌 Project Specifications

- **Signal Type**: Square wave
- **Oscillation Frequency (f₀)**: Adjustable between 22 – 66 kHz
- **Duty Cycle**: 0.5
- **Output Load (RL)**: 22 kΩ
- **Peak-to-Peak Output Voltage (V₀)**: Adjustable between 0 – 4.4 V
- **DC Offset**: None
- **Operating Temperature Range**: 0°C – 70°C
- **Power Supply Presence Indication**: LED

## ⚙️ System Architecture

The circuit is composed of the following functional blocks:
- Comparator-based oscillator with feedback
- Differential amplification stage
- Class AB output stage
- LED-based power indication
- Frequency and amplitude adjustment via potentiometers

## 🔍 Working Principle

The comparator controls the oscillation using a capacitor (C1) and a potentiometer (Pfrecv), generating a stable square wave. The circuit includes:

- **Current Mirror**: Using Q1, Q2, Q3
- **Differential Stage**: Q4 and Q5 amplify differential signals and reject common-mode noise
- **Common-Emitter Stage**: Q6 amplifies the output signal
- **Class AB Output**: Q7 and Q8, with diodes U9 and U10 for V_BE compensation
- **Control**: Potentiometers for adjusting both frequency and output amplitude

### Step-by-Step Operation:

1. **Startup**: Capacitor C1 charges via Pfrecv. The op-amp output initially sets to Vcc.
2. **Feedback Loop**: A voltage divider formed by resistors R3 and R4 feeds back part of the output voltage.
3. **Switching Point**: When the capacitor voltage exceeds a threshold, the op-amp switches to Vee.
4. **Discharge and Repeat**: The capacitor discharges and recharges in the opposite direction, restarting the cycle.
5. **Continuous Oscillation**: A stable rectangular waveform is continuously generated.

## 🧪 Simulations

Simulations were performed under the following conditions:
- **Frequencies**: 22 kHz and 66 kHz
- **Voltages**: 0 Vpp and 4.4 Vpp
- **Temperatures**: 0°C, 25°C, 70°C

Results confirm stable functionality and performance across all test conditions.

## 🧱 Component List

| No. | Component IDs        | Value           |
|-----|-----------------------|------------------|
| 1   | D9, D10               | 1N4148           |
| 2   | Q6, Q8                | QBC817-25        |
| 3   | Q1–Q5, Q7             | QBC807-25        |
| 4   | R5, R6, R100          | 100 Ω            |
| 5   | R3, R4, R12–R15       | 1 kΩ             |
| 6   | R7                    | 1.5 kΩ           |
| 7   | RL3                   | 2 kΩ             |
| 8   | R1                    | 6.8 kΩ           |
| 9   | RL1, RL2              | 10 kΩ            |
| 10  | PFRECV                | 10 kΩ potentiometer |
| 11  | Pamplit               | 500 kΩ potentiometer |
| 12  | C1                    | 100 nF           |
| 13  | L1, L2                | LED              |

## 🖼️ PCB Layout

- Top and bottom electrical layers
- Top silk screen
- Solder mask layer
- Combined layout (TOP + Silk Screen)

## 👨‍🎓 Project Contributors

- **Student**: Popescu Vlad Gabriel  
- **Group**: 433E  
- **Supervisors**:  
  - Prof. Mihaela Pantazica  
  - Prof. Florin Drăghici  

---


