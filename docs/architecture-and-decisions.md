# NULL Motherboard — Architecture & Decision Log

This document tracks design choices for the Raspberry Pi Zero 2 W carrier PCB. Decisions remain **proposed** until reviewed in the schematic and validated against official documentation.

## System boundary

The Raspberry Pi Zero 2 W remains the compute module. This project designs a carrier PCB around it; it does not recreate the SoC, memory, Wi-Fi, or the module's internal circuitry.

## Functional blocks to plan

- Raspberry Pi Zero 2 W mounting / 40-pin connection
- Power input and protection
- USB OTG access and peripheral connection
- GPIO expansion / optional onboard interfaces
- Mechanical mounting, board outline, and connector access

## Open decisions

| Decision | Status | What must be checked |
|---|---|---|
| Power input | Open | 5 V source, current budget, protection, connector |
| Pi connection | Open | Header/socket choice, orientation, keep-outs |
| USB OTG | Open | Connector, routing, host/device use |
| GPIO allocation | Open | Pin functions, 3.3 V logic, reserved pins |
| Board outline | Open | Module dimensions, mounting holes, cable access |
| Expansion | Open | Which features are actually required |

## Design rules

1. Do not assume a GPIO pin is 5 V tolerant.
2. Do not feed power into multiple Pi power inputs without understanding the power path.
3. Check the official pinout and mechanical drawings before assigning footprints.
4. Keep high-current power paths short and sized appropriately.
5. Review ERC and DRC, then independently inspect the schematic and PCB.

## Decision log

Add dated entries below. Include the reason, alternatives, and verification source.

| Date | Decision | Reason / evidence | Status |
|---|---|---|---|
| TBD | Raspberry Pi Zero 2 W as compute platform | Project scope | Selected |

## Official references

- [Raspberry Pi Zero 2 W product brief](https://datasheets.raspberrypi.com/rpizero2/raspberry-pi-zero-2-w-product-brief.pdf)
- [Raspberry Pi Zero documentation](https://www.raspberrypi.com/documentation/computers/zero.html)
- [Reduced schematics](https://datasheets.raspberrypi.com/rpizero2/raspberry-pi-zero-2-w-reduced-schematics.pdf)

*This is a planning document, not an approved electrical design.*