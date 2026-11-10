# Bill of Materials (BOM)

**Project:** Autonomous Object Tracking System (AOTS)  
**Revision:** v0.1 — November 10, 2026  
**Stage:** Parts selected; purchases, delivery, fit, and electrical tests not yet confirmed.

This document records the components selected for the initial two-axis camera-tracking prototype. **Selected** does not mean ordered, received, installed, or validated.

## Selected components

| ID | Category | Selected product | Quantity / package | Status | Notes |
| --- | --- | --- | --- | --- | --- |
| AOTS-001 | Microcontroller | Raspberry Pi Pico | 1 | **Already owned** | MicroPython; USB connection to MacBook |
| AOTS-002 | Pan/tilt actuators | Miuzei MG90S-style metal-gear positional servos | 4-pack (2 planned in assembly; spares) | Selected | Confirm positional 180° version and physical dimensions before final CAD |
| AOTS-003 | Servo PWM driver | AITRIP PCA9685 16-channel, 12-bit I²C board | 1 | Selected | Separate servo supply at V+; 3.3 V Pico logic |
| AOTS-004 | Servo power adapter | Facmogu regulated 5 V, 4 A AC/DC adapter | 1 | Selected | Advertised 5.5 × 2.5 mm center-positive plug; verify actual output/polarity |
| AOTS-005 | DC power lead | GGIPOWY 16 AWG DC5525 female 5.5 × 2.5 mm barrel-to-bare-wire, 0.8 ft | 3-pack | **Selected replacement** | Replaces earlier DC5521 (5.5 × 2.1 mm) option; check fit and polarity |
| AOTS-006 | Jumper wires | ELEGOO 120-piece Dupont jumper assortment | 1 kit | Selected | Confirm suitable connector genders/lengths |
| AOTS-007 | Fasteners | Fgruh 1,760-piece metric screw/nut assortment | 1 kit | Selected | Final thread sizes and lengths depend on CAD |
| AOTS-008 | Servo extensions | Apex RC 150 mm 3-pin servo extension cables | 5-pack | Selected | Check cable reach during assembly |
| AOTS-009 | Camera | Logitech USB webcam | 1 | Selected | Exact model not recorded; confirm macOS/OpenCV support, dimensions and mass |
| AOTS-010 | 3D printing filament | Polymaker PolyLite PLA, black, 1.75 mm, 1 kg | 1 spool | Selected | For Prusa MK4S; verify makerspace's approved filament policy |

## Purchase and validation checklist

- [ ] Confirm final cart quantities and variants; save product URLs/ASINs and actual prices.
- [ ] Confirm the servo is **positional**, not continuous-rotation.
- [ ] Confirm webcam model and mass before finalizing the tilt bracket.
- [ ] Complete UNC Charlotte FDM printer training and confirm permitted PLA.
- [ ] Verify the 5.5 × 2.5 mm barrel connection fits securely.
- [ ] With the PCA9685 disconnected, measure power lead output with a multimeter: approximately **+5 V DC** and correct polarity.
- [ ] Connect verified positive to PCA9685 **V+** and negative to **GND**; never assume wire color alone proves polarity.
- [ ] Power servo rail from the external 5 V supply; connect Pico 3.3 V to PCA9685 logic **VCC**, I²C SDA/SCL, and a common ground. Do not power servos from Pico 3.3 V.
- [ ] Test one servo first, then both; monitor supply stability and heating.
- [ ] Measure received servo and camera dimensions and update Fusion 360 mounts before printing.

## Scope and exclusions

- The **GGIPOWY DC5521 (5.5 × 2.1 mm)** cable was considered earlier but is **not** the selected final cable.
- **Polymaker HT-PLA** and **Polymaker ABS** were considered but **not selected**. The selected material is regular **PolyLite PLA**.
- A bearing-supported pan axis, buzzer, and other optional mechanical components remain **under design / not yet selected**.
- No prices, seller claims, confirmed delivery dates, or testing results are recorded without evidence.

## Engineering documentation

As parts arrive, update the status to **Ordered → Received → Measured → Tested → Integrated**, recording the date, measured dimensions, datasheet, and any substitutions. Store purchase screenshots privately when they contain account or order information; add only non-sensitive product references to this public repository.

See [README.md](README.md) for the project overview and [CAD/](CAD/) for the initial base plate design.
