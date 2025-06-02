# Project Report: Design and Development of a Motorized Assistive Cart

## 1. Introduction

This report presents the systematic design, development, and implementation of a motorized assistive cart project. The objective was to create a compact and user-friendly device capable of assisting individuals with moderate loads while navigating inclines and uneven surfaces. The system integrates mechanical, electrical, and control engineering principles, focusing on efficiency, safety, and cost-effectiveness.

## 2. Project Objectives

* Develop a motorized cart powered by a 24V, 400W brushless DC motor.
* Ensure smooth speed control, reliable torque output, and user safety.
* Design a complete electronic system including battery management, motor control, and user interface.
* Implement a functional schematic and Bill of Materials (BoM).

## 3. Requirements Analysis

* **Load Capacity:** Up to 80 kg
* **Speed:** Target range of 4–6 km/h
* **Slope Handling:** Up to 6 degrees
* **Battery Runtime:** Minimum 30 minutes of continuous use
* **Control Interface:** Thumb throttle and emergency stop
* **Safety Features:** Overcurrent, reverse polarity, and overvoltage protection

## 4. System Architecture

The design was broken down into three subsystems:

* **Mechanical Subsystem:** Includes the DC motor, gearbox, and frame mounting
* **Electrical Subsystem:** Includes motor driver, battery pack, throttle, microcontroller, and protection devices
* **Control Subsystem:** Includes feedback regulation via Hall sensors and PWM signal processing

## 5. Component Selection

### 5.1 Motor

* **Model:** Transmotec B86112-24
* **Specs:** 24V, 400W, 3200 RPM, 20A peak current

### 5.2 Battery

* **Type:** Li-ion 7S3P
* **Specs:** 24V, 30Ah, integrated BMS

### 5.3 Motor Driver

* **IC:** TMC2160A-TATQFP48-EP
* **Features:** StealthChop, SpreadCycle, high-current capability

### 5.4 Microcontroller

* **Model:** ESP32-WROVER-IE-N16R8
* **Features:** Dual-core, Wi-Fi, Bluetooth, 16MB Flash

### 5.5 Power Regulation

* LM2596 (5V output)
* AP2112 (3.3V output)

### 5.6 Safety Components

* Fuse: 10A fast-blow
* Schottky Diodes: Reverse polarity protection
* TVS Diodes: Voltage spike protection

### 5.7 User Interface

* Thumb throttle with LED voltage display
* Emergency stop switch

## 6. Functional Design

* **Throttle Signal Processing:** Reads voltage and converts it to PWM
* **Motor Speed Feedback:** Via Hall-effect sensors integrated in the motor
* **Control Logic:** Regulates PWM to maintain desired speed
* **Emergency Stop:** Immediately cuts off power to motor driver

## 7. Schematic Design

The complete schematic was developed in KiCad. It includes all power, logic, and signal connections with appropriate test points, labels, and mounting options. Special attention was given to voltage levels, trace widths, and grounding techniques.

## 8. Bill of Materials (BoM)

A comprehensive BoM was generated, listing:

* All components
* Package types
* Voltage/current ratings
* Function in the circuit
* Justifications
* Supplier pricing data

## 9. Risk Analysis

A Design-FMEA (D-FMEA) was conducted, identifying key risks such as motor overload, power loss, and user error. Mitigating measures were implemented via hardware protection and control logic redundancies.

## 10. Testing and Validation

* Simulated full load operation and speed variation
* Verified PWM response to throttle input
* Confirmed protection circuit responses (fuse, diode clamping)
* Measured voltage drop across shunt resistors for current sensing

## 11. Challenges

* Converting schematic to Eagle-compatible format due to XML limitations
* Ensuring compatibility between connectors and power lines
* Matching motor specifications with available battery configurations

## 12. Conclusion

The motorized assistive cart project successfully met its design goals, including motor control, user safety, and functional stability. All major subsystems were integrated and validated through simulations and schematic analysis. Future steps include PCB layout, physical prototyping, and firmware development.

## 13. Appendices

* Final Schematic Diagram (PDF)
* Updated BoM (Excel)
* D-FMEA Table
* Datasheets for major components
