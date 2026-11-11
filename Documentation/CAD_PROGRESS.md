# AOTS CAD development log

## November 10, 2026 — Base plate
- Designed a rounded rectangular base plate with four mounting holes in Fusion 360.
- Documented initial Fusion design and STEP AP242 export in the repository.
- **Pending:** dimension checks, mounting hole fit, manufacturing review.

## November 11, 2026 — Pan/tilt layout
- Modeled a rectangular pan-servo mounting collar and established its rigid relationship to the base.
- Modeled a nominal 60 mm diameter, 4 mm thick circular pan platform.
- Modeled a pair of upright tilt-support brackets and established a rigid CAD relationship with the platform.
- Imported a Tower Pro MG90S servo reference model to examine packaging and shaft alignment.
- Selected/ordered MG90S-class servos; purchased hardware has not yet been physically verified.

### Open engineering questions
1. How will the pan servo be mechanically secured through its mounting tabs?
2. How will the pan platform attach to the servo horn, and is independent bearing support required?
3. Where will the tilt servo and opposite pivot be mounted?
4. What are the camera's actual dimensions, mass, and center of gravity?
5. What servo torque margin, clearances, fasteners, and motion limits are needed?
6. How will the two revolute joints be defined and tested in Fusion 360?

### Next steps
- Model and verify servo horn/platform fastening.
- Complete pan and tilt revolute joints and a camera cradle.
- Check collisions and rotation limits.
- Measure delivered components before committing to fabrication.
- Upload updated original CAD exports and screenshots when ready.

### Reference
[GrabCAD pan-tilt servo bracket assembly with Eachine 1000 camera](https://grabcad.com/library/pan-tilt-servo-bracket-assembly-with-eachine-1000-camera-1) — mechanical inspiration, not a blueprint.

**Status:** CAD work in progress. No fabricated assembly, physical tests, or tracking accuracy measurements yet.
