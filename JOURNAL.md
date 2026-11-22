**Ignis Frost — Build Journal**

***Total Time Spent: ~7 hours***

November 14, 2026 — Schematic & Picking Parts (4 hours)
Finished the full schematic in KiCad. I went with the ESP32-C3-MINI-1 because it's small enough for a 40 mm × 40 mm board and already has a built-in PCB antenna.
For flight telemetry, I paired a BMP280 barometer (for tracking altitude and catching apogee) with an LSM6DS3 6-axis IMU over I2C, powered by a 2-pin JST-PH battery connector so a small LiPo can plug straight in without loose jumper wires rattling around inside the rocket airframe.

<img width="1335" height="732" alt="6" src="https://github.com/user-attachments/assets/18881ad6-979d-4d44-a415-c6a5b996a478" />

<img width="1327" height="729" alt="7" src="https://github.com/user-attachments/assets/3783ac44-9b4a-4160-9790-eace74fb6769" />

<img width="1325" height="728" alt="8" src="https://github.com/user-attachments/assets/e72cea46-28d4-4df3-8b6c-ef6bf81de3ad" />




November 17, 2026 — PCB Routing, DRC Clearance, & Manufacturing Prep (3 hours)
Today was all about turning the schematic into an actual board I can build. After figuring out track widths and how to handle ground, I jumped straight into routing.
I hand-routed all 28 nets between the ESP32-C3-MINI-1 (U1), LSM6DS3 IMU (U2), BMP280 barometer (U3), and JST-PH battery connector (J1) using 0.15 mm–0.25 mm traces, keeping everything neat without tight bottlenecks. I flooded the bottom copper layer (B.Cu) as a solid GND plane so the circuit has a clean return path and some extra shielding.
I ran a Design Rule Check to catch any clearance, spacing, or silkscreen slip-ups and got it down to zero errors and zero unrouted nets. After that, I generated the Gerbers (-FCu, -BCu, -FMask, -BMask, -FSilkscreen, -EdgeCuts) along with the plated and non-plated .drl drill files, packed them into Ignis-Frost-Gerbers.zip, and got the files set for fabrication and the Hack Club hardware grant submission.

<img width="1530" height="699" alt="5" src="https://github.com/user-attachments/assets/d90053e4-4074-40c1-adb7-71b1e6e49b91" />

<img width="1532" height="697" alt="4" src="https://github.com/user-attachments/assets/bd4903c4-2c72-42af-b312-88d32e5dbeb5" />




November 20, 2026 — Grant BOM, Power & Soldering Setup [1 hour]
Today I pulled the grant BOM together so I can actually source the parts and put the board together on my bench here in India (230V / 50Hz mains where needed). I locked in the 10-component core PCB BOM at ₹678.11 (~$7.31 USD).
I also checked soldering and test gear—a 60W temperature-controlled soldering kit with LED helping hands (₹1,399), a Koptal brass tip cleaner (₹257), and an APTECH DEALS 2000-count digital multimeter (₹269)—while skipping the pricey ₹5,978 silicone mat so I have room left for PCB fabrication and rework flux/wick.

<img width="1233" height="667" alt="Capture" src="https://github.com/user-attachments/assets/81b2fcac-747c-40b5-ad11-564c437f0ca9" />

<img width="1598" height="820" alt="09" src="https://github.com/user-attachments/assets/ed55e551-fa70-4ed6-95a7-cb3677affc6d" />

                                                                            -------END--------


