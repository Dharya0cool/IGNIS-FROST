# Ignis Frost 🚀❄️

I designed **Ignis Frost** from scratch because I wanted a real, reliable flight computer for my model rockets instead of a fragile breadboard full of loose jumper wires. 

The name comes from the extreme contrast a rocket faces during launch: blistering engine heat at liftoff (*Ignis*) meeting freezing air high up in the atmosphere (*Frost*). Everything is packed onto a single compact circuit board built to fit inside a rocket airframe and survive the stress of flight.

## What It Does
* **Tracks Altitude Live:** Uses a BMP390 barometric pressure sensor to measure climb rate and height down to centimeters.
* **Senses Motion:** An onboard 6-axis IMU tracks acceleration and tilt throughout boost, coast, and descent.
* **Logs Flight Data:** Saves telemetry (`CSV`) to onboard storage so I can pull the data after landing and graph the flight curve.
* **Deploys the Parachute:** Automatically detects the exact second the rocket hits apogee (peak height) and triggers a MOSFET switch to fire the parachute ejection charge.

## Hardware Specs
* **Brain:** ESP32-C3-MINI-1
* **Barometer:** BMP390
* **Motion Sensor (IMU):** 6-Axis Accelerometer & Gyroscope
* **Power & Recovery:** 3.3V LDO Regulator + N-Channel MOSFET Ejection Circuit
* **Designed In:** KiCad 8

## What's in This Repo
* `/hardware` — KiCad schematic, PCB layout, and Gerber files for manufacturing
* `/bom` — Full parts list and sourcing links
* `/firmware` — Flight control, sensor filtering, and data-logging code
<img width="1532" height="697" alt="2" src="https://github.com/user-attachments/assets/e702c57b-3a1b-4c82-9f90-392da05ef858" />

<img width="1532" height="697" alt="4" src="https://github.com/user-attachments/assets/90ceacea-327c-4d2c-88e1-e2b4da3e9d4d" />

<img width="1530" height="699" alt="5" src="https://github.com/user-attachments/assets/80ed268e-625f-41c4-83f0-583e76e7dd21" />

<img width="1335" height="732" alt="6" src="https://github.com/user-attachments/assets/4a271b20-9d7f-4b25-86af-63a044afa443" />

<img width="1327" height="729" alt="7" src="https://github.com/user-attachments/assets/439c4fc9-cd91-43a7-9f4c-058658c88a23" />

<img width="1325" height="728" alt="8" src="https://github.com/user-attachments/assets/3a567ed4-5a00-4268-a059-405465ef0cc6" />



