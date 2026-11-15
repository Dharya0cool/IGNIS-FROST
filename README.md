# IGNIS-FROST
**Ignis Frost** is a custom-designed, open-source rocket avionics flight computer built from scratch to handle the thermal extremes of high-altitude flight—from blistering launch propulsion (*Ignis*) to sub-zero upper-atmospheric air (*Frost*).

Instead of fragile breadboards or loose jumper wires, Ignis Frost packs real-time telemetry, flight logging, and parachute recovery control onto a single compact PCB engineered to fit inside a model rocket airframe.

## Core Functions
* **Real-Time Altitude Tracking:** Uses a high-precision barometric pressure sensor to measure climb rate and altitude changes down to centimeters.
* **6-Axis Motion Sensing:** Tracks acceleration, pitch, roll, and yaw throughout boost, coast, and descent phases.
* **High-Speed Flight Data Logging:** Records flight telemetry (`CSV`) to onboard storage for post-flight curve analysis.
* **Autonomous Apogee Recovery:** Detects peak altitude and safely triggers a MOSFET deployment switch to eject the parachute at the exact top of the trajectory.

## Hardware Architecture
* **Microcontroller:** ESP32-C3-MINI-1
* **Barometer:** BMP390 High-Precision Pressure Sensor
* **IMU:** 6-Axis Accelerometer & Gyroscope
* **Power & Recovery:** 3.3V LDO Regulator + N-Channel MOSFET Ejection Circuit
* **CAD / EDA Tool:** KiCad 8

## Repository Structure
* `/hardware` — KiCad schematic (`.kicad_sch`), PCB layout (`.kicad_pcb`), and Gerber fabrication files
* `/bom` — Bill of Materials and component sourcing list
* `/firmware` — Flight control, Kalman filtering, and data-logging code
