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
