# Phase 5 — Clock & Control

This final phase adds the **clock and control system**, allowing the ALU and registers to operate as one integrated datapath using either manual or automatic clock pulses.

<p align="center">
  <img src="photos/final-build.jpg" width="700">
</p>

## Goal

The goal was to connect the previously completed ALU and registers with a shared clock and a set of control inputs.

The completed system includes:

* Load A
* Load B
* Store Output
* Reset
* Manual Clock
* Automatic Clock
* Manual / Auto clock selection
* 2-bit ALU operation control

## Clock Circuit

An `NE555` timer generates automatic clock pulses for the registers.

A separate pushbutton provides a manual clock, while an SPDT switch selects between **manual and automatic operation** via mux.

A white LED provides a visual clock-mode indicator, remaining solid in manual mode and flashing with the automatic clock.

## Control Switches

Control switches determine when values are loaded and stored:

* **Load A** — enables the A register
* **Load B** — enables the B register
* **Store Output** — enables the output register
* **Reset** — clears the registers
* **ALU OP** — selects ADD, SUB, AND, or XOR

Together, these controls allow data to be manually moved through the datapath.

## Problems Encountered

The main challenges were integrating the clock with the register enable signals, handling the active-low control inputs of the `SN74HC173N`, and ensuring reliable switching between manual and automatic clock sources.

Testing the clock and control sections independently before full integration helped isolate wiring and timing issues.

## What I Learned

This phase reinforced:

* Clock generation with the `NE555`
* Manual and automatic clocking
* Register enable signals
* Active-low control logic
* Timing and synchronization
* Datapath control
* Integrating multiple digital subsystems

## Demos

* [Clock Circuit Demo](demo/)
* [Control Switches Demo](demo/)
* [Final Build Demo](demo/)

## Final Result

With the clock and control circuitry complete, the system can **load two operands, select an ALU operation, calculate the result, and store that result in an output register** using either manual or automatic clock pulses.

This completes the final phase of the project.
