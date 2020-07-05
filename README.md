# SPICE Simulation Repository

A collection of design simulations used for determining components for circuit
design. Preferred SPICE tool is LTspice by Linear Technology, which is free and
fully functional without any restriction on components and net sizing. Although
it appears to be Window-only, it runs very well in Wine.

## Contributing

All LTSPICE format simulations used in the creation of a team circuit design
should be submitted to this repository for records. Important information
about the circuit should either be written directly into the simulation
schematic as a text block, or included in an accompanying `md` file with the
simulation.

### WARNING: Coordinating Modifications

Like KiCAD schematics, SPICE files are not fully merge compatible, so check with
other people to ensure no one else is currently modifying the simulation you
want to work on. You should always work on a personal branch and ping the channel
before merging.

### Prereqs

* [LTspice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
* Basic understanding of SPICE simulation commands and setup

### Setup

1. Copy folders in `lib/` to the correct location
  1. Copy `lib/sub` to `$USERDIR/Documents/LTspiceXVII/lib`.
  2. Copy `lib/sym` to `$USERDIR/Documents/LTspiceXVII/lib`.
  3. Apppend contents of `lib/model/patch_\*.txt` to the corresponding file in `$USERDIR/Documents/LTspiceXVII/cmp`
2. Open the desired `*.asc` file in `simulations` in LTspice

## Listing

* Isolator_Speed_Study - Circuit design study to improve the propagation
  delay and rise/fall times of a slow 4ch optocoupler

## Disclaimer: Vendored Simulation Libraries

All libraries vendored under `lib/` are provided by their respective manufacturers
to aid circuit design. The Hopkins Rocketry Team disclaims any ownership and
responsibility for these files, which are governed by the respective licenses
in `licenses/`. By using these components, you implicitly agree to the manufacturer
licenses attached to each library, and agree not to redistribute the files
without including the relevant licenses. All files in the `lib/` folder are exempt
from the repository license.