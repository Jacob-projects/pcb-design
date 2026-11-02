# Voltage Divider

A simple KiCad voltage-divider project stored in `~/kicad-projects/voltage-divider-project/`. The project name is `voltage-divider`. This separate folder preserves the pre-existing `~/kicad-projects/voltage-divider/` directory.

## Circuit

- **J1, 5V IN:** pin 1 is `/+5V`; pin 2 is `/GND`.
- **R1:** 10 kΩ from `/+5V` to `/MID`.
- **R2:** 10 kΩ from `/MID` to `/GND`.
- **J2, VOUT:** pin 1 is `/MID`; pin 2 is `/GND`.

With a 5 V input and equal resistors, the ideal midpoint output is 2.5 V with no load. The output voltage will change under load according to the load impedance.

## PCB

The board is a 60 mm × 35 mm rectangular, two-layer design. All components are through-hole:

- J1 and J2 use 2-pin, 2.54 mm pin headers.
- R1 and R2 use horizontal axial DIN0207 resistor footprints with 10.16 mm lead spacing.
- The `/+5V`, `/MID`, and `/GND` tracks are routed on copper layers; the ground routing uses the back layer.

## Validation

Latest KiCad 10.0.7 checks:

- **ERC:** 0 errors, 0 warnings.
- **DRC:** 0 errors, 0 warnings, 0 unconnected items, and 0 schematic-parity findings.

Reports are in `voltage-divider.erc.json` and `voltage-divider.drc.json`.

## Files

- `voltage-divider.kicad_pro` — project settings.
- `voltage-divider.kicad_sch` — schematic.
- `voltage-divider.kicad_pcb` — routed PCB.
- `fab/voltage-divider-netlist.xml` — exported schematic netlist.
- `voltage-divider.erc.json` and `voltage-divider.drc.json` — validation reports.
- `voltage-divider.kicad_prl` — local KiCad settings file.
- `.backups/` — automatic backups created during editing.

## Open in KiCad

Open KiCad and choose **File → Open Project…**, then select:

`~/kicad-projects/voltage-divider-project/voltage-divider.kicad_pro`

From the KiCad project window, open the schematic or PCB editor using the corresponding project buttons.
