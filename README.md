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

| Question         | Response                                                                                                                                          |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Power source     | `Battery (Li-ion pack)`                                                                                                                           |
| Voltage required | `~6–8.4V for motors (via driver), stepped down to 5V for ESP32 (buck converter)`                                                                  |
| Current concerns | `Motors can draw high current under load, which may cause voltage drops affecting ESP32 and WiFi stability`                                       |
| Safety concerns  | `Avoid over-discharging Li-ion batteries, ensure proper voltage regulation, prevent short circuits, and secure wiring to avoid loose connections` |

---

# 10. Software Planning

## 10.1 Software Tools

| Tool / Platform                | Purpose                                        |
| ------------------------------ | ---------------------------------------------- |
| `[MicroPython]`                | `Control ESP32`                                |
| `[Python/PyGame/OpenCV]`       | `Track markers, game logic, create projection` |
| `[Fusion/Blender/Illustrator]` | `[Prototyping structure]`                      |
|                                |                                                |

## 10.2 Software Logic

Describe what the code must do.

Include:

- startup behavior,
- input handling,
- sensor reading,
- decision logic,
- output behavior,
- communication logic,
- reset behavior.

**Response:**  
`

- **Startup behavior:**  
  The ESP32 initializes motor pins, PWM control, and starts a WiFi access point with a web server. The laptop initializes camera input, tracking system, and projection mapping.
- **Input handling:**  
  Movement commands are received from the laptop (pygame sends http requests)
- **Sensor reading:**  
  The camera continuously captures frames, and OpenCV detects ArUco markers to determine the car’s position and orientation.
- **Decision logic:**  
  The system maps the car’s position into a virtual coordinate system and checks for nearby obstacles or collisions. If movement is valid, the command is allowed; if not, it is blocked or replaced with a feedback action (like a slight shake).
- **Output behavior:**  
  The ESP32 drives the motors using PWM signals to control speed and direction. The projector displays the updated game environment, including obstacles, targets, and feedback visuals.
- **Communication logic:**  
  The laptop sends HTTP requests (e.g., `/forward`, `/left`) to the ESP32 over WiFi. The ESP32 parses these commands and executes motor actions.
- **Reset behavior:**  
  If no command is received within a short timeout, the ESP32 stops the motors. The game resets when a level is completed or restarted.`

## 10.3 Code Flowchart

Insert a flowchart showing your code logic.

Suggested sequence:

- start,
- initialize,
- wait for input,
- read input,
- decision,
- trigger output,
- repeat or reset,
- error handling.

**Insert image below:**  
<img width="1600" height="1200" alt="image" src="" />
<img width="1600" height="1200" alt="image" src="" />




# 11. Bill of Materials

## 11.1 Full BOM

| Item                             | Quantity | In Kit? | Need to Buy? | Estimated Cost | Material / Spec               | Why This Choice?          |
| -------------------------------- | --------:| ------- | ------------ | --------------:| ----------------------------- | ------------------------- |
| `[ESP32]`                        | `1`      | `Yes`   | `No`         | `0`            | `38 Pin ESP32`                | `[To control components]` |
| `[Motor Driver]`                 | `[1]`    | `[Yes]` | `[No]`       | `0`            | `[LN296]`                     | `[To drive both motors]`  |
| `[DC Motors and wheel]`          | `[2]`    | `[No]`  | `[Yes]`      | `[150]`        | `[BO Motors and 6 cm wheels]` | `[high torque motors]`    |
| `[Buck Converter]`               | `[1]`    | `[No]`  | `[Yes]`      | `[75]`         |                               |                           |
| `[Li-ion batteries with holder]` | `[1]`    | `[No]`  | `[Yes]`      | `[200]`        |                               |                           |

## 11.2 Material Justification

Explain why you selected your main materials and components.

**Response:**  
`DC motors (BO motors) were chosen instead of servos or steppers because the system requires continuous rotation for movement rather than precise angular control (Previously, we were considering using steppers as we were planning on tracking movement on the ESP using its relative position from an origin, but since we're using a camera now, this is not required). A motor driver (L298N) was used to allow bidirectional control and speed variation using PWM.`


## 11.3 Items You chose

| Item                 | Why Needed               | Purchase Link | Latest Safe Date to Procure | Status       |
| -------------------- | ------------------------ | ------------- | --------------------------- | ------------ |
| `BO Motors + Wheels` | `Drive system for car`   | `robu.in`     | `15th April`                | `[Received]` |
| `Buck Converter`     | `Stable power for ESP32` | `local store` | `before testing`            | `[Received]` |
| `Li-ion Batteries`   | `Portable power`         | `local store` | `before testing`            | `Recieved`   |

## 11.4 Budget Summary

| Budget Item           | Estimated Cost              |
| --------------------- | ---------------------------:|
| Electronics           | `[400]`                     |
| Mechanical parts      | `[200]`                     |
| Fabrication materials | `[0 (Available on campus)]` |
| Purchased extras      | `[0]`                       |
| Contingency           | `[300]`                     |
| **Total**             | `[900]`                     |

## 11.5 Budget Reflection

If your cost is too high, what can be simplified, removed, substituted, or shared?

**Response:**  

---

# 12. Planning the Work

## 12.1 Team Working Agreement

Write how your team will work together.

Include:

- how tasks are divided,
- how decisions are made,
- how progress will be checked,
- what happens if a task is delayed,
- how documentation will be maintained.

**Response:**  


## 12.2 Task Breakdown

| Task ID | Task                    | Owner    | Estimated Hours | Deadline     | Dependency | Status |
| ------- | ----------------------- | -------- | ---------------:| ------------ | ---------- | ------ |
| T1      | `[Finalize concept]`    | `[Both]` | `2`             | `1st April`  | `None`     | `Done` |


