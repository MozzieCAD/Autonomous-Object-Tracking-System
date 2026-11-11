# CAD file organization

This directory contains original AOTS mechanical designs and exports.

## Organization
- **Existing files in `CAD/`** — retained in place to preserve links and revision history.
- **`Assembly/`** — place future full pan/tilt assembly exports (`.f3z` when linked Fusion designs require an archive, or `.step` for neutral geometry).
- **`Components/`** — place future individual original component source files and STEP exports.
- **`../Images/`** — place assembly screenshots and prototype photos; GitHub accepts PNG and JPG images.

GitHub does not track empty directories. The `Assembly/` and `Components/` folders will appear once their first files are committed.

## Suggested filenames
- `AOTS_Pan_Tilt_Assembly_v1.f3z` or `.step`
- `AOTS_Pan_Servo_Mount_v1.step`
- `AOTS_Pan_Platform_v1.step`
- `AOTS_Tilt_Support_Bracket_v1.step`

Use the actual design revision and export format; do not rename or move existing files just to match these suggestions.

## Export notes
- STEP AP242 is suitable for geometry exchange, but does not replace editable Fusion 360 design history.
- Confirm external linked components are included when exporting an assembly.
- Keep third-party CAD references separate and check redistribution rights before committing them.
- Do not claim dimensional validation or fit testing until real hardware is measured and tested.
