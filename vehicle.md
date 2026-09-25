# 4-Way Powertrain Telemetry Comparison (10-100 mph)

This document tracks a full-throttle acceleration sweep at 10 mph increments from 10 to 100 mph. It highlights four completely different automotive engineering philosophies:
1. **The Diesel Hot Hatch:** Volkswagen Golf Mk7.5 GTD (2.0L I4 Turbo-Diesel)
2. **The Plug-in Hybrid SUV:** Land Rover Defender P400e (2.0L I4 PHEV)
3. **The Mild-Hybrid V8 Off-Roader:** Land Rover Defender OCTA (4.4L Twin-Turbo V8 MHEV)
4. **The Performance Hybrid Supercar:** Porsche Turbo S 992.2 (3.6L Flat-Six T-Hybrid)

---

## The Telemetry Matrix

| Speed | Golf Mk7.5 GTD <br>*(184 hp / 380 Nm)* | Defender P400e <br>*(404 hp / 640 Nm)* | Defender OCTA <br>*(635 hp / 750 Nm)* | Porsche Turbo S (992.2) <br>*(711 hp / 800 Nm)* |
| :--- | :--- | :--- | :--- | :--- |
| **10 mph** | 90 hp / 380 Nm / **1st** / 1,800 | 220 hp / 640 Nm / **1st** / 2,500 | 350 hp / 750 Nm / **1st** / 3,300 | 420 hp / 800 Nm / **1st** / 2,300 |
| **20 mph** | 145 hp / 380 Nm / **1st** / 2,500 | 315 hp / 640 Nm / **1st** / 3,500 | 520 hp / 750 Nm / **1st** / 4,950 | 580 hp / 800 Nm / **1st** / 4,000 |
| **30 mph** | 184 hp / 350 Nm / **1st** / 3,800 | 404 hp / 640 Nm / **1st** / 5,500 | 635 hp / 750 Nm / **1st** / 6,000 | 711 hp / 800 Nm / **1st** / 6,500 |
| **40 mph** | 130 hp / 380 Nm / **2nd** / 2,000 | 320 hp / 640 Nm / **2nd** / 3,600 | 480 hp / 750 Nm / **2nd** / 4,500 | 520 hp / 800 Nm / **2nd** / 3,800 |
| **50 mph** | 170 hp / 380 Nm / **3rd** / 3,200 | 390 hp / 620 Nm / **2nd** / 5,200 | 610 hp / 750 Nm / **2nd** / 5,800 | 711 hp / 800 Nm / **2nd** / 6,500 |
| **60 mph** | 184 hp / 320 Nm / **3rd** / 4,000 | 330 hp / 580 Nm / **3rd** / 4,000 | 500 hp / 750 Nm / **3rd** / 4,700 | 560 hp / 800 Nm / **3rd** / 4,200 |
| **70 mph** | 140 hp / 280 Nm / **4th** / 2,200 | 385 hp / 550 Nm / **3rd** / 5,000 | 590 hp / 750 Nm / **3rd** / 5,600 | 711 hp / 800 Nm / **3rd** / 6,500 |
| **80 mph** | 165 hp / 280 Nm / **4th** / 3,000 | 325 hp / 510 Nm / **4th** / 4,500 | 510 hp / 750 Nm / **4th** / 4,800 | 590 hp / 800 Nm / **4th** / 4,500 |
| **90 mph** | 180 hp / 260 Nm / **5th** / 3,800 | 360 hp / 480 Nm / **4th** / 5,300 | 580 hp / 740 Nm / **4th** / 5,500 | 711 hp / 800 Nm / **4th** / 6,500 |
| **100 mph** | 150 hp / 230 Nm / **5th** / 4,200 | 340 hp / 440 Nm / **5th** / 5,500 | 635 hp / 720 Nm / **5th** / 6,000 | 640 hp / 800 Nm / **5th** / 5,200 |

---

## Architectural Insights

* **The Porsche PDK Precision:** The 911 Turbo S targets **6,500 RPM** perfectly across multiple gears. The tight, close-ratio steps of the 8-speed PDK keep the high-voltage performance hybrid locked into its lethal peak performance envelope.
* **The Defender Mirroring Gearing:** The P400e and OCTA have completely different engines but utilize closely paired variants of ZF 8-speed automatic gearboxes. Notice how their gear shifts occur at identical speed points, though the OCTA operates with a massive displacement power advantage.
* **The Diesel Drop-off:** The Golf GTD punches hard early with **380 Nm of torque** at low speeds. However, because diesel engines struggle to breathe effectively at high RPM, its torque falls off sharply down to **230 Nm** by 100 mph, requiring the car to short-shift early.