## 12.3 Responsibility Split

| Area                 | Main Owner | Support Owner |
| -------------------- | ---------- | ------------- |
| Concept              | `[Gopal]`  | `[Kader]`    |
| Electronics          | `[]`       | `[]`     |
| Coding               | `[]`       | `[]`     |
| Mechanical build     | `[]`       | `[]`    |
| Testing              | `[]`       | `[]`    |
| Documentation        | `[]`       | `[]`     |

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

| Week   | Planned Goal   | What Actually Happened | What Changed   | Next Steps     |
| ------ | -------------- | ---------------------- | -------------- | -------------- |
| Week 1 | `[Write here]` | `[Write here]`         | `[Write here]` | `[Write here]` |
| Week 2 | `[Write here]` | `[Write here]`         | `[Write here]` | `[Write here]` |
| Week 3 | `[Write here]` | `[Write here]`         | `[Write here]` | `[Write here]` |
| Week 4 | `[Write here]` | `[Write here]`         | `[Write here]` | `[Write here]` |

---

# 14. Risks and Unknowns

## 14.1 Risk Register

| Risk                                                            | Type         | Likelihood | Impact   | Mitigation Plan                                                                       | Owner                |
| --------------------------------------------------------------- | ------------ | ---------- | -------- | ------------------------------------------------------------------------------------- | -------------------- |
| WiFi connection between laptop and ESP32 becomes unstable       | `Technical`  | `Medium`   | `High`   | Keep ESP32 close, ensure stable power supply, reduce network load, add fail-safe stop | `[Gopal]`           |


## 14.2 Biggest Unknown Right Now

What is the single biggest uncertainty in your project at this stage?

**Response:**  


---

# 15. Testing 

## 15.1 Technical Testing Plan

| What Needs Testing     | How You Will Test It                                                                 | Success Condition                                                                                    |
| ---------------------- | ------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `[Wifi connection]`    | `[Check if motor spins via app button]`                                              | `[Both motors accurately respond to wifi signals]`                                                   |
                       |
## 15.2 Testing and Debugging Log

| Date          | Problem Found                         | Type         | What You Tried                                | Result               | Next Action                                    |
| ------------- | ------------------------------------- | ------------ | --------------------------------------------- | -------------------- | ---------------------------------------------- |
| `18th April`  | `Car not balancing properly`          | `Mechanical` | `Add low-friction caster support to one side` | `Worked`             | `improve caster structure`                     |


## 15.3 Playtesting Notes

| Tester      | What They Did                        | What Confused Them                    | What They Enjoyed                         | What You Will Change                          |
| ----------- | ------------------------------------ | ------------------------------------- | ----------------------------------------- | --------------------------------------------- |
| `Gopal` | `Tried navigating through obstacles` | `Some obstacles ewren't clear enough` | `Liked projection + real car interaction` | `Add a slight red highlight around obstacles` |


---

# 16. Build Documentation

## 16.1 Fabrication Process

Describe how the project was physically made.

Include:

- cutting,
- 3D printing,
- assembly,
- fastening,
- wiring,
- finishing,
- revisions.

**Response:**  
`The fabrication process involved designing, manufacturing, assembling, and refining both the physical structure and electronic integration of the system.`

`Design (CAD Modeling):
The initial model was created using CAD software, where components were designed based on the actual dimensions of the electronic parts. This ensured accurate fitting and minimized errors during assembly.
Cutting (Laser Cutting):
The designed parts were fabricated using laser cutting techniques. Sheets were cut precisely according to the CAD model to create the structural base and mounts for components.`

`Components were fixed using adhesives and mechanical supports. Certain parts were intentionally kept modular (not permanently fixed) to allow easy replacement and modification of electronics.
Surface Finishing:
Some parts were sanded to smooth rough edges after cutting. Sawdust mixed with adhesive was used to fill gaps and uneven edges, improving structural finish. The final structure was then painted for better aesthetics and durability.`

`Environment Setup (Dark Room Fabrication):
To enhance projection visibility, a controlled dark environment was created using Z-boards, paper sheets, and bedsheets. This minimized external light interference and improved projection clarity.
Revisions and Iterations:
Multiple adjustments were made throughout the process, including refining alignment, improving structural stability, repositioning components, and optimizing the interaction between the physical car and projected environment.`

## 16.2 Build Photos

Add photos throughout the project.

Suggested images:

- early sketch,
- prototype,
- <img width="960" height="1280" alt="WhatsApp Image 2026-04-24 at 9 46 02 AM (1)" src="https://github.com/user-attachments/assets/74baa570-5770-483e-be6d-d2f03386e37c" 
- electronics testing,
- mechanism test,
- app screenshot,
- final build.
- <img width="960" height="1280" alt="WhatsApp Image 2026-04-24 at 9 46 02 AM (1)" src="https://github.com/user-attachments/assets/74baa570-5770-483e-be6d-d2f03386e37c" />





# 17. Final Outcome

## 17.1 Final Description

Describe the final version of your project.

**Response:**  


## 17.2 What Works Well



## 17.3 What Still Needs Improvement


## 17.4 What Changed From the Original Plan

How did the project change from the initial idea?

**Response:**  


---

# 18. Reflection

## 18.1 Team Reflection

What did your team do well?  
What slowed you down?  
How well did you manage time, tasks, and responsibilities?

**Response:**  


## 18.2 Technical Reflection

What did you learn about:

- electronics,
- coding,
- mechanisms,
- fabrication,
- integration?

**Response:**  


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


