# Phase 1 — Discrete Logic

This phase introduces the fundamental digital logic concepts used throughout the project by building basic logic circuits from discrete `2N2222A` NPN transistors.

The phase includes a **NAND gate**, **AND gate**, and **half adder**, providing a transistor-level foundation before moving to integrated logic circuits in later phases.

<p align="center">
  <img src="photos/half-adder-1.jpg" width="700">
</p>

## Goal

The goal of this phase was to understand how digital logic can be constructed from individual transistors before using dedicated IC circuits. With this 'ground up' approach, I can understand the underlying logic concepts in more complex computer architectures.

The circuits built during this phase were:

* NAND gate
* AND gate
* Half adder

## NAND Gate

The NAND gate was one of the first transistor-based logic circuits built for the project.

A NAND gate produces a LOW output only when both inputs are HIGH.

|  A |  B | Output |
| -: | -: | -----: |
|  0 |  0 |      1 |
|  0 |  1 |      1 |
|  1 |  0 |      1 |
|  1 |  1 |      0 |

Building the gate from individual transistors helped demonstrate how transistor switching can directly implement Boolean logic.

<p align="center">
  <img src="photos/nand-gate.jpg" width="600">
</p>

## AND Gate

The AND gate builds upon the NAND circuit by inverting its output.

An AND gate produces a HIGH output only when both inputs are HIGH.

|  A |  B | Output |
| -: | -: | -----: |
|  0 |  0 |      0 |
|  0 |  1 |      0 |
|  1 |  0 |      0 |
|  1 |  1 |      1 |

This circuit demonstrated how simple logic functions can be combined to create additional gates.

<p align="center">
  <img src="photos/and-gate.jpg" width="600">
</p>

## Half Adder

The final circuit in this phase was a half adder.

A half adder performs binary addition on two single-bit inputs and produces two outputs:

* **SUM** — the least significant bit of the result
* **CARRY** — indicates when the addition produces a second bit

|  A |  B | Sum | Carry |
| -: | -: | --: | ----: |
|  0 |  0 |   0 |     0 |
|  0 |  1 |   1 |     0 |
|  1 |  0 |   1 |     0 |
|  1 |  1 |   0 |     1 |

The SUM output follows XOR behavior, while the CARRY output follows AND behavior.

<p align="center">
  <img src="photos/half-adder-1.jpg" width="600">
</p>

## Build Process

The circuits were built and tested incrementally.

1. Test a single `2N2222A` transistor as a digital switch.
2. Combine transistors to construct a NAND gate.
3. Add inversion to produce an AND gate.
4. Combine logic functions to construct the half adder.
5. Test every possible binary input combination.
6. Verify each output using LEDs.

Testing each circuit independently made it easier to identify wiring mistakes before progressing to more complicated designs.

## Problems Encountered

### Transistor Pinouts

One of the important considerations when working with discrete transistors was correctly identifying the collector, base, and emitter pins.

Unlike an integrated logic gate, wiring a transistor incorrectly can completely change the behavior of the circuit.

Checking the transistor datasheet and verifying the physical pinout before wiring became an important part of the build process.

### Undefined Logic Levels

The circuits also demonstrated the importance of ensuring that digital inputs always have defined HIGH or LOW states.

Inputs left electrically floating could produce unpredictable behavior, making pull-down resistors and deliberate input wiring important for reliable operation.

### Circuit Complexity

Even relatively simple Boolean functions required several discrete components when implemented directly with transistors.

This made it clear why integrated logic ICs are useful: they package many transistor-level circuits into compact, predictable logic gates.

## Testing

Each gate was tested against its complete truth table.

For the half adder, all four possible input combinations were tested:

|  A |  B | Expected Result |
| -: | -: | --------------- |
|  0 |  0 | `00`            |
|  0 |  1 | `01`            |
|  1 |  0 | `01`            |
|  1 |  1 | `10`            |

The two-bit result is represented as:

`Carry Sum`

For example:

`1 + 1 = 10`

## What I Learned

This phase provided hands-on experience with:

* NPN transistors as digital switches
* Boolean logic
* NAND and AND gate construction
* XOR behavior
* Binary addition
* Half-adder architecture
* Pull-down resistors
* Defined versus floating logic inputs
* Reading transistor pinouts and datasheets
* Incremental circuit testing

Most importantly, this phase provided a transistor-level view of the logic that would later be implemented using integrated circuits throughout the rest of the project.

## Demonstrations

Demonstrations for each circuit are available in the [`demo`](demo/) directory.

* NAND Gate
* AND Gate
* Half Adder

## Next Phase

[Phase 2 — 2-Bit Adder/Subtractor](../02-2bit-adder/) expands the single-bit half adder into a multi-bit arithmetic circuit capable of performing both binary addition and subtraction.
