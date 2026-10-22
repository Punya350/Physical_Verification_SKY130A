# Physical Verification Using SKY130A PDK

**A practical guide to CMOS inverter design, circuit simulation, physical layout, Design Rule Check (DRC), and Layout Versus Schematic (LVS) verification using open-source EDA tools.**

## About This Project

This repository documents the process of learning and performing physical verification of CMOS circuits using the open-source SkyWater SKY130A Process Design Kit (PDK).

The experiments cover tool setup, inverter design, transient simulation, physical layout creation, design rule checking, and layout-versus-schematic verification.

## Tools Used

- **open_pdks** — PDK configuration and technology support
- **Magic** — Layout editing and design rule checking
- **ngspice** — Circuit simulation
- **Xschem** — Schematic capture and netlist generation
- **Netgen** — Layout Versus Schematic (LVS) comparison

## Index

- [Chapter 0 — Getting the Tools](#chapter-0--getting-the-tools)
- [Chapter 1 — Understanding the Design Flow](#chapter-1--understanding-the-design-flow)
- [Chapter 2 — DRC and LVS Fundamentals](#chapter-2--drc-and-lvs-fundamentals)
- [Chapter 3 — DRC Issues and Debugging](#chapter-3--drc-issues-and-debugging)
- [Chapter 4 — LVS Verification](#chapter-4--lvs-verification)
- [Simulation Results](#simulation-results)
- [Project Status](#project-status)

---

## Chapter 0 — Getting the Tools

The first step is to prepare the SKY130A design environment and verify that the required EDA tools work correctly.

Tools covered:

- open_pdks
- Magic
- ngspice
- Xschem
- Netgen

**Evidence:** Tool versions, terminal outputs, and screenshots will be documented here.

## Chapter 1 — Understanding the Design Flow

This chapter covers the CMOS inverter design and simulation process.

1. Create or inspect the CMOS inverter schematic in Xschem.
2. Configure the PMOS and NMOS transistor properties.
3. Generate the SPICE netlist.
4. Run transient simulation using ngspice.
5. Plot and analyze the input and output waveforms.
6. Create the physical layout in Magic.
7. Extract the layout netlist for verification.

### Inverter Simulation

The inverter simulation uses a 1.8 V supply and the SKY130A typical-typical (TT) process corner.

Simulation files:

- `sky130_inverter.cir` — SPICE circuit netlist
- `sky130_inverter_waveform.txt` — Transient simulation data
- `sky130_inverter_waveform.png` — Input and output waveform plot

## Chapter 2 — DRC and LVS Fundamentals

This chapter introduces physical design verification.

### Design Rule Check (DRC)

DRC checks whether a layout follows the manufacturing rules defined by the process technology.

### Layout Versus Schematic (LVS)

LVS compares the extracted electrical connectivity of a physical layout against the reference schematic or circuit netlist.

Actual verification reports and screenshots will be added after the checks are executed successfully.

## Chapter 3 — DRC Issues and Debugging

This chapter will document:

- DRC error messages
- Identification of layout rule violations
- Corrections made to the layout
- DRC reports before and after corrections
- Final verification results

## Chapter 4 — LVS Verification

This chapter will document:

- Reference schematic netlist
- Extracted layout netlist
- Netgen comparison results
- Identification and correction of mismatches
- Final LVS report

## Simulation Results

The SKY130A CMOS inverter transient simulation has been completed. The circuit netlist, waveform data, and waveform image will be included in this repository.

## Project Status

| Task | Status |
|---|---|
| SKY130A inverter transient simulation | Completed |
| Simulation files organized in GitHub | In progress |
| Physical inverter layout | Pending |
| DRC verification | Pending |
| LVS verification | Pending |

## References

- [SkyWater SKY130 PDK](https://github.com/google/skywater-pdk)
- [open_pdks](https://github.com/RTimothyEdwards/open_pdks)
- [Magic VLSI](http://opencircuitdesign.com/magic/)
- [ngspice](https://ngspice.sourceforge.io/)
- [Xschem](https://xschem.sourceforge.io/)
- [Netgen](http://opencircuitdesign.com/netgen/)

---

*This repository records the experiments, commands, screenshots, and verification results as the work progresses.*
