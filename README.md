# Autonomous Object Tracking System

**Status:** Planning and initial mechanical design — no physical prototype or validated tracking results yet.

## Overview
An independent mechanical engineering and robotics project to design, fabricate, and evaluate a low-cost desktop, two-axis pan/tilt object-tracking platform. A camera will detect a moving object, a host computer will calculate tracking error, and a Raspberry Pi Pico will command servo movement. Initial demonstrations will use a camera and/or LED indicator rather than a laser.

## Engineering objectives
- Design an original, parametric pan/tilt assembly in Autodesk Fusion 360.
- Select actuators based on payload mass, geometry, and torque calculations.
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

## Planned tools and hardware
| Category | Planned tools/components |
| --- | --- |
| CAD | Autodesk Fusion 360; STEP exports and technical drawings |
| Fabrication | 3D printing; filament type to be confirmed with printer operator |
| Controller | Raspberry Pi Pico (already owned) |
| Actuation | Two micro servos (model not yet selected/purchased) |
| Vision | USB camera or available webcam; Python and OpenCV |
| Electronics | External servo supply, wiring, fasteners |

**Note:** Component specifications, dimensions, and cost estimates are provisional until parts and printer compatibility are verified.

## Repository structure
- `CAD/` — source/design exports and engineering drawings
- `Firmware/` — Pico MicroPython firmware
- `Computer-Vision/` — host-side Python/OpenCV software
- `Calculations/` — torque, loading, tolerances, and engineering analysis
- `Documentation/` — requirements, decisions, assembly notes, and revision history
- `Testing/` — test procedures, datasets, plots, and results
- `Images/` — CAD screenshots, prototype photos, and demo media

## Development roadmap
- [ ] Define measurable requirements and select camera/servo specifications
- [ ] Design initial base and pan/tilt components in Fusion 360
- [ ] Verify clearances, travel limits, and actuator loading
- [ ] Fabricate and assemble first prototype
- [ ] Demonstrate manual pan/tilt control
- [ ] Implement camera-based autonomous object tracking
- [ ] Measure and improve tracking performance
- [ ] Publish final CAD, drawings, test data, and demonstration

## Current progress
Repository initialized. Initial mechanical design is the next milestone. No CAD files, hardware assembly, or test results have been completed or uploaded yet.

## Documentation principles
Design files and test results will be labeled by revision. Planned features will not be presented as completed work. Only original work or files approved for public sharing will be published.
