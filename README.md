This set of PCBs are designed to use with various projects in the
[phobos](https://github.com/oliverlee/phobos) repository.

## Bill of Materials
The bill of materials is maintained [here](https://docs.google.com/spreadsheets/d/1CJe4dBAEXy64Y3e8YSP1X_Nll6x3aowWz7-QJbUk4VQ/edit?usp=sharing)

It may be out of date so take a look at it carefully.

## Errata
### v0.1
### mc pcb
- Description for solder jumper switch S3 on silkscreen layer is reversed.
- Description for solder jumper switch S4 on silkscreen layer is reversed.
- SDIO CMD line missing pullup resistor. A 33k resistor can be added at EXT1
  connecting pins 5 and 11. The leads must be kept as short as possible to
  minimize overshoot and ringing.

### power pcb
- +24V mount pad not connected to +24V rail.
- GND mount pad not connected to ground planes.
- The measure line of the Kistler torque sensor cannot be pulled to ground. A
  fix requires the removal of transistor Q2 and the measure line to be connected
  to the collector end of transistor Q1. This bypasses and disables switch S1.
- Description for solder jumper switch S2 on silkscreen layer is reversed.
- Silkscreen on J1, J3 incorrect: WIND1 and WIND2 reversed.
- Trace for HALL2_S2 between Ext3 and J3 is completely missing.
