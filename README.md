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

### power pcb
- +24V mount pad not connected to +24V rail.
- GND mount pad not connected to ground planes.
- The measure line of the Kistler torque sensor cannot be pulled to ground. A
  fix requires the removal of transistor Q2 and the measure line to be connected
  to the collector end of transistor Q1. This bypasses and disables switch S1.
