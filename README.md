# NULL Motherboard

A custom carrier/motherboard PCB project designed around the **Raspberry Pi Zero 2 W**, using **KiCad 10**.

> **Status:** Design in progress. The PCB has not been fabricated or assembled.

## Project goal

The goal is to design a custom carrier board that makes the Raspberry Pi Zero 2 W easier to use as the core of a compact computer. The design work includes planning power input, connectors, GPIO access, mechanical mounting, and board layout.

This project is a carrier-board design. It is **not** an attempt to design the Raspberry Pi processor or the Zero 2 W module itself.

## Platform

- Raspberry Pi Zero 2 W
- KiCad 10
- Custom carrier PCB

## Current status

- [x] Raspberry Pi Zero 2 W selected as the platform
- [ ] Functional block diagram and requirements
- [ ] Power architecture and protection decisions
- [ ] GPIO and connector mapping
- [ ] Schematic capture
- [ ] PCB placement and routing
- [ ] ERC and DRC review
- [ ] BOM and fabrication files
- [ ] Physical assembly and testing

Only mark an item complete when the corresponding work has actually been reviewed.

## Technical documentation

- [Architecture and decision log](docs/architecture-and-decisions.md)

## Important design decisions still to make

- Power input method, protection, and current budget
- How the Pi Zero 2 W will connect mechanically to the carrier
- USB OTG and peripheral connector arrangement
- GPIO signals reserved for onboard functions
- Board dimensions, mounting holes, and connector placement

## Project history note

An earlier **Front Panel PCB** was designed separately and is archived. It is not automatically part of this Raspberry Pi carrier-board design. The new motherboard must be developed and validated independently.

## References

- [Raspberry Pi Zero 2 W product brief](https://datasheets.raspberrypi.com/rpizero2/raspberry-pi-zero-2-w-product-brief.pdf)
- [Raspberry Pi Zero documentation](https://www.raspberrypi.com/documentation/computers/zero.html)
- [Raspberry Pi hardware documentation](https://www.raspberrypi.com/documentation/computers/raspberry-pi.html)

## Safety and validation

A clean ERC or DRC report does not prove that a board is electrically safe or will work. Power, connector pinouts, clearances, and the finished assembly must be checked before applying power.

---
*Personal learning and hardware-design project by MrNullbyte01.*