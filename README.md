# Touchless Motion Control Switch with CD4017 ✋⚡

## 📝 Project Overview
This project is a Touchless Motion Control Switch designed for the Electronic Devices and Circuits Lab (NECC209). The system operates by detecting motion using an infrared (IR) sensor, which triggers a CD4017 decade counter IC. This allows the circuit to control a relay or LED, toggling appliances on or off without physical contact.

## 🎥 Working Demonstration
You can view the working video of the hardware prototype in my Google Drive folder:
👉 **[Watch the Demonstration Video](https://drive.google.com/drive/folders/1h1LWQVSgBJHF3x3ekIg_NyHnviaalaBU)**

## ⚙️ Working Principle
The circuit's operation is broken down into the following stages:

1. **Motion Detection:** An IR emitter sends out infrared light. When motion occurs in its path, the reflected light changes, prompting the IR detector to send a signal.
2. **Signal Processing:** An LM358 IC acts as a comparator/amplifier to process the sensor's signal. Upon detecting a change, it sends a trigger to a BC547 transistor. 
3. **Current Amplification:** The IR sensor and LM358 provide small currents. The BC547 transistor acts as a switch to drive higher current components like the relay.
4. **Sequential Control:** The CD4017 is a 7-output decade counter. It receives the pulse from the motion detection circuit and sequentially increments its active output. This determines whether the connected device is powered on or off.
5. **Output Stage:** The triggered CD4017 output energizes a 5V SPDT relay to switch external AC devices (like a fan or light), or it can directly toggle indicator LEDs.

## 🛠️ Components Used
* **ICs & Transistors:** CD4017 IC, LM358 IC, BC547 Transistor
* **Sensors:** IR LED pair (Detector & Emitter)
* **Relay & Diodes:** 5V SPDT Relay, 1N4007 Diode (for flyback protection)
* **Capacitors:** 100uF 25V, 1000uF 25V (for power smoothing and noise filtration)
* **Resistors:** 220-ohm (0.25W) x4, 10k (0.25W), 10k Trimmer (to fine-tune sensor threshold)
* **Indicators:** 5mm LEDs x2, Bulb
* **Misc:** Breadboard, Connecting Wires

## 🔌 Circuit Diagram
*(Upload your screenshot of the circuit diagram to your repository and ensure it is named `circuit_diagram.png` for this image to appear)*

![Circuit Diagram](./circuit_diagram.png)

## 💡 Practical Applications
* **Touchless Switches:** Interfaces with 110V/220V AC appliances, improving hygiene in bathrooms, kitchens, or smart homes without expensive automation systems.
* **Energy Conservation:** Can be configured to automatically shut off devices when a person leaves a specific area.
* **Security Alarms:** Acts as a perimeter alert, triggering a siren when the IR beam is interrupted.
* **Industrial Safety Barriers:** Detects if hands enter dangerous zones in workshops, using the relay to instantly cut machine power.
* **Public Hygiene:** The underlying LM358 and BC547 detection principle is identical to the logic used in automatic hand sanitizer and soap dispensers.
