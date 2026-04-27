# SKILL LAB PRATICAL HACKATHON

## Final Project README

> **Project Weight:** 100%  
> **Team Size:** 4/3 students  
> **Project Duration:** 8 hours  
> **Total Time Available:** 32 effort-hours per team  
> **Project Type:** Playful, interactive, technology-based experience

---

# Before you begin

## Fork and rename this repository

After forking this repository, rename it using the format:

`SKILLLAB_PROR-2026-TeamName`

### Example

`SKILLLAB_PROR-2026-AuroWizards`

Do not keep the default repository name.

---

# How to use this README

This file is your team’s **working project document**.

You must keep updating it throughout the build period.  
By the final review, this README should clearly show:

- your idea,
- your planning,
- your design decisions,
- your technical process,
- your build progress,
- your testing,
- your failures and changes,
- your final outcome.

## Rules

- Fill every section.
- Do not delete headings.
- If something does not apply, write `Not applicable` and explain why.
- Add images, screenshots, sketches, links, and videos wherever useful.
- Update task status and weekly logs regularly.
- Use this file as evidence of process, not only as a final report.

---

# 1. Team Identity

## 1.1 Studio / Group Name

<img width="1280" height="720" alt="picture " src="https://github.com/user-attachments/assets/6c1dd57c-a289-45a6-ad6e-6023d66f1ec9" />


---

## 1.2 Team Members

| Name               | Primary Role                             | Secondary Role        | Strengths Brought to the Project              |
| ------------------ | -----------------------------------------| --------------------- | -------------------------------------------- |
| Sakshi Gupta       | Electronics & Hardware Implementation    | System Integration    | Circuit Design, Embedded Systems, Debugging   |
| Kunal Dewangan     | Electronics & Software Development       | Fabrication           | Prototyping, Component Handling, Assembly     |
| Prisha Ale         | Electronics                              | Testing & connections | Clear Writing, Creativity, Presentation Skills|
| Shubham Kulkarni   | Documentation                            | Research & Planning   | Technical Writing, Organization, Analysis     |

---

## 1.3 Project Title

<img width="1536" height="1024" alt="track bot" src="https://github.com/user-attachments/assets/9f8d940d-ea44-42ad-9427-551a0479ecfe" />

Check out the working demo of our **Electronic Nose + Obstacle-Aware Smart Robot**:

