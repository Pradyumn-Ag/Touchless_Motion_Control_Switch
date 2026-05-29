# Touchless Motion Control Switch with CD4017 ✋⚡

## 📝 Project Overview
[cite_start]This project is a Touchless Motion Control Switch designed for the Electronic Devices and Circuits Lab (NECC209)[cite: 7, 13]. [cite_start]The system operates by detecting motion using an infrared (IR) sensor, which triggers a CD4017 decade counter IC[cite: 15]. [cite_start]This allows the circuit to control a relay or LED, toggling appliances on or off without physical contact[cite: 16].

[cite_start]**Team Members (Group 08):** [cite: 8]
* [cite_start]Pradyumn Agrawal [cite: 9]
* [cite_start]Poli Hitesh Reddy [cite: 10]

## 🎥 Working Demonstration
You can view the working video of the hardware prototype in our Google Drive folder:
👉 **[Watch the Demonstration Video](https://drive.google.com/drive/folders/1h1LWQVSgBJHF3x3ekIg_NyHnviaalaBU)**

## ⚙️ Working Principle
The circuit's operation is broken down into the following stages:

1. **Motion Detection:** An IR emitter sends out infrared light. [cite_start]When motion occurs in its path, the reflected light changes, prompting the IR detector to send a signal[cite: 18, 19].
2. [cite_start]**Signal Processing:** An LM358 IC acts as a comparator/amplifier to process the sensor's signal[cite: 21]. [cite_start]Upon detecting a change, it sends a trigger to a BC547 transistor[cite: 23]. 
3. **Current Amplification:** The IR sensor and LM358 provide small currents. [cite_start]The BC547 transistor acts as a switch to drive higher current components like the relay[cite: 24].
4. [cite_start]**Sequential Control:** The CD4017 is a 7-output decade counter[cite: 26]. [cite_start]It receives the pulse from the motion detection circuit and sequentially increments its active output[cite: 28]. [cite_start]This determines whether the connected device is powered on or off[cite: 29].
5. [cite_start]**Output Stage:** The triggered CD4017 output energizes a 5V SPDT relay to switch external AC devices (like a fan or light), or it can directly toggle indicator LEDs[cite: 31].

## 🛠️ Components Used
* [cite_start]**ICs & Transistors:** CD4017 IC, LM358 IC, BC547 Transistor [cite: 42, 43, 44]
* [cite_start]**Sensors:** IR LED pair (Detector & Emitter) [cite: 51]
* [cite_start]**Relay & Diodes:** 5V SPDT Relay, 1N4007 Diode (for flyback protection) [cite: 40, 52, 53]
* [cite_start]**Capacitors:** 100uF 25V, 1000uF 25V (for power smoothing and noise filtration) [cite: 35, 36, 45, 46]
* [cite_start]**Resistors:** 220-ohm (0.25W) x4, 10k (0.25W), 10k Trimmer (to fine-tune sensor threshold) [cite: 37, 38, 47, 48, 49]
* [cite_start]**Indicators:** 5mm LEDs x2, Bulb [cite: 50, 85]
* [cite_start]**Misc:** Breadboard, Connecting Wires [cite: 54]

## 🔌 Circuit Diagram
*(Upload your screenshot of the circuit diagram to your repository and ensure it is named `circuit_diagram.png` for this image to appear)*

![Circuit Diagram](./circuit_diagram.png)

## 💡 Practical Applications
* [cite_start]**Touchless Switches:** Interfaces with 110V/220V AC appliances, improving hygiene in bathrooms, kitchens, or smart homes without expensive automation systems[cite: 87, 89, 90].
* [cite_start]**Energy Conservation:** Can be configured to automatically shut off devices when a person leaves a specific area[cite: 91].
* [cite_start]**Security Alarms:** Acts as a perimeter alert, triggering a siren when the IR beam is interrupted[cite: 92, 93].
* [cite_start]**Industrial Safety Barriers:** Detects if hands enter dangerous zones in workshops, using the relay to instantly cut machine power[cite: 94].
* [cite_start]**Public Hygiene:** The underlying LM358 and BC547 detection principle is identical to the logic used in automatic hand sanitizer and soap dispensers[cite: 95, 96].
