# Autonomous Object Tracking System (AOTS)

**Status (November 11, 2026):** Mechanical CAD assembly in progress. Initial base plate files have been documented in the repository; pan/tilt components are being modeled in Fusion 360. Hardware has been ordered but has not yet been assembled or tested.

## Overview
An independent mechanical engineering and robotics project to design, fabricate, and evaluate a low-cost desktop, two-axis pan/tilt object-tracking platform. A camera will detect a moving object, a host computer will calculate tracking error, and a Raspberry Pi Pico will command servo movement. Initial demonstrations will use a camera and/or LED indicator rather than a laser.

## Engineering objectives
- Design an original, parametric pan/tilt assembly in Autodesk Fusion 360.
- Select and evaluate actuators based on payload mass, geometry, and torque calculations.
- Create manufacturable 3D-printed parts, assembly models, and engineering drawings.
- Implement manual servo movement before autonomous tracking.
- Use Python and OpenCV for camera-based object detection and tracking.
- Evaluate tracking accuracy, response time, vibration, and repeatability.
- Document iterations, failures, design decisions, and measured results.

## Planned architecture
1. **Camera:** captures images of a colored test object.
2. **MacBook (Python + OpenCV):** detects the object and calculates its image-space position.
3. **USB serial connection:** sends movement commands to the Pico.
4. **Raspberry Pi Pico (MicroPython):** controls two servos.
5. **Custom pan/tilt mechanism:** positions the camera.

The servos will use a suitable external regulated power supply, with a common ground shared with the Pico.

## Tools and hardware
| Category | Current selection or plan |
| --- | --- |
| CAD | Autodesk Fusion 360; editable design files and STEP AP242 exports |
| Fabrication | 3D printing planned; material and printer compatibility pending |
| Controller | Raspberry Pi Pico (already owned) |
| Actuation | MG90S-class metal-gear micro servos ordered; physical dimensions and performance not yet verified |
| Vision | Camera and Python/OpenCV tracking planned |
| Electronics | External regulated servo supply, wiring, and mechanical fasteners; integration pending |

**Important:** The imported Tower Pro MG90S CAD model is a *reference* for packaging. The purchased servos may differ in geometry. Physical fit, shaft/horn interface, torque margin, electrical requirements, and camera payload must be checked before fabrication.

## Repository structure
- `CAD/` — editable Fusion 360 designs and neutral exports; see [CAD organization](CAD/README.md)
  - `CAD/Assembly/` — future complete assembly exports
  - `CAD/Components/` — future individual component exports
- `Firmware/` — Pico MicroPython firmware
- `Computer-Vision/` — host-side Python/OpenCV software
- `Calculations/` — torque, loading, tolerances, and engineering analysis
- `Documentation/` — requirements, decisions, assembly notes, and revision history
- `Testing/` — test procedures, datasets, plots, and results
- `Images/` — CAD screenshots, prototype photos, and demo media

Folders for future files may not appear in GitHub until they contain committed files. Existing CAD files are intentionally left at their current paths to avoid breaking links.

## Development roadmap
- [ ] Finalize measurable requirements and verify camera/servo specifications
- [x] Create and export initial base plate CAD model (Fusion 360 and STEP AP242)
- [x] Model initial pan servo collar, pan platform, and dual tilt support brackets
- [x] Establish rigid CAD relationships between stationary mount/base and platform/bracket subassembly
- [ ] Complete servo fastening, horn connections, pan/tilt revolute joints, and camera cradle
- [ ] Verify clearances, travel limits, fastener fit, and actuator loading
- [ ] Fabricate and assemble first prototype
- [ ] Demonstrate manual pan/tilt control
- [ ] Implement camera-based autonomous object tracking
- [ ] Measure and improve tracking performance
- [ ] Publish final CAD, drawings, test data, and demonstration

## Current progress
**Milestone 1 — Initial base plate CAD (November 10, 2026):** Modeled a rounded rectangular base plate with four through-holes in Fusion 360. Initial source and STEP AP242 exports are documented as `CAD/AOTS_Base_Plate_v1.f3d` and `CAD/AOTS_Base_Plate_v1.step`. Geometry is not yet validated for manufacturing.

**Milestone 2 — Pan/tilt mechanical layout (November 11, 2026):** Modeled a pan servo mounting collar, a nominal 60 mm diameter × 4 mm thick circular pan platform, and two upright tilt support brackets. Set up rigid CAD assembly relationships and imported an MG90S servo reference model to study positioning. The pan shaft-to-platform connection, tilt axis, servo mounting fasteners, camera cradle, and complete motion simulation remain unfinished. These newer CAD models are work in progress; their publication in the repository has not been verified.

**Next milestone:** Finish the mechanical drive interfaces and camera cradle, verify the real servos' dimensions when parts arrive, and evaluate clearances and servo loading before fabrication. No physical prototype or tracking performance results are available yet.

For more detail, see [CAD progress notes](Documentation/CAD_PROGRESS.md).

## Design references
- [GrabCAD pan-tilt bracket assembly with Eachine 1000 camera](https://grabcad.com/library/pan-tilt-servo-bracket-assembly-with-eachine-1000-camera-1) — inspiration only; not a copied design.
- A third-party Tower Pro MG90S CAD reference was imported for layout study. Redistributing third-party CAD requires checking its license.

## Documentation principles
Design files and test results will be labeled by revision. Planned features will not be presented as completed work. Only original work or files approved for public sharing will be published.