[![Watch the Demo](https://img.youtube.com/vi/x_7ZoRCEao4/0.jpg)](https://youtube.com/shorts/x_7ZoRCEao4?feature=share)

## 1.4 One-Line Pitch

`A mobile robot that uses an electronic nose and obstacle-aware navigation to autonomously detect harmful gases, identify their type, and respond with real-time alerts.`

---

## 1.5 Expanded Project Idea

The project is a smart autonomous robot built using **Shrike Lite RP2040** that combines multiple sensing and response systems into one compact platform. The system uses an **electronic nose approach**, where multiple gas sensors (MQ2, MQ4, MQ7) work together to detect and differentiate gases such as smoke, LPG, methane, and carbon monoxide. Instead of relying on a single sensor, the system compares patterns across sensors to identify the type of gas present.

An **obstacle detection system** using an ultrasonic sensor ensures that the robot can safely navigate its environment without collisions. The robot continuously measures distance from nearby objects and adjusts its movement accordingly.

The **actuation system** includes a buzzer, RGB LEDs, and a servo motor. The servo rotates the sensor array to scan the surroundings like a radar system, helping identify the direction of gas concentration. LEDs indicate safety levels (green, yellow, red), while the buzzer provides alert signals based on danger level.

Together, the system creates an interactive experience where the robot can move through an environment, detect hazardous gases, identify them, avoid obstacles, and alert users — all autonomously. The project integrates embedded programming, sensor fusion, and real-time decision-making.

---

# 2. Philosophy Fit

## 2.1 Experience, Not Social Problem

This project focuses on creating an **interactive technological experience** rather than solving a large abstract social problem.

The robot acts as a **smart embedded artifact** that physically senses, processes, and reacts in real-time. Watching the robot move, scan its surroundings, change LED colors, and trigger alerts creates an engaging and dynamic demonstration of embedded systems in action.

It fits into the category of:
- Interactive machine  
- Kinetic artifact  
- Smart sensing system  

The experience of seeing a robot “sniff” the environment and respond to invisible threats makes the project both educational and engaging.

---

# 3. Inspiration

## 3.1 References

| Source Type | Title / Link | What Inspired You |
| ----------- | ------------ | ----------------- |
| Concept | Biological Olfaction (Human Nose) | Using multiple sensors to identify different smells (electronic nose concept) |
| Technology | MQ Sensor Datasheets (Winsen) | Understanding cross-sensitivity of gas sensors |
| Concept | SONAR / Radar Systems | Rotational scanning using servo motor |
| Practical | Industrial Gas Detectors | Inspired idea of detecting gas but making it mobile |

---

## 3.2 Original Twist

What makes this project original is the **combination of mobility, multi-gas detection, and directional sensing** in a single system.

Most gas detectors are static and detect only one type of gas. Most robots with obstacle avoidance do not detect environmental hazards.

This project combines both and adds a **servo-based scanning system**, allowing the robot to detect not only the presence of gas but also the direction of highest concentration.

Additionally, the use of **multiple gas sensors together (MQ2, MQ4, MQ7)** enables basic gas type identification, which is not possible with a single sensor.

The result is a robot that:
- Moves autonomously  
- Detects multiple gases  
- Identifies gas types  
- Avoids obstacles  
- Alerts users in real-time  

This transforms a simple detector into an **active hazard tracking system**.

---
# 4. Project Intent

## 4.1 User Journey 
Imagine a factory worker notices a faint smell near a storage room but isn't sure if it's dangerous or where it's coming from. Instead of walking in blind, he deploys the robot.
The robot powers on — the green LED lights up, confirming the system is ready. It begins moving forward through the corridor on its own. The HC-SR04 constantly watches ahead; when it spots a wall or object within 60 cm, the yellow LED flicks on, the robot slows, the servo starts sweeping left and right like a radar head, scanning for a clear path and simultaneously rotating the gas sensors to check all directions.
As it rounds the corner near the storage room, MQ2 and MQ4 readings spike. The robot immediately cross-checks the pattern — MQ2 high, MQ4 high, MQ7 low — and classifies it as an LPG leak. The red LED switches on. The buzzer fires a rapid repeating alarm. The servo locks onto the direction of highest concentration and holds there, pointing like a compass toward the source.
The worker, watching from a safe distance, sees the red light, hears the alarm, and knows exactly — gas detected, type identified, direction found. He can now take action without ever entering the hazardous zone himself.
 

                                                  |





# 5. Definition of Success

## 5.1 Definition of “Usable”
The project is considered usable when all three subsystems work together in real time without manual intervention:

The robot moves forward and avoids obstacles autonomously
At least one gas type (LPG, methane, or CO) is correctly detected and classified when introduced near the sensors
The correct LED colour activates and the buzzer sounds in response to the detected hazard level
The servo sweeps and holds direction during a scan cycle

If all four of these conditions are met simultaneously in a live test, the system is usable



## 5.2 Minimum Usable Version

What is the smallest version of this project that still delivers the core experience?

The smallest version that still delivers the core experience is:

MQ2 + MQ7 only (two sensors instead of three) detecting smoke and CO
HC-SR04 stopping the robot when an obstacle is detected — no servo sweep, just a full stop
Red LED + buzzer activating when gas threshold is crossed
Robot mounted on a static base (no motor drive) if chassis isn't ready — sensors, detection, and alerting still demonstrate the full concept

This version proves the electronic nose concept and the alert system even if mobility is incomplete.


## 5.3 Stretch Features

What features are nice to have but not essential?

Full servo radar sweep with directional gas concentration mapping (identifying which angle has the highest reading)
Differentiating buzzer beep patterns per gas type (e.g. slow beep for smoke, fast continuous for CO)
Serial/WiFi dashboard on laptop showing live MQ2, MQ4, MQ7 readings as a graph
Auto-return behaviour — robot reverses and halts in safe zone after detecting danger threshold
PPM estimation using sensor calibration curves for quantitative gas reporting


# 6. System Overview

## 6.1 Project Type

Check all that apply.

- [x] Electronics-based

- [ ] Mechanical

- [x] Sensor-based

- [ ] App-connected

- [x] Motorized

- [x] Sound-based

- [x] Light-based

- [ ] Screen/UI-based

- [x] Fabricated structure

- [ ] Game logic based

- [ ] Installation

- [ ] Other:

## 6.2 High-Level System Description

Explain how the system works in simple terms.

Include:

- input,
- processing,
- output,
- physical structure,
- app interaction if any.

**Response:**  

## 6.3 — Input / Output Map

| System Part | Type | What It Does |
|------------|------|-------------|
| **MQ2 Gas Sensor** | Analog Input | Detects smoke, LPG, and general combustible gases — outputs voltage proportional to concentration |
| **MQ4 Gas Sensor** | Analog Input | Detects methane (CNG) — higher sensitivity to CH₄ than MQ2 |
| **MQ7 Gas Sensor** | Analog Input | Detects carbon monoxide (CO) — most critical life-safety sensor in the array |
| **HC-SR04 Ultrasonic Sensor** | Digital Input | Measures distance to nearest obstacle — triggers stop, caution, or scan behaviour |
| **Microcontroller** | Processing | Reads all inputs, runs classification and obstacle logic, and drives all outputs |
| **Green LED** | Digital Output | Indicates safe state — no gas detected, path clear |
| **Yellow LED** | Digital Output | Indicates caution — moderate gas reading or obstacle in caution zone (30–60 cm) |
| **Red LED** | Digital Output | Indicates danger — gas threshold exceeded or obstacle in critical zone (< 30 cm) |
| **Buzzer** | Digital Output | Sounds alarm on danger detection — pattern varies by gas type |
| **Servo Motor** | PWM Output | Rotates sensor array (0–180°) for directional scanning during obstacle or gas events |
| **DC Drive Motors** | PWM Output | Propels robot forward, slows in caution zone, stops in critical zone |

# 7. Sketches and Visual Planning

## 7.1 Concept Sketch

## 🔗 Interactive Flowchart

View full diagram here:  
👉 https://app.eraser.io/workspace/5mr0YmXaqiqY6TQQ3xRs?origin=share&diagram=D9Y5CVfxsq_JOQrnAcpen

Add an early sketch of the full idea.
**Insert image below:**  
<img width="960" height="1280" alt="WhatsApp Image 2026-04-27 at 3 29 07 PM" src="https://github.com/user-attachments/assets/a92cefab-515e-4f6c-adb7-0fab73dd0bc6" />





## 7.2 Labeled Build Sketch

Add a sketch with labels showing:

- structure,
- electronics placement,
- user touch points,
- moving parts,
- output elements.

**Insert image below:**  
`[Upload image and link here]`
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/95637f31-b4e7-4427-a9e1-4b63fbeb0ac5" />

## 7.3 Approximate Dimensions

| Dimension        | Value   |
| ---------------- | ------- |
| Length           | `22 cm` |
| Width            | `16 cm` |
| Height           | `8 cm`  |
| Estimated weight | `750 g` |

---

## 8. Electronics Planning

### 8.1 Electronics Used

| Component                     | Quantity | Purpose                                      |
| ---------------------------- | -------- | -------------------------------------------- |
| Shrike Lite RP2040           | 2        | Main microcontroller (processing & control)  |
| MQ2 Gas Sensor               | 1        | Detect smoke, LPG, combustible gases         |
| MQ4 Gas Sensor               | 1        | Detect methane (CNG)                         |
| MQ7 Gas Sensor               | 1        | Detect carbon monoxide (CO)                  |
| HC-SR04 Ultrasonic Sensor    | 1        | Obstacle detection                           |
| Servo Motor (SG90)           | 1        | Rotate sensors for directional scanning      |
| L298N Motor Driver           | 1        | Control DC motors                            |
| BO Motors                    | 2        | Drive wheels (robot movement)                |
| Robot Chassis                | 1        | Base structure of the robot                  |
| Buzzer                       | 1        | Audio alert for gas detection                |
| LEDs (Red, Yellow, Green)    | 3        | Visual status indication                     |
| Resistors (220Ω)             | 3        | Current limiting & circuit stability         |
| Li-ion Battery Pack          | 1–2      | Power supply for entire system               |
| Jumper Wires                 | Multiple | Circuit connections                          |
| Breadboard / PCB             | 2        | Prototyping and circuit assembly             |

## 8.2 Wiring Plan

Describe the main electrical connections.
### 🔹 ADC (Analog Inputs)
- The **RP2040** provides **3 ADC pins only**:
  - `GP26`
  - `GP27`
  - `GP28`
- Suitable for analog sensors like:
  - MQ2 (Smoke)
  - MQ4 (Methane)
  - MQ7 (Carbon Monoxide)

---

### 🔹 Digital I/O Pins
- GPIO pins are labeled as:
  - `GP0` to `GP28`
- ⚠️ Note:
  - Unlike Arduino boards, pins are **not labeled as D2, D5, etc.**
  - Always use **GPIO numbering (GPx)**

---

### 🔹 PWM Support
- PWM is available on **almost all GPIO pins**
- Example:
  - Servo motor works on `GP9`

---

### 🔹 Voltage Logic (IMPORTANT ⚠️)
- The RP2040 operates on **3.3V logic**
- MQ sensors can output **up to 5V on AOUT**

#### ✔ Solution:
- Use a **voltage divider** or **level shifter**
- Protects the board from damage

---

### 🔹 Power & Programming
- **USB-C onboard**
- Used for:
  - Power supply
  - Code uploading

---

### ✅ Summary
| Feature | Details |
|--------|--------|
| ADC Pins | GP26, GP27, GP28 |
| GPIO Range | GP0–GP28 |
| PWM | Available on most pins |
| Logic Level | 3.3V |
| USB | USB-C (Power + Programming) |

## Pin Configuration Map

| Pin | Component | Signal Type | Direction |
|-----|----------|------------|-----------|
| **GP26 (ADC0)** | MQ2 AOUT | Analog | Input |
| **GP27 (ADC1)** | MQ4 AOUT | Analog | Input |
| **GP28 (ADC2)** | MQ7 AOUT | Analog | Input |
| **GP2** | MQ2 DOUT | Digital | Input |
| **GP3** | MQ4 DOUT | Digital | Input |
| **GP4** | MQ7 DOUT | Digital | Input |
| **GP5** | HC-SR04 TRIG | Digital | Output |
| **GP6** | HC-SR04 ECHO | Digital | Input |
| **GP9** | Servo SG90 PWM | PWM | Output |
| **GP10** | Red LED | Digital | Output |
| **GP11** | Yellow LED | Digital | Output |
| **GP12** | Green LED | Digital | Output |
| **GP13** | Buzzer (via NPN transistor) | Digital | Output |

## 8.3 Circuit Diagram

Insert a hand-drawn or software-made circuit diagram.

**Insert image below:**  
`[Upload image and link here]`
<img width="867" height="1156" alt="" src="" />


# 9. Power Plan

| Question | Response |
|----------|---------|
| **Power source** | Li-ion battery pack (2S, 7.4V nominal) |
| **Voltage for motors** | 5V via onboard VBUS from USB-C or direct Li-ion regulated output |
| **Voltage for RP2040** | 3.3V from onboard regulator |
| **Voltage for MQ sensors (heater)** | 5V from VBUS — each heater draws ~150 mA |
| **Voltage for servo** | 5V from VBUS — separate decoupled line with 100µF capacitor |
| **MQ AOUT to ADC** | 5V output stepped down to ~2.5V using 10kΩ + 10kΩ voltage divider before ADC pins |
| **Current concern** | All three MQ heaters draw ~450 mA total — ensure VBUS can handle this along with servo peak (~250 mA) |

---

### ⚠️ Safety Considerations

- Avoid over-discharging Li-ion battery below **3V per cell**
- Add a **1A polyfuse** on the 5V rail for protection
- Ensure all wiring is properly insulated using **heat shrink**
- Avoid exposed conductors, especially near **MQ sensor heater elements**
- Provide adequate ventilation around MQ sensors to prevent overheating

# 10. Software Planning

## 10.1 Software Tools

| Tool / Platform              | Purpose                                          |
|-----------------------------|--------------------------------------------------|
| Arduino (RP2040 Core)       | Programming and controlling Shrike Lite RP2040   |
| Serial Monitor              | Debugging sensor values and system behavior      |
| Embedded C/C++              | Writing logic for motors, sensors, and control   |

---

## 10.2 Software Logic

### Startup Behavior
The **Shrike Lite RP2040** initializes all required peripherals:
- GPIO pins (input/output)
- ADC channels (MQ2, MQ4, MQ7 gas sensors)
- PWM outputs (servo motor)
- Digital pins (HC-SR04 ultrasonic sensor, LEDs, buzzer, motor driver)

A **20-second warm-up delay** is applied to stabilize MQ gas sensors.  
The servo motor is set to **90° (center position)**, and the **Green LED** is turned ON to indicate system readiness.

---

### Input Handling
The system operates **fully autonomously**, without external communication.

Inputs are received from:
- **MQ2, MQ4, MQ7 gas sensors (analog inputs)**
- **HC-SR04 ultrasonic sensor (distance measurement)**

---

### Sensor Reading
The RP2040 continuously samples sensor data:

- **Gas Sensors (ADC):**
  - MQ2 → Smoke / LPG detection  
  - MQ4 → Methane detection  
  - MQ7 → Carbon Monoxide detection  
  - Read every **500 ms** with averaging  

- **Ultrasonic Sensor:**
  - Distance measured using trigger/echo pulse timing  
  - Read every **100 ms**

---

### Decision Logic

#### Gas Detection Logic
Sensor values are compared with predefined thresholds:
- MQ2 High → Smoke / LPG detected  
- MQ4 High → Methane detected  
- MQ7 High → CO detected (**highest priority**)  

#### Obstacle Detection Logic
Distance-based classification:
- **> 60 cm** → Safe zone  
- **30–60 cm** → Caution zone  
- **< 30 cm** → Critical zone  

#### Combined Decision Logic
- If obstacle detected → Stop and scan surroundings  
- If gas detected → Trigger alert system  
- If both occur → Prioritize **safety (stop + alert)**  

---

### Output Behavior

#### Motor Control
- Moves forward in safe conditions  
- Slows down in caution zone  
- Stops and reroutes in critical zone  

#### Servo Motor
- Rotates from **0° to 180°**
- Identifies:
  - Direction with maximum clearance  
  - Direction with highest gas concentration  

#### LED Indicators
- 🟢 Green → Safe  
- 🟡 Yellow → Warning  
- 🔴 Red → Danger  

#### Buzzer
- Activated during hazardous conditions  
- Pattern varies based on severity  

---

### Communication Logic
- No wireless communication is used  
- Internal communication via:
  - ADC (sensor data)
  - GPIO (digital signals)
  - PWM (servo control)

(Optional USB serial debugging)

---

### Reset Behavior
- System resets on power restart  
- If invalid readings occur → Motors stop (fail-safe)  
- Default state ensures **safe shutdown in error conditions**

---

## 10.3 Code Flowchart

![Flowchart](flowchart.png)

> 📌 Replace `flowchart.png` with your actual uploaded diagram in the repository.

---

### Flow Description
```text
Start
  ↓
Initialize RP2040 (GPIO, ADC, PWM)
  ↓
Warm-up MQ Sensors (20 sec)
  ↓
Set Servo to Center (90°)
  ↓
Loop Start
  ↓
Read MQ2, MQ4, MQ7 (ADC)
  ↓
Read Distance (Ultrasonic)
  ↓
Is Distance < 30 cm?
   ├── YES → Stop Motors
   │        → Perform Servo Scan (0–180°)
   │        → Find Best Direction
   │        → Turn Robot
   │
   └── NO
        ↓
   Is Distance < 60 cm?
        ├── YES → Slow Down + Yellow LED
        └── NO → Move Forward
  ↓
Classify Gas Type
  ↓
Is Hazard Detected?
   ├── YES → Activate Red LED + Buzzer
   └── NO → Green LED
  ↓
Update Outputs
  ↓
Repeat Loop
```

# 11. Bill of Materials

## 11.1 Full BOM

| Item | Quantity | In Kit? | Need to Buy? | Estimated Cost (INR) | Material / Spec | Why This Choice? |
|------|---------|---------|--------------|----------------------|------------------|------------------|
| Shrike Lite RP2040 | 1 | Yes | No | 0 | RP2040-based board | Main microcontroller for processing and control |
| Motor Driver | 1 | Yes | No | 0 | L298N Dual H-Bridge | To control both DC motors |
| DC Motors + Wheels | 2 | No | Yes | 150 | BO Motors + 6 cm wheels | Provides sufficient torque for movement |
| Li-ion Batteries + Holder | 1 | No | Yes | 200 | 2x 18650 cells | Portable and rechargeable power source |
| MQ2 Gas Sensor | 1 | Yes | No | 0 | LPG/Smoke sensor | Detects smoke and combustible gases |
| MQ4 Gas Sensor | 1 | Yes | No | 0 | Methane sensor | Detects methane (CNG) |
| MQ7 Gas Sensor | 1 | Yes | No | 0 | CO sensor | Detects carbon monoxide (critical gas) |
| Ultrasonic Sensor | 1 | Yes | No | 0 | HC-SR04 | Measures distance for obstacle avoidance |
| Servo Motor | 1 | Yes | No | 0 | SG90 180° servo | Enables directional scanning |
| Buzzer | 1 | Yes | No | 0 | Active buzzer | Provides audio alerts |
| LEDs (Red, Yellow, Green) | 3 | Yes | No | 0 | 5mm LEDs | Visual hazard indication |
| Resistors | 6 | Yes | No | 0 | 220Ω, 1kΩ | Current limiting and protection |
| Robot Chassis | 1 | No | Yes | 200 | Acrylic 2-wheel base | Structural support |
| Jumper Wires | 1 set | Yes | No | 0 | Male-Male wires | Circuit connections |
| Breadboard | 1 | Yes | No | 0 | Standard | Prototyping and testing |

## 11.2 Material Justification

The selection of components in this project was based on reliability, simplicity, cost-effectiveness, and suitability for real-time embedded sensing and control.

The **Shrike Lite RP2040** was chosen as the main microcontroller because it provides sufficient processing power, multiple ADC channels for sensor input, and PWM capabilities for motor and servo control. It also allows a fully self-contained embedded system without requiring external modules like WiFi.

**BO DC motors** were selected instead of servo or stepper motors because the robot requires continuous rotation for movement rather than precise positional control. These motors provide adequate torque, are low-cost, and are ideal for simple mobile robotic platforms.

The **L298N motor driver** was used to control the motors, as it supports bidirectional movement and speed control using PWM signals from the RP2040. It also allows safe interfacing between the motors and the microcontroller.

The **MQ2, MQ4, and MQ7 gas sensors** were chosen to implement an electronic nose system. Each sensor has different sensitivity characteristics, and together they enable basic gas classification (LPG, methane, carbon monoxide) using pattern-based detection instead of relying on a single sensor.

The **HC-SR04 ultrasonic sensor** was selected for obstacle detection due to its accuracy, low cost, and ease of integration. It enables real-time distance measurement, which is essential for collision avoidance.

A **servo motor (SG90)** is used to rotate the sensor assembly, allowing the robot to scan its surroundings. This adds directional awareness, helping the system identify both obstacle-free paths and areas of higher gas concentration.

The **LED indicators (red, yellow, green)** were included to provide simple and intuitive visual feedback for system status and hazard levels, while the **buzzer** provides an immediate audible alert in critical conditions.

The **Li-ion battery pack** was selected for portability and sufficient current supply, ensuring the system can operate independently without external power.

Overall, the chosen components balance functionality, cost, and ease of implementation, making the system effective for a hackathon-scale autonomous safety robot.


## 11.3 Items You Chose

| Item | Why Needed |
|------|-----------|
| BO Motors + Wheels | Drive system for robot movement |
| Li-ion Batteries + Holder | Portable power supply for entire system |
| Robot Chassis | Structural base to mount all components |
| Jumper Wires | Electrical connections between components |
| Breadboard | Prototyping and testing circuits |
| L298N Motor Driver | Control direction and speed of motors |
| MQ2 Gas Sensor | Detect smoke and LPG gases |
| MQ4 Gas Sensor | Detect methane gas |
| MQ7 Gas Sensor | Detect carbon monoxide (CO) |
| Ultrasonic Sensor (HC-SR04) | Obstacle detection and distance measurement |
| Servo Motor (SG90) | Rotates sensors for scanning environment |
| Buzzer | Audio alert system for hazards |
| LEDs (Red, Yellow, Green) | Visual indication of system status |

## 11.4 Budget Summary

| Budget Item           | Estimated Cost              |
| --------------------- | ---------------------------:|
| Electronics           | `[300]`                     |
| Mechanical parts      | `[350]`                     |
| Fabrication materials | `[0 (Available on campus)]` |
| Purchased extras      | `[0]`                       |
| Contingency           | `[250]`                     |
| **Total**             | `[900]`                     |

## 11.5 Budget Reflection

If the overall project cost needs to be reduced, several optimizations can be considered without significantly affecting functionality.

The **robot chassis** can be replaced with a low-cost or DIY alternative (cardboard, acrylic scrap, or 3D-printed parts available on campus), reducing mechanical expenses.

The **Li-ion battery pack** can be substituted with a **power bank** or shared between teams to avoid additional purchase costs.

Some components like **breadboard, jumper wires, and LEDs** can be reused from existing lab kits instead of purchasing separately.

If further cost reduction is required, the system can operate with **fewer gas sensors (e.g., using only MQ2)** for basic detection, though this will reduce gas classification accuracy.

The **servo motor** can also be removed in a simplified version, limiting the system to forward-only sensing instead of directional scanning.

Overall, the project is already cost-efficient, and most expenses are due to essential components like motors and power systems. With minor substitutions and shared resources, the total budget can be reduced further while maintaining core functionality.

# 12. Planning the Work

## 12.1 Team Working Agreement

Our team followed a collaborative and structured approach to complete the project efficiently within the given time.

Tasks were divided based on individual strengths.  
- **Sakshi Gupta** handled electronics and hardware implementation.  
- **Kunal Dewangan** focused on prototyping and fabrication.  
- **Prisha Ale** supported testing, wiring, and system connections.  
- **Shubham Kulkarni** managed documentation, research, and planning.  

All major decisions (component selection, circuit design, and logic flow) were made through group discussions to ensure everyone contributed and agreed before implementation.

Progress was checked regularly after completing each module such as sensor integration, motor setup, and coding. Small testing checkpoints helped identify and fix issues early.

If any task was delayed, responsibilities were adjusted dynamically. Other team members assisted in completing the task to ensure the overall project timeline was maintained.

Documentation was maintained alongside development. Notes on circuit design, code logic, and testing results were recorded continuously to avoid last-minute work and ensure a well-structured final report.

---

## 12.2 Task Breakdown

| Task ID | Task                          | Owner              | Estimated Hours | Status |
| ------- | ----------------------------- | ------------------ | ---------------:| ------ |
| T1      | Finalize project concept      | All                | 2               | Done   |
| T2      | Component selection & BOM     | Sakshi, Shubham    | 2               | Done   |
| T3      | Circuit design & wiring       | Sakshi             | 4               | Done   |
| T4      | Prototyping & assembly        | Kunal              | 4               | Done   |
| T5      | Sensor integration            | Sakshi, Prisha     | 3               | Done   |
| T6      | Coding & logic implementation | Sakshi             | 5               | Done   |
| T7      | Testing & debugging           | Prisha, All        | 4               | Done   |
| T8      | Final assembly                | Kunal              | 3               | Done   |
| T9      | Documentation & report        | Shubham            | 3               | Done   |

---

## 12.3 Responsibility Split

| Area                 | Main Owner        | Support Owner        |
| -------------------- | ----------------- | -------------------- |
| Concept              | All               | -                    |
| Electronics          | Sakshi Gupta      | Prisha Ale           |
| Coding               | Sakshi Gupta      | Kunal Dewangan       |
| Mechanical build     | Kunal Dewangan    | Prisha Ale           |
| Testing              | Prisha Ale        | All                  |
| Documentation        | Shubham Kulkarni  | All                  |

---

# 13. 2 hour Milestones

## 13.1 8-hour Plan

### Bi Hour 1 — Plan and De-risk

Expected outcomes:

- [x] Idea finalized
- [x] Core interaction decided
- [x] Sketches made
- [x] BOM completed
- [x] Purchase needs identified
- [ ] Key uncertainty identified
- [x] Basic feasibility tested

### Bi Hour 2 — Build Subsystems

Expected outcomes:

- [x] Electronics tests completed
- [ ] CAD / structure planning completed
- [ ] App UI started if needed
- [x] Mechanical concept tested
- [x] Main subsystems partially working

### Bi Hour 3 — Integrate

Expected outcomes:

- [x] Physical body built
- [x] Electronics integrated
- [x] Code connected to hardware
- [ ] App connected if required
- [x] First playable version exists

### Bi Hour 4 — Refine and Finish

Expected outcomes:

- [x] Technical bugs reduced
- [x] Playtesting completed
- [x] Improvements made
- [x] Documentation completed
- [x] Final build ready

## 13.2  Update Log

| Hour | Planned Goal | What Actually Happened | What Changed | Next Steps |
|------|-------------|----------------------|--------------|-----------|
| **Hour 1** | Finalise plan + test divider circuit | Finalised project architecture, checked all components, started basic sensor testing | Shifted focus from divider circuit to full sensor validation since multiple sensors were used | Complete individual sensor calibration and wiring |
| **Hour 2** | Test all subsystems individually | Tested MQ sensors, ultrasonic sensor, and motor driver separately; identified noise in sensor readings | Added averaging/filtering logic for stable readings | Integrate sensors with RP2040 and begin motor control testing |
| **Hour 3** | Full integration + first live run | Integrated sensors, motors, and servo; performed first full system test | Encountered unstable movement and delay issues → optimized code and wiring | Fix delays, improve response time, and refine logic |
| **Hour 4** | Tune + document + submit | Tuned thresholds, improved obstacle detection, finalized working demo; completed documentation | Reduced complexity by simplifying some logic for stability | Final testing, README upload, and submission |

---

# 14. Risks and Unknowns

## 14.1 Risk Register

| Risk                                                            | Type         | Likelihood | Impact   | Mitigation Plan                                                                       | Owner                |
| --------------------------------------------------------------- | ------------ | ---------- | -------- | ------------------------------------------------------------------------------------- | -------------------- |
| WiFi connection between laptop and ESP32 becomes unstable       | `Technical`  | `Medium`   | `High`   | Keep ESP32 close, ensure stable power supply, reduce network load, add fail-safe stop | `[Gopal]`           |


## 14.2 Biggest Unknown Right Now

The single biggest uncertainty in our project at this stage is the upgrade to LoRa communication and the optimization of the ultrasonic sensing system.

At present, our system works effectively at a short range using onboard processing and local communication. However, it is still unclear how reliably the system will perform in long-range or isolated environments once LoRa is integrated. Factors such as signal stability, data loss, and real-world transmission range under obstacles remain uncertain.

Additionally, the ultrasonic sensing aspect still has limitations in terms of accuracy and consistency under different environmental conditions. Improving its reliability for real-time obstacle detection and ensuring stable readings during robot movement is another key area that requires further testing and refinement.

---

# 15. Testing

## 15.1 Technical Testing Plan

| What Needs Testing        | How You Will Test It                                      | Success Condition |
|--------------------------|-----------------------------------------------------------|-------------------|
| Gas sensor readings (MQ2, MQ4, MQ7) | Expose sensors to smoke/lighter gas and observe values | Sensors show clear variation and correct gas detection |
| Ultrasonic sensor        | Place obstacles at different distances and measure output | Accurate distance measurement within expected range |
| Motor control            | Run motors forward, backward, and turning                 | Smooth and correct movement in all directions |
| Servo scanning           | Rotate servo from 0° to 180° and observe movement         | Smooth rotation and correct angle positioning |
| Obstacle avoidance logic | Place object in front and observe robot behavior          | Robot stops and changes direction correctly |
| Gas detection alert system | Trigger gas sensors and check LED + buzzer response     | Correct LED (green/yellow/red) and buzzer activation |
| Full system integration  | Run robot in real environment with obstacles + gas source | Robot detects gas and avoids obstacles simultaneously |

---

## 15.2 Testing and Debugging Log

| Date       | Problem Found                          | Type        | What You Tried                                      | Result   | Next Action |
|------------|----------------------------------------|------------|----------------------------------------------------|----------|-------------|
| 27th April | Unstable sensor readings               | Electrical | Applied averaging and filtering in code            | Worked   | Fine-tune thresholds |
| 27th April | Motors not responding properly         | Electrical | Checked wiring and motor driver connections        | Worked   | Secure wiring |
| 27th April | Servo jittering                        | Electrical | Provided stable power and adjusted PWM signal      | Improved | Optimize power supply |
| 27th April | Incorrect gas detection                | Software   | Adjusted threshold values and classification logic | Worked   | Test with more samples |
| 27th April | Robot not stopping near obstacle       | Software   | Fixed ultrasonic timing and logic conditions       | Worked   | Improve response speed |
| 27th April | Delay in system response               | Software   | Reduced delays and optimized loop                  | Improved | Further optimize code |

---

## 15.3 Playtesting Notes

| Tester        | What They Did                              | What Confused Them                     | What They Enjoyed                          | What You Will Change |
|---------------|--------------------------------------------|----------------------------------------|---------------------------------------------|----------------------|
| Sakshi        | Tested gas detection and obstacle handling | Delay in response at times             | Real-time gas detection + alert system      | Improve response speed |
| Kunal         | Drove robot through obstacles              | Servo movement seemed slow             | Obstacle avoidance behavior                 | Increase servo speed |
| Prisha        | Observed system alerts                     | LED indications not very distinct      | Buzzer alerts and visual feedback           | Improve LED clarity |
| Shubham       | Reviewed full system operation             | Slight inconsistency in detection      | Overall system integration                  | Fine-tune sensor thresholds |


# 16. Build Documentation

## 16.1 Fabrication Process

The fabrication process involved designing, cutting, assembling, fastening, wiring, and refining the physical structure and electronic system of the robot. Each stage was done carefully to ensure proper integration of mechanical and electronic components.

---

### Cutting
The base structure of the robot was made using a transparent acrylic sheet. The sheet was precisely cut according to the required chassis dimensions. Holes were drilled into the acrylic sheet to mount motors, the caster ball, and electronic components securely. This ensured proper alignment and stable fitting of all parts.

---

### Assembly
The mechanical assembly mainly included fixing the chassis structure, attaching the two DC motors, and mounting the caster ball for balance and movement. The wheels were attached to the motor shafts to complete the movement system of the robot.

---

### Fastening
All components were secured onto the acrylic chassis using screws, nuts, and mechanical mounts. Fastening was done in a way that allowed stability during movement while still keeping some parts accessible for future modifications or replacements.

---

### Wiring
The wiring process involved connecting all electronic components, including the Shrike (RP2040) board, L298N motor driver, ultrasonic sensor, servo motor, and gas sensors. Proper connections were made between control pins, power supply, and ground to ensure stable operation. Care was taken to avoid loose connections and ensure correct signal flow between modules.

## 16.2 Build Photos

<img width="1200" height="1600" alt="WhatsApp Image 2026-04-27 at 5 12 17 PM" src="https://github.com/user-attachments/assets/e28130bc-0d7e-4921-9b34-0845be5bb330" />
<img width="1200" height="1600" alt="WhatsApp Image 2026-04-27 at 5 12 23 PM (1)" src="https://github.com/user-attachments/assets/306762f9-b0a6-426a-acf0-1c2fab15119f" />
<img width="1200" height="1600" alt="WhatsApp Image 2026-04-27 at 4 52 36 PM" src="https://github.com/user-attachments/assets/422b79bc-48cc-4405-8642-1b4ec8e8594f" />






## 17. Final Outcome

---

### 17.1 Final Description
The final version of our project is a smart autonomous robot built using a Shrike (RP2040-based) controller. The robot is capable of detecting environmental conditions using multiple sensors and moving using a motor-driven chassis. It integrates gas detection, obstacle detection, and servo-based scanning using an ultrasonic sensor. The system processes real-time data and responds by controlling movement and providing environmental feedback.

---

### 17.2 What Works Well
The sensor system works effectively in detecting environmental changes. The gas sensors successfully detect variations in gas levels, and the ultrasonic sensor reliably measures distance for obstacle detection. The motor system allows controlled movement of the robot, and the servo motor enables directional scanning for better environmental coverage. Overall, the integration of sensors and movement provides a functional working prototype.

---

### 17.3 What Still Needs Improvement
The system can be improved by enhancing sensor accuracy and stability through better-quality industrial-grade sensors. The communication range can be extended using technologies like LoRa for long-distance data transmission instead of limited WiFi range. Additionally, power efficiency and battery life can be improved to support longer operational time. A more robust casing and optimized wiring would also increase durability for real-world deployment.

---

### 17.4 What Changed From the Original Plan
Initially, the project was planned as a simple stationary sensor-based system that only focused on detecting environmental parameters like gas or flame. However, during development, we enhanced the idea by integrating mobility into the system. We converted it into a moving robot capable of navigating its environment while collecting data. This upgrade significantly improved its functionality by allowing active monitoring instead of passive sensing, making the system more practical and impactful.
## 18.1 Team Reflection

### What did our team do well?
Shubham AND Sakshi managed firmware architecture and documentation efficiently, keeping the system modular so each subsystem could be tested independently. Kunal and Sakshi both handled hardware assembly with precision — the voltage divider soldering and servo mount were built cleanly under time pressure.Prisha tested all the components so that they do not create any obstacle during working of our model. The biggest time drain was the MQ sensor calibration: clean-air baseline values needed more time than anticipated. Tasks were divided effectively and communication was direct throughout the 8-hour session.
---

### What slowed us down?
connections and minor issues
---

### Time, Task, and Responsibility Management
We managed our tasks by clearly dividing responsibilities among team members, which improved efficiency. Although initial delays occurred due to hardware debugging and integration issues, we gradually improved coordination. Overall, task distribution was effective, and each member contributed actively to their assigned roles, which helped complete the project successfully.  


## 18.2 Technical Reflection

### Electronics
We learned about practical electronics by working with real components such as the Shrike (RP2040) board, L298N motor driver, ultrasonic sensor, servo motor, and gas sensors. We understood how power distribution, grounding, and voltage levels affect the stability of the entire system.

---

### Motor Driver and Sensors
We learned how a motor driver (L298N) acts as an interface between low-power microcontroller signals and high-power DC motors. We also explored how different sensors like ultrasonic and gas sensors convert physical signals into electrical data that can be processed by the controller.

---

### Coding
We gained experience in programming microcontrollers to control hardware components. This included writing logic for motor control, reading sensor values, and integrating multiple modules together to achieve real-time behavior in the robot system.

---

### Mechanisms
We learned how mechanical movement is achieved using DC motors and how a servo motor can be used for controlled rotation. We also understood how the physical structure of the robot affects movement stability and performance.

---

### Fabrication
We worked on assembling the robot chassis, mounting sensors, and securely fixing components. This helped us understand the importance of proper wiring, structural stability, and physical alignment in embedded systems.

---

### Integration
We learned how to integrate hardware and software components into a single working system. Combining sensors, actuators, and control logic allowed us to build a functional autonomous robot that responds to real-world inputs in real time.

### Motor Driver and Sensors
We learned how a motor driver (L298N) acts as an interface between low-power microcontroller signals and high-power DC motors. We also explored how different sensors like ultrasonic and gas sensors convert physical signals into electrical data that can be processed by the controller.

---

### Coding
We gained experience in programming microcontrollers to control hardware components. This included writing logic for motor control, reading sensor values, and integrating multiple modules together to achieve real-time behavior in the robot system.

---

### Mechanisms
We learned how mechanical movement is achieved using DC motors and how a servo motor can be used for controlled rotation. We also understood how the physical structure of the robot affects movement stability and performance.

---

### Fabrication
We worked on assembling the robot chassis, mounting sensors, and securely fixing components. This helped us understand the importance of proper wiring, structural stability, and physical alignment in embedded systems.

---

### Integration
We learned how to integrate hardware and software components into a single working system. Combining sensors, actuators, and control logic allowed us to build a functional autonomous robot that responds to real-world inputs in real time.


## 18.3 Design Reflection

What did you learn about:

- designing ,
- delight,
- clarity,
- physical interaction,
- understanding,
- iteration?

**Response:**  


## 18.4 If You Had One More hour

What would you improve next?

**Response:**  

` `

---

# 19. Final Submission Checklist

Before submission, confirm that:

- [x] Team details are complete
- [x] Project description is complete
- [x] Inspiration sources are included
- [x] Sketches are added
- [x] BOM is complete
- [x] Purchase list is complete
- [x] Budget summary is complete
- [x] Mechanical planning is documented if applicable
- [ ] App planning is documented if applicable
- [x] Code flowchart is added
- [x] Task breakdown is complete
- [x] Weekly logs are updated
- [x] Risk register is complete
- [x] Testing log is updated
- [x] Playtesting notes are included
- [x] Build photos are included
- [x] Final reflection is written
<img width="1131" height="1600" alt="image" src="" />

---


---


