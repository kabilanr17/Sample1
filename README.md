# DC to DC Buck Converter

This project implements a **DC-DC Buck Converter** using the LM2596S-ADJ regulator. It is designed to step down a higher DC voltage to a lower DC voltage efficiently using switching regulation.

## 🧩 Components Used

| Component      | Value/Part No.   | Description                        |
|----------------|------------------|------------------------------------|
| U1             | LM2596S-ADJ      | Adjustable Buck Regulator IC       |
| D1             | 1N5822           | Schottky Diode for flyback         |
| L1             | 470 µH           | Inductor for switching circuit     |
| C1             | 100 µF           | Input filter capacitor              |
| C2             | 100 nF           | Input bypass capacitor              |
| C3             | 220 µF           | Output filter capacitor             |
| C4             | 100 nF           | Feedback filter capacitor           |
| R1             | 10 kΩ (103)      | Voltage divider for feedback        |
| R2             | 330 Ω            | Current limiting for diode          |
| J2/J3          | Conn_01x01       | Power input connectors              |
| J4/J5          | Conn_01x01       | Power output connectors             |

## 🔧 Working Principle

The LM2596S-ADJ is a step-down switching regulator capable of driving 3A load with excellent line and load regulation. The feedback pin (FB) and voltage divider (R1) are used to set the output voltage.

The inductor (L1) and output capacitor (C3) smooth out the pulsating DC output of the switching regulator. The Schottky diode (D1) provides a path for inductor current when the switch inside LM2596 is off.

## ⚙️ How to Use

1. **Input Voltage**: Connect a DC voltage (e.g., 12V) to the input pins (J2, J3).
2. **Output Voltage**: The output is available at pins J4, J5.
3. Adjust R1 (or add a potentiometer in series) to set the desired output voltage.
4. Ensure proper heat sinking for the LM2596 if output current exceeds 1.5A continuously.
