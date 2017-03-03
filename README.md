This set of PCBs are designed to use with various projects in the
[phobos](https://github.com/oliverlee/phobos) repository. The PCBs are designed
to be used with the following items:
- [OLIMEX STM32-H405](https://www.olimex.com/Products/ARM/ST/STM32-H405/)
- [Maxon ESCON Module 50//5](http://www.maxonmotor.com/maxon/view/product/control/4-Q-Servokontroller/438725)

## Bill of Materials
The bill of materials is maintained [here](https://docs.google.com/spreadsheets/d/1CJe4dBAEXy64Y3e8YSP1X_Nll6x3aowWz7-QJbUk4VQ/edit?usp=sharing)

It may be out of date so take a look at it carefully.

## Notes
- In order to use the SDIO peripheral, R27 on the OLIMEX STM32-H405 must be
  disconnected from from the SDIO_CMD line (EXT1-11). This can be done by
  cutting the trace connecting EXT1-11 and R27.

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
- J1, J3 molex pins can not withstand motor windings 1,2,3 current. Motor windings cable must be connected directly to motor dive.
- J1, J2 male molex vertical headers must be changed with right hand headers to allow motor drive fit to EXT2 & EXT1.