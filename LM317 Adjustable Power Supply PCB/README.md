# 🔌 LM317 Adjustable Voltage Regulator – PCB

A compact adjustable linear voltage regulator PCB based on the LM317 (SOT-223 package).  
Designed to provide a stable, adjustable DC output voltage for embedded systems, testing setups, and general-purpose power applications.

---

## 📌 Overview

This project implements an LM317 adjustable voltage regulator with improved ripple rejection and output stability.

The output voltage can be adjusted using a potentiometer connected to the ADJ pin.

---

## ⚙️ Key Features

- Input Voltage Range: 7V – 30V DC  
- Adjustable Output Voltage: ~1.25V to Vin − 3V  
- Output Current: Up to 1A (with proper heat dissipation)  
- Built-in Current Limiting & Thermal Shutdown (LM317 internal)  
- Adjustable Output via 5k Potentiometer  
- Ripple Rejection Capacitor (10µF at ADJ)  
- Reverse Protection Diode  

---

## 🧠 Working Principle

The LM317 maintains a constant 1.25V reference between the Output and Adjust pins.

Output Voltage Formula:

\[
V_{out} = 1.25 \times \left(1 + \frac{R2}{R1}\right)
\]

Where:

- R1 = 240Ω  
- R2 = Potentiometer value  

By rotating the potentiometer, R2 changes and adjusts the output voltage.

---

## 📐 Design Specifications

| Parameter        | Value              |
|------------------|-------------------|
| PCB Size         | Custom Compact Layout |
| Layers           | 2                 |
| Copper Thickness | 1 oz              |
| Regulator Package| SOT-223           |
| Potentiometer    | 5kΩ               |

---

## 🔧 Circuit Components

- LM317 (SOT-223)
- R1 = 240Ω
- RV1 = 5k Potentiometer
- C1 = 1µF (Output)
- C2 = 10µF (Adjust)
- C3 = 0.1µF (Input)
- D1 = 1N4002 (Protection Diode)

---

## 🖥️ Schematic

![Schematic](ASSETS/output.pdf)

---

## 🧾 PCB Layout

Design considerations:

- Short trace between LM317 and capacitors  
- Wide traces for current path  
- Ground plane for stability  
- Thermal copper area under SOT-223  

![PCB Layout](ASSETS/layout.png)

---

## 🔥 Thermal Considerations

Since this is a linear regulator:

Power Dissipation:

\[
P = (V_{in} - V_{out}) \times I
\]

Example:

If:
- Vin = 12V  
- Vout = 5V  
- I = 1A  

Then:

\[
P = (12 - 5) \times 1 = 7W
\]

⚠ Heatsinking or copper area is mandatory for high current operation.

---

## 📦 Manufacturing Files

all in manufacturing folder

Compatible with JLCPCB, PCBWay, and standard Gerber manufacturers.

---

## 🧪 Testing & Validation

HAVEN'T DONE THAT 

---

## 🚀 Future Improvements

- Add reverse polarity protection at input  
- Add output LED indicator  
- Add current limiting resistor  
- Replace with switching regulator for higher efficiency  

---

## 📁 Project Structure
